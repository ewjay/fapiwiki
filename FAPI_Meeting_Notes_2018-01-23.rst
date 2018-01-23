============================================
FAPI WG Meeting Notes (2018-01-23)
============================================
Date & Time: 2018-01-23 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:05 UTC. 

Roll Call
===========
* Attending: 
   * Guest: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* 

External Orgs 
==================
FS-ISAC (Anoop)
---------------------------------
* FS-ISAC response
* Want to confirm that there are less secure Read Only use cases (Part 1). 

ANSI/X9 (Paul)
------------------

ISO/TC 68 (Paul)
----------------------


Upcoming Events
======================
Open Banking (Don)
---------------------
Workshop https://www.eventbrite.co.uk/e/openid-foundationopen-banking-implementation-entity-workshop-tickets-42005257857

Remote participation may be available


API Days (Nat)
-----------------
Nat will be attending to do presentation about FAPI and OpenBanking


Specs Discussion
=======================
Issues
=============
#129 TLS cipher restrictions should be relaxed for the authorise endpoint
-----------------------------------------------------------------------------
What is currently in the pull request seem to be a good text. 
If there is no objection, we should adopt it. 

ASK: Adoption of the pull request. 

#127 CIBA: security issues
---------------------------------
Text for the security consideration was proposed. 
When the text is added, the ticket should be closed. 

ASK: Adoption of the proposed text. 

#116 CIBA - authentication methods and proof of possession
--------------------------------------------------------------
New text was provided. 

ASK: Review the text. 

#110 more definition of s_hash
-------------------------------------
Brian wants the behavior of the AS when `state` is not in the request to be specified. 
Nat suggested that `s_hash` must not be in the ID Token if the request did not have `state` specified. 

ASK: Would this proposal acceptable? 

#114 Require state
------------------------
Linked to #110. 
Nat proposed to require `state` in pure OAuth, while making it optional for OIDC. 

ASK: Adopt the direction. 

#100 Signing API response payloads
-------------------------------------
OB uses detached JWS. 

ASK: WG to confirm the direction. 


Implementer's Draft (Edmund)
--------------------------------


Dynamic Client Registration (Pam)
-----------------------------------
* Skipped since Pam was not available for discussion

Files: https://bitbucket.org/openid/obuk/src/4630771db004da59992fb201641f5c4ff2c881f1/uk-openbanking-registration-profile.md?at=master&fileviewer=file-view-default

* What OBUK is working on is different and closer to the earlier version of OIDC registration. 
* It could, however, be reasonable for their use cases. 
* Need to be clear on the requirements, e.g., non-repudiation, etc. 
* We could bring some idea back to OIDC and OAuth. 
* Perhaps we can discuss more in details in the Atlantic call. 


AOB
===========


Next Call (Atlantic)
-----------------------
The next call is scheduled to be in the Atlantic time zone. 

* The meeting was adjourned at 23:__ UTC.