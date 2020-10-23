============================================
FAPI WG Meeting Notes (2020-10-21) 
============================================
* Date & Time: 2020-10-21 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call 
===========
* Attending: Nat, Kosuke, Don, Ralph, Daniel, Joseph, Stuart, Brian, Francis, Steiner Dave, Brian, Bjorn, Dave, Dima

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================

* Events
* External Orgs
* PRs


Events 
======================

IIW (Nat)
------------------
It is going on this week. 
Lots of sessions around decentralized identity. 

FDX/OIDF (Don)
-------------------
You are not required to register for the workshop as a presenter but welcome to do so: https://www.eventbrite.com/e/openid-foundation-virtual-workshop-tickets-121075932373 
This is a direct link to the virtual workshop session: https://global.gotomeeting.com/join/825700629

Workshop will provide workgroups progress and summaries of activities.

There will be Keynote focused on FAPI with panelists (Nat Sakimura, Don Cardinal, Anoop Saxena)

 
IdentityNorth (Nat)
---------------------

Will be on 10/28-10/29, mostly about distributed decentralized identity

APIDays London (Dave)
-----------------------
* Next week. https://www.apidays.co/london
* 10/27 - 10/28
 

External Organizations
========================
Berlin Group (Francis)
------------------------
New name: openFinance API Framework
SUBSCRIBE TO OPENFINANCE PUBLICATIONS

 Cf. https://www.berlin-group.org/ofa


ETSI (Torsten/Dave)
---------------------

There was a meeting to discuss draft which was attended by one person.



Australia (Stuart)
------------------------

* Treasury is taking over Rule’s responsibility from the ACCC and some of the registers components.
* Daniel MaAuliffe- OpenBanking Product owner inside the Treasury seems to be listening.
* The big four mentoring meeting - doesn’t look like any of them will meet 100% of the requirements for November deadline.  * There are exemptions until Feb 2021 for PAR
* Intuit is officially a data recipient by ACCC -  requires (ASAE) 3150 
* Only a 5th bank - Rachel Australia Bank will meet  requirements
* There's consultation on the next round of rules that's going to alleviate or soften the accreditation.
* May draft an open letter to them.


European Commission (Mark/Torsten)
------------------------------------
* 


UK (Ralph)
---------------------

* No updates

PRs (Dave/Nat)
=====================

* pull request #199
    -  editorial / accepted 
* pull request #200 regarding returning PII in ID Token
    - Encryption is not encourages, claims can be returned in the back channel
    - Encryption is abd for third parties
    - Change to "should not return PII in ID Token, but if you do, then you should encrypt"
* pull request #198 - unclear TLS ciphersuites language
    - Joseph concerned about new text.
    - BCP195 had recommended and permitted ciphers 
    - Don’t want to allow not permitted ciphers
    - Old text allows only BCP195 permitted ciphers whereas new text allows non-permitted ciphers.
    - Old disability/accessibility software may be using old ciphers which will limit their access.
    - To be continued...
* pull request #197 - added BCP195 reference links
    - Accepted
* issue #329 - Rename FAPI Titles
    - Most support for changing to Part 1: Baseline and Part 2: Advanced
    - Keeping "Part 1" and "Part 2" since they will be submitted to ISO which will require putting these in the titles
    - Daniel concerned that Part 1 Advanced is closer to FAPI 2.0 Baseline
* pull request #163 - mix-up mitigation
    - Not sure whether to go with isser parameter or new mechanism
    - OAuth WG proposing mix-up mitigation proposal draft
    - Can either standardize at OAuth or FAPI WGs
* issue #330 - potentially misleading language WRT JWT ATs - language is confusing
    - Suggested removing "opaque"
    - Intent is tat AT is not to be consumed by clients
    - remove "opaque" and reword note, make it similiar to RFC 6749 language that AT is usually opaque to clients






Drafts progress
=================
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


AOB
==========================


The meeting was adjourned at 15:00 UTC.