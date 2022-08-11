============================================
FAPI WG Meeting Notes (2022-08-10) 
============================================
* Date & Time: 2022-08-10T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-07-10_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Brian Campbell
  * Chris Michael
  * Dave Tonge
  * George Fletcher
  * Joseph Heenan
  * Kosuke Koiwai
  * Mike Leszcz
  * Nat Sakimura
  * Pieter Kasselman
  * Rifaat Shekh-Yusef
  * Takahiko Kawasaki
  * Wesley Dunnington
  * Ali Adnan
  * Craig Borysowich
  * Dima
  * Don Thibeau
  * Filip Skokan
  * Lukasz Jaromin


* Regrets: 

* Guest: 

Adoption of Agenda (Nat)
================================

* Events and External Organizaions
* PR & Issues



Events & Liaisons (Joseph on behalf of Mike L.)
====================================================




External Orgs & Liaisons
====================================================
Brazil
-----------------
NA

SAMA
-----------------
 
Letter to SAMA has been published to OIDF website 

https://openid.net/wordpress-content/uploads/2022/08/OIDF_FAPI-Profiles-Comparisons_2022-07-27.pdf


Global Open Finance Center of Excellence
-----------------


Nigeria
-----------------
NA


PRs (Nat)
=================

* Pr #362 - FAPI2MsgSign: Fix various links to the httpbis drafts

  * Fixed broken links to httpbis message signing drafts
  * Merged

* Pr #363 - FAPI2SP: Add requirement for RP to use discovery

  * Specs required OPs to publish discovery docs
  * Added requirement for RPs to use discovery doc only from OP

* PR #364- FAPI2SP: Add security consideration for cuckoo's token attack

  * Added some background information regarding the attack
  * Attack obtains access token from leak/attack and tricks client into using the token
  * Summarizes the conditions for the attack and adds possible mitigation such as 1) per issuer DPOP keys, MTLS certificates, and non-standard way for client to indicate to the OP the origin of the token
  * There are reservations regarding using non-standard ways to indicate token origin
  * Joseph suggested to using a central directory as an alternative
  * This is an unlikely attack which requires a leaked access token  a pre-condition, but it is part of the attacker model.
  * Joseph will add text regarding the unlikelihood of the attack
  * Another possible way is to make short lived access tokens

* PR #365 - FAPI2SP: Document DPoP proof leaks

  * Attacker obtains DPoP proof that can be replayed
  * Added mitigations

    * Short lived DPoP nonces
    * Replay prevention using JTI
    * Using MTLS instead of DPoP

  * Brian suggested to add some information on how proof is obtained and change attacker to A7 and that mitigations may not be necessary due to unlikelihood and the tradeoffs of complexity, security, vs scalability.
  * Suggesting to use MTLS for a DPoP issue may imply it is more than a suggestion. Change text to “consider” instead of use.
  * Nat suggested adding implementation guidance for using MTLS vs DPoP.
  * Companies/teams may have one preference over the other and may depend on network infracture, gateways, endpoint introspection, etc..
  * Add the consideration to the deployment guidance document.
  * Wait for further review and create new issue for implementation advice regarding tradeoffs of MTLS vs DPoP

* PR #361 - Improve comparison table

  * Improved table for comparing FAPI 1 vs FAPI 2
  * To be merged

* PR #359 - Privacy considerations based on FAPI 1

  * Added some privacy considerations based on FAPI 1
  * WG asked to review.

* PR #358 - Improve description of attacker model

  * Added more detailed information about how attacker model works and its applications.
  * WG asked to review.




Issues (Nat)
=====================

* #532 - Token chaining and ID Token / multiple bearer tokens

  * Issue originated from FDX org member
  * It’s related to transmitting the identity of the user from service to service internally. 
  * Service A calls Service B which calls Service C. 
  * Want to propagate the identity information from service to service.
  * Created a way for the client to pass ID token via headers through the call chain.
  * But ID Token is for client and not for RS so audience would not match.
  * Looking for best practices/alternatives  to propagate identity information through the system.
  * Internally user access token becomes a service access token. Unbinding of identity from access token loses a lot of security.
  * George suggested using API gateway at the security perimeter and mint new short lived access tokens for downstream services. Newly minted token can contain identity data in original user access token and can contain narrower scope. 
  * This suggestion is similar to what Brian and Wesley suggested in this issue.
  * The new token should contain enough identity data for validation purposes, e.g. session, user, etc..
  * Bearer access tokens can call userinfo endpoint to get user data.
  * IETF, Netflix Passport has/is working on something similar
  * Wesley asked whether you can put multiple audiences into the ID Token.
  * Yes, ID Token audience is an array but there is no text about when to use multiple audiences.
  * Peter asked why the ID Token is necessary and what’s in it that is needed. Need some more contextual information about whether it’s a problem or not.
  * Making multiple calls to userinfo endpoint is problematic for performance.
  * Wesley to update the ticket with more information.

* #534 - Authorization Request Leaks lead to CSRF

  * Need more information for the attack and in what context the attack is valuable or less risky.
  * The attack suggests that the attacker in this case is powerful enough to achieve this via easier means.




AOB (Nat)
=================

The call adjourned at 15:03 UTC