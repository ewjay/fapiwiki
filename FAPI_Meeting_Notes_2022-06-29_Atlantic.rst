============================================
FAPI WG Meeting Notes (2022-06-29) 
============================================
* Date & Time: 2022-06-29T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat)
======================
* Attending: 
* Regrets: Dave Tonge
* Guest: 

Adoption of Agenda (Nat)
================================
* N/A

Events (Nat)
======================


Internal Liaison (Nat)
================================
Security Analysis
---------------------------
* Need to get an update offline from Gail.  

Certification (Joseph/Mike)
----------------------------
* n/a


External Organizations (Nat)
===================================


Specs (Dave)
================
Grant Management (Dima)
----------------------------------------
* There are now a couple of PRs and Issues. 
* Couple of issues left before going to implementer's draft. 

FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* N/A 

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
* Name change PR etc. is yet to be created. 

JARM (Dave)
----------------------------------------
* https://openid.bitbucket.io/fapi/openid-fapi-jarm.html
* Need feedback before last call for final draft.
 
Addressing "User Interface Hijack attack" in FAPI 2? (Nat)
-----------------------------------------------------------
* https://lists.openid.net/pipermail/openid-specs-fapi/2022-May/002619.html
* Provide incentives for ecosystems to adopt FAPI 2 if addressed
* Discuss on list and next call

PRs (Nat)
=================

To be merged
----------------
* PR #341 - clarify scopes

  * Related issue #441

Under discussion
----------------------
* PR #322 – Pull in key management clauses

  * Pull in language from FAPI 1 regarding jwks_uris


* PR #315 - FAPI2 iss + JARM

  * Added clarifying text for returning iss when using JARM

* PR #342 – No Authorization Response encryption is required

  * Need feedback from Ralph. 

* PR #343 - Change name from baseline to the security profile

  * Remove Financial-grade from the name and just use FAPI
  * Change the Baseline name to Security Profile and add references to other specs.
  * The text “we recommend” feels informal.

Issues (Dave)
=====================


AOB (Dave)
=================
* none



The call adjourned at 15:59 UTC