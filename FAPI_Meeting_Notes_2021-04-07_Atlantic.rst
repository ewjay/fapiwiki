============================================
FAPI WG Meeting Notes (2021-04-07) 
============================================
* Date & Time: 2020-04-07 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-04-07_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
* Attending: Nat, Dave, Don, Kosuke, Lukasz, Daniel, Dima, Francis, Joseph, Stuart, Brian, Torsten, Ralph
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* 




Events (Nat)
======================

Austalia FAPI Workshop
----------------------------------
* EventBrite listing is now available 


External Organizations (Nat)
================================


Brazil
-------
* No new updates
* Recommendations were adopted so everyone can begin learning


FDX
-----
* Global Summit April 15
* Joseph will be presenting a topic on FAPI and certification

W3C Payments
-------------
* General consensus was that there are sufficient placeholders like storage of keys etc.. that could be used for generic payment types.



UK (Don/Ralph)
-----------------
**OpenFinance **

* Some orgs are pushing open savings, investments, and pensions
* Dave pushing for standards and conformance tests
* There is broad acceptance and alignment with FAPI but still requires accreditation, regulatory onboarding, trust frameworks, etc..

* Federation spec can potentially be recommended for directory
* OpenBanking Brazil FAPI certification directory has been accredited. Directory based on Federations spec.
* Would be helpful to work out how to collect the various standard into a ecosystem
* Ralph will share some ideas to the mailing list regarding the standards, where they’re used, the various actors


FAPI 2.0 Baseline and Attacker Model
====================================
* Will start the process for implementer’s draft 
* Requires 45 day review period. 
* Send the draft to Mike Jones, OIDF Secretary to start review period
* Dave and Daniel will prepare document for initiating the process
* Members are asked to review the drafts


PRs
===================

pull request #258 - Add a suggested transition process for FAPI 1.0 ID2 -> Final
----------------------------------------------------------------------------------
* Reviewers requested


pull request #259 Adds copyright and license to  document
----------------------------------------------------------------------------------
* Approved and merged



pull request #260 - Resolve 404 errors when accessing FAPI1 draft locations
----------------------------------------------------------------------------------
* Approved and merged



pull request #251 Grant Management: Use cases section added
----------------------------------------------------------------------------------
Feedback requested

Outlines supported and unsupported use cases and related issues

* Basic use cases:

  * Revoking a grant
  * Replace grant details
  * Update grant details
  * Support concurrent grants

* Unsupported Use cases

  * Historical grant, authorization or consent records
  * Consent resource shared with other parties


Lukas asked if there is a need for API to list grants for a client

Torsten asked what would the client do with such data?

Currently, the user is not associated with a grant. Exposing session api is very dangerous.

You need to share a common user identifier between data holder and data recipient

The client should already have knowledge of the grants.

Could be used for cleaning up grants, list and then delete, but it’s an edge case.

Could be added as extension later, but the core grant management should keep things strict to reduce attack * surface vectors.


Issues
==========

#397 - query over certification test for access tokens being revoked when authorization codes are reused
----------------------------------------------------------------------------------
* Can be closed
* leaving open to link to conformance test issue, Joseph wil update conformance suite issue tracker

#400 - create bitbucket pipeline for converting markdown files into html
----------------------------------------------------------------------------------
* eKYC has pipeline which could be used for FAPI 2.0
* Already works on Grant management
* Stuart will work on pipeline for FAPI 2.0
* OIDF should have its own Docker image location




Chat Log
============