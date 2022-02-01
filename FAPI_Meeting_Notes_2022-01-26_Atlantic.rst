============================================
FAPI WG Meeting Notes (2022-01-26) 
============================================
* Date & Time: 2022-01-26 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-01-26_Atlantic
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
  * Filip Skokan
  * Gail hodges
  * George Fletcher
  * Joseph Heenan
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Ray Gauss
  * Ali Adnan
  * Brian Campbell
  * Daniel Fett
  * Don Thibeau
  * Elizabeth Garber
  * Rifaat Shekh-Yusef
  * Srivathsan Morkonda

* Regrets: Dave
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* 

Events (Dave/Nat)
======================

Identiverse
------------
Meeting with organizers to follow up on OIDF submissions as well as OIDF sponsorship of Identiverse.

Will be confirming speakers in Mid-February.

EIC
----

The EIC closing date for proposals Feb 28 - https://www.kuppingercole.com/events/eic2022/callforspeakers

TechSprint (Michael Palage)
----------------------------
* https://www.fincen.gov/news/news-releases/fdic-and-fincen-launch-digital-identity-tech-sprint

FDIC and Fincen event focusing on identity.

Planning on accepting 10 teams/participants for 6 week event.

There will be two weeks at the end of January to solicit  interest.

Selected teams will have 6 weeks to formulate proposals and present them to a panel.

Judges will select winners for several categories.


External Organizations (Dave/Nat)
===================================
Australia (Mike)
------------------------------------
Had a call with CDR team last week. Follow up call on Feb 1.

The CDR team is interested in supporting FAPI 2.0 security analysis.

There are some issues with them providing funding to offshore universities/organizations.

CDR team is looking at local universities to be involved, potentially partnering with the University of Stuttgart.


Brazil (Mike L.)
---------------------------
Awaiting feedback from the Central bank’s plans to finalize the CIBA specification for Brazil OB as well as milestones for requiring  CIBA certification. 

Certification queue is up to date with remaining requests still awaiting payment.

RP certifications continue to come in.


Berlin Group (Dave)
--------------------------------
Dave to follow up. 

FDX (Mike)
------------------
Taka and Joseph had a meeting to discuss detailed specifications for DCR.

Joseph pointed out that the DCR request is changing the definition of scope parameters.

Will change definition to align with standard DCR spec.



The Middle East and North Africa (Ali)
---------------------------------------
MOU between the DIFC and OIDF is under review at the OIDF.


Nigeria
-------------
OIDF in the process of coordinating several calls with the  Nigerian Banking Trustee.

Nigerian open banking trustees. Call on Feb. 1
 

Mexico (Gail)
------------------
n/a

Russia (Dima/Mike)
--------------------

UK (Chris)
--------------------
https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/1048212/Final_revised_Agreed_Arrangements_190122.pdf


CMA published arrangement on future state of OBIE but it doesn’t say much. It’s more about the governance structure and remaining impartial.

Also there are discussions between FCA, Treasury, and the CMA about extending the agreement into open finance. But there are funding issue and changes may or may not required legislation. These will take time.



GAIN (Mike)
---------------
Gail is working on finalizing the participation agreement.

GOFCOE
-------------------
Meeting this Thursday 


Specs
================
FAPI DCR/M (Dynamic client registration and Management) (Joseph)
------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/466/proposal-for-fapi-dcr-dcm-dynamic-client




Grant Management (Dima)
----------------------------------------
* Working on some PRs and issues


PRs (Dave/Nat)
=================
* PR #305 - FAPI2 Baseline: Align the chapter etc. structure to FAPI 1

  * Tried to align it with the structure of FAPI 1.0. The normative references is in a different location and Joseph is not sure how to get MMark or XML2RFC to put it into different location.
  * The objective is to make it comparable to FAPI 1.0 so that people can do a good comparison.
  * Looked at top level headings but will need to look at subheadings.

* PR #302 - Clarify token introspection responses

  * Waiting for feedback from Torsten.
  * Dima will reach out.

* PR #306 - Add refresh token rotation clause and note

  * #456 should we remove support for refresh token rotation from FAPI 2.0 (one of the drafts)
  * Changed wording and added a note to start discussion.
  * There are significant operational issues with refresh token rotation on every token exchange causing interoperability problems.
  * Don’t want an outright ban because there may be use cases for it.
  * New wording would require AS to still allow the previous refresh token until that has been a successful exchange with the new refresh token. Allows it to be tested for conformance.
  * Clients will need to support it.
  * May have to keep 2 valid tokens which undermines rotation.
  * The intention is to discourage refresh token rotation.
  * Put security consideration that refresh token rotation in the context of  a confidential client provides little value and creates operational complexities.

* PR #307 -  Rework the TLS section re issue #461

  * 2 issues
  * Rework the Network layer section with numeric clauses
  * We’ll follow BCP on TLS 1.2. Add language “When using TLS 1.2 shall follow the guidance recommendations in RFC 7525” and a note to say that recommendations and should clauses in 7525 ought to be treated as shall to be compliant.
  * BCP is long and contains many shoulds.
  * FAPI 1.0 had “The recommendations for Secure Use of Transport Layer Security in BCP195 shall be followed”
  * Follow FAPI 1.0 text and call out specific sections that require SHALL language
  * Dave will update PR

* PR #308 - Add login hint token type registry values to CIBA

  * Have a standard parameter to put ecosystem specific values
  * Defines the backchannel_endpoint_login_hint_token_types_supported parameter in discovery doc to list what token types are supported  by login _hint_token
  * Main CIBA spec is final so cannot be changed.


Issues (Dave/Nat)
=====================



AOB (Nat)
=================
The following was mentioned: 

The Strategic Task Force, a subset of the Board, is keen to learn more about how OIDF might support healthcare and IoT use cases. At least one market is considering FAPI for healthcare. IoT is another area where our standards might find traction. If you or one of your colleagues have experience and relationships in those domains please contact Gail (gail@oidf.org) and/or Mike Lescz(mike.leszcz@oidf.org), as we’re keen to see how we might add value to those domains.





The call adjourned at 15:00 UTC