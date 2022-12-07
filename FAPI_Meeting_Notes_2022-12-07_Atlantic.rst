===========================================
FAPI WG Agenda & Meeting Notes (2022-12-07) 
===========================================
* Date & Time: 2022-12-07T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-11-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 



* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Daniel asked if it is possible to provide the Stuttgart team with the number of implementations for FAPI 1 and 2. Nat replied that the number for FAPI 1 can be drawn from the certification results, but FAPI 2 is more challenging. It was decided to track it in the ticket that Daniel is going to make. 
* Peter reported ... 


Events (Mike L.)
====================================================

OIDF Workshop at Visa
-----------------------------
The presentation deck has been published

https://openid.net/workshops/openid-foundation-workshop-at-visa-monday-november-14-2022/

Identiverse 2023
-----------------------------
The call for presentations is open until January 6, 2023: https://www.abstractscorecard.com/cfp/submit/login.asp?EventKey=RDBGWULG 

EIC 2023
-----------------------------
The call for presentations is open until February 28, 2023: https://www.kuppingercole.com/events/eic2023/callforspeakers

Mike will be developing a spreadsheet for Gail and Mike to track OIDF submissions for both conferences.
Mike will communicate the above to all WG co-chairs via email. 

Joseph noted that it seems the earlier you submit for EIC, the better your chances of getting submitted. 

Open Banking World Congress
-----------------------------
To be held end of Feb 2023 in Riyadh

Don Thibeau may attend

Open Banking for Latin America Regulators
---------------------------------------------
To be held March 2023 in Rio

Details TBD



External Orgs & Liaisons (Mike L./Chris)
============================================
SAMA
----------------
OIDF is still awaiting their final KSA FAPI Profile specification and to develop the conformance tests. We communicated to SAMA that it would likely be the end of December or early January before the production tests and certification is available.

Other regional regulators are watching SAMA’s approach to Open Banking.

Brazil 
----------------
Chicago Advisory Partners, Administrator of Open Finance Brazil,  has joined the OIDF board and attended the board meeting on Nov 14.


Open Finance Brazil
----------------
The certification team continue to receive re-certification requests. 

OPIN
----------------
The certification team is starting to see initial FAPI certification requests and requests may increase throughout Dec.


Australia
----------------
Stuttgart has completed work package 1.

Need to create blogs to communicate completion.

Work package 2 is pending funding approval and contract release by Australian Treasury by the end of the week

Australia asked questions regarding JARM and encrypted JARM


Open Banking Cross Borders Paper
----------------
https://docs.google.com/document/d/176au5lZcR0vHbQG43wE7pZr7PBgVd7O7AqAzb6rqDzU/edit

Last call for comments will be sent



Open Banking Nigeria
----------------
The Central Bank of Nigeria has stalled on open banking since they released the draft guidance last May. It may be that their priorities have shifted from Open Banking to fighting inflation, releasing new currency designs, and pushing the e-Naira CBDC. Open Banking Nigeria have decided it wouldn’t be easy to pull off auth and authorization over USSD with OAuth2 and FAPI at this time however, the team is still exploring some ideas to see how to make this work.



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