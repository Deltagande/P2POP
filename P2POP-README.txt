﻿
P2POP

What I would like to see is what I call a P2P email system, in which emails between users are not stored on a public server such as an ISP, outlook.com, gmail.com and others, and thus be less available to be picked up by outsiders.

I envisage an application on a user's computer which acts as a bridge between the local user's email client and other remote users with whom the local user exchanges email.  I will call these luser and ruser.  In a given luser's p2pop installation the names of rusers can be catalogued.  When luser wishes to send a message to, say, ruser1, p2pop will determine the current-ip of ruser1 and attempt to transmit the message to ruser1@<current-ip>.  If ruser1 is not online, the message will be put on hold, and p2pop will try again at configurable intervals until contact is made and the message transferred.  When ruser1 is online, the p2pop at ruser1's computer will receive the message and forward it to ruser1's email client.  Indeed, p2pop can, of course, function inwards as an IMAP server for ruser1's client.

One immediate reaction is that such a system would hardly work with other than POP between users since there would be no central server to which a p2pop instance could connect via IMAP.  However, it is possible that a user's p2pop installation could handle incoming email intended for the email client as IMAP, and even allow the user's other units, computers, smartphones, etc. to connect.

Another, potentially weak link is that a dyndns system would be necessary to ensure that users' computers can advise the system of the users current-ip.  Users with a fixed ip address could have their addresses noted as fixed by other users.  

Since emails will be addressed to ruser1@<current-ip>, messages sent to the wrong ip address which happens to be a p2pop user would be rejected at the receiving end, since the user at that address is not ruser1.  This might provide a way to reduce the number of dyndns lookups.  If luser's computer discovers that ruser1 had ip-adress1 when last contacted, a message could be sent to ruser1@ip-adress1.  If it is rejected for any reason, luser's computer will then do a new dyndns lookup, and store the new address.

I envisage that p2pop would be modular, with one or more central core functions for handling receipt, despatch and possibly storage of incoming and outgoing emails and dns control, and separate modules for connecting the core functions to different email clients.

The problem I have is that it is 100 years since I did any programming, and that was more in the nature of hacking existing code.  In other words, I'm opening up here for the possibility for those who really are programmers to build a system or tell me I'm barking up the wrong tree.  Either way I win, for if someone builds the system, I have, hopefully, a free copy, and if I'm barking up the wrong tree, at least I know that and can forget about the idea.
