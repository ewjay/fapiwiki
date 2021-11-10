============================================
FAPI WG Meeting Notes (2021-11-10) 
============================================
* Date & Time: 2020-11-10 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlanti20
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 


* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Adopted as is. 

Events (Dave/Nat)
======================

OIDF virtual workshop
------------------------------
* Thursday, December 9th at 9 AM PT. 
* Link with registration details: https://openid.net/2021/10/19/registration-open-for-openid-foundation-virtual-workshop-thursday-december-9-2021/

Workshop with Berlin Group
--------------------------------
* WS -1 : Monday Nov 15th 1pm-4pm (CET)

  * Need to collect reading material
  * Francis suggested using the Summary/Introductory document that the group wrote as starting point and send for feedback

* WS - 2: Wed Nov 24th (1pm to 4pm or 2pm to 5pm)
* WS - 3: Friday Dec 10th (2pm to 5pm)

Reading Materials will be sent by Dave - target Close of Business Day today. 

GSMA (Gail)
---------------------
* OIDF/GSMA Workshop is being planned towards the end of November to give them overview of OIDF projects. 
* Speakers tbd. 

External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
* No major updates. 
* Transition from FAPI I.D.2 to FAPI 1.0 Final - public consultation going on. staged approach for transition from FAPI 1 ID2 to FAPI 1 final
** Decision Proposal 209 - Transition to FAPI 1.0 Advanced Profile #209 https://github.com/ConsumerDataStandardsAustralia/standards/issues/209#issuecomment-964665004
Brazil (Mike L.)
---------------------------
* Test suites are stable now. 
* Encouraging RP to take certification through community group. 
* 130 certifications by now. 
* Phase 2 live since Oct. 29. 
* Receiving consistent flow of certification. 

Berlin Group (Francis)
--------------------------------
* Focused on Workshop

Canada (Mike)
------------------
* n/a

FDX (Mike)
------------------
* Draft blog received and responded to them. 
* OIDF blog draft also sent. 
* Gail is following up. 

The Middle East and North Africa (Ali)
---------------------------------------
* n/a

Russia (Dima/Mike)
--------------------
* Had a call with the Russian Fintech Association on Oct. 29. 
* Expecting feedback soon. 

UK (Chris)
--------------------
* Some of the CMA 9 came through with Annual Certification Updates. 
* Debates on whether "Brands" should be treated as a single system. 
* They have different domains and configurations - different .well-known and issuer so they should be treated as different systems.  

PRs (Dave)
=================
PR289: Claims parameter clarification (Dima/Dave)
-------------------------------------------------------
https://bitbucket.org/openid/fapi/pull-requests/289

Issues (Dave/Nat)
=====================
#443: Missing Discovery Metadata (Dave)
-----------------------------------------
Callers agreed to the approach - to add the metadata to FAPI CIBA. 


#411: HTTP Signing Scheme for FAPI 2.0 Advanced (Dave)
----------------------------------------------------------
Three options: 

* UK: Detached JWT
* BG: Draft Cavage and Draft HTTP Singing @ IETF
* DPoP: 

HTTP Signature mechanism for PoP seems controversial and not yet adopted.

For implementer’s draft, may have 3 different options and then select one as mandatory in the final draft. 

Need some implementation experience.


#455: Impact of grant_management_action=update (Dima)
-----------------------------------------------------------
This issue relates to how we represent historical updates to Scopes and resources relationship and when we query grant management APIs

There was a suggestion to Flatten the structure but it was pointed out that it might be too much change introduced to the ecosystem.

Maybe too complex for too little value.

Introducing a new structure into access tokens is too invasive for a theoretical problem.

Brian suggested that putting guards  at the data model or restricting what’s actually issued or being careful with what's issued would be sufficient to address the issue.



AOB (Nat)
=================
The FDX Blog Post (Gail)
----------------------------
WG discussed the blog post text to come and made some edits to the text.

Changed protocols to standards

Put more emphasis on security and interoperability

A modified sister blog will also be posted on OIDF website


Two Open Polls 
-----------------------
* Federation
* eKYC & IDA


The call adjourned at 15:00 UTC