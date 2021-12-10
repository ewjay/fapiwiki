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
* 

Events (Dave/Nat)
======================

OIDF virtual workshop (Mike L.)
--------------------------------
* Thursday, December 9th at 9 AM PT. 
* Link with registration details: https://openid.net/2021/10/19/registration-open-for-openid-foundation-virtual-workshop-thursday-december-9-2021/
* 

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
Started in the certification group on what they might be able to do for FAPI 2.0 Baseline test. 

Brazil (Mike L.)
---------------------------
Increase in RP certification. 
Domingos and Markus had real positive impact. 
Open Banking Brazil milestones are quite fluid. 


Berlin Group (n/a)
--------------------------------
n/a

FDX (Gail)
------------------
Blog post on FAPI 1 v.s. 2. 

The Middle East and North Africa (Ali)
---------------------------------------
Received the draft MOU today.

Mexico (Gail)
------------------
n/a



Russia (Dima/Mike)
--------------------
n/a

UK (Chris)
--------------------
n/a

GAIN (Gail)
---------------
Participation agreement
~~~~~~~~~~~~~~~~~~~~~~~
It is being worked on by Gail and Tom. 

Don is now reviewing it. 

G5
~~~
Consensus on MOU among the five. 
Now socializing with their boards. 

Roadmap (Don)
~~~~~~~~~~~~~~~~
Identifying participants. 



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


Budget (Gail)
===============


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