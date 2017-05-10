============================================
FAPI WG Meeting Notes (2017-05-10)
============================================
Date & Time: 2017-05-10 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call
===========
* Attending: Nat, Dave, Henrik, Joseph, Ralph, Sasch, Tony, Tom

* Regrets: 

Adoption of the Agenda (Nat)
==================================
* 

External Orgs
================

Euro Retail Payments Board (Dave)
-------------------------------------
* https://www.ecb.europa.eu/paym/retpaym/euro/html/index.en.html
* Need to create a report by June. 
* Establish formal rel. with them? 
* Dave will meet with them next week. 

Concern on separatism. 
Recommend FAPI profile. 

UK Open Banking (Ralph)
-------------------------
0.1 draft out. 
Lots of comments came in. 
FAPI did not have too much decent. 
Redirect usecases. 
Screen scraping continue? Direct access model is good enough? 
Add context headers. 

OB session with UK Verify. 
22nd meeting. Go to market activity. 
Automatic KYC. 

Microsoft B2C participating in Verify UK for private provider access. 
Berclay IdP for ID attestation. 
Providing ID Claims direct in authz flow. 

Hookup B2c to Prototype with Verify as it supports JWT ID Token. 

With very little effort UK FI can be IdPs. 

Q. Any dates for being public? 
A. Website update late but it is public. 
   Open Banking has adopted RW FAPI Spec. 
   CMA + OIDF conformance profile. OIX event on 22nd. 


ISO/TC68 (Nat)
-------------------
* 

Mobile Connect (Dave)
-----------------------
* Attribute attestation. 
* Which bank would be part of verify? 
    * Berclay
    * Challenger banks wants automated KYC. Atom, Staling, etc. 
    * Passport verification svc not available to all banks. 

Lobbying vendors to support federated claims. 

Q. Reasonal Target date? 
A. Atom and Sterling wants ASAP. 
   No reason why banks cannot consume payloads. 


Others
------------


Part 2: WGLC Issues 
===========================
* #93: Not clear why AS needs to support signed+encrypted ID Token
* #92: Put cipher suite recommendations in the security considerations
* #91: Id mix up attack
    clarify. 
* #89: s_hash needs to be defined more precisely
   close. 
* #88: Sender constraining the code
* #87: Need create request_uri endpoint in AS
* #78: Malicious Endpoint Attack
* #77: IdP Confusion Attack
* #60: Only one method to Token Bind AT rather than two?

* Public client defintion. 

AOB
===========
Next Call (Pacific)
-----------------------

Meeting was adjourned at __:__ UTC.