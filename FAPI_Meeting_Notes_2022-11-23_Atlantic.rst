===========================================
FAPI WG Agenda & Meeting Notes (2022-11-23) 
===========================================
* Date & Time: 2022-11-23T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-11-23_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Daniel Fett
  * Dave Tonge
  * Dima
  * Filip Skokan
  * Jacob Ideskog
  * Joseph Heenan
  * Lukasz Jaromin
  * Nat Sakimura
  * Nik Kramaric
  * Pieter Kasselman
  * Takahiko Kawasaki
  * Bjorn Hjelm
  * Chris Michael
  * Kosuke Koiwai
  * Michael Palage
  * Ralph Bragg
  * Ramesh Narayanan
  * Takahiko Kawasaki


* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Daniel asked if it is possible to provide the Stuttgart team with the number of implementations for FAPI 1 and 2. Nat replied that the number for FAPI 1 can be drawn from the certification results, but FAPI 2 is more challenging. It was decided to track it in the ticket that Daniel is going to make. 

  * FAPI 2 tests need some updates. Authlete and Filip have tested.
  * Australia/Brazil/SAMA plans to migrate to FAPI 2

* Peter reported in IETF 115, there was strong support for cross device BCP.

  * There was call for adoption in OAuth mailing list
  * https://datatracker.ietf.org/doc/draft-kasselman-cross-device-security/
  * https://mailarchive.ietf.org/arch/msg/oauth/tm4ZUqrTvnbuEN4Dmt6Jabq_dtc/
  * Supporters are welcomed to participate in work



Events (Mike L.)
====================================================

OIDF Workshop at Visa
-----------------------------
The presentation deck has been published. Awaiting recording from Visa but will publish as soon as available.

Identiverse 2023
-----------------------------
The call for presentations is open until January 6, 2023: https://www.abstractscorecard.com/cfp/submit/login.asp?EventKey=RDBGWULG 

EIC 2023
-----------------------------
The call for presentations is open until February 28, 2023: https://www.kuppingercole.com/events/eic2023/callforspeakers

Mike will be developing a spreadsheet for Gail and Mike to track OIDF submissions for both conferences.
Mike will communicate the above to all WG co-chairs via email. 

Joseph noted that it seems the earlier you submit for EIC, the better your chances of getting submitted. 


External Orgs & Liaisons (Mike L./Chris)
============================================
SAMA
----------------
OIDF is still awaiting their final KSA FAPI Profile specification and hope to receive the end of this week. This is impacting Joseph and the team developing the conformance test. We communicated to SAMA that it would likely be the end of December or early January before the production tests and certification is available.

Open Finance Brazil
---------------------------
The certification team continue to process a large volume of re-certification requests. We are also receiving quite a few new FAPI certification requests from Brazil as well.

OPIN
------ 
The certification team is starting to see initial FAPI certification requests. OIDF and OPIN hosted a second FAPI outreach workshop recently for the OPIN ecosystem. Domingos Creado, with the certification team, delivered the workshop in Portuguese, which was very well received. I will be posting both OPIN workshop recordings to the OIDF website.

Open Banking Nigeria
----------------------------
The Central Bank of Nigeria has stalled on open banking since they released the draft guidance last May. It may be that their priorities have shifted from Open Banking to fighting inflation, releasing new currency designs, and pushing the e-Naira CBDC. Open Banking Nigeria have decided it wouldn’t be easy to pull off auth and authorization over USSD with OAuth2 and FAPI at this time however, the team is still exploring some ideas to see how to make this work.

Website
------------
Joseph sent a request to update the FAPI name on the website and microsite. 

Mike responded that it doesn't make sense to update the microsite as that will be sunsetted by the end of the year. That's now been scheduled and will be offline by December 7th. We will have online access to the microsite once sunsetted, as we will repurpose most of the content within the new OIDF website.

Bruno with Design Factory just installed a tool this morning on the current OIDF website to make it most efficient to update the FAPI name and help ensure I don't miss any instances. I will try to get to this later today, but it may be early next week as I'm out of the office tomorrow through next Monday for the Thanksgiving holiday.


PRs (Dave)
===============
* PR #390 - FAPI2 editorial and file name changes

  * Changed FAPI 2 Advanced Profile to FAPI 2 Security Profile and placeholders
  * Needs to fix build problems
  * Need update for other specs names also, CIBA, and Grant Management

* PR #388 - Fix some typos in Security Considerations

  * Editorial and spelling updates

* PR #387 - Fix typo in DPoP Proof Replay Security Considerations

  * Fixes typos

* PR #389 - Add grant metadata

  * Add metadata parameters for Grant Management
  * To be merged

* PR #386 - Replace reference to Lodging intent with the a reference to RAR

  * Need updates for comment

* PR #385 - Remove Financial from CIBA in line with FAPI?

  * Need to address Joseph’s comments



Issues (Dave)
==================
* #553 - More details on obtaining tokens for existing grant use case

  * The use case in spec where clients can obtain fresh access and refresh tokens based on existing grants, if they re-use the authorization requests, referencing the user's grant, and follow the rest of the authorization code flow, but it’s not clear how to proceed. Needs more detail on how to obtain new token and refresh token if there is no replace/merge.
  * Result of previous discussion : User needs to go through authorization flow and the intent was to not allow refresh tokens if you just have a grant ID. Need to go through authorization flow to get new tokens.
  * Dima will confirm if that is true.
  * Nik’s use case is to obtain new tokens for expired tokens but consent is still valid. Refresh token expires before the consent expires.
  * Might describe details in deployment advice. Leave refresh tokens open ended and make policy decision each time to grant refresh token or not. Refresh token rotation is discouraged in FAPI.
  * What parameters are needed to obtain refresh token given the same Grant ID.
  * 3.7 is not clear on how to obtain new token given a grant ID.
  * In this case, it needs to restart the authorization flow referencing the Grant ID and it’s up to the As to update or replace the grant.
  * Nik’s use case is to not update or replace the grant but reuse existing grant.
  * Section can be clarified that new authorization request must be started so that Grant ID does not act like a refresh token.
  * Dima will investigate and clarify the actions required.


* #210 - (ed) A number should be assigned to the last sentence in FAPI Part 2, 5.2.3

* #489 - Align FAPI-CIBA to FAPI2-baseline/advanced

  * Will discuss in a different call to decide on course of action.
  * Could update the existing spec to work with FAPI 2 if changes are compatible with FAPI 1
  * OB-UK and Brazil references CIBA so it may affect them
  * Will need to update requirements for FAPI 1 and FAPI 2 separately
  * Make signing conditional for clients when using FAPI 1


AOB (Dave)
=============
FAPI 2 Message Signing Last call has been sent to the mailing list.


The call adjourned at 15:__