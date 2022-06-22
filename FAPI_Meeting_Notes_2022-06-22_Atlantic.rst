============================================
FAPI WG Meeting Notes (2022-06-22) 
============================================
* Date & Time: 2022-06-22T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

* Regrets: 
* Guest: 

Adoption of Agenda (Dave)
================================
* Whitepaper feedback. 

Events (Dave)
======================
Identiverse (Mike)
------------------------------
* F2F FAPI meeting Wednesday 6/22 normal meeting time (8AM local time) in Summit 2 room. 
* Remote attending available via normal GotoMeeting conference link. 
* Nat, Joseph, Mike, Riffat, Dave, Brian

IETF 114
------------------------------
July 23-29, 2022. Philadelphia, USA

https://www.ietf.org/how/meetings/114/


Internal Liaison (Dave)
================================
Security Analysis
---------------------------
* Need to get an update offline from Gail.  

Certification (Joseph/Mike)
----------------------------
* n/a


External Organizations (Nat)
===================================
Australia (Mike L.)
------------------------------------
* N/A

Brazil (Mike L.)
---------------------------
* Outreach workshop to support Open Insurance certifications. 66 to be certified by Sept 1. 
* Open Banking Brazil finalizing CIBA spec. Early-Mid July to finalize it. Certification to work on it then. 
* Coordinating with Chicago Advisory Partners to re-certify 200 by Dec. 15, starting in Sept. 


Berlin Group (Daniel)
--------------------------------
* N/A

Canada (Gail)
-----------------
* Two sessions with Dept. of Finance.  (Abraham Tachjian & others)
* Abraham is the open banking lead (https://www.canada.ca/en/department-finance/news/2022/03/government-moves-forward-with-open-banking-and-names-a-lead.html)
* Mostly Q and A on OIDF response
* Doing due diligence on standards and organizations
* Will hold discussions with members in both FDX and FAPI



EU DIW ARF (Gail)
------------------
* Torsten, Gail and Nat had meeting on June 9 with European Commission member
* Discussed how OIDF work can fit into architecture
 

FDX (Rifaat/Joseph)
--------------------
* Started a process on adopting FAPI 1.0 Part 1. 

GAIN (Dima/Joseph)
---------------------
* Next call on Thursday. 
* Listening tour on trust management going on. 
* Trying to address global trust management


IETF OAuth WG (Rifaat)
-------------------------
* Meeting in six weeks - two official sessions and two side sessions. 
* Agenda being finalized. 
 

ISO/TC68 (Nat/Dave)
----------------------
* n/a

The Middle East and North Africa (Chris)
-----------------------------------------
* Meeting with Open Banking Saudi Arabia (SAMA) during Identiverse. 

Mexico (Gail)
------------------
* n/a

New Zealand (Mike) 
------------------------------
* Will have call at 18:30 Pacific on June 15

Nigeria (Mike)
---------------
* Follow-up call is scheduled for June 16.

OECD (Nat)
-------------
* n/a

UK (Chris)
--------------------
* n/a

USA (Gail)
----------------
* n/a 

Whitepaper (Dima)
=========================
* Dima provided an overview of the whitepaper that he is working on. 
* Open Banking and Open Data go Global – 
 https://docs.google.com/document/d/176au5lZcR0vHbQG43wE7pZr7PBgVd7O7AqAzb6rqDzU/edit
* Perhaps publish it at Identiverse if it's ready?
* Building on a previous paper by WG which focused on FAPI security profile and it’s global adoption.
* This paper looks at the wider scope of open data banking, open data and the next steps of global interoperability. 
* Focused on use cases and not technical aspects.


WhitePaper Structure

* API Ecosystems

  * Private ecosystems
  * Open banking ecosystems
  * Expansion of open banking into open finance and open data

* Learnings

  * Use cases
  * Building blocks

    * Identity
    * API security profile
    * Trust Management
    * API specifications 

* What’s next

  * Global interoperability

* Global use cases

  * Global RPs
  * Sharing economy
  * Social networks
  * Cross border payments
  * Credit card schements

* Solutions

  * Intermediary providers (True Layer, Plaid, Stripe)

    * Different APIs for different jurisdictions

  * Interoperability Layers

    * Identity
    * API Security Profile
    * Trust Management
    * API Specifications

* Collaboration with others (SWIFT, STET, Berlin Group, FSB, DGX, etc…)

Specs (Dave)
================
Grant Management (Dima)
----------------------------------------
* There are now a couple of PRs and Issues. 
* Couple of issues left before going to implementer's draft. 

FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* N/A 

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
* Name change PR etc. is yet to be created. 

JARM (Dave)
----------------------------------------
* https://openid.bitbucket.io/fapi/openid-fapi-jarm.html
* Need feedback before last call for final draft.
 
Addressing "User Interface Hijack attack" in FAPI 2? (Nat)
-----------------------------------------------------------
* https://lists.openid.net/pipermail/openid-specs-fapi/2022-May/002619.html
* Provide incentives for ecosystems to adopt FAPI 2 if addressed
* Discuss on list and next call

PRs (Dave)
=================

To be merged
----------------


Under discussion
----------------------
* PR #342 – No Authorization Response encryption is required

  * Encryption does not add much value, PKCE prevents use if leaked
  * Nothing in the code that needs encryption
  * The section seems disorganized and the statement regarding encryption seems out of place.
  * Will need a full description on why encryption is not needed.
  * Need to make a clear statement so there is a reference point for various ecosystems.
  * Main point is to make it clear that encryption does not add much value.
  * Suggestion to add it in security considerations instead of a note
  * Reference 5.4  of JARM to require additional protections even if encryption is used.

* PR #343 - Change name from baseline to security profile

  * Remove Financial-grade from the name and just use FAPI
  * Change the Baseline name to Security Profile and add references to other specs.
  * The text “we recommend” feels informal.

Issues (Dave)
=====================


AOB (Dave)
=================
* none



The call adjourned at 15:59 UTC