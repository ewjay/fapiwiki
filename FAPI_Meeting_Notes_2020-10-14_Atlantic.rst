============================================
FAPI WG Meeting Notes (2020-10-14) 
============================================
* Date & Time: 2020-10-14 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call 
===========
* Attending: 

 * Anthony Nadalin
 * Bjorn Hjelm (Verizon)
 * Brian Campbell
 * Chris Michael
 * Daniel Fett (yes)
 * Dave Tonge
 * Dima Postnikov
 * Don Thibeau
 * Francis Pouatcha (adorsys)
 * Joseph Heenan (Authlete)
 * Kosuke Koiwai (KDDI)
 * Nat Sakimura (NAT.Consulting)
 * Ralph Bragg
 * Bjorn Hjelm (Verizon)

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================

* Events
* External Organizations
* PRs
* Drafts
* Issues
* FAPI 1.0 Last Call
* OBIE / ETSI JWT Profile


Events 
======================
Open Banking (Chris)
------------------------
* 120 attendees
* Video avaiable
* Takeaway: Good opportunity to push libraries authors to get through the certification. 
* Implementers should use libraries if possible.
* Will send out survey for feedback later
* Will reach out to OIDC compliant implementers to test for FAPI certification
* EBA, FCA and other authorities don’t have any certification requirements yet
* Banks will not do it themselves without regulatory requirement or strong commercial benefit
* FCI and other regulators aren’t not very specific about which standards/certifications should be complied to.
* Seems to be too early phase for banks to be very specific technically
* Need to let EBA issue requirements instead of individual regulators
* Might take some security breaches before issuing requirements?
* EBA right now focused on customer experience complaints


IIF (Nat)
------------------
* Drew attention to IIF and OIDF collaboration
* FAPI and eKYC WG will be establish collaboration here
* IIF membership largely of regulators, law makers, and policymakers
 * Opportunity to point out merits of conformance, testing, and standards

 
FDX/OIDF (Don)
-------------------
You are not required to register for the workshop as a presenter but welcome to do so: https://www.eventbrite.com/e/openid-foundation-virtual-workshop-tickets-121075932373 This is a direct link to the virtual workshop session: https://global.gotomeeting.com/join/825700629
 
* Workshop will have keynote panel (Nat Sakimura, Don Cardinal, Anoop Saxena)
* Will talk about OIDF and FDX path going forward
* FDX acting like SRO (Self Regulatory Org)
* FDX announcing unofficial support of FAPI and collaboration of FAPI 2.0
* 3 areas of engagement

  1. Concurrent outreach/collaboration like Global Summit
  2. Concurrent technical collaboration
  3. FDX Increasing Conformance to OIDC and FAPI

     * Will drive demand for certification services
 

External Organizations
========================
Mexico (Chris)
-------------------

* Documents show support for implicit flow.
* Chris to try to find definitive source documents for requirements.
* Timeline is uncertain.



ETSI (Torsten/Dave)
---------------------
* Dave sent a draft response to FAPI mailing list regarding OBE/PRETA JWS HTTP Signing Profile for feedback. Will need to finalize it within the next few days.
* Profile uses JWS 7797 without base64 encoding payload
* May want to propose creating a more generic FAPI which they could profile into depending on their response.
* PRETA is attempting a commercial Open Banking directory for Europe. Seems like a enterprise version of OBIE. Supports literal interpretation os PSD2.
* None of the standards bodies have agreed to implement the draft spec yet.



Australia (Dima/Stuart)
------------------------

* Had another Data recipient accreditation.
* A version of the  rules consultation circulated focusing on different types of credited people sharing data in a few complicated scenarios.
* Last week, "conformance test suite" was presented.
* Accreditation process is very manual, hidden.
* Around July, they had a testing environment with a list of manual test cases.
* Test checks are not complete.
* It's designed for regulators instead of assisting participants for accreditation. It’s trying to remove industry testing environment.
* Maybe moving towards sandboxes?
* There are no mandates for Banks to support sandboxes.
* Industry testing environment ironed out a lot of issues due to data recipients and data holders connecting to each other.
* It’s essentially payload testing of contents not like FAPI testing different scenarios. Mainly focused on CDS specification.
* No timeline for banks to test each other’s APIs at the moment.



Berlin Group (Francis)
------------------------
* n/a till mid of November. 

European Commission (Mark/Torsten)
------------------------------------
* n/a


UK (Ralph)
---------------------


Drafts progress
=================
FAPI 1.0 Last Call (Nat)
-----------------------------
* Closes today
* Public review period will be for 6 weeks
* See Issues


* Revisiting question regarding changing FAPI 1.0 to Baseline and Advanced 
 * Still possible to provide feedback 
 * Changing from R/RW will affect introductory text
 * Also implementations already exist and refers to R/RW
 * Another suggestion was to call it Part ½
 * Nat will solicit feedback from group regarding name, will also create issue ticket


FAPI 2.0 Baseline (Daniel)
---------------------------
* Need to bring in more reviewers. 

FAPI 2.0 Advanced (Daniel)
---------------------------
* Main sticking point is signatures. #309. 
* ETSI and OBIE discussion is relevant. 

Grant Management (Torsten/Stuart)
------------------------------------


Issues (Dave/Nat)
=====================
#322 Editorial: Section 5.2.2.2.1. Duplicate Clause? (Ralph)
----------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/322/editorial-section-52221-duplicate-clause

A lengthy discussion on how to test. 
The discussion to be continued. 

PRs (Dave/Nat)
=====================
We did not have time to get to it. 

AOB
==========================
WG members should feel free to take editorial tickets on FAPI 1.0 and start sending PRs. 
Joseph would be greatful if folks can take some of his. 

The meeting was adjourned at 15:00 UTC.