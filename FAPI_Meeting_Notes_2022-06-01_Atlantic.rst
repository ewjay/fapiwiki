============================================
FAPI WG Meeting Notes (2022-06-01) 
============================================
* Date & Time: 2022-06-01T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

  * Bjorn Hjelm
  * Dave Tonge
  * David Januchowski
  * Dima
  * Gail Hodges
  * Joseph Heenan
  * Kosuke Koiwai
  * Lukasz Jaromin
  * Mike Leszcz
  * Nat Sakimura
  * Takahiko Kawasaki
  * Brian Campbell
  * Danillo Branco
  * Don Thibeau
  * Filip Skokan
 
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================
Added potential FAPI 2 value add

Feedback on Canadian OB comments


Events (Nat)
======================
Identiverse (Mike)
------------------------------
* F2F FAPI meeting Wednesday 6/22 normal meeting time
* Remote attending available. 


Internal Liaison (Nat)
================================
Certification (Joseph/Mike)
----------------------------
* Norway Health Group testing FAPI 2.
* Paypal

  * Discussed interoperability challenges in implementing FAPI in various jurisdictions
  * Indicated they will move onto FAPI 2
  * Testing FAPI 2 tests
  * Will have meeting later


Security Analysis
---------------------------
* Questions from analysis team:

  * Which commit to analysing? 
  * Contact points? 

    * Use Mailing list


External Organizations (Nat)
===================================
Australia (Mike L.)
------------------------------------
* Work of FAPI 2.0 security analysis on the way @ U. Stuttgart. 
* Gail was introduced to South Wales University of Australia who will help with the analysis

Brazil (Mike L.)
---------------------------
* Still trying to finalize CIBA for Open Banking.
* Outreach Workshops for Open Insurance in July and August

  * Will cover specs and conformance testing and submission

* Phase 2 certifications to start in September 2022
* Working on finalizing recommendation changes to certification program requested by Brazil and Saudi 


Berlin Group (Daniel)
--------------------------------
* N/A

Canada (Gail)
-----------------
* Discussed Feedback response for FAPI 2 on Canadian OB policy requirements
* https://docs.google.com/document/d/1-99-DU_B24NjywHpD_zS-Ga5FLoXgghRaL0DB91PvB0/edit
* Accessible and inclusive for all accredited system participants without requiring additional arrangements (such as bilateral contracts)

  * FAPI specs are open and do not require contracts for usage
  * Add that specs are IPR protected to protect implementors from getting sued

* Enable a positive consumer experience without overly onerous steps that the consumer must follow to realize the benefits of open banking

  * FAPI only defines the wire protocol
  * Ecosystems define the user experience guidelines
  * FAPI supports a range of user experiences 

* Enable the safe and efficient transfer of data among system participants

  * Specs are formally verified
  * Certification program verifies implementations 
  * Serves as an ***informal***, global defense against the global threat of criminal networks and rogue nation states…

* Capable of evolving with technological change to keep pace with the rapidly evolving sector

  * Add that FAPI is expanding breath of capabilities (e.g. Grant Management, CIBA, Dynamic Client Registration)
  * Mention various OIDF work (GAIN, Open Data/Health, Verifiable Credentials, etc…)
  * Canadian Participants can join OIDF to participate in work

* Sufficiently flexible to enable the development of new and innovative products

  * FAPI specs do not only apply to OB and Finance but to others (Insurance, telecom, health, etc…)
  * Can explore options for others applications

* Compatible and interoperable with international approaches

  * Specs are inherently compatible
  * Leading security profile selected by most markets
  * Core specs enable cross border use cases  

* Add links to OpenID for Identity Assurance


EU DIW ARF (Gail)
------------------
* n/a

FDX (Rifaat)
------------------
* Discussions on step-up authentication. 
* Mentioned the draft about it @ OAuth WG. 

GAIN (Dima)
---------------------
* 

IETF OAuth WG (Rifaat)
-------------------------
* DPoP shepherd writeup being done. 
* Some implementation feedback to be incorporated. 

ISO/TC68 (Nat/Dave)
----------------------
* n/a

The Middle East and North Africa (Chris)
-----------------------------------------
* n/a

Mexico (Gail)
------------------
* n/a

Nigeria (Mike)
---------------
* Follow up call to be scheduled for June 15 or 16.

OECD (Nat)
-------------
* n/a


UK (Chris)
--------------------
* n/a


USA (Gail)
----------------
* n/a 


Specs (Dave)
================
Addressing "User Interface Hijack attack" in FAPI 2? (Nat)
-----------------------------------------------------------
* https://lists.openid.net/pipermail/openid-specs-fapi/2022-May/002619.html
* Provide incentives for ecosystems to adopt FAPI 2 if addressed
* Discuss on list and next call


Grant Management (Dima)
----------------------------------------
* Please respond to https://bitbucket.org/openid/fapi/issues/439/grant-management-api-query-response


FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* N/A 

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
* Name change PR. 

JARM (Dave)
----------------------------------------
* https://openid.bitbucket.io/fapi/openid-fapi-jarm.html
* Need feedback before last call for final draft.
 

PRs (Dave)
=================

To be merged
----------------

* PR #334 - Restructure FAPI2 baseline

  * https://bitbucket.org/openid/fapi/pull-requests/334 

* PE #339 - Issue 499c

  * https://bitbucket.org/openid/fapi/pull-requests/339 
  * Add references in introduction to Messsage Signing, CIBA, Grant Mangement and RAR

* PR #338 - change user to resource owner

  * https://bitbucket.org/openid/fapi/pull-requests/338

Under discussion
----------------------
* PR #336 Grant Management - rename update to merge
    
  * https://bitbucket.org/openid/fapi/pull-requests/336
  
* PR #337 - Add note referring to client credentials grant
  
  * https://bitbucket.org/openid/fapi/pull-requests/337

Issues (Dave)
=====================


# 479 -- Change to the naming of FAPI (Dave)
------------------------------------------------
* Just moving to "FAPI" 
* FAPI 2 Baseline ==> FAPI 2 Security Profile
* FAPI 2 Advanced ==> FAPI 2 Message Signing

etc. 

PR is to be created. 



AOB (Nat)
=================
* none



The call adjourned at 15:59 UTC