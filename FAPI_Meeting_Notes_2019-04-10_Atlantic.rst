============================================
FAPI WG Meeting Notes (2019-04-10) 
============================================
Date & Time: 2019-04-10 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: Anoop, Dave, Nat, Bjorn, Brian, John H-A (Radium), Joseph, Torsten
* Regrets:      
  * 

Adoption of the Agenda (Nat)
==================================
* 

External Organizations
==========================

STET (Torsten)
----------------




Open Banking (Dave)
--------------------
* Some of the banks having problems with eIDAS certs. 
* Problems includes: 
* ETSI changing the spec. 
* QTSP's lengthy and tiresome process for getting the certs. 
* QTSPs are not checking the "currentness" of the information on the certs. OB Directory is checking them. 
* Organization identifier number changes as the organization obtains new licence making it difficult to map to a previously obtained consent. 
* etc. 

Instead, OB is checking the currentness and reflects them in the protocol. 

So, moving from OB certs to eIDAS poses significant risk to the UK Banks and FCA is allowing it. 

Berlin Group (Dave)
------------------------
* Dave is sending reminders to them but there has been no response. 



Testing & Certification 
============================
* 2 providers got certified, Authlete (Full) and Forgerock (Not MTLS)
* https://openid.net/certification/#FAPI_OPs
* Torsten asked for a link in the FAPI page. 
* RP testing is partially open. Still "beta" till June. 
* Nat asked if there is any marketing material on it. 
* Joseph told that he may be able to provide a short silent video. 

Draft Status (Nat/Dave)
===========================
CIBA FAPI Profile (Dave)
---------------------------
* Finalizing attaker model. It is expected to take another week. 

TR Cross-Browser Payment Initiation Attack (Daniel/Torsten)
-------------------------------------------------------------
* TR-Cross_browser_payment_initiation_attack.md
* Torsten introduced a blog post quoting this in LinkedIn. 

TR Lodging Intent Pattern (Torsten)
-------------------------------------------
* Financial_API_Lodging_Intent.md
* Torsten etc. are writing a Medium post to solicit more information. They have not come to a conclusion on how to consolidate various approaches found in the wild. Writing on Medium hopefully attracts more comments. 
* Nat pointed out that there is no IPR protection in the comments acquired that way and an appropriate way needs to be sought. 

Events
=========
* IIW
* EIC
* Identiverse: There will be open banking track. 

Issues
==========================
* Issues will be dealt with in the next week's "issues" call. 


AOB
==========================
PSU IDENTITY, HISTORIC CHALLENGES AND HOW TO SOLVE THEM (John)
---------------------------------------------------------------------
* John created a blog post on the use of `sub` in ID Token used in Open Banking. 
* https://www.raidiam.com/blog/2019/4/9/psu-identity-historic-challenges-and-how-to-solve-them
* There is other information as well. 
* Any comments are much appreciated. 

Next Call
-------------------------
* Atlantic "Regular" call next week. 

The meeting was adjourned at 14:50 UTC.