============================================
FAPI WG Meeting Notes (2021-11-10) 
============================================
* Date & Time: 2020-11-10 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Brian Campbell (Ping Identity)
  * Daniel Fett (yes)
  * Dave Tonge
  * Dima Postnikov
  * Francis Pouatcha (adorsys)
  * Gail Hodges (OIDF, she/her)
  * Joseph Heenan (Authlete / OpenID Foundation)
  * Lukasz Jaromin (Cloudentity)
  * Mike Leszcz
  * Nat Sakimura
  * Stephane Mouy
  * Stuart Low (Biza.io)
  * Takahiko Kawasaki (Authlete)
  * Travis Spencer (Curity)
  * AF
  * Ayomi Igandan
  * Daniel Fearns
  * Don Thibeau
  * Edmund Jay
  * Kosuke Koiwai
  * Michael Palage
  * Ralph Bragg

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
  * Francis suggested using the Summary/Introductory document that the group wrote as a starting point and send for feedback

* WS - 2: Wed Nov 24th (1pm to 4pm or 2pm to 5pm)
* WS - 3: Friday Dec 10th (2pm to 5pm)

Reading Materials will be sent by Dave - target Close of Business Day today. 

Share general summary of FAPI and then converging points with FAPI 2.0

BG redirect approach is not complete, would be ideal to replace with FAPI

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
* Encouraging RP to take certification through RP community group Slack Channel. 
* 130 certifications by now. 
* Phase 3 live since Oct. 29. 
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

  * Australia has issues with case sensitivity of issuer well-known location
  * Dave may create issue for discussion

* Some banks have reconfigured systems resulting in non-compliance


PRs (Dave)
=================
PR289: Claims parameter clarification (Dima/Dave)
-------------------------------------------------------
https://bitbucket.org/openid/fapi/pull-requests/289

Still some discussions on the wordings around claims. 


* `claims`: JSON array containing the names of all OpenID Connect claims (see [@!OIDC]) as requested by the client (acting as OpenID Connect RP) and consented by the End-User in one or more authorization requests associated with the respective grant.
* * Brian Campbell: This still seems like it could be potentially interpreted as requiring OIDC scopes to be 'expanded' into claims.

Taka pointed out that this is related to #450. 

Discussion

* Current wording isn’t clear that it’s implementation specific
* Allow servers to expand the scope values into claim names, but not to require it. 
* Adding some explanation on "clients" and "RPs". 
* Claims parameters with values (like in UK) v.s. RAR. 


Brian asked whether the problem is more complicated

* Whether actual claims request content needs to be persisted
* Should it distinguish consent to the release of claims through userinfo vs id token
* Should it distinguish between consenting to release of claims with a specific value versus not a specific value

Dave suggested adding note to clarify that expanding the claims or not is implementation specific

Dima will be adding Notes explaining these. 

* JSON Schema was proposed but several people pushed back. 


Merging,update, replace has been discussed but no consistency implementation

Should leave it up to implementers but need consistency for RPs

Maybe simplify it  to allow replace only

Is this a fruitful endeavor?


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

2 active polls still open but already at quorum but voting is still encouraged




The call adjourned at 15:__ UTC