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
* Attending: (In the room) Nat Sakimura, Dave Tonge, Riifaat Shekh-Yusef, Domingos Creado, Don Thibeau, Mike Leszcz, Tatsuo Kudo, Joseph Heenan 
** Remotely: Ali Adnan, Daniel Fett, Dima, Gail Hodges, Jacob Ideskog, Takahiko Kawasaki, Bjorn Hjelm


* Regrets: 
* Guest: 

Adoption of Agenda (Dave)
================================
* N/A

Events (Dave)
======================
Identiverse (Mike)
------------------------------
* F2F FAPI meeting Wednesday 6/22 normal meeting time (8AM local time) in Summit 2 room. 
* Remote attending available via normal GotoMeeting conference link. 
* Nat, Joseph, Mike, Riffat, Dave, Brian
* There will be an Open Banking Discussion Panel

IETF 114
------------------------------
July 23-29, 2022. Philadelphia, USA

https://www.ietf.org/how/meetings/114/

Some works being discussed :
* SD-JWT (selective disclosure JWTs)
* Multi-subject JWTs


IIW
------
Nov. 15 - 17

OIDF Workshop
---------------
Nov. 14

Authenticate Seattle
-----------------------
Oct. 17 - 20

Mike and Gail will attend

FDX Meeting
--------------
Oct. 17 -19 @ Dallas

IETF 115 London 
------------------
5 Nov 2022 - 11 Nov 2022

Money 2020 Las Vegas
--------------------------
End of October in Las Vegas

Big Payments conference


Identity Week Asia
--------------------------
September 6-7 2022

https://www.terrapinn.com/exhibition/identity-week-asia/index.stm

Nat will be speaking about Open Banking



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
* Sorting out contractual issues for security analysis. 
* Australia will fund their part of their security proof work from July to end of Sept
* Review of model approach in mid-July to share concerns/issues with proof work


Brazil (Mike L.)
---------------------------
* Open Insurance (66 orgs) certification in August. 
* Open Banking recertification (approx 200) from Sept. till Dec. 13. 

  * DCR certification required. 

Berlin Group (Daniel)
--------------------------------
* N/A

Canada (Gail)
-----------------
* Three calls by now to address their questions. 
* Making an introduction to thought leaders. 
* Vittorio and Riffaat meeting next Monday. 

EU DIW ARF (Gail)
------------------
* N/A

FDX (Rifaat/Joseph)
--------------------
* Process of reviewing FAPI security profile internally going on. 
* Some documents they want to work on security and step-up authentication.  

GAIN (Dima/Joseph)
---------------------
* GAIN presentation / meeting 11 AM and 1 PM today at Summit 2. 


IETF OAuth WG (Rifaat)
-------------------------
Current draft agenda ideas

* OAuth 2.1
* Browser-based application
* Step up authentication
* GitHub and token theft
* Multi-subject JWT
* SD-JWT
* Security BCP
* DPoP 
 
ISO/TC68 (Nat/Dave)
----------------------
* New working group is setup for Natural Person Identifier convened by Patrick Curry, maybe relevant to eKYC group

The Middle East and North Africa (Mike L.)
--------------------------------------------
* Meeting with Open Banking Saudi Arabia (SAMA/Central bank) on June 21 at Identiverse.

  * Discussed FAPI 1 vs 2.0
  * Conformance and certification
  * Exploring different certification models

* Another meeting is scheduled for 9 AM tomorrow @ Summit 2. 
* DFC call next week to discuss SAMA progress.  

Mexico (Gail)
------------------
* n/a

New Zealand (Gail) 
------------------------------
* Call on June 15. to discuss FAPI and 3rd party certification. 
* NZ Gov working towards consumer data rights legislation to be published later this year. 
* After that, third-party certifications could come in. 

Nigeria (Mike)
---------------
* They were not prepared to review USSD use cases at this time. 
* Having a follow-up in July. 
* They have legislation policy from the central bank but it’s not very detailed yet.


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
* White paper (draft) https://docs.google.com/document/d/176au5lZcR0vHbQG43wE7pZr7PBgVd7O7AqAzb6rqDzU/edit
* Would like more feedback
* Health and Global Interoperability Paper will take same approach
* The goal is to get the papers into a Implementer’s draft via community feedback
* Work on the English phrasing so points are clear
* Use whitepaper to invite a wider community for feedback discussions
* Papers will be presented at the Identiverse panel for comments


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
* PR #341 - clarify scopes

  * Related issue #441

Under discussion
----------------------
* PR #322 – Pull in key management clauses

  * Pull in language from FAPI 1 regarding jwks_uris


* PR #315 - FAPI2 iss + JARM

  * Added clarifying text for returning iss when using JARM

* PR #342 – No Authorization Response encryption is required

  * Need feedback from Ralph. 

* PR #343 - Change name from baseline to security profile

  * Remove Financial-grade from the name and just use FAPI
  * Change the Baseline name to Security Profile and add references to other specs.
  * The text “we recommend” feels informal.

Issues (Dave)
=====================

#496 clock sync and FAPI2 baseline (Jacob/Dave)
----------------------------------------------------
Three Options: 

1) jti

   *  jti approach will introduce a large skew.

2) challenge

   * Challenge is the most secure but needs a new spec.

3) HTTP date header

   * HTTP header may be good but will need to explicitly mention that it wont prevent pre-generation of assertions
   * Client resends assertion after seeing error and checking the date header


AOB (Dave)
=================
* none



The call adjourned at 15:59 UTC