============================================
FAPI WG Meeting Notes (2022-02-09) 
============================================
* Date & Time: 2022-02-09 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-02-09_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Brian Campbell
  * Chris Michael
  * Daniel Fett
  * Dave Tonge
  * Dima Postnikov
  * Don Thibeau
  * George Fletcher
  * Joseph Heenan
  * Lukasz Jaromin
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Ralph Bragg
  * Takahiko Kawasaki
  * Kosuke Koiwai
  * Rifaat Shekh-Yusef

* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Focus on PRs and Issues

Events (Dave/Nat)
======================

Identiverse
------------

EIC
----
The EIC closing date for proposals Feb 28 - https://www.kuppingercole.com/events/eic2022/callforspeakers

TechSprint (Michael Palage)
----------------------------
* https://www.fincen.gov/news/news-releases/fdic-and-fincen-launch-digital-identity-tech-sprint

FDIC and Fincen event focusing on identity.

Planning on accepting 10 teams/participants for 6-week event.

There will be two weeks at the end of January to solicit interest.

Selected teams will have 6 weeks to formulate proposals and present them to a panel.

Judges will select winners for several categories.


External Organizations (Dave/Nat)
===================================
Australia (Gail/Mike L.)
------------------------------------



Brazil (Mike L.)
---------------------------


Berlin Group (Dave)
--------------------------------

FDX (Mike L.)
------------------

GAIN (Gail/Mike L.)
---------------------

GOFCOE (Don)
-------------------

ISO/TC68 (Nat/Dave)
----------------------
* ISO NP 24377 Natural person identifier (NPI) -- authentication, issuance
and identification

The Middle East and North Africa (Ali)
---------------------------------------

Nigeria (Gail)
---------------
 

Mexico (Gail)
------------------
n/a

Russia (Dima/Mike)
--------------------

UK (Chris)
--------------------

USA (Gail)
----------------
NIST.IR.8389-draft - https://nvlpubs.nist.gov/nistpubs/ir/2022/NIST.IR.8389-draft.pdf

We will discuss it as an independent topic below. 

Draft NISTIR8389 Cybersecurity Considerations for Open Banking Technology and Emerging Standards
==================================================================================================

Response to OIDF Strategic Taskforce
=========================================
The Strategic Task Force, a subset of the Board, is keen to learn more about how OIDF might support healthcare and IoT use cases. At least one market is considering FAPI for healthcare. IoT is another area where our standards might find traction. If you or one of your colleagues have experience and relationships in those domains please contact Gail (gail@oidf.org) and/or Mike Lescz(mike.leszcz@oidf.org), as we’re keen to see how we might add value to those domains.

Specs
================
FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/466/proposal-for-fapi-dcr-dcm-dynamic-client


Grant Management (Dima)
----------------------------------------
* Working on some PRs and issues


PRs (Dave/Nat)
=================

* PR #309 - Update PAR draft references in FAPI2 baseline to RFC9126 (issue #472)

  * Merged


* PR #307 - Rework the TLS section re issue #461

  * Itemize requirements for network security
  * Align spec with FAPI 1.0 in regards to TLS 1.2 
  * Brian suggested “when using TLS 1.2, follow the recommendations for Secure Use of Transport Layer Security in RFC7525]” to avoid SHALL/SHOULD language.
    
    * Dave will make changes with the suggestion.

  * Taka wants additional ciphers added and make the ordering of ciphers significant.
  * Question was raised whether prescribing ciphers makes sense at all?
  * PR listed 3 ciphers but text mentions 4.
  * How would prescriptive language for ciphers affect certification if each ecosystem specifies their own also?
  * FAPI 1.0 conformance suite tests for the allowed and disallowed ciphers.
  * Legislations are starting to mention allowed ciphers based on FAPI 1.0 and in multiple locations. It would be better to reference IETF BCP for TLS 1.2.
  * Stronger cipher should be allowed while preserving interoperability.
  * Should spec say the allowed ciphers are sufficiently safe enough or should it defer to a more definitive spec?
  * References to other specs cause more confusion and too many dependencies.
  * Chris suggested spec say that the allowed ciphers are secure enough but it doesn’t preclude equivalent strength or stronger ciphers and also point to definitive sources.
  * Interoperability requires the minimum mentioned ciphers.
  * Also need to prepare for when we deprecate ciphers.
  * Referencing external sources might be better but currently there is no such reference for TLS 1.2.
  * IETF will replace it with TLS 1.3 instead of updating BCP for TLS 1.2.
  * Consultation/collaboration with other groups (FDX) might be needed for appropriate requirements.
What happens when legislation weakens allowed ciphers? How would OIDF handle certifications for ecosystems that are contradictory to specs? 
  * Language allowing for jurisdiction specific flexibility will maintain compliance but is it something we want to do?
Need clause requiring clients to support TLS 1.3 because server may only support TLS 1.3.
  * Change text to allow the 4 mentioned ciphers or stronger.
  * If spec allows stronger ciphers, why not move to TLS 1.3 instead of adding to TLS 1.2?
  * Limit TLS 1.2 ciphers to keep backwards compatibility otherwise use TLS 1.3.
  * Dima will consult with Russia Open Banking regarding TLS and GOST protocol.

* PR #306 - Add refresh token rotation clause and note

  * Related to #456 - should we remove support for refresh token rotation from FAPI 2.0
  * Change text to “received and successfully processed”
  * Also added note to make it clear that refresh tokens are discouraged and it doesn’t bring any security benefits for confidential clients, but are allowed provided requirements in clause 20 are met.
  * Feedback is requested.


Issues (Dave/Nat)
=====================
* #475 - certification: FAPI2-Baseline - is OpenID Connect support optional?

  * FAPI 1.0 conformance required openid scope, but was technically optional in the specs.
  * FAPI 2.0 makes it more obvious that openid scope is optional.
  * Should conformance implement tests without requiring openid scope. If we do, should we distinguish between servers that do and do not support OIDC?
  * FAPI 1.0 was using OIDC as a pseudo-security layer using detached signatures for responses.
  * FAPI 2.0 no longer requires it so tests should reflect such.
  * Add clause to say if server supports OIDC then you need to run tests with OIDC support but make it clear that OIDC support is optional.
  * FAPI 2 servers cannot be certified for OIDC alone because interoperability aims of protocol and tests are completely orthogonal.
  * If the server supports OIDC, does it allow front-channel or back-channel ID Tokens? Joseph has a separate issue for that.
  * Would like to keep the simplicity of not supporting OIDC, but if the server supports it, we need to define the behavior due to conflicts. Otherwise the combination would not be secure.
  * A user’s authentication information conveys some security so would not like to see OIDC and FAPI separated. Removing implicit OIDC support would undermine security characteristics of the protocol significantly.
  * What are we losing if we don’t require OIDC?
  * There are use cases for resource servers using plain OAuth with no need for user authentication experience, but authentication information contributes significantly to the decision making process and trustworthiness of the operation. 
  * FAPI conformance suite does basic OIDC tests but is not as comprehensive as the OIDC conformance suite.
  * Need to make it clear that servers that support OIDC/OAuth which passes FAPI conformance test does not necessarily mean they pass OIDC/OAuth conformance. 
  * Conformance should check metadata for OIDC support and run tests accordingly.
  * Need to define behavior when there are incompatibilities between the specs.
  * Need to have ways to allow deployment of a single instance that supports both specs.
  * Should put a new section in spec for handling servers with OIDC support, FAPI/OIDC profile.



AOB (Nat)
=================






The call adjourned at 15:00 UTC