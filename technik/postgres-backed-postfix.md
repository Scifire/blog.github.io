---
layout: page
title: "postgres-backed postfix denylist"
permalink: technik/allgemein/postgres-backed-postfix-blacklist
---
*Published on: 2018-06-28*

While the mail infrastructure in the company I was working was growing and we´re sending more and more mails every day we decide to use Amazon SES to send out our mails.
To hold the servers reputation good Amazon only allows a bounce rate of 5% to 10%, which means if we are exceeding this rate Amazon will block us.

Amazon use their SNS service to inform us about our preferred way about every bounced mail.

To not publish the SES credentials on every server we decide to setup internal postfix servers which are working as relay.  So we have the benefit that we can apply some routing voodoo(internal over office 365, external about SES), some header rewriting (change sender address) and finally a denylist.

With this postgres-backed postfix denylist we can fill the table direct from SNS notifications into the postgres. Then postfix checks the postgres if the recipient address is on our denylist.
Simple postfix denylist

For simple denylisting in postfix we add the following entry to the postfix main.cf:      
`smtpd_recipient_restrictions = check_recipient_access hash:/etc/postfix/access`     

With this line postfix will check every recipient address against the “access” file. If the address is there it will do what is written down after the address. All the things behind are posted as comment to the log.

So syntax for the access file is:      
`test@example.com DISCARD SES bounced mailaddress`     
All actions and further configuration can be found on the [postfix manual](http://www.postfix.org/access.5.html).     
But for this we have to maintain a single file. Also we need to create a hash with postmap from this access and every time we change it we have to reload postfix.
So let´s switch to denylisting backed by postgres

First install postfix-pgsql:

`apt install postfix-pgsql`

Then we need to change the main.cf a bit:

`smtpd_recipient_restrictions = check_recipient_access pgsql:/etc/postfix/pgsql-access.cf`

As you can see we use now the postgres for checks.

The pgsql-access.cf looks like:
```
hosts = 10.10.1.227
user = postfix
password = 123456
dbname = postfix-denylist
table = denylist
select_field = action
where_field = mailaddress
result_format = DISCARD by internal denylist
```
Where is

Host= postgres server
User= user which have access to the database and table
Password= of course password
Dbname= Name of the Postgres db
Table= name of the postgres table where addresses are stored
Select_field= what should happen if there is a matching entry
Where_field= which field should be checked to match
Result_format= What should be printed out, could be static (above) or dynamic with %s

To test what happens when postfix will check the mail we could use postmap:

`postmap -q "test@example.de" pgsql:/etc/postfix/pgsql-access.cf`

We´re testing the address “test@example.com” against the postgres via our config file. If we have an entry which is “test@example.com” the result should be “DISCARD by internal denylist” cause in my example i configured it statically. If there is no entry like this nothing should be printed out.

Now the postfix checks after a restart of the postfix it should now check every mail which is send out against the postgres.

 

 

Helpful links/manual:    
http://www.postfix.org/access.5.html     
http://www.postfix.org/PGSQL_README.html     
http://www.postfix.org/pgsql_table.5.html     
