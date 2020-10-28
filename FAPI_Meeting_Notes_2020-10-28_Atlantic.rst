============================================
FAPI WG Meeting Notes (2020-10-28) 
============================================
* Date & Time: 2020-10-28 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call 
===========
* Attending: Nat, Bjorn, Don, Kosuke, Stuart, Thakhiko, Joseph, Brian, Francis Dima Dave, 

* Regrets: Daniel
* Guest: 

Adoption of Agenda (Nat)
===========================




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
* Dave gave a talk. 
* A vendor gave FAPI Workshop. Akana. 
 

External Organizations
========================
Berlin Group (Francis)
------------------------
https://www.berlin-group.org/single-post/press-release-berlin-group-starts-new-openfinance-api-framework

* Taskforce: Banks only. Now other FIs including insurance. 
* Advisory board: Francis sits here. 


ETSI (Dave)
---------------------
OBE signature profile coming out. They did not accept base64 proposals. 

Dave, Francis, and Brian will be coming up with a signature draft for the WG to consider. 



Australia (Stuart)
------------------------
Consent revocation proposal adds a lot of complexity. 
There is no standards to built upon. 

* https://github.com/ConsumerDataStandardsAustralia/standards-maintenance/issues/247


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