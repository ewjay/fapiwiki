============================================
FAPI WG Meeting Notes (2020-11-04) 
============================================
* Date & Time: 2020-11-04 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call 
===========
* Attending: 



* Regrets: Daniel
* Guest: 

Adoption of Agenda (Nat)
===========================

Events 
======================



External Organizations
========================
Berlin Group (Francis)
------------------------
https://www.berlin-group.org/single-post/press-release-berlin-group-starts-new-openfinance-api-framework

* Taskforce: Banks only. Now other FIs including insurance. 
* Advisory board: Francis sits here. 

* Published open findings of the framework
* Berlin Group Next Gen
* Tool is renamed to Open Finance RP Framework
* Broadening the scope beyond banking to include financial assets , bankable assets
* Berlin group is structured into 2 main groups,

  *  task force, was limited to banks, now open for insurances and all financial institutes
  * Advisory board, constituted of the markets 

    * Francis is a member
    * Will be renamed to Open Finance Advisory Board, includes service providers, TPPs, and other market players
  * Press releases coming out
  * Francis will keep track
  * Going towards sharing more than just banking data
  * Still have problem of authorization and API mixed into single interface

    * Francis putting pressure to split it
    * FAPI can be reused for other areas instead of reinventing everything
  * Don asked if OIDF can be member or observer of board

    * Francis will address this with 2 chairs
  * Board has quarterly meetings

    * Members elect 10 board members
    * OIDF can join as member now and be eligible for board for 2021-2022 term
    * Francis will invite Don to the next session
  * Francis asked if OIDF proposed liaison agreement to Berlin group

    * Agreement was proposed earlier pre-Covid, still no response
    * Francis will attempt to get agreement through the board instead of task force
    * Don volunteered Torsten to join discussions



ETSI (Dave)
---------------------
* OBE signature profile coming out. 
* They did not accept base64url encode payload proposal.
* OBE talking about detached signatures, and RFC 7797 encodes the payload but OBE signing digest headers only
* WG has a working document regarding requirements for signing compile dby Joseph
* WG decided to make draft for non-repudiation
* Will need initial draft for adoption
* Stuart asked if we should have a separate profile for non-repudiation or make it part of FAPI 2.0
* Might be better to have a profile that can be referenced from FAPI 2.0
* Brian suggested to keep it simple and prevent scope creep.
* Current available signing standards don’t seem to meet requirements or still work in progress
* Dave, Francis, and Brian will be coming up with a signature draft for the WG to consider.



Australia (Stuart)
------------------------
Consent revocation proposal adds a lot of complexity. 
There is no standards to built upon. 

* https://github.com/ConsumerDataStandardsAustralia/standards-maintenance/issues/247


* Big 4 banks and recipients going into Phase 2 of consumer data sharing

  * Includes new products
  * Tweaks to information security profile
  * Joint accounts
  * Still finalizing consultation, looks very complex

    * No existing technical standards available to achieve goals

      * Intermediaries
      * Cascading consents (communicating consents via third parties)
  * OAC conformance testing

    * Joseph has CDR version of test on production and certification
  * Joseph still finalizing Australian response letter

      * Still don’t know where to send it
      * Might be better to do open letter and CC the chair


European Commission (Mark/Torsten)
------------------------------------
* 


UK (Ralph)
---------------------

* No updates

PRs (Dave/Nat)
=====================


Issues (Dave/Nat)
=====================



AOB
==========================


The meeting was adjourned at 15:00 UTC.