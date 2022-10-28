============================================
FAPI WG Meeting Notes (2022-08-24) 
============================================
* Date & Time: 2022-08-24T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-08-24_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Brian Campbell
  * Dave Tonge
  * Dima Postnikov
  * Filip Skokan
  * George Fletcher
  * Joseph Heenan
  * Jules
  * Kosuke Koiwai
  * Lukasz Jaromin
  * Michael Palage
  * Naohiro Fujie
  * Nat Sakimura
  * Takahiko Kawasaki
  * Dima
  * Domingos Creado
  * Justin Richer

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================
Adopted as is

Events & Liaisons (Joseph on behalf of Mike L.)
====================================================
IETF London November
-----------------
Open for registration

Brazil
-----------------
Open Insurance Brazil (OPIN) -- deadline for FAPI certifications has been pushed back to December 31, 2022. 

OPIN is finalizing details with the regulator and will communicate updates to the ecosystem later this week or early next week. 


SAMA
--------------
SAMA has confirmed receipt of letter and paper from Gail and the Foundation. They are finalizing their FAPI approach currently as well as their OIDF membership.


Nigeria
-----------------


PRs (Nat)
=================

* PR #358 - Improve description of attacker model

  * Had conversation about reducing different messages in the non-repudiation section
  * Dave will update text and merge



Issues (Nat)
=====================

* #534 - Authorization Request Leaks lead to CSRF

  * Dave suggested some wording in the issue comments to clarify the attack and the conditions that could cause authorization request leaks.
  * The attack requires the authorization request to leak and the attacker to block the honest users flow and then perform CSRF within the authorization code time window.
  * Mitigation 2 is unclear

    * Requiring the Client to only submit a PKCE code_verifier once. This will prevent attacks where the attacker was unable to block the honest user’s flow.
    * Helps to mitigate attacks where the attacker is unable to stop the user’s flow
    * Alternatively suggested to change to “ for each time the client invokes the authorization server, it should only submit one token endpoint request”. There is no need to record code_verifiers but instead just record whether the token endpoint has been invoked for the session.
    * Best practices to use state once to prevent CSRF, but clients are not required to detect second usage. Clients should destroy the state information once it’s used so a second request cannot be used successfully.
    * FAPI 2 doesn’t  require state since PKCE provides the same mitigation
    * The attack is using CSRF so no other devices/browsers are involved
    * Another mitigation is to reduce authorization code lifetime. RFC 6749 recommends 10 minutes max but that seems too long.

  * Dave will create issue about authorization code lifetime and raise the issue in OAuth WG
  * For this scope, no specific authorization code lifetime value is prescribed. The value should be prescribed elsewhere. Perhaps consider the issue of code lifetime separately.


AOB (Nat)
=================


The call adjourned at 15:03 UTC