============================================
FAPI WG Meeting Notes (2022-08-17) 
============================================
* Date & Time: 2022-08-17T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-08-17_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Joseph Heenan
  * Filip Skokan
  * Domingos Creado
  * Leonardo Raimundo
  * Julie Maas
  * Dave Tonge
  * Takahiko Kawasaki
  * Lukasz Jaromin
  * Mike Leszcz
  * Travis Spencer
  * Dima Postnikov
  * Ralph Bragg
  * Bjorn Hjelm
  * Kosuke Koiwai
  * George Fletcher

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================
Adopted as is

Events & Liaisons (Joseph on behalf of Mike L.)
====================================================
Brazil
-----------------

OPIN certification deadline of Sept 1 has been extended.
New deadline will be available next week.

Brazil is changing format of certificates

* Stop using the organization unit field
* Transitioning to organization ID
* Adding a field to indicate OPIN or OB


SAMA
--------------

Nigeria
-----------------


PRs (Nat)
=================

* PR #363 - FAPI2SP: Add requirement for RP to use discovery

  * Required clients to use discovery
  * Will be merged

* PR #361 - Improve comparison table

  * Enhancements to the table
  * Will be merged

* PR #359 - Privacy considerations based on FAPI 1

  * Pull in privacy considerations from FAPI 1 with some editorial changes
  * Will be merged

* PR #364 - FAPI2SP: Add security consideration for cuckoo's token attack

  * Added 

    * Pre-conditions for the attack and requirement for powerful attacker
    * Attack is easier if a central directory is present
    * Mitigation using short-lived access tokens with refresh token
    * Will be merged

* PR #365 - FAPI2SP: Document DPoP proof leaks

  * Added DPoP Proof replay and mitigations using Message Signing
  * Removed Attacker A8
  * Consider MTLS sender constraining instead of DPop
  * Clarified that attacker is very powerful and that mitigations may not be necessary
  * Need leaked token to work
  * Awaiting review/feedback

* PR #360 - Attempt to explain attacker model better

  * Explained the attack using leaked authorization request/responses
  * Need feedback

* PR #358 - Improve description of attacker model

  * Joseph mentioned there are 3 messages that are not affected by the spec
  * Most likely copied over rather than pull in by reference
  * Pull out some messages since there aren’t any non-repudiation for them
  * NR5 already contains non-repudiation, explain using existing ID Token non-repudiation
  * Brian mentioned non-repudiation for token request/responses but was not accepted
  * Dave will update PR


Issues (Nat)
=====================
* #528 - C. PKCE Chosen Challenge Attack

  * Closed - non-relevant to FAPI2

* #534 - Authorization Request Leaks lead to CSRF

  * Agreed that nothing can be done for this attack
  * Can be prevented using a one time code in real world
  * Add PR to explain attack and can be mitigated by ensuring one time use of request_uri 
  * Dave will add PR

* #526 - Decide on B. Access Token Injection with ID Token Replay

  * https://arxiv.org/pdf/1901.11520.pdf shows the attack sequence
  * Needs PR

* #527 - Create security note/consideration on B. Access Token Injection with ID Token Replay (FAPI 1.0 Advanced)

  * Needs PR

* #290 - x-fapi-interaction-id across client to AS and RS interactions

  * Move to implementation guide
  * Need to work on implementation guide
  * Torsten suggested to expand interaction id for AS also
  * Dima also brought up using the same interaction id in some cases
  * Need review/feedback



AOB (Nat)
=================


The call adjourned at 15:03 UTC