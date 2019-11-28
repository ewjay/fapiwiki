============================================
FAPI WG Meeting Notes (2019-11-27) 
============================================
Date & Time: 2019-11:27 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
Attending:
--------------------
#. Dave
#. Nat
#. Brian
#. Daniel
#. Joseph
#. Kosuke
#. Ralph
#. Stuart
#. Torsten
#. Bjorn
#. Pedram Hosseyni


Regrets: 
---------------------    

Adoption of the Agenda (nat)
==================================
* Adding #153
* Adding ETSI Report

Report from Pacific Call (Nat)
========================================
* Stances towards FDX, ACDS, Open Banking, etc. 
* Abstracted model for Consent and Revoke as an International Standard Token Establishment for multi-regional
    * Special Call at 5 PM Pacific Time on the December 5th. 

Events (Nat)
===============
OpenID Summit Tokyo and associated events (Nat)
-------------------------------------------------
* Jan 23, 24, 27, 28. 
* Tokyo and Miyazaki
* Details: http://lists.openid.net/pipermail/openid-specs-fapi/2019-November/001613.html

FDATA Summit
------------------------------
* December 5, 2019
* Edinborough 
* MoneyHub etc. shortlisted in the award. 
* https://fdata.global/summit/awards-2019/

ETSI (Ralph)
---------------------
* Pushing JWS HTTPS. 
* Draft JWS Headers due shortly before Jan 20 next meeting. 
* eIDAS scheme are based on CMS and JWS is a good candidate to replace it. 
* Polish API, STET coming together. Portugal deferred to Berling Group. BG committed to JWS. 
* ETSI wants to reuse IANA registry. 

IETF (Torsten)
---------------------
* Justin presented OAuth XYZ, Torsten on PAR and RAR. 
* There would be an activity to do OAuth 3.0 based on XYZ but there would be 2.1. 
* Migration path needs to be prepared, e.g., versioned endpoints. 

* Cavage was presented to Sec Dispatch and Justin and Annabel is writing a new draft to be presented to HTTP group. 


Issues
================
https://bitbucket.org/openid/fapi/issues/

#163: more description of the security model (Daniel)
----------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/163/more-description-of-the-security-model



#255: certification clarification request: location of discovery document
----------------------------------------------------------------------------
Joseph is going to create a pull request. 

#207: RS256 vs PS256 (again)
--------------------------------------
Nat need to create a pull request. 

#236
---------------
Closed with pull request #145

#216 TLS_ECDHE_ECDSA cipher suites
-----------------------------------------
Pending Dave's email intraction with crypto experts. 

#232: Part 1: Complete the privacy consideration section
-------------------------------------------------------------
Nat to write the text. 

#240: FAPI-R: length/entropy of authorization code / refresh token / client_secret
-----------------------------------------------------------------------------------
Waiting for Dave's text. 

#242: Missing Bibliography Reference to FAPILI
--------------------------------------------------
Around Xmas time by Stuart. 

#273: Security considerations re large access tokens
------------------------------------------------------
To be recorded in the implementer's advice document. 
Concrete text is needed. 


Pull Requests
=================

https://bitbucket.org/openid/fapi/pull-requests/




AOB
==========================




The meeting was adjourned at 14:56 UTC.