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
* Attending: Nat Sakimura Dave Tonge Riifaat Shekh-Yusef Domingos Creado Don Thibeau Mike Leszcz Tatsuo Kudo Joseph Heenan (In the room)
** Remotely: 



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

IETF 114
------------------------------
July 23-29, 2022. Philadelphia, USA

https://www.ietf.org/how/meetings/114/

IIW
------
Nov. 15 - 17

OIDF Workshop
---------------
Nov. 14

Authenticate Seattle
-----------------------
Oct. 17 - 20

FDX Meeting
--------------
oct. 17 -19 @ Dallas

IETF 115 London 
------------------
5 Nov 2022 - 11 Nov 2022

Money 2020 Las Vegas
--------------------------



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

Brazil (Mike L.)
---------------------------
* Open Insurance certification in August. 
* Open Banking recertification (approx 200) from Sept. till Dec. 13. DCR certification required. 

Berlin Group (Daniel)
--------------------------------
* N/A

Canada (Gail)
-----------------
* Three calls by now. 
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
* n/a

The Middle East and North Africa (Mike L.)
--------------------------------------------
* Meeting with Open Banking Saudi Arabia (SAMA/Central bank) on June 21 at Identiverse.
* 9 AM tomorrow @ Summit 2. 
* DMC next week.  

Mexico (Gail)
------------------
* n/a

New Zealand (Gail) 
------------------------------
* Call on June 15. FAPI and 3rd party certification. 
* NZ Gov working towards consumer rights legislation. 
* After that, 3PC could come in. 

Nigeria (Mike)
---------------
* They were not prepared to review USSD use cases at this time. 
* Having a follow-up in July. 

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