===========================================
FAPI WG Agenda & Meeting Notes (2022-09-07) 
===========================================
* Date & Time: 2020-09-07T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-09-07_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Daniel Fett
  * Dave Tonge
  * Filip Skokan
  * George Fletcher
  * Joseph Heenan
  * Justin Richer
  * Mike Leszcz
  * Nat Sakimura
  * Tim Würtele
  * Craig Borysowich
  * David Januchowski
  * Dima Postnikov
  * Justin Richer
  * Lukasz Jaromin
  * Pieter Kasselman 
  * Rifaat Shekh-Yusef 
  * Takahiko Kawasaki
  * Kosuke Koiwai


* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
Adopted as is. 

External Orgs & Liaisons (Dave/Nat)
====================================================

 FIDO Authenticate Conference
---------------------------------------------
October 19, 2022 - FAPI presentation

OIDF Workshop (Mike)
-------------------------
Monday Nov 14 @ San Jose

Mike will send the Registration link to the mailing list when it’s ready

Saudi Central Bank
-------------------------
Awaiting feedback from Saudi Central Bank and acknowledged the cover letter and paper recommending their path for FAPI adoption.

Nigeria
-------------------------
Mike is following up to schedule a call with them to understand USSD use cases

Brazil (Mike/Joseph)
----------------------
Open Insurance BR original  milestone for 66 certifications by September 1 is pushed back to December 31.

Received CIBA specification for BR.

Joseph is reviewing and raising issues

https://github.com/OpenBanking-Brasil/specs-seguranca/blob/main/open-banking-brasil-financial-api-CIBA-1_ID1.md

Central Bank is mandating annual recertifications. Anticipate 106 recertification to be completed by the end of the year 


ISO SC27 (Nat)
-------------------
NA


PRs (Dave/Nat)
=================

* PR #367 - Add security consideration for CSRF attack

  * Related to #534 - Authorization Request Leaks lead to CSRF
  * Affects redirect based flows
  * Proposed mitigations reduce the attack surface but may not prevent the attacks
  * Daniel to review and propose wording to align with security BCP
  * Security analysis will formulate the session integrity properties to exclude this case

* PR #363 - FAPI2SP: Add requirement for RP to use discovery

  * Already required OP to support discovery so requiring RPs to use it provides extra protections for some attacks as discussed in #525 - decide-on-what-to-do-for-a-cuckoo-s-token
  * And #526 - Decide on B. Access Token Injection with ID Token Replay
  * The attacker model states for A5:
    
     * When the token endpoint address is obtained from an authoritative source and via a protected channel, e.g., through OAuth Metadata obtained from the honest AS, this attacker is not relevant.

  * In reality, attacker’s issuer URL can be injected 
  * Add clause for clients to verify the issuer value in the discovery document matches the discovery URL. But it is a problem for multi-tenancy where they do not have control of the URLs
  * Many clients do not check the issuer to the location of the discovery document.
  * A lot of implementations are not really very strict around the relationship between issuer and the discovery metadata.
  * Daniel to provide wording.

* PR #364 - FAPI2SP: Add security consideration for cuckoo's token attack

  * Related to #525 - Decide on what to do for A. Cuckoo’s Token Attack
  * PR does not prevent attack but makes it more difficult to attack 
  * Preconditions for attack are listed
  * 3 mitigations are proposed
  * Client checks the authorization server from which access token is received and is the authority AS for the resource server. This is implicitly implied and is not in the specs.
  * Document this in the analysis.

* PR #368 - Add mentions of Authorization Code Binding to DPoP key

  * Added that AS shall support “Authorization Code Binding to DPoP Key” but is optional for clients

* PR #366 - Add place holder so links to JARM spec in old location aren't 404s

  * Merged
 

Issues (Dave/Nat))
=====================
* #541 HTTP Signatures (Justin)

  * Feedback for requirements for HTTP signatures
  * Don’t sign ‘date’ header but the ‘created’ header


* #540 - Use of eKYC-IDA spec with CIBA/FAPI-CIBA

  * IDA requires use of CIBA and claims parameters but CIBA does not support claims parameter.
  * Need to decide in which WG to resolve this issue (eKYC, Modrna, or CIBA)



AOB (Dave/Nat))
=================

The call adjourned at 15:00 UTC


Chat Log
============