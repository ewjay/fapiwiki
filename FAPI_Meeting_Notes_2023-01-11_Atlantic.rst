===========================================
FAPI WG Agenda & Meeting Notes (2023-01-11) 
===========================================
* Date & Time: 2023-01-11T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-11-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 



* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================

Second Implementer’s Drafts of Two FAPI 2.0 Specifications
===========================================================


Events (Mike L.)
====================================================
* https://openid.net/foundation/calendar-of-events/ has been updated. 

Internal Liaisons
======================
Modrna WG
-----------------
Bjorn gave a report about claims parameter support for CIBA to organize a call for interested parties to work on it.


* https://lists.openid.net/pipermail/openid-specs-fapi/2022-December/002764.html
* https://bitbucket.org/openid/mobile/issues/206/ciba-iana-actions
* https://bitbucket.org/openid/mobile/issues/210/use-of-ekyc-ida-spec-with-ciba-fapi-ciba

iGov WG
-----------
* Multiple `acr` values in requests as an array expressing a preference. 

  * Conformance suite behavior seems to be different
  * Only EAP profile specifies ACR values
  * George states that if some prefer a combination of acr values, having an array for stating preference doesn’t work and would need to create a new acr value that is a combination of preferred values.
  * Theres not much implementation of ACR
  * Some would not like to NIST values due to list of requirements

* The WG is to consider creating a profile so that it can be tested. 

External Orgs & Liaisons (Mike L./Chris)
============================================
Brazil (Mike)
----------------
Continuing to receive recertification requests.

Open Finance Brazil if finalizing CIBA profile which may be available next year

OPIN certifications are slow. Seems like many organization won’t be able to meet the end of year deadline.

SAMA (Mike)
---------------
* Finalized KSA FAPI Profile. We expect access to the mock bank to create a certification test. 
* New milestone - initial KSA FAPI profile January 16. Three banks agreed to test the test. Feb. 1 for the production target for 12 banks to certify then. 


Drafts Updates (Nat)
============================================
Security Profile
-----------------------
* Need to merge some editorial fixes/typos

Message Signing
-----------------------
* Not much feedback from Last Call
* A bunch of issues are being filed. We need to resolve them before moving forward. 
* WG members are asked to chime into the tickets early to create PRs. 

Grant Management
-----------------------
n/a

CIBA
--------
* Dave will investigate possibility of making it compatible with FAPI 1 and 2
* A joint call with Modrna WG is being planned. 

Implementation and Deployment Advice
----------------------------------------------
* A bunch of issues updated. 

Advanced Authorization
-----------------------
n/a



PRs (Nat)
===============

* PR # 392 - FAPI 2.0 sec profile: there is no 20, which seems to be 9 now
Wrong clause number
Merged

* PR #394 - FAPI 2.0 sec profile: there is no 20, which seems to be 9 now

  * Moved “Shall” References to normative references section


* PR #393 - use ticks so it doesn't end up as privatekeyjwt - fapi-2_0-message-signing.md edited online with Bitbucket

  * Editorial change to preserve spacing for the keyword private_key_jwt

* PR #391 - clarification re new tokens

  * Clarifies using ‘merge’ action for obtaining new tokens for existing grants
Needs update for Jacob’s comment

* PR #385 - Remove Financial from CIBA in line with FAPI?

  * Changed wording ‘Financial-grade API’ to FAPI

* PR #395 - FAPI2MS: Create acknowledgements section

  * Added acknowledgements
  * Anyone left out should add their name
  * Merged


Closed a few. 



Issues (Nat)
==================
* #561- Intro need to be fixed

  * Need to create text 
  * Suggestions are welcome

* #559 - Co-ordinate a joint call with Modrna WG on claims parameter for CIBA

  * Joseph will check with Bjorn regarding status

* #420 - Multi Party Consents

  * Waiting for use case

* #537 - Document trade-offs between DPoP and MTLS

  * Will put in Implementation and Deployment Advice document
  * Joseph will provide text

* #104 - User friendly names and registration of providers

  * Most likely related to Federation or Dynamic Client Registration
  * Propose to close if no feedback from Tom

* #229 - FAPI CIBA and ID Tokens

  * Was postponed to 2nd implementer’s draft
  * CIBA Core requires “openid” scope
  * Suggest Modrna WG adjust text. Joseph will check if there are anything is affected.

* #242 - Missing Bibliography Reference to FAPILI

  * References have been removed
  * Closed

* #273 - Security considerations re large access tokens

  * Remind Dave to update status

