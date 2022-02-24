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

  * Brian Campbell
  * Chris Michael
  * Daniel Fett
  * Dave Tonge
  * Dima Postnikov
  * Joseph Heenan
  * Lukasz Jaromin
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Rifaat Shekh-Yusef
  * Stuart Low
  * Kosuke Koiwai
  * Sunpreet


* Regrets: Dave Tonge
* Guest: 

Adoption of Agenda (Nat)
================================
* Security Analysis
* IETF
* FAPI 2.0 Timeline
* Issues


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


IETF
-----------------------------------
https://www.ietf.org/how/meetings/113/

19 Mar 2022 - 25 Mar 2022

Hybrid model with virtual and in-person in Vienna at the end of March.

OAuth WG will host 2 sessions. Interested parties are encouraged to attend.


OIDF IIW Workshop
-----------------------------------
End of April

Looking for presenters


EIC
-----------------------------------
May



Security Analysis
======================
The purpose of security analysis is make sure security mechanisms are correct and to answer remaining questions :
* ID token in front channel

Will be conducted in 2 parts
* OIDF will sponson first half  to be conducted by University of Stuttgart
* The Australian government will sponsor the second half.

Scope will involve 
* Formalizing the current specification and dependent specs( DPoP, etc..)
* Formal definition of security properties
* Conduct proof to show FAPI 2.0 is secure

Security analysis on FAPI 2.0 Baseline first and then Advanced will come later.

WG needs to set an expectation of scope of the analysis.
* Baseline
* Dynamic client registration (Australia is interested but not required in Baseline)
* Questions that need to be answered by analysis.

Daniel has written a document describing the project.
https://docs.google.com/document/d/1ygOFAylABXmQe65SMx1KifqA2Te0d_rrppO0hxByUnI/edit?usp=sharing

WG members should review the  document and comment regarding scope, identify potential questions, and areas in specification that need focus.

Feedback requested by the end of the week.

Australia uses a  version of Dynamic Client Registration that is compatible with IETF RFC.

Should we still perform analysis on such? 

OIDC DCR has only a small portion relevant to security. Maybe the model is still the same or requires a small change.

DCR by itself may not be complicated, but establishing trust in relation to the registers will be complicated.                                     

Trust questions are out of scope for security analysis but the Australian university may consider it as part of their work scope.

Other points to consider :
* RAR
* Grant Management

Getting analysis on Baseline and non-jurisdiction based parts will be a good start.

FAPI 1.0 analysis included OIDC and OAuth.

FAPI 2.0 model will be based on FAPI 1.0 model and so will include OIDC and OAuth.


FAPI 2.0 Timeline
================================
Possible timelines:

ID2 end of March

FAPI 2.0 Baseline conformance suite beta in March

FAPI 2.0 Baseline Conformance certification around June




Internal Liaison (Nat)
================================
iGov WG (Nat)
-----------------

Modrna WG 
-------------------------


External Organizations (Nat)
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

Mexico (Gail)
------------------


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

JARM
----------------------------------------
JARM is still in implementer’s spec and is referenced by FAPI 1.0 final which is problematic.

Needs to be finalized.

Need to update FAPI 1.0 references.

Not mentioned in FAPI 2.0 Baseline and not much used in the market, so should we still put significant effort into it?

It’s referenced in FAPI 1.0 final and FAPI 2.0 advanced so we should continue it to finalization.

Depending on the results of security analysis, we may need to bring JARM back into Baseline.

Are there current market implementations of it? Authlete, Filip’s Node, IdP, Key Cloak, various implementations passed JARM certification listed at https://openid.net/certification/#FAPI_OPs

Also mandated in Australia with code flow and PKCE/JARM. 

Members to review JARM to see if there are any open issues.

JARM tests are included in the FAPI 1.0 conformance suite and are included in certification results.

WG to  finalize JARM, hopefully without breaking changes.



PRs (Dave/Nat)
=================



Issues (Nat)
=====================

#411- http-signing
------------------------------------------------------------------------------------
* #411 

Need decision on HTTP signing and DPoP.

Cavage spec is now on the standards track but still far from final.

The new draft is also dependent on a new digest headers draft for digesting payload content.

The HTTP signing spec is only a toolkit/framework. FAPI WG will need to profile it to specify what is signed in the request and response.

Update issue with current relevant information to facilitate discussion.





AOB (Nat)
=================



The call adjourned at 14:58 UTC