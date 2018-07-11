============================================
FAPI WG Meeting Notes (2018-07-10)
============================================
Date & Time: 2018-07-10 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:05 UTC. 

Roll Call
===========
* Attending: Nat, Tony, Sarah, Anoop
* Guests: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Adopted as is

Events
==========
IETF Montreal
----------------
IETF Montreal will be in the week of 16th. 
John, Torsten, Mike, Justin, Brian, Tony will be there. 
It would probably be a good opportunity to advance the general security documentation cited in #150. 

Tokyo F2F
------------
A bunch of WG members will be in the conference in Tokyo for the week of July 23. 
Authlete kindly provided a space for a F2F on the morning of the 24th. 
Details will be sent later. 

Issues
================
* No new issues. 

CIBA Refactoring Status
===============================
* https://docs.google.com/spreadsheets/d/10QVqqCWnD4uLbE8wsNIUUytIBRY4Aoi9KPlv8vW_U10/edit?usp=sharing

Liaison Reports (If any)
===========================

ISO/TC 68 (Tony)
-----------------
API Spec Draft is coming up but it seems to be coming up with new flows. 
Now it has 4 flows instead of 3. 
Those with the access to the document should take a look at it. 

FS-ISAC (Anoop)
-----------------
New API request for returning PDF or well-formed JSON is being proposed. 
Also, there is now a bulk file transfer using SFTP server. 
SFTP server is set up between the bank and the fintech by contract. 
A file can contain many accounts. Chunking is supported. 
With the use of it, banks can reduce the load to its servers. 
HTTPS API endpoint instead of SFTP was also proposed but it was not taken up by the banks for now. 

Data Schema Plans (Anoop)
==============================
Anoop is leading the sub committee on the data schema. 
To start with, he will start analyzing the delta between the FS-ISAC DDA and Open Banking. 
Nat also pointed out that both are pretty thin in the investment banking side, that it lacks various pre-trade information making it hard to judge whether a transaction can be made. 
Unavailability of pricing data for investment instruments is also adding complexity. 
One usually have to purchase it. 

As to the meeting structure, we could create dedicated meetings or allocate time slots within the current meeting schedules. 

Anoop will draw a plan with regard to the data schema subcommittee and announce it to the list. 

AOB
===========

Demo Movie
---------------
Tony introduced to the group a demo movie of FAPI/Fido etc. combination. 

* https://www.w3.org/2018/06/lyra-webauthpay.mp4

Next Call
-----------------------
Due to the overlap with IETF, the call next week will be cancelled. 

* The meeting was adjourned at 23:50 UTC.