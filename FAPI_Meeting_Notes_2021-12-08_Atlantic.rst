============================================
FAPI WG Meeting Notes (2021-12-08) 
============================================
* Date & Time: 2020-12-08 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 


* Regrets: Dave
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* FAPI DCR/M (Dynamic client registration and Management)

Events (Dave/Nat)
======================

OIDF virtual workshop (Mike L.)
--------------------------------
* Thursday, December 9th at 9 AM PT. 
* Link with registration details: https://openid.net/2021/10/19/registration-open-for-openid-foundation-virtual-workshop-thursday-december-9-2021/

GSMA (Gail/Bjorn)
---------------------
The second workshop is on Nov. 29 for deeper technical dive. 

Joseph presented on behalf of FAPI WG. 

Quite a lot of questions about eKYC. 

Recording will be released when available.

OAuth Security Workshop (Daniel)
------------------------------------
OAuthSecurityWorkshop2021 

This is the zoom link we'll use for the event: https://us02web.zoom.us/j/81871097591?pwd=S3U4NTlHZythZXhKa3RkOGFMVTBCUT09

OWS zoom link: https://us02web.zoom.us/j/81871097591?pwd=S3U4NTlHZythZXhKa3RkOGFMVTBCUT09


External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
n/a

Brazil (Mike L.)
---------------------------
Recording from the RP Workshop is now available:

* https://www.youtube.com/watch?v=o5-qTnZB1n8

They banned Refresh Token rotation. 

Lots of RP testing going on. (Banks and payment providers.) 

Anyone initiating faster payment or PIX payment scheme has to join Open Banking and certify.

Participants tend to use conformance test suite as reference instead of actual specs. Coding for the test suite. There were lots of retests/failures.

120 Payment providers and expected to grow.

Open Insurance 68 providers going live. Going faster. 
It is related to Phase 4 but not entirely. 

* https://openinsurance.susep.gov.br/documentos-de-referencia/
* Looking to do FAPI conformance testing in the middle of next year.

Berlin Group (Francis)
--------------------------------
n/a

FDX (Mike)
------------------
n/a 

The Middle East and North Africa (Ali)
---------------------------------------
MOU being developed by DIFC. Expected to be next week.


Russia (Dima/Mike)
--------------------
n/a

UK (Chris)
--------------------
FCA published yesterday that they have revised the position on the 90 days re-authentication requirement. 

TPPs have to re-conform consent every 90 days but not notify the Banks.

TPPs don’t have to redirect the customers to the bank or use any bank authentication to re-confirm consent. It reduces a significant barrier to adoption.

FCA ruled out use of modified custom interfaces for the majority of accounts.

FCA effectively mandating dedicated API for personal and SMB accounts ... 

Modified custom interfaces are still available for corporate accounts or high net worth individual accounts with lowTPP usage.

https://www.fca.org.uk/publications/policy-statements/ps21-19-changes-sca-rts-and-guidance-approach-document-and-perimeter-guidance-manual

Specifically see pages 14 and 17 here https://www.fca.org.uk/publication/policy/ps21-19.pdf

EBA is not in the same position. May extend 90 days requirement to 180 days.


Mexico (Gail)
------------------
n/a

GAIN (Gail)
---------------
Tom is working on the participation agreement to the GAIN POC. 

FAPI DCR/M (Dynamic client registration and Management) (Joseph)
====================================================================
Joseph - WG interested in documenting the best practices? 

UK DCR spec is not compatible with RFC 7591 or OIDC DCR

Australia is the same as the UK.

Brazil’sDCR is more closer to RFC 7591.

It initially left out lots for security requirements for DCM.

New document will be a limited spec, will include

* Extra behaviors for Software statement assertion like validity and contents
* Require Software Statement assertions at the DCM endpoint
* Require registration access token for DCM endpoint to be sender constrained or similarly security

A lot of divergences from the RFCs are related to various regulators' desire to describe things in the metadata.


will be Profile of RFC 7591, 7592. 

Joseph suggests making recommendations rather than hard requirements, no ecosystem specific metadata.

The new spec will allow generic FAPI DCR/M certifications.

Certain attributes need to be taken from the Software statement to confirm that OPs can process Software statements as outlined in RFC7591

Chris asked how much adoption/take up from the community is expected? 

Won't’ affect current ecosystems but will help with new ones.

Scope and proposed TOC will be provided by Joseph to the WG list to solicit comments. 

Brian pointed out that it could be harder than it may seem at the outset, esp. registry. 

Travis pointed out that Brazil learning can be brought back to the WG to be shared with the World. 

European Payments Initiative/Open Banking  (Anders)
====================================================================

Security Analysis Planning (Nat)
===================================================
7.1 CIBA-FAPI Profile Security Analysis (Nat)
--------------------------------------------------------

7.2. FAPI 2.0 Security Analysis (Nat)
--------------------------------------------------------

PRs (Nat)
=================
Skipped. 

Issues (Dave/Nat)
=====================
* Issue #459: Should JARM be mandated for code flow with PAR and PKCE?

Australia on transition to FAPI 1.0 and will adopt code flow with PKCE but questions the value in adopting JARM which can potentially delay adoption.

Alternative is to stay in Hybrid flow.

Dima asks if there is a way to change the spec or should we create new draft which brings it closer to FAPI 2.0.

Just moving to code flow and PKCE lacks message authentication/integrity. Also have mixup attacks, etc…

Invalidates formal security analysis.

JARM is still in draft so it may have pushback by vendors.

WG should push JARM to final.

FAPI 1.0 is final so it can’t be changed.

Australia is looking to be fully transitioned by July 2022. March - July will be  in transition period.

Adopting JARM will allow smoother transition to FAPI 2.0

Change is a possibility for FAPI 2.0 but not FAPI 1.0

Provide advice to Australia ecosystem to maintain FAPI 1.0 compliance and work on it in FAPI 2.0


AOB (Nat)
=================
none


The call adjourned at 15:02 UTC