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
* https://openid.net/2023/01/08/notice-of-vote-for-proposed-second-implementers-drafts-of-two-fapi-2-0-specifications/


Events (Mike L.)
====================================================
OIDF Calendar
------------------
* https://openid.net/foundation/calendar-of-events/ has been updated. 

Identiverse submissions 
----------------------------

EIC Submission due Feb. 8
-----------------------------

Open Banking Latin America
------------------------------
Gavin Littlejohn organising. 
May or June. 
Likely to be in Rio


Internal Liaisons
======================
Open Banking Paper
---------------------

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

CFPB Comments
------------------------
https://files.consumerfinance.gov/f/documents/cfpb_data-rights-rulemaking-1033-SBREFA_outline_2022-10.pdf 

https://files.consumerfinance.gov/f/documents/cfpb_data-rights-rulemaking-1033-SBREFA-high-level-summary-discussion-guide_2022-10.pdf 


External Orgs & Liaisons (Mike L./Chris)
============================================
Brazil (Mike)
----------------
* Continuing to receive high volume of recertification requests.
* CIBA spec certification is coming up. 
* Open Finance (Insurance) conforming coming. Domingo etc. had an event this Monday. 


SAMA (Mike)
---------------
* Finalized KSA FAPI Profile. We expect access to the mock bank to create a certification test. 
* New milestone - initial KSA FAPI profile January 16. Three banks agreed to test the test. Feb. 1 for the production target for 12 banks to certify then. 

Security Analysis
----------------------
* Next phase contract is done. Kicking off. 

OIDF-J Event: BizDay
-------------------------
* 

IETF
-----------
* DPoP is in IETF last call. 
* Step up authentication WG finished. AD/IESG stage. 

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
* Dave will investigate the possibility of making it compatible with FAPI 1 and 2
* A joint call with Modrna WG is being planned. Tracked as issue #559 - Co-ordinate a joint call with Modrna WG on claims parameter for CIBA


Implementation and Deployment Advice
----------------------------------------------
* A bunch of issues updated. 

Advanced Authorization
-----------------------
n/a



PRs (Dave)
===============
401 - FAPI2MS: Reword section about testing
------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/401

400 - FAPI2MS: Make [security profile] a real reference
-------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/400

309 - Remove old specs
-------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/398

397 - FAPI-CIBA: Remove FAPILI from normative references
---------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/397

396 - FAPI2MS: Make security considerations a top level section
--------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/396

399 - Update JARM ref in message signing
----------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/399

393 - use ticks so it doesn't end up as privatekeyjwt - fapi-2_0-message-signing.md edited online with Bitbucket
------------------------------------------------------------------------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/393

394 - FAPI2MS: Make normative references normative
-----------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/394

Issues (Nat)
==================
Message signing issues: https://bitbucket.org/openid/fapi/issues?component=FAPI2%3A+Message+Signing&status=new&status=open

* #565 - Add privacy consideration

  * Nat to own the ticket. 

* #561 - Intro need to be fixed

  * Dave to own the ticket. 

* #479 - Change to the naming of FAPI

  * To be closed

* #487 - RS must check x-fapi-interaction-id is an UUID or IP address

  * Implementation notes to include clarified text. 

* #558 - update filenames for grant management and CIBA

  * Dima to clarify with Mike Jones. 

* #104 - User friendly names and registration of providers

  * Closing the ticket. 

* 567 - Clause 20" does not exist any longer...

  * Closing as resolved. 


AOB (Nat)
=============
* GNAP going through WGLC. 

The call adjourned at 15:00

Chat Transcripts
========================
Me to Everyone	11:03 PM	Draft Agenda

1.   Roll Call (Dave/Nat)
2.   Adoption of Agenda (Nat)
3.   Second Implementer’s Drafts of Two FAPI 2.0 Specifications
4.   Events (Mike L.)
5.   Internal Liaisons
5.1.   Modrna WG
5.2.   iGov WG
6.   External Orgs & Liaisons (Mike L./Chris)
6.1.   Brazil (Mike)
6.2.   SAMA (Mike)
7.   Drafts Updates (Nat)
7.1.   Security Profile
7.2.   Message Signing
7.3.   Grant Management
7.4.   CIBA
7.5.   Implementation and Deployment Advice
7.6.   Advanced Authorization
8.   PRs (Nat)
9.   Issues (Nat)
10.   AOB (Nat)

#. Mike Leszcz - (OpenID Foundation) to Everyone	11:05 PM	https://openid.net/2023/01/08/notice-of-vote-for-proposed-second-implementers-drafts-of-two-fapi-2-0-specifications/
#. Me to Everyone	11:05 PM	https://openid.net/2023/01/08/notice-of-vote-for-proposed-second-implementers-drafts-of-two-fapi-2-0-specifications/
#. Mike Leszcz - (OpenID Foundation) to Everyone	11:06 PM	https://openid.net/foundation/calendar-of-events/
#. Mike Leszcz - (OpenID Foundation) to Everyone	11:16 PM	https://docs.google.com/document/d/1mjmqPzfRI1l0ki9qnyaSz2YwAkH54gfG8A4lJtzA0WI/edit?usp=sharing
#. Me to Everyone	11:17 PM	https://files.consumerfinance.gov/f/documents/cfpb_data-rights-rulemaking-1033-SBREFA_outline_2022-10.pdf 
#. 
#. https://files.consumerfinance.gov/f/documents/cfpb_data-rights-rulemaking-1033-SBREFA-high-level-summary-discussion-guide_2022-10.pdf 
#. 
#. Joseph Heenan (OIDF/Authlete) to Everyone	11:18 PM	This was the announcement from CPFB: https://www.consumerfinance.gov/about-us/newsroom/cfpb-kicks-off-personal-financial-data-rights-rulemaking/
#. Kosuke Koiwai to Everyone	11:30 PM	more than 50 registerd to attend on site, 330 people registered to watch online
#. Dave Tonge (Moneyhub) to Everyone	11:35 PM	https://bitbucket.org/openid/fapi/pull-requests/401
#. Dave Tonge (Moneyhub) to Everyone	11:36 PM	https://bitbucket.org/openid/fapi/pull-requests/400
#. Dave Tonge (Moneyhub) to Everyone	11:36 PM	https://bitbucket.org/openid/fapi/pull-requests/398
#. Dave Tonge (Moneyhub) to Everyone	11:37 PM	https://bitbucket.org/openid/fapi/pull-requests/397
#. Dave Tonge (Moneyhub) to Everyone	11:38 PM	https://bitbucket.org/openid/fapi/pull-requests/396
#. Dave Tonge (Moneyhub) to Everyone	11:38 PM	https://bitbucket.org/openid/fapi/pull-requests/395
#. Dave Tonge (Moneyhub) to Everyone	11:39 PM	https://bitbucket.org/openid/fapi/pull-requests/399
#. Dave Tonge (Moneyhub) to Everyone	11:39 PM	https://bitbucket.org/openid/fapi/pull-requests/393
#. Dave Tonge (Moneyhub) to Everyone	11:39 PM	https://bitbucket.org/openid/fapi/pull-requests/394
#. Joseph Heenan (OIDF/Authlete) to Everyone	11:41 PM	https://bitbucket.org/openid/fapi/issues?component=FAPI2%3A+Message+Signing&status=new&status=open
#. Dave Tonge (Moneyhub) to Everyone	11:41 PM	https://bitbucket.org/openid/fapi/issues/565/add-privacy-consideration
#. Dave Tonge (Moneyhub) to Everyone	11:43 PM	https://bitbucket.org/openid/fapi/issues/561/intro-need-to-be-fixed
#. Chris Michael to Everyone	11:46 PM	Hi all - sorry have to jump off now
#. Dave Tonge (Moneyhub) to Everyone	11:46 PM	https://bitbucket.org/openid/fapi/issues/479/change-to-the-naming-of-fapi
#. Dave Tonge (Moneyhub) to Everyone	11:48 PM	https://bitbucket.org/openid/fapi/issues/487/rs-must-check-x-fapi-interaction-id-is-an
#. Dave Tonge (Moneyhub) to Everyone	11:53 PM	https://bitbucket.org/openid/fapi/issues/558
#. Dave Tonge (Moneyhub) to Everyone	11:55 PM	https://bitbucket.org/openid/fapi/issues/104/user-friendly-names-and-registration-of
#. Dave Tonge (Moneyhub) to Everyone	11:56 PM	https://bitbucket.org/openid/fapi/issues/567/clause-20-does-not-exist-any-longer