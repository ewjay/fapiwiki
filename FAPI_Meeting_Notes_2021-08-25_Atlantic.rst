============================================
FAPI WG Meeting Notes (2021-08-25) 
============================================
* Date & Time: 2020-08-25 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-08-25_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Nat, Mike L., Brian, Daniel, Joseph, Francis, Steiner, Takahiko, Travis, Stuart, Kelly, Ali, Torsten, Mark@Curity, Dave. Gail, Chris, Dima, Lukasz, Danillo, Edmund, Kosuke
* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Voting on Grant Management started: Link:
https://openid.net/foundation/members/polls/246

Events (Dave/Nat)
======================
EIC (Dave)
---------------------
Mike L. is in contact with event organizers about travel restrictions etc. 

Will share information once it’s available.

PCR test with 72 hours of arrival is needed from US. 

US and UK - double vaccination needed. 

* Workshop presentation: https://docs.google.com/presentation/d/13KT5IEXh65IJiLnW5cPYKe4cterLhupaI4tYEstcbIo/edit?usp=sharing
* Proposed workshop timetable: https://docs.google.com/document/d/1IrV_s7djw6tm1Q7iZbfGikqj-DhsgL3loffNCPSPxJg/edit?usp=sharing

OAuth Security Workshop (Daniel)
-------------------------------------
* Virtual event planned for Nov 30 -  Dec 1, 2021
* https://barcamps.eu/osw2021/
* https://oauth.secworkshop.events/

Daniel is asking for suggestions on potential session topics on the event website.


Japan Workshop (Nat)
------------------------
OIDF Japan had a virtual meeting yesterday with 540 registrants, but some had to be waitlisted due to 500 limit on Zoom.

Discussed FAPI, Grant management


FAPI Webinar (Travis)
------------------------
Also had a webinar yesterday with 70+ registrants. 

It was recorded and will be available on demand later.



External Organizations (Dave/Nat)
===================================

Australia (Dima/Joseph)
------------------------------------
Mike L. reported that the outline for  the open standard analysis  report by Mark Haine was shared with CDR team.

DSB call Thursday evening. 

The DSB team published their decision regarding the future direction of the CDR info spec profile.

https://github.com/ConsumerDataStandardsAustralia/standards/files/7043506/Decision.182.-.Information.security.uplift.for.write.-.Final.pdf

Significant work remains to be done in transition to FAPI 2.0

The document provides clear signal that CDR is in alignment with FAPI.

Australia went live with Open Banking with just read only. 

Will try to introduce payment initiation on 2 years.

One of the prerequisites have been identified:

* Need fine grained consent and
* improved strength of  authentication



Berlin Group (Francis/Mike.L)
--------------------------------
No updates

Brazil (Mike)
---------------------------
* Central bank is considering moving the deadline from Aug. 30 to a later date. 
* Certification team was asked to hold on on processing phase 3 certifications
* Quite a few certification submissions were received. 
* Waiting for feedback from Central Bank via Mirow on updated milestones
* RP community group pilot is being set up to encourage RP certifications by providing RP knowledge base for FAPI certification.
* Filip S will join the group to provide expertise.
* Chris: Banking certification should go first, then RPs. 
* Banks having a hard time understanding what needs to be done between CG, Mirow, and OIDF with hard dependencies. 
* Phase 3 tests require Payments API but Payments API was just published.
* Only banks are allowed on the directory makes it a challenge for smaller banks to test.
* But regulators are listening and allowing more time.
* 18 ph.3 banks
* Gail banks and implementation partners are under unrealistic expectations. A breakout group to share best practices under change management etc. would be valuable. 
* We should make it smoother than other regulators can follow without fear. 
* Travis pointed out the importance of openness and ability to certify. 
* Joseph pointed out that certifications for Banks and vendors are different.
* Danillo and Travis pointed out that vendors cannot access DCR. 
* Joseph asked vendors to get in touch with certification@oidf.org if they have problems certifying.  

FDX (Mike)
------------------
* FDX has been quiet since the last meeting with updated partnership proposal.
* MileL and Gail will follow up



UK (Fiona/Ralph/Chris)
--------------------
* New 3.1.9 is out for public comment. Has minor changes.
* Due for publication by the end of September
* Future of OBIE is still unknown. Recommendations will be published soon.



Russia (Don/Dima)
--------------------
* Potentially doing official translation for OIDC and FAPI in Russian. 
* Waiting for feedback from Russia. 

Middle East and North Africa (Ali)
-------------------------------------
* No updates. 
* In a week time, probably have a zoom call with Gail/Don. 
* Saudi Arabia is closed to start Open Banking following the model in UK. 

Canada (Gail)
------------------
Announced the intent to start Open Banking. 

If you are involved, please get in touch with Gail. 

Some discussion on the consent model. Chris. 

PRs (Dave/Nat)
=================
n/a

Issues (Dave/Nat)
=====================

#432 – FAPI2 Trust Framework structure
-----------------------------------
https://bitbucket.org/openid/fapi/issues/432/fapi2-trust-framework-structure

FAPI 2.0 will remain a security profile but will have interoperable way to do advanced authorization

Grant Management and RAR will become optional separate specs to create a framework of specifications (Attacker model, implementation advice, etc…)

Work on Advanced Authorization profile will use RAR and Grant Management

Will leave issue open for visibility


#433 – Track FAPI compliant RP libraries
------------------------------------
Feedback is welcome on the library information sheet: 

* https://docs.google.com/spreadsheets/d/1vO0FJY9FDeq3Z5CPkbfM26ZSBHuRZpjclPCYkRreAvU/edit#gid=0

#426 – FAPI 2 - Multiple audience values in client authentication assertions
---------------------------------------------------------------------------------
Concerns against the proposal were expressed by multiple participants. 

From a security perspective, there aren’t any reasons to have multiple audience values in a client authentication assertion.

Limiting it to a single value might cause more problems due to ambiguity on what the proper audience is. This might hurt interoperability.

Does a single audience require it to be a single string value versus a single element array?

Audience is an OR statement so requiring the receiver to understand all audience values will affect general purpose libraries interoperability.

AOB (Dave/Nat)
=================
* Please vote for CIBA Final. Voting link: https://openid.net/foundation/members/polls/241
* Please vote for Grant Management 1st Implementer's Draft: https://openid.net/foundation/members/polls/246 


The call adjourned at 15:__ UTC