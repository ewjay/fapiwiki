============================================
FAPI WG Meeting Notes (2022-02-02) 
============================================
* Date & Time: 2022-02-02 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-02-02_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Ali Adnan
  * Brian Campbell
  * Chris Michael
  * Dave Tonge
  * Dima Postnikov
  * George Fletcher
  * Joseph Heenan
  * Kosuke Koiwai
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Domingos Creado
  * Lukasz Jaromin
  * Ralph Bragg
  * Rifaat Shekh-Yusef
  * Takahiko Kawasa

* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* 

Events (Dave/Nat)
======================

Identiverse
------------
June 21, 2022 Denver, Colorado

https://identiverse.com/

Awaiting results for speakers.

EIC
----
The EIC closing date for proposals Feb 28 - https://www.kuppingercole.com/events/eic2022/callforspeakers

OIDF will host workshop on Tuesday, 9:00 AM - 12:30 PM localtiime

Will have a different agenda this year.

* There will be pre-conference workshops.
* Deeper technical dive workshops on Wednesday and Thursday.

Presenters are being accepted.

George will talk about Dynamic Client Registration


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
There was a call with the CDR team to follow up on FAPI 2 security analysis and identifying which university to participate and maybe in partnership with University of Stuttgart.

There were some discussions about certification for Australia and Joseph will follow up.



Brazil (Mike L.)
---------------------------
Currently, still receiving some RP certifications.

Still waiting to confirm details for CIBA certification for Brazil which was originally scheduled for the end of Q1/beginning of Q2. Mostly likely will be extended.


Berlin Group (Dave)
--------------------------------
Waiting to hear from them. Dave will follow up.

FDX (Mike L.)
------------------

GAIN (Gail/Mike L.)
---------------------
Draft MOU for G5 has been presented for feedback and will be presented to the executive committee this Thursday for review and approval.

Participation agreement has been circulated. Comments are due at the end of today (Feb 2, 2022).

POC agreement will be reviewed with EC Thursday also.

GOFCOE (Don)
-------------------

ISO/TC68 (Nat/Dave)
----------------------
* ISO NP 24377 Natural person identifier (NPI) -- authentication, issuance
and identification

New work is being started. Will need to keep updates on it.

The Middle East and North Africa (Ali)
---------------------------------------
Waiting for OIDF response to MOU.

DFC made a request for a 2 or 3 pager document summarizing what OIDF does so they can explain to counter parties within their organization.

Ali will follow up with Mike and Gail.

Nigeria (Gail)
---------------
 Gail is in talks with Open Banking Nigeria and will have a call in a couple of weeks.

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
https://docs.google.com/document/d/10GTmFGtyZO96CpigzvZ1kyl5rIqVqsjwfR9IMAay3yk/edit

Comments are Due March 3, 2022

Dima started working on a response.

Dima went over basic structure of document

Basic introduction on Open Banking

Described use cases, current state of various jurisdictions, UK, US, AU, India

People from these jurisdictions should review

Very small section on API security

OIDF can help with this section

Can talk about formal security analysis, OAuth 2 best security practices, best current practices

This section is very concerning since NIST papers are trusted sources of information around the world

Use cases are not comprehensive

Use cases have different importance in different markets

Doesn’t talk about alternatives to card payments and retail payments

Purpose, audience, and significance of the paper are unclear which makes if difficult to decide if it even warrants a response

Title mentions Cybersecurity Considerations but there is not much content regarding it

Response format will be decided depending on the amount of commentary.

WG previously discussed getting in touch with the authors.

Need more feedback from wider audience

Focus feedback on 7.3



Response to OIDF Strategic Taskforce
=========================================
The Strategic Task Force, a subset of the Board, is keen to learn more about how OIDF might support healthcare and IoT use cases. At least one market is considering FAPI for healthcare. IoT is another area where our standards might find traction. If you or one of your colleagues have experience and relationships in those domains please contact Gail (gail@oidf.org) and/or Mike Lescz(mike.leszcz@oidf.org), as we’re keen to see how we might add value to those domains.

Currently coordinating a call with Deb Bucci,  former co-chair of HEART WG,  regarding healthcare.


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

* PR #305 - FAPI2 Baseline: Align the chapter etc. structure to FAPI 1

  * OK to merge

* PR #307 -Rework the TLS section re issue 461

  * Brian suggested we use wording from FAPI 1.0 regarding RFC7525 but it uses SHALL follow
  * Dave suggested that SHOULD be used instead.
  * Language is ambiguous and overreaching, but BCP itself doesn’t have any SHALLs.
  * Joseph mentioned that NIST does have a list of TLS recommendations/requirements that are more recent than the BCP.
  * https://media.defense.gov/2021/Jan/05/2002560140/-1/-1/0/ELIMINATING_OBSOLETE_TLS_UOO197443-20.PDF
  * Dave will change language back to SHALL follow.




Issues (Dave/Nat)
=====================
* #469 - Add protocol version and variant identifier

  * Need more details on where the version and identifiers are sent, e.g. on every call, at registration etc..
  * Sounds like a version of API security instead of a version of the API. This might confuse people.
  * It’s needed so that appropriate verification methods can be invoked.
  * Might be easier just to document which FAPI version an API conforms to.
  * Building the conformance level into the messaging layer doesn’t seem like a good idea and might create interoperability problems.
  * Need more discussion and a concrete text proposal.

* #410 - FAPI and UMA 2.0

  * Perform analysis for using UMA with FAPI
  * UK Pensions Dashboard project is planning to use UMA 
  * Can be used for delegated authorizations and  step up authentication.
  * Can use existing acr claim to do step up authentication.



AOB (Nat)
=================






The call adjourned at 15:00 UTC