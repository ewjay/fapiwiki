===========================================
FAPI WG Agenda & Meeting Notes (2023-05-18) 
===========================================
Date & Time: 2023-06-16 00:00 UTC
Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09 


.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 00:00 UTC. 

Roll Call (Anoop)
=====================
* Attendees:   Dave, Gail, Mike, Victor Lu, Chris Michael, Dima, Justin, Brian, Nat
* Regrets:    

Agenda

* Events Update

* * OSW - OAUTH sec Workshop - https://oauth.secworkshop.events/osw2023 
* * IETF

    July 22-28, 2023. San Francisco, USA
    https://www.ietf.org/how/meetings/117/

* Liaison/Ext Org
* * Saudi
* * FDX
* * Brazil
* * AU
 
* Issues
* * 599 : FAPI Acronym - https://bitbucket.org/openid/fapi/issues/599/fapi-acronym
* * 570 Deprecation & removal of FAPI 1 Implementer's Draft conformance certification tests/programme. OBIE getting ready to transition to FAPI1 final sometime next year. Joseph is in discussions with them regarding implications - https://bitbucket.org/openid/fapi/issues/570/deprecation-removal-of-fapi-1-implementers 
* * 466 - Proposal for FAPI DCR/DCM (Dynamic Client Registration/Management) profile
    Priority dropped since Australia decided not to use DCR, no other ecosystem waiting for DCR
    Priority given to using Federation with FAPI (OPIN and Open Finance Brazil is considering using 
Federation) - https://bitbucket.org/openid/fapi/issues/466/proposal-for-fapi-dcr-dcm-dynamic-client 

* * 487 - RS must check x-fapi-interaction-id is an UUID or IP address
    Interaction ID was removed but is mentioned in implementation advice.
    May need to add additional clause  https://bitbucket.org/openid/fapi/issues/487/rs-must-check-x-fapi-interaction-id-is-an


Events 
=====================


OSW - OAUTH sec Workshop 
--------------------------
https://oauth.secworkshop.events/osw2023


IETF
--------------------------
 July 22-28, 2023. San Francisco, USA https://www.ietf.org/how/meetings/117/


EIC OIDF Workshop
--------------------------
presentation is published - https://openid.net/wp-content/uploads/2023/06/OIDF_Workshop-at-EIC_FINAL_2023-05-09.pdf

Next OIDF workshop will be prior to Fall IIW on Monday October 9, 2023 in Mountain View, California





Liaison/Ext Org
================================
Saudi
--------------------------
Finished phase 1certifications

Will discuss phase 2 in call with them next week

FDX
--------------------------

Brazil
--------------------------
Continue to process OpenFinance certifications

Elcio Calefi from Chicago Advisory Partners was at Identiverse and had discussed ongoing adoption of FAPI and certification. Normal recertification is expected.

OPIN - still a few phase 1 certifications trickling in.Currently, in discussion with OPIN board on recertification requirements. Anticipate updates by next week and Q3 recertifications.

AU
--------------------------
ConnectID - In discussion for direct funding for ConnectID OP & RP tests and pricing bundles.Will be finalizing in the next 2 weeks.

OB Canada
--------------------------
Mark Hain and Gail spoke with OB lead last week. Finalizing analysis and working on writeup.

Asia
--------------------------
Deciding on which Asian countries to visit prior to OpenID Japan meeting in Jan 19, 2024

Anyone with information on prospective markets may contact Gail

Latam
--------------------------
Also discussing with Chicago Advisory Group and central bank regarding a roadshow

University of Stuttgart & Australian Treasury
--------------------------
Will have meeting next Monday regarding scope of work for Package 3

Gail sent via Chat


FYI these are the components in Work Package 3.0, which would not start until after Work Package 2.0 is complete. I want to ensure we have an idea of the high level scope and approach, and identify any co-funding partners interested in this work.

o FAPI-Grant Management
o Security Event Token (SET) [RFC8417]
o OpenID Shared Signals and Events Framework Specification 1.0 - draft 01
o OpenID Continuous Access Evaluation Profile 1.0 - draft 02
o OpenID Connect for Identity Assurance 1.0

Only Grant Management is relevant to FAPI WG

Need to discuss with regulators if there are concrete plans for each of the specs (SET, CAEP, IdA), otherwise security analysis will be difficult

Need to setup a subgroup across working groups to work on strategic direction before beginning analysis

Website
--------------------------
WG page is outdated

Old site content was moved over.

New issues can be filed at https://docs.google.com/spreadsheets/d/1xBvK2hgB7eTjLVkdEa39dSmN61bacmDF/edit?usp=sharing&ouid=109991067428230720221&rtpof=true&sd=true

Issues are currently being resolved.

Need to update the  WG charter or add explanation regarding direction taken



PRs
==============================

* PR　#420 - Add draft to FAPI 2 SP title

  * editorial

* PR #417 -ciba refactor to support FAPI2

  * Not ready yet, need to address feedbacks

* PR #411 - attempt at clarifying request-response binding

  * Jusin to review feedback and approve. Message Signing removed whole section on HTTP signing and agreed to use IETF HTTP signatures spec. 
  * Just signing request and response is insufficient for binding. Need to sign all relevant parameters.


Issues
==============================

* #604 - Please put "Draft" in the title of drafts

  * Will leave open
  * Waiting for PRs for all specs

* #603 - Require servers to allow for clock skew

  * Allowing for clock skew is not required but is desirable for interoperability
  * Adding to specs would be good for interoperability
  * Filip recommended Conformance test issue warnings for clock skew but may result in interoperability problems 
  * Should allow for several minutes of clock skew. 
  * Should be general so as not to be specific to DPoP
  * It is common to reject future iat within some tolerance. Spec doesn’t have normative language so should not be done.
  * Private Key assertions does not use iat 
  * Adding some general guidance on reasonable clock skew is a good idea
  * Conformance suite should issue failure if clock skew is not allowed to increase interoperability
  * Iat clock skew problem is more likely to manifest than exp so that can be highlighted as an example
  * A note makes sense but may be ignored if not made a requirement
  * Skew duration should take into context the validity period
  * Conformance suite can determine the minimum successful clock skew for tests
  * Can copy phrasing from DPoP spec

* #487 - RS must check x-fapi-interaction-id is an UUID or IP address Interaction ID was removed but is mentioned in implementation advice

  * Removed from security profile since it’s not related to security
  * Put into errata for FAPI1 and then put into implementation and deployment advice for FAPI2
  * Clients send value but no normative text on servers to check it
  * Shall check for UUID format, log the value, and send back in response
  * Add shall log the value

* Victor asked 

  * my beginner question. I Found this thread about jwt parsing complexity concern. How to respond if discussion about x.509 and jwt parsing complexity security concerns come up ? https://news.ycombinator.com/item?id=16159301
  * Asked how to counter argument on why JWTs are bad
Victor will file new issue


 
Next Call
==============================
Next call will be an Pacific Call. 
Next Pacific call will be in two weeks (06-01-2023 @ 5pm PST) UTC - 06-02-2023 1:00 AM.