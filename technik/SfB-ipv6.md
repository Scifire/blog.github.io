---
layout: page
title: "Skype for Business IPv6 problem"
permalink: /technik/skype-for-business-ipv6-problem/
---
*Published on: 2018-10-08*

In our company we recently enabled IPv6 in Dual-Stack mode (which means we have a ipv4 and a ipv6 address). We have noticed nearly no failures but since we enabled ipv6 for the client network Skype for business isn´t able to login anymore.
We found out a workaround to disable ipv6, login and enable it again which will also work but it isn´t satisfactory for us.

I found then some threads about MTU problem from sfb and tried this on my pc on this also works.

On Windows 10 it is possible to change the MTU of a single interface only for ipv6 or ipv4, so i changed the ipv6 mtu from 1500 (which is standard) to 1480 with which sfb will work.

`Netsh interface ipv6 show interfaces`

to detect which is the currently active interface

`Netsh interface ipv6 set subinterface “7” mtu=1480 store=persistent`

to set the MTU of the interface to 1480.

This is also not a nice workaround but needs to done done only a single time and not every day. Hopefully Microsoft will fix this someday…

 

Sources:     
<https://answers.microsoft.com/en-us/msoffice/forum/msoffice_sfb-mso_mac-mso_o365b/skype-for-businesslync-services-dont-appear-to/c204b511-8b0b-4338-924e-729603627413/>    
<https://www.skypefeedback.com/forums/299913-generally-available/suggestions/33748453-fix-the-badly-broken-ipv6-stack/>

<https://krausens-online.de/windows-10-setzen-der-mtu-aller-netzwerkkarten-ausser-loopback/>
