============================================
FAPI WG Meeting Notes (2022-04-06) 
============================================
* Date & Time: 2022-04-06T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-06_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:04 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Ali Adnan
  * Brian Campbell
  * Dave Tonge
  * Dima Postnikov
  * Filip Skokan
  * Gail hodges
  * Joseph Heenan
  * Kosuke Koiwai
  * Mike Leszcz
  * Nat Sakimura
  * Takahiko Kawasaki
  * Brian Campbell
  * Dima Postnikov
  * Lukasz Jaromin
  * Rifaat Shekh-Yusef 

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================
* Default agenda. 
* issue #490

Events (Nat)
======================
OpenID Foundation Mountainview Workshop (Mike)
----------------------------------------------------
April 25 @ Google. 

https://openid.net/2022/03/22/registration-open-for-openid-foundation-workshop-at-google-monday-april-25-2022/

Hybrid possibility is now under investigation. 

OpenID Foundation Berlin Workshop (Mike)
------------------------------------------
May 10, Tue. 

https://www.kuppingercole.com/sessions/5048/1


Internal Liaison (Nat)
================================
n/a

External Organizations (Nat)
===================================
Australia (Gail/Mike L.)
------------------------------------
n/a

Brazil (Mike L.)
---------------------------
Mike, Gail, Joseph had call with Open Insurance Brazil

Will do follow up call today regarding certification process and requirements 

Plan to start certifications in June 2022

Mike will give update next week

Berlin Group (Dave)
--------------------------------

FDX (Mike L.)
------------------
* n/a

GAIN (Mike L.)
---------------------

ISO/TC68 (Nat/Dave)
----------------------
* ISO/TS 14742　Recommendations on cryptographic algorithms and their use: Started
* ISO 11568　Key management (retail) -- Principles, symmetric ciphers and asymmetric cryptosystems, their key management and life cycle: DIS
* ISO 23195 Security objectives of information systems of third-party payment services: Published June 2021
* ISO/NP TS 9546 Guidelines for security framework of information systems of TPP services: Starting
* ISO/AWI 5158  Customer identification guidelines: KYC related spec. DIS. 
* ISO/AWI 5201  customer identification guidelines: QRcode/Barcode payment security. WD. 
* ISO　24366  Natural Person Identifier (NPI): Published Nov 2021. 
* ISO NP 24377 Natural person identifier (NPI) -- authentication, issuance and identification: Starting
* ISO 5009　Official organizational roles — Scheme for official organizational roles: Published Feb 2022. MA is being set up. 

The Middle East and North Africa (Chris)
-----------------------------------------
In process to schedule call with Open Banking Saudi Arabia to focus on technical aspects of specifications and certification.

Dubai International Center asked Mayer Brown law firm (UK) to help update the laws to support advancement of digitalization of financial services businesses in the region.

Ali Had discussion with them regarding what needs to be regulated, what needs to be market driven, security and conformance testing.

Ali asked them to speak with OIDF and will coordinate meeting with Gail.


Mexico (Gail)
------------------
n/a

Nigeria (Mike)
---------------
In process to schedule second call.

OECD (Nat)
-------------


UK (Chris)
--------------------

USA (Gail)
----------------
n/a 


Specs (Dave)
================
Grant Management (Dima)
----------------------------------------



FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------


Advanced authorization (Dima)
----------------------------------
To be addressed after Grant Management. 

FAPI 2 Attack, Baseline and Advanced (Dave)
----------------------------------------------
Aiming to get to the first implementer's draft for the end of April. 

JARM (Dave)
----------------------------------------


PRs (Dave)
=================
N/A

Issues (Dave)
=====================

* #490 - Request for suggestions for tests for FAPI2-Baseline RP/client testing

  * Currently, certification team is working on FAPI 2.0  RP tests
  * Uses FAPI 1.0 tests as starting point, but many are related to front-channel ID token validation, so they do not apply to FAPI 2.0.
  * ID Token validation in backchannel via TLS is not required by specs.
  * Tests related to nonce, state are no longer relevant since they’re not required. 
  * PKCE requirement mitigates attacks when nonce/state are not used.
  * Make sure the security analysis model takes into account the lack of state/nonce requirement.
  * Joseph will email Daniel.
  * OP/RP tests already test for PKCE
  * DPoP tests are in development. Many at RS side.
  * RP tests mainly tests happy flow where PKCE/DPoP parameters are sent correctly.
  * There are 20 checks for DPoP at the RS.
  * Filip asked that to perform same checks at AS
  * End to end binding of authorization_code to DPoP was recently added which can apply to PAR.
  * https://www.ietf.org/archive/id/draft-ietf-oauth-dpop-07.html#name-dpop-with-pushed-authorizat
  * Should perform checks for DPoP at PAR endpoint also.
  * Need to check PKCE code_verifier for enough randomness in RP tests
  * Also need to check that code_verifiers are different for each request
  * Requiring AS to check code_verifier reuse may be burdensome
  * ID Token validation should still be performed if returned.
  * More discussions to follow


* #469 - Add protocol version and variant identifier 

  * Discussions indicate it’s good in principle
  * May work well for dynamic client registration management endpoints
  * May cause problems for authorization/token endpoints.
  * Wait for formal analysis results before closing


* #479 -  Change to the naming of FAPI

  * Nat proposed changing the name to Fortified API since FAPI can be applied to non-financial APIs (healthcare, etc…)
  * WG asked for suggestions for other suitable names

* #477 - fapi2 + dpop nonces

  * DPoP nonces are not required but AS/RS can require clients to support them
  * If there is no substantial security benefit, then don’t require nonces.
  * If security analysis shows problems, then nonces will be required.
  * Put clause that AS/RS must not send nonce
  * FAPI should not prohibit something that is meant to add additional security.
  * Nonce provides liveliness checks for pre-generated proofs and also provides work arounds for time sync issues but the      value in the context of FAPI is limited due to confidential client requirement.
  * Interoperability problems will occur if there is no clear guidance.
  * Make PR removing the nonce requirement for review.
  * Can always add it back if problems arise.

* #480  - Baseline: shall support authorization details if scope is not expressive enough needs enhancement to cover standard oidc claims.

  * Currently, there is text that
  * AS shall support the `authorization_details` parameter according to RAR to convey the authorization clients want to obtain if the `scope` parameter is not expressive enough for that purpose
  * There was prior discussion to create a separate profile for advance authorization protocol that provides guidance for these use cases and grant management..
  * Text has been removed from Grant management but is still present in Baseline.
  * Separate the advanced authorization requirements from the security profile.
  * Action to remove  clause from Baseline.

* #336 - FAPI 2 Baseline - Client types

  * FAPI 2.0 currently requires that AS shall support confidential clients but that is unclear whether that is “shall only” support confidential clients.
  * AS should be free to support other clients for non-FAPI use cases.
  * OAuth 2.1 defines a credential client that has credentials but has no prior relationship which is almost like a confidential client.
  * FAPI will not reference the term credentialed client and the requirement for client authentication disallows public clients.
  * Can put text in the scope that states FAPI 2.0 is to be considered in the context of a confidential client.



AOB (Nat)
=================
n/a


The call adjourned at 15:00 UTC