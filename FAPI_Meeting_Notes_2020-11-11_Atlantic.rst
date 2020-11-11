============================================
FAPI WG Meeting Notes (2020-11-11) 
============================================
* Date & Time: 2020-11-11 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Bjorn, Daniel, Stuart, Dima, Takahiko, Joseph, Brian, Kosuke, Francis, Don, Dave

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
Adopted as is. 


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
Australia (Dima/Stuart)
--------------------------
* Status of 2nd phase of consumer data sharing that went live on 1-Nov-2020
* Open Letter
* CDR regulator restructure

Berlin Group (Francis)
------------------------
* Next week meeting

ETSI (Dave)
---------------------


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
* Kicked off variable paiments. 
* Consultation links: ttps://www.openbanking.org.uk/about-us/latest-news/obie-launches-variable-recurring-payments-and-sweeping-consultation/

Bahrein (Chris)
------------------
* BCB 
* https://bahrainob.atlassian.net/wiki/spaces/BH/pages/309985587/Security+Standards+and+Guidelines

Canada ()
------------
* https://ciostrategycouncil.com/

US-FDX ()
-----------
* Ping is now a co-chair of the technical group. 

Certification (Don)
=====================
Please provide your input to changs to the OpenID Foundation Directory of Conformance director@oidf.org the goal is to make the conformance list easier to navigate, etc

Drafts
===========
FAPI 2.0 (Daniel)
-------------------
Now ready to move to next stage. 


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