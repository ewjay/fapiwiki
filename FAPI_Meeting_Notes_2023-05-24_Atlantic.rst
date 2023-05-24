============================================
FAPI WG Agenda & Meeting Notes (2023-05-24) 
============================================
* Date & Time: 2023-05-24T14:00Z
* Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2023-05-24_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:02 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Nat, Joseph, Dave, Brian, Daniel, Craig, Dima, Domingo, Kosuke, Lukasz, Rifaat, Takahiko
* Regrets: Mike L. 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Default agenda used. 


Events (Mike L)
====================================================
Identiverse (Mike L)
-----------------------
Identiverse is next week in Las Vegas - all OIDF members have received a discount code for registration that is good through May 30th for any last-minute registrations.

OAuth Security Workshop (Daniel)
-------------------------------------
* The site https://oauth.secworkshop.events/osw2023 opened. 
* Call for papers
* Some travel information is also available. 

External Orgs & Liaisons (Nat/Mike L.)
============================================

Open Finance Brazil
---------------------- 
* continue to receive both new FAPI certs as well as FAPI reverts

Open Insurance Brazil 
------------------------------
* working to confirm their FAPI recertification requirements. We anticipate hearing back from OPIN in May 26th. 
* FAPI reverts would begin in Q3 2024, and we anticipate approximately 70 OP and 70 RP reverts

SAMA
---------
* continue to receive and process Phase 1 OP and RP certifications. We’ve had a number of Saudi fintech join the Foundation.

ConnectID/AUS
------------------
* continue to work through certification bundled pricing options

Spec Status
====================
Grant Management 
------------------------
* Vote has been announced. 


PRs (Dave)
===============




Issues (Dave)
==================
* #599 - FAPI Acronym

  * Suggestion for a new FAPI acronym - Formally Analyzed Protection Interface
  * linked with #600 - Errata to remove "Financial-grade" references from FAPI1.
  * Should just use FAPI and not mention any acronym.
  * FAPI became a family of protocols
  * People are still associating FAPI with Financial-grade API
  * Formally analyzed is an afterthought and was not a design goal and may not apply to all specs in the FAPI family
  * Name is being updated in new OIDF website design
  * Just be persistent to call it FAPI  and not associate it with Financial-grade.

* #570 - Deprecation & removal of FAPI 1 Implementer's Draft conformance certification tests/programme

  * OBIE getting ready to transition to FAPI1 final sometime next year
  * Joseph is in discussions with them regarding implications

* #598 - Version identifier for FAPI 2.0

  * To avoid mix-up of protocol versions, it’s good practice to put version number in the protocol
  * Discussed before regarding where the version will go, e.g. client registration
  * It was decided that it’s difficult to work with older version and various profiles
  * Duplicate of #469 - Add protocol version and variant identifier

* #597 - Add text about conformance testing to FAPI2

  * Awaiting PR

* #600 - Errata for FAPI 1.0 to fix the title. 

  * Assigned to Nat

* Implemnter's guidance related tickets including #306 needs to be re-looked. 

  * #306 - Webhook Support in FAPI 

    * May not necessary need new spec
    * Changed to component “Implementation & deployment Advice”
  
  * #293 - PKCE & Nonce Security Considerations

* #466 - Proposal for FAPI DCR/DCM (Dynamic Client Registration/Management) profile

  * Priority dropped since Australia decided not to use DCR, no other ecosystem waiting for DCR
  * Priority given to using Federation with FAPI (OPIN and Open Finance Brazil is considering using Federation)



Discussed process for doing FAPI 1 errata

* Make changes
* Public review
* Vote


AOB (Nat)
=============
* none

The call adjourned at 14:50