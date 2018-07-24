============================================
FAPI WG Meeting Notes (2018-07-24)
============================================
Date & Time: 2018-07-24 01:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 03:08 UTC. 

Roll Call
===========
* Attending: Nat, Kengo (Folio), Mark (Radium), Dave, Henrik (Authlete), Joseph (Authlete), Hide (Authlete), Taka (Authlete), Wada 8NRI), Hiroshi Aiba (NRI), Ralph (Radium), Justin (Fintech Labs). 
* Guests: Takashi Uematsu (Hitachi), Yukawa (DeNA)
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Adopted as is

CIBA (Dave) 
===============
* Concerns raised on posting token out. Just notify the client/resource. 
    * #66 in CIBA. People should look at it. This is the biggest change to be made at CIBA core spec. 
    * This will make the CIBA Profile in FAPI very lightweight. 
    * This implies that existing MNO behaviour has to put into an MNO profile rather than in the core. 

Security Report and ID2 (Nat)
=============================
1) Mandate AT hash. 
2) It works. The mitigation suggested is to
   a) Claimed HTTPS URI --> Add a note about native apps. For the platforms without support for it, 
   b) Dynamic Client Registration
3) It can be done. It was discussed before. Perhaps it should be done in the security documentation. 
Credit tarnishing attack can be a real use case. 

App2app (Dave)
====================
Need to add a note explaining how native apps can be user agent for confidential client. 
Many cases using an app as user agent/browser. 

Redirect URI place and security consideration. 

Reference BCP. 

Dave to propose the text. 

Open Banking Update (Ralph)
============================
Discussed about an "exciting" new development. 
The information will be shared as soon as it becomes sharable. 

AOB
===========

Next Call
-----------------------
There will be a Pacific call tomorrow. 

* The meeting was adjourned at 03:08 UTC.