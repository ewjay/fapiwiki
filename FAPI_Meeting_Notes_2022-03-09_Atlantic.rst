============================================
FAPI WG Meeting Notes (2022-03-09) 
============================================
* Date & Time: 2022-03-09T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-02-02_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:04 UTC. 

Roll Call (Nat)
======================
* Attending: 
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================
* Adopted as is

Events (Nat)
======================
OSW 2022 (Daniel)
--------------------
Early bird ticket is available for the next 8 days. 

* https://oauth.secworkshop.events/osw2022

IIW Workshop (Mike)
---------------------
* April 25
* Still trying to find the location in Mountain View. 
* Full WS details will be available this week. 
* Working group updates
* Guest speakers
* Torsten will give GAIN PoC updates
* Debbie Bucci on open data initiatives in healthcare. 

IETF OAuth (Rifaat)
---------------------
* DPoP etc. 

Internal Liaison (Nat)
================================
iGov WG
----------------




External Organizations (Nat)
===================================
U. Stuttgart
--------------------------
FAPI 2.0 security review: delivered contract on Tuesday. 

Saudi Arabia
-------------------
Call with Central bank of SA. 

Berling Group 
-----------------------
Next meeting end of April. 



Specs (Nat)
================
FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/466/proposal-for-fapi-dcr-dcm-dynamic-client
* n/a

Grant Management (Dima)
----------------------------------------
* n/a 

JARM
----------------------------------------
* Dave to send out the WGLC. 

PRs (Dave)
=================
PR306 - Add refresh token rotation clause and note
---------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/306

PR307 - Rework the TLS section re issue 461
-----------------------------------------------
Follow BCP. s/4/3/. 

PR311 - Remove support for hybrid flow
-----------------------------------------------
Tending to remove. Please chime in if you think that is not a good idea. 

PR312 - Make clear that we only support code flow
-------------------------------------------------------
Change back to "shall support" instead of "shall use". 

PR310 - withdraw clause re introspection (re: #417)
------------------------------------------------------

PR315 - FAPI2 iss + JARM (Re: #478)
-------------------------------------
The text should be modified to make the client not use `iss` outside JWT. 

JARM is not required in FAPI 2.0 Baseline. 

PR316 - Explicitly mention mtls_endpoint_aliases (re: #415)
---------------------------------------------------------------

PR314 (re: #471)
----------------------
* https://bitbucket.org/openid/fapi/pull-requests/314
Add explicit clause about lifetime of request_uri

Maybe a good idea but the attacker model does not directly imply that. 
Also, it may act as a limiting factor for some use-cases. 

Issues (Dave)
=====================

* #481 - try to absorb it in FAPI 2.0 Advanced. 


AOB (Nat)
=================
n/a


The call adjourned at 15:00 UTC