* #288 - FAPI WG & Specs pages are woefully out of date

  * Mike will make the changes as part of transition to new site

* #212 - FAPI-CIBA; should id_token tie itself to the auth request?

  * Need to know the attacker model for CIBA before proceeding.

* #295 - Possible support for "embedded" SCA mode

  * Will leave for the moment

* #260 - Add section in the "Implementation Advice" document about supporting Mobile Apps

  * Put app2app documentation into Implementation Advice
  * Joseph and Dima may have some text
  * George pointed out that Android’s app link is not as secure as IOS universal links and may be possible to impersonate.  App attestation comes into play.
  * Joseph pointed out that in the latest Android, it is fixed, but it will take a long time for Android deployments to catch up.

* #197 - New Document Proposal: FAPI Implementation Guide

  * Will need to add text to document


* #153 - Add level of assurance to scope

  * Will add to Implementation Advice


* #291 - Remove older specs from master

  * PR #398 to remove old specs
  * Will close



AOB (Nat)
=============
* Happy holidays and new year! 

The call adjourned at 15:00

Chat Transcripts
========================

Mike Leszcz - (OpenID Foundation) to Everyone	11:04 PM	https://openid.net/foundation/calendar-of-events/
Mike Leszcz - (OpenID Foundation) to Everyone	11:04 PM	mike.leszcz@oidf.org
Me to Everyone	11:08 PM	https://lists.openid.net/pipermail/openid-specs-fapi/2022-December/002764.html
Joseph Heenan (OIDF/Authlete) to Everyone	11:08 PM	https://bitbucket.org/openid/mobile/issues/210/use-of-ekyc-ida-spec-with-ciba-fapi-ciba
Me to Everyone	11:27 PM	https://bitbucket.org/openid/fapi/pull-requests/392
Me to Everyone	11:28 PM	https://bitbucket.org/openid/fapi/pull-requests/394
Me to Everyone	11:29 PM	https://bitbucket.org/openid/fapi/pull-requests/393
Me to Everyone	11:29 PM	https://bitbucket.org/openid/fapi/pull-requests/391
Me to Everyone	11:31 PM	https://bitbucket.org/openid/fapi/pull-requests/385
Me to Everyone	11:34 PM	https://bitbucket.org/openid/fapi/issues/561/intro-need-to-be-fixed
Me to Everyone	11:36 PM	https://bitbucket.org/openid/fapi/issues/559/co-ordinate-a-joint-call-with-modrna-wg-on
Me to Everyone	11:37 PM	https://bitbucket.org/openid/fapi/issues/537/document-trade-offs-between-dpop-and-mtls
Joseph Heenan (OIDF/Authlete) to Everyone	11:37 PM	https://bitbucket.org/openid/fapi/pull-requests/395
Me to Everyone	11:40 PM	https://bitbucket.org/openid/fapi/issues/104/user-friendly-names-and-registration-of
Me to Everyone	11:42 PM	https://bitbucket.org/openid/fapi/issues/229/fapi-ciba-and-id-tokens
Me to Everyone	11:45 PM	https://bitbucket.org/openid/fapi/issues/242/missing-bibliography-reference-to-fapili
Me to Everyone	11:46 PM	https://bitbucket.org/openid/fapi/issues/273/security-considerations-re-large-access
Me to Everyone	11:47 PM	https://bitbucket.org/openid/fapi/issues/288/fapi-wg-specs-pages-are-woefully-out-of
Me to Everyone	11:49 PM	https://bitbucket.org/openid/fapi/issues/212/fapi-ciba-should-id_token-tie-itself-to
Me to Everyone	11:51 PM	https://bitbucket.org/openid/fapi/issues/295/possible-support-for-embedded-sca-mode
Me to Everyone	11:52 PM	https://bitbucket.org/openid/fapi/issues/260/add-section-in-the-implementation-advice
Me to Everyone	11:56 PM	https://bitbucket.org/openid/fapi/issues/197/new-document-proposal-fapi-implementation
Me to Everyone	11:57 PM	https://bitbucket.org/openid/fapi/issues/153/add-level-of-assurance-to-scope
Me to Everyone	11:58 PM	https://bitbucket.org/openid/fapi/issues/291/remove-older-specs-from-master
Craig Borysowich (Payments Canada) to Everyone	11:59 PM	Happy holidays folks!!
Mike Leszcz - (OpenID Foundation) to Everyone	12:00 AM	Happy Holidays!
Mike Leszcz - (OpenID Foundation) to Everyone	12:03 AM	https://openid.net/foundation/calendar-of-events/