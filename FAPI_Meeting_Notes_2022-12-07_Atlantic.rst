===========================================
FAPI WG Agenda & Meeting Notes (2022-12-07) 
===========================================
* Date & Time: 2022-12-07T14:00Z
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

Adoption of Agenda (Dave/Nat)
================================

Message Signing
=====================
It should be ready to go for I-D. 

Grant Management (Dima)
============================
PR 391 Dima Postnikov clarification re new tokens
------------------------------------------------------
s/either/e.g./

Proceeding for Implementer's Draft
---------------------------------------
* Last Call was Oct. 23. Now all the issues came up are addressed. 


Events (Mike L.)
====================================================
n/a


External Orgs & Liaisons (Mike L./Chris)
============================================


Brazil (Mike)
----------------
* A steady flow of re-certification from Open Finance Brazil
* Open Insurance BR certification request has started to come in. 

SAMA (Mike/Chris)
---------------------
* Call on Monday this week. Clarified KSA profile. 
* Model Bank will be available on Dec. 15. 
* KSA profile testing to start Jan. 16. Three banks agreed to test the test. 
* Expected to be in production in February. 

* OIDF email was out due to the Rackspace outage from Friday to Sunday. Please re-send. 
* Please vote for Mobile SSO. 



FAPI Specs
===============

* Security Profile

  * Need to merge some editorial fixes/types

* Message Signing

  * Last call message has been sent last week
  * No feedbacks yet
  * Will start Implementer’s draft process

* Grant Management

  * Discussed some issues last week
  * One outstanding issue to address before it’s ready for ID 

* JARM

  * Spec is final

* CIBA

  * Dave will investigate possibility of making it compatible with FAPI 1 and 2

* Implementation and Deployment Advice

  *Some issues have been filed
  * Daved asked if there is interest to continue work on this draft

    * YES

  * Will act like a BCP instead of a normative spec
  * Will put focus on this after Grant Management

* Advanced Authorization

  * Work Spec will be dropped and deleted



PRs (Dave)
===============

* PR #390 - FAPI2 editorial and file name changes

  * Merged

* PR #388 - Fix some typos in Security Considerations

  * Merged

* PR #387 - Fix typo in DPoP Proof Replay Security Considerations

  * Merged

* PR #386 - Replace reference to Lodging intent with the a reference to RAR

  * Needs review

* PR #385 - Remove Financial from CIBA in line with FAPI?

  * Needs review 




Issues (Dave)
==================
* #554 - Mention U of Stuttgart researchers in Acknowledgements

  * Will take names from Paper and add to Attacker Model and Security Profile
  * Dave will create PR

* #557 - [FAPI 2.0] Move "MTLS Protection of all endpoints" from [Message Signing] to [Security Profile]

  * WG decided it should be removed from Message Signing and moved to Security Profile
  * Will perform change after Message Signing is in ID

* #555 - Tracking: Implementers of FAPI 1.0 and FAPI 2.0

  * WG members are asked to add known implementations 
  * Some banks in Japan use FAPI but it is not required by regulator

* #553 - More details on obtaining tokens for existing grant use case

  * Provides more details about using existing grants
  * It is unclear about the grant action to use
  * Client should tell AS what action to use otherwise result may depend on AS
  * Refresh token rotation is discouraged for FAPI 
  * User must go through full authorization flow to get a new token
  * For this use case, clients should specify Merge as the action
  * Many implementations refresh refresh tokens upon use during validity period
  * UK-OB refresh tokens are tied to lifetime of consent
  * The semantics differences between the grant and the refresh token is not clear adding to the confusion
  * Refresh token is independent of grant
  * Further discussion is needed



AOB (Dave)
=============


Chat Transcripts
=============

Mike:

US I assume FAPI WG has discussed the CFPB announcements from Money 20/20 on open banking regulation. If anyone has heard about comment periods being open or anything please keep WG updated including Gail.


Canada Open banking lead Abraham made public comments at a conference the Thursday before thanksgiving on their plans. https://www.theglobeandmail.com/events/article-mapping-canadas-path-to-open-banking/

Open Banking Implementation Website is hosting all the results of the working group meeting materials and conclusions for last 6 moths. They plan to move to data sharing in 2023 (not payment). I have not read all information, but they are closed analysing UK, Australia and other models around consumer data rights, and specifically mention that OBIE uses OIDF to certify and Australia does not. https://www.canada.ca/en/department-finance/programs/financial-sector-policy/open-banking-implementation.html


The call adjourned at 15:__