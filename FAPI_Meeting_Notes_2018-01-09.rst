============================================
FAPI WG Meeting Notes (2018-01-09)
============================================
Date & Time: 2018-01-09 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:05 UTC. 

Roll Call
===========
* Attending: Bjorn, John, Nat, Dave, Don, Tom, Joseph, Edmund
   * Guest: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* 

External Orgs 
==================

ANSI/X9 (Nat)
------------------

ISO/TC 68 (Nat/Dave)
----------------------

Open Banking (Joseph)
-------------------------
* https://openbanking.atlassian.net/wiki/spaces/DZ/pages/23856067/OB+OIDC+Conformance+Suite

* Conformance suite is available.
* Banks will go live on Saturday, but some may have conformance issues.


* OBUK's directory solution is Europe wide
* Can join by registering with gateway regulator of European country

* Conformance test suite has no test for Oauth token binding
* There are no implementations to test against yet 
* John mentioned Ping Access has support for Token Binding
* Token Binding spec is stable but OAuth Token Binding still not finalized
* It is too soon for proper test for Token Binding




FS-ISAC Response (Anoop)
---------------------------------
Files: Privately shared. Please contact Anoop or Nat to get the document. 

Upcoming Events
======================
Open Banking (Don)
---------------------
We have planned an OpenID/Open Banking workshop for the afternoon of 30th January - unfortunately as Nat is not available, we won’t have a FAPI working Group meeting that day. Venue is RISE London, Barclays Accelerator, 41 Luke Street, London (near Shoreditch) Please feel free to register at this Eventbrite link if you and your colleagues wish to attend: https://www.eventbrite.co.uk/e/openid-foundationopen-banking-implementation-entity-workshop-tickets-42005257857

Remote participation may be available


API Days (Nat)
-----------------
Nat will be attending to do presentation about FAPI and OpenBanking


Specs Discussion
=======================
CIBA Spec Update (Dave)
---------------------------
* PRs -- https://bitbucket.org/openid/fapi/pull-requests/41/ciba-imrovements/diff
* Updated issues
* Device ID 
* Feedbacks from F2F in November should be properly reflected
* Post the notice to the list when PR accepted 


* Results from discussion from the November 2017 F2F are that sending device ID may not work. However geo-location and device type may be of use. Terms for device type are not specified and out of scope

* Members asked to review CIBA spec


User questioning API (Bjorn)
--------------------------------
* Had discussion on 12/20/2017
* How does FAPI WG want to proceed? Is it to proceed with making User Questioning profile for FAPI or does WG need more discussion and dialogue and are there unaddressed questions?
* WG will need to look at use cases first but it seems User Questioning will be a more restricted use case
* User Questioning supporters want to move spec forward
* Interest from FAPI validates some enhancements and will be accommodated if possible



Implementer's Draft (Edmund)
--------------------------------
* Most issues have been resolved and closed.
* Some assigned issues are still open
* Assignees should double check if issue is still valid
* Nat will review issues 
* WG feels that new implementer's drafts should be postponed until CIBA spec is ready in order to garner more exposure  



Dynamic Client Registration (Pam)
-----------------------------------
* Skipped since Pam was not available for discussion

Files: https://bitbucket.org/openid/obuk/src/4630771db004da59992fb201641f5c4ff2c881f1/uk-openbanking-registration-profile.md?at=master&fileviewer=file-view-default

* What OBUK is working on is different and closer to the earlier version of OIDC registration. 
* It could, however, be reasonable for their use cases. 
* Need to be clear on the requirements, e.g., non-repudiation, etc. 
* We could bring some idea back to OIDC and OAuth. 
* Perhaps we can discuss more in details in the Atlantic call. 


AOB
===========

* A question was raised that since that most organizations are taking FAPI Part 2, is there a reason to keep Part 1?
* OBUK uses Part 2 even though their API is read-only
* Nat stated that FS-ISAC uses Part 1
* Will raise question to WG


Next Call (Atlantic)
-----------------------
The next call is scheduled to be in the Atlantic time zone. 

* The meeting was adjourned at 23:42 UTC.