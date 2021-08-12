============================================
FAPI WG Meeting Notes (2021-08-11) 
============================================
* Date & Time: 2020-08-11 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-07-21_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:04 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Nat, Dave, Joseph, Kosuke, Brian, Dima, Dominbos, Ion, Daniel, Fiona, Stuart, Taka, Lukasz, Filip, Ralph, Francis, Daniello, Edmund. 
* Regrets:
* Guest: Mike Lesczc

Adoption of Agenda (Dave/Nat)
================================
* 

Events (Dave/Nat)
======================
EIC (Dave)
---------------------
Nat, Dave, Joseph, Ralph, etc. would be there. 

Proposed workshop timetable: https://docs.google.com/document/d/1IrV_s7djw6tm1Q7iZbfGikqj-DhsgL3loffNCPSPxJg/edit?usp=sharing

OAuth Security Workshop (Daniel)
-------------------------------------
Virtual event planned for Nov 30 -  Dec 1, 2021

Daniel is in the process of setting it up before making an official announcement.



External Organizations (Dave/Nat)
===================================
Mike L. Report
--------------------------
Dave reported Mike's written report. 

### FDX

No updates. Discussed with Don and he suggested we allow Gail to pick this up when she's back from family leave in a couple of weeks.

### Australia

#### DSB team

Working to coordinate a call as they are interested in getting involved in the FAPI WG. They have signed a contribution agreement.

#### CDR team

Call scheduled tomorrow, August 12th, to introduce the Considrd Consulting team and to scope the FAPI analysis paper that the CDR team has requested and to be supported by directed funding.

### Brazil

Phase 2 - still have approximately 10 banks to certify and have missed the updated deadline. Awaiting feedback from the Mirow team in BR on when we should expect the remaining Phase 2 banks to certify.

Phase 3 - we  have recommended new milestones based on the payments API have just been confirmed and now waiting for Raidiam to update the mock bank. There are 160 banks registered for Phase 3 with 63 banks (66 implementations) confirmed. We have started receiving Phase 3 certification requests. And we have approximately eight Phase 3 banks joining the Foundation.
RP Community Group Pilot - proceeding with coordinating this pilot to be supported by $50k directed funding from Mirow. Goal is to create a community group for information sharing as well as best practices, reference implementation, etc. so that RPs are successful in FAPI conformance and certification. With this pilot confirmed, the central bank will next mandate that RPs certify. A key component of the central bank mandating RP certification was to get the certification fees to the member price of $1,000 which this pilot will enable. We anticipate Filip Skokan rejoining the certification team to help moderate the community group and provide SME to the BR ecosystem. 

### Berlin Group

Nat provided additional background earlier today on the prior conversations and the goals of the subcommittee that I will review with Tom Smedinghoff.


Australia (Dima/Joseph)
------------------------------------
Meeting scheduled for Tomorrow and Tuesday next week with ACCC to scope request from John Otway.


Berlin Group (Francis)
----------------------------
Setup some time in one of the September WG meetings to discuss how to proceed and clear IP issues on both sides.

OIDF is still performing legal review. Nat will update once there is a definitive answer from OIDF consul (Tom).

OIDF exploring ways to use the model used for the OIDF Workshop “Note Well”.  Will show the “Note Well” at the beginning and only those who have agreed to the “Note Well” will be allowed to stay. Awaiting feedback from the consul regarding this matter.

Francis and Danillo will on work on some material and present to the group for feedback.



Brazil (Ralph/Taka)
---------------------
* Last minute change on the spec. Signing is now mandated. Signed JWT. Everyone is madly implementing it. 
* Some suggestions to push back the deadline for the submission of the conformance test for Phase 3 to August 30. 
* Relying party testing meeting among the certification team planned for tomorrow. The team is considering following the UK examples. 
* We may also need to encourage the RP libraries to support FAPI. 

FDX (Don)
------------------
* Expected to adopt FAPI in the next Summit. 


UK (Ralph/Chris)
--------------------
* Ver. 3.1.9 is being published. Target release will be end of September.
* CMA supporting Variable Recurring Payment (VRP) for Sweeping transactions.. 
* Brand new payment type considered in the Roadmap, e.g., Smart Direct Debit. There is nothing similar outside of UKOB.
* Still waiting for CMA9's decision on the next step of the Open Banking IE. Still 2.5 weeks till we learn it. 

Russia (Don/Dima)
--------------------
* Russia: Russian Federation: Open API standards https://openbankingrussia.ru/open-api-standards/
* Live ecosystem with FAPI 1.0 I-D2. 
* Some certification programme. 
* Running in pilot mode, 2 banks and 1 fintech. FAPI 1.0 ID2. 99% up to the spec. Only the difference is the cypher spec. It may be mandated in 1 or 2 years. 

5.8.3.5. Криптографические ключи, используемые в протоколе TLS, и ключи протокола OIDC должны быть различными. 5.8.3.6. Должны использоваться только следующие криптонаборы: – TLS_GOSTR341112_256_WITH_KUZNYECHIK_CTR_OMAC (Р 1323565.1.020), – TLS_GOSTR341112_256_WITH_MAGMA_CTR_OMAC (Р 1323565.1.020), – TLS_GOSTR341112_256_WITH_28147_CNT_IMIT [37].

They had to write their own test suite but there may be value if OIDF could help by supporting their cypher suite. 

Dima is reaching out to see how OIDF can help.


PRs (Dave/Nat)
=================
Pull request #283 - FAPI Grant Management ID1 Review: Editorial Fixes
Will be merged when authors are ready


Issues (Dave/Nat)
=====================

#433 Track FAPI compliant RP libraries (Dave)
-------------------------------------------------
Joseph reported that for iOS AppAuth, it’s pretty much intractable a problem without forking the library, as there are various policies (e.g. supporting a very wide range of iOS versions and not pulling in third party libraries) that make it very hard to support FAPI. It was discussed a bit here https://github.com/openid/AppAuth-iOS/issues/290 though this was a while ago so I don’t know if much has changed. AppAuth is more intended for plain OIDC cases.

Daniel reported that on node.js, there are people uses Filip's library but otherwise they have to write their own. 

Stuart reported that on Java side Biza has one for their own use but achieving abstraction is challenging. 
As a crypto library, Nimbus one seems to be the most popular, but requires a lot of wrappings to make it worthwhile. 

Jose4J is another choice for crypto.

Can raise some issues to libraries with active maintainers.


#432 FAPI2 Trust Framework structure (Dima)
---------------------------------------------------
Looks like there is a consensus on the need for FAPI2 Advanced authorization profile spec. 

Naming and diagrams need review to make them less confusing.

New document to be prepared by Dima, Stuart, and Torsten to be adopted by the working group. 

Need to come to agreement on names and scope of specs.


#429 FAPI Certification with Lodged Intent or RAR - User Consent vs Technical Process Certification
------------------------------------------------------------------------------------------------------
Joseph explained to the WG that testing this is a bit complex, especially on the live bank system. 

There is no pushback for the need for it though. 

#412 FAPI 2.0 - Hard requirement to support Grant Management Requirement
--------------------------------------------------------------------------------
Consensus to remove hard requirement reference to Grant Management from the Baseline. 

As a step, there needs to be a new document to put the removed material, then remove the reference. 

#434 Certification Team Query: error messages shown by OPs (Joseph)
--------------------------------------------------------------------------------
There is a range of possibilities: From factually not incorrect to informative to developers. 

Joseph believes the later is more useful for the integration work. 

WG opinion is sought. 


AOB (Dave/Nat)
=================
Please vote for CIBA Final. Voting link: https://openid.net/foundation/members/polls/241


The call adjourned at 15:01 UTC