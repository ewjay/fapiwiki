============================================
FAPI WG Meeting Notes (2022-02-23) 
============================================
* Date & Time: 2022-02-2314:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-02-02_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat)
======================
* Attending: 


* Regrets: Dave Tonge
* Guest: 

Adoption of Agenda (Nat)
================================
* 

Events (Nat)
======================
OAuth Security Workshop (Daniel)
-----------------------------------
* Link: https://oauth.secworkshop.events/osw2022
* A workshop to bring standard people and academics together to discuss the security aspect of esp. OAuth. 
* May 6 - 10. 
* Early bird ticket available until March 17. 
* Hotel booking code is also available. 
* Two parts: Unfonference and more classic part with reviewed submissions. 
* Submissions can be done through calls for sessions page. 


Internal Liaison (Nat)
================================
iGov WG (Nat)
-----------------
* PassKey proposal by Apple (Nat)
    * There are discussions going on in W3C, and Microsoft and Google are likely to follow Apple.
https://github.com/w3c/webauthn/wiki/Explainer:-broadening-the-user-base-of-WebAuthn#device-key-extension

There seems to be some security implications. It may not be classified or assigned AAL in terms with current SP-800-63-4 drafts.

Interested parties should join the discussions.

NIST SP-8-00-63-4 was supposed to be released at the end of January but will be delayed until April due to biometrics discussions.

Modrna WG 
-------------------------


External Organizations (Nat)
===================================
Australia (Gail/Mike L.)
------------------------------------
Continued to collaborate with DSB to find academic partner in Australia to perform security analysis with U. Stuttgart.

DSB timeline schedule is quite challenging and U. Stuttgart is evaluating the feasibility.

Deadline is late summer/late fall this year.


Brazil (Mike L.)
---------------------------
Meeting with open insurance brazil yesterday. 

Very early on but they probably adopt OBB Security (FAPI) and certification.

70 institutions for OIB.

Outreach workshops will probably help.

Phase 1 certifications are expected this summer.

Berlin Group (Dave)
--------------------------------
* skipped

FDX (Mike L.)
------------------
* n/a

GAIN (Gail/Mike L.)
---------------------
OIDF BOD approved MOU and participation agreements.

The latter will be sent out this morning for signatures.

GAIN PoC Community Group will be published on the OIDF site.

A separate page will list executed participation agreements.


GOFCOE (Don)
-------------------
* n/a

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

The Middle East and North Africa (Ali)
---------------------------------------

Nigeria (Mike)
---------------
Had the first call this monday. 

Strong need for USSD support for feature phones. Will setup deeper technical dive into FAPI and MODRNA to understand USSD requirements.

Mexico (Gail)
------------------
n/a

Russia (Dima/Mike)
--------------------
n/a

UK (Chris)
--------------------
* 3.1.0 is out for consultations including. Variable Recurring Payments. 
* Link: https://www.openbanking.org.uk/news/your-chance-to-have-your-say-on-version-3-1-10-of-the-obie-standard/

USA (Gail)
----------------
NIST.IR.8389-draft - https://nvlpubs.nist.gov/nistpubs/ir/2022/NIST.IR.8389-draft.pdf

We will discuss it as an independent topic below. 

Draft NISTIR8389 Cybersecurity Considerations for Open Banking Technology and Emerging Standards
==================================================================================================
* Link: https://csrc.nist.gov/publications/detail/nistir/8389/draft
* Commentary link : https://docs.google.com/document/d/10GTmFGtyZO96CpigzvZ1kyl5rIqVqsjwfR9IMAay3yk/edit#

Due: March 3

Purpose and audience of paper unclear. Dima will reach out to authors.

API security section is paltry.

WG should draft a more comprehensive section on API security and provide comments on other sections..

Current state of Open Banking in Japan is also inaccurate. Nat will provide commentary.

People familiar with various jurisdictions/sections should comment on respective parts.

Finalize comments next week.

Specs
================
FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/466/proposal-for-fapi-dcr-dcm-dynamic-client
* Joseph to work on it

Grant Management (Dima)
----------------------------------------
* Working on some PRs and issues


PRs (Dave/Nat)
=================



Issues (Nat)
=====================

#475 - certification: FAPI2-Baseline - is OpenID Connect support optional?
------------------------------------------------------------------------------------
* #475 
Discussed in detail last week.


#469 - Add protocol version and variant identifier
------------------------------------------------------------------------------------
* #469 

Allows AS to determine which protocol version the request is for without analyzing the request.

Keep open until security analysis is done.

Mixing up two protocols might have some consequences if using same endpoint for 2 protocol versions.

Might be useful in multi-tenant situations and migration from FAPI 1.0 to 2.0.


#476 - is response_type=code id_token permitted in FAPI2 Baseline? (Joseph)
------------------------------------------------------------------------------------
* #476

Dynamic client registration spec explicitly says that clients using hybrid must request the implicit grant.

Might impact OAuth 2.1

The assumption of “token returned from the front channel” is an access token.

May need to update OIDC Core Errata also.

FAPI 2.0 Advance allows ID Token in the front channel for backwards compatibility.

Prohibiting would have ramifications on various specs.

ID Tokens in the front-channel can be modified so RP cannot be certain if ID Token has not been compromised.

Attacker can intercept  request and fetch new ID Token for the same nonce.

If using PAR, the attacker cannot get nonce to switch ID Tokens.

Is there any material exploit if the ID Token is attacked?

FAPI 1.0 supported this response type. Disallowing it would question the work of FAPI 1.0.

Daniel will double check formal analysis of FAPI 1.0 / 2.0 to make sure this is not a problem.


AOB (Nat)
=================



The call adjourned at 14:58 UTC