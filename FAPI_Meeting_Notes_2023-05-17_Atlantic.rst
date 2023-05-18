============================================
FAPI WG Agenda & Meeting Notes (2023-05-17) 
============================================
* Date & Time: 2023-05-17T14:00Z
* Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2023-05-17_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:02 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Nat, Joseph, Mike L., Daniel, Dave, Filip, Rifaat, Victor, Dima, Domingos, Brian
* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Default agenda used. 

Implemnter's Draft of FAPI 2.0 Message Signing approved (Dave/Nat)
-------------------------------------------------------------------------
* 65 members voted with 0 objections so it has been quorate and approved. 
* Congratulations to the team. 


Events (Mike L)
====================================================
Identiverse
-----------------------
We have a room for the call on the week of identiverse but that is going to be 7 AM local time. 
Nat is going to ask if the WG wants to have the call that week to the list. 

External Orgs & Liaisons (Nat/Mike L.)
============================================

Brazil (Mike L.)
---------------------------------
* Certification coming in from Open Insurance. They are now close to 80 OP and 70 RP and mostly complete. 
* They will start looking at re-certification starting this fall. 
* They may look at the same model as in Open Finance Brasil where OPIN joins the OIDF BoD for reduced certification fees of $2000 fo non-members and $1000 for members.
* Will meet with their board next Friday
* Continuing SAMA phase-1 certifications



PRs (Dave)
===============
* Now that Message Sining voting has ended, we can apply the approved PRs. 

  * PR #416 - fapi2ms: require use of jarm, require use of jar, define response modes client metadata
  * PR #418 - Update affiliation to Authlete, add Dave as editor on the Security Profile, list Dave first for the Message Signing document
  * PR #419 -  FAPI2MS: Change 'above 3' to 'above 4'



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