============================================
FAPI WG Meeting Notes (2020-11-04) 
============================================
* Date & Time: 2020-11-04 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: 

  * Brian Campbell
  * Chris Michael
  * Daniel Fett (yes)
  * Dave Tonge
  * Dima Postnikov
  * Don Thibeau
  * Francis Pouatcha (adorsys)
  * Joseph Heenan (OpenID Foundation)
  * Nat Sakimura (OIDF Chair)
  * Bjorn Hjelm (Verizon)
  * Brian Campbell (Ping Identity)


* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================


1.   Roll Call
2.   Adoption of Agenda (Nat)
3.   Events
4.   External Organization

     4.1.   Berlin Group (Francis) 
     4.2.   ETSI (Dave)
     4.3.   Australia (Stuart)
     4.4.   European Commission (Mark/Torsten)
     4.5.   UK (Ralph)

5.   Drafts

     5.1.   FAPI 2.0 (Daniel)
     5.2.   HTTP Signing (Dave)

6.   PRs (Dave/Nat)
7.   Issues (Dave/Nat)
8.   AOB


Events 
======================

OBIE Webinar (Chris)
-----------------------
Webinar on Response to alternative replacement  for EIDAS certificates in UK..
9:30 -11 UK time tomorrow.
Message Chris for an invite


Launch Event for variable payment 
------------------------------------
OBIE doing launch event on 11/11 at 10:00 AM to 12:00 PM UK time.
Introduces new requirements and draft standards for long lived consent for payments initiation.

 

External Organizations
========================
Berlin Group (Francis)
------------------------
No updates
Francis still working with co-Chair of the group on how to bring the BG’s market side and FAPI together.



ETSI (Dave)
---------------------
No updates.

ETSI has agreed to some of the headers in spec but not to other changes.
Waiting to hear back from them in regards to working together.

Dave, Brian, and Francis had a call. Identified 2 different streams of work.
Francis’ proposal stated in issue #297 - Open Banking Europe JWS PROFILE for OpenBanking regarding slimmed down signing profile 
Work is continuing

Dave and Brian are exploring the possibility of HTTP signing profile which is a lightweight extension of what’s defined in DPOP.



Australia (Dima)
------------------------
2nd phase of consumer data sharing is live from 1-Nov-2020 (additional account types, joint accounts and cdr_arrangement_id for revocations). PAR will be introduced before February 2021 (mandated from November 2020  but exemptions were granted to some if not all data holders).

Joseph, Don and the team is working on OIDF Conformance Test Suite proposal (follow up letter) for collaboration for Australia.

CDR regulator restructure is coming. The exact details or impact is unclear.

We should finalize the letter and then make a decision om how/where to send (e.g. blog, letter, etc..).
Need to stress the importance that OIDF is willing to work with authorities and the importance of standards adoption and conformance test suite to ensure standards integrity.



European Commission (Mark/Torsten)
------------------------------------
No updates



UK (Ralph)
---------------------
Sam and Chris started looking at extended attributes for bridging banks that provide PSD2 data to banks providing extended attributes for identity (e.g. Bank ID). 
OBIE looking to extend APIs beyond limits of PSD2.
UK has 4 more FAPI certifications:

* Barclays
* RBS
* NatWest
* Ulster

Don to post blog post referencing new certifications and can be used to point this out to Australian community that FAPI certifications are increasingly gaining traction.

Chrise suggested that FAPI certifications get its own part in the certifications page as opposed lumping them all with regular OIDC certifications.

ODIC executive committee will consider new program on how to display and share results of conformance testing.
Might be good to have separate profile certifications. E.g. national profile (UK, CDR, 5.0)
Send feedback and suggestions to Don.







Drafts
===========
FAPI 2.0 (Daniel)
-------------------

Concise list of compliance/requirements is preferable to saying “shall adhere to security BCP”.
Will do that in next revision.
Baseline profile is close to implementer’s draft.
Advanced profile still requires work on HTTP signing.
Baseline can proceed to implementer’s first. 
Nat will solicit feedback from the mailing list in this regard.


Will remove the recommendation for distinct `redirect_uris`. 
Will make use of the `iss` parameter in the authorization request.


HTTP Signing (Dave)
----------------------

Francis, Dave, and Brian will come up with a potential solution based on DPOP for the WG.

There is no desire in UK to adopt new changes.

Francis is also waiting to hear back from OBIE to corroborate on a potential solution.


PRs (Dave/Nat)
=====================
Pull request #205  - opaque access tokens 
-----------------------------------------------------
* Use “Clients are expected to treat”
* Link to  ISO Directive Part 2 need to be fixed

ACT: Nat will create a new issue

Pull request #191  - 
-----------------------------------------------------
* Pending update from Dima

Pull request #163  -  Add clarification on mix-up mitigation
-----------------------------------------------------------------
* Daniel will update with iss changes

Pull request #206  - Add references to security analyses
--------------------------------------------------------------
* Some attacks are possible under certain circumstances
* Code can be phised 
* Need to refine text and provide more context




Issues (Dave/Nat)
=====================


AOB
==========================


The meeting was adjourned at 15:00 UTC.