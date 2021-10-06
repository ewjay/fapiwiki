============================================
FAPI WG Meeting Notes (2021-10-06) 
============================================
* Date & Time: 2020-10-06 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-06_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================


Events (Dave/Nat)
======================

Authenticate/FIDO (Gail)
---------------------------
Authenticate happening on Oct. 18-22. 

Link: https://fidoalliance.org/event/authenticate-2021-conference/


GAIN PoC Meetings
---------------------------
OIDF is planning 2 listening sessions regarding a proposed proof of concept along the lines of the GAIN white paper, Global Assured Identity Network. 

https://gainforum.org/GAINWhitePaper.pdf

Will have 2 listening events and a call for comments via OIDF blog.

* One following Authenticate in Seattle
* One following OIX in London

Purpose will be to educate the community about the POC, solicit questions, feedback, and contributions about the POC.

Feedback will be the basis of the first POC meeting targeted for December.

Questions can be addressed to Don, Torsten, or Donna (donna@oidf.org)

Legal matters can be addressed to Gail.

The PoC effort will require a participation agreement that is distinct and separate from contribution agreement required for OIDF Workgroups.



IIW
------------
October 12-14, 2021 

Topics are mostly on Self-Sovereign Identity right now

Mike J. is coordinating with organizers to allocate the second morning  to do OIDF work.


External Organizations (Dave/Nat)
===================================
ISO/TC 68 (Nat/Dave)
-----------------------------

Nat has drafted a liaison statement and have distributed it to the liaisons committee.

* Final specs published

  * FAPI 1.0 
  * CIBA Core 1.0 

* Implementer’s Drafts

  * Grant Management
  * SSE
  * CAEP
  * FAPI 2.0 Baseline
  * FAPI 2.0 Attacker Model

* GAIN Whitepaper
* Current Projects


Australia (Dima/Joseph)
------------------------------------
OIDF to work on assessment for AAAC. They have provided direct funding for assessing :

* Migration from 1.0 to 2.0.
* Gaps relative to paper by OIDF in 2019 and 
* Any agreements or divergent views from recommendations in their 88 paper and decision 182
* Outlook of interoperability and future
* Other OIDF standards that may fit
* Mark Haine has agreed to help draft the paper
* MikeL will schedule call with CDR Team and ACCC to review updated outline

Gail is reaching out for guidance to scope the assessment.

https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-09-29_Atlantic

Berlin Group (Nat)
--------------------------------
Nat had a call with Bruno.

OIDF-Note-Well : Nat explained that any OIDF publication is validated beforehand, therefore there is no such risk as Wijnand raised for the BerlinGroup.

And the text as proposed by the ODIF is approved as is.

Sub-Committee planning: We concurred that the workstream should be 2 phases :

Phase 1: Share approaches and identify requirement domains to elaborate
Phase 2: Build the requirements for the joint Initiative
 

Phase 1 will break down across 3 workshops:

#. Mutual presentation (ie The Berlin-Group and OIDF) on the key domains which might be beneficial for each other: 3 hours Workshop to be set during the week of Oct the 25th. 

#. To improve this first workshop, both the Berlin-Group openFinance Editor and the OIDF will share documents they have to highlight the specific areas of potential mutual interest (Action : as soon as possible)

   Investigation and definition of the areas to investigate jointly

#. Final definition and plan requirement definitions: Plan Phase 2 (ie what and when)
 

Phase 1 is targeted to end before Christmas (2021) and here are 3 doodles (one for each of the 3 phase 1 workshops) to share with the SC members :

#. Mutual Presentation WS: https://doodle.com/poll/uq6fnuwtc7zpsg2c?utm_source=poll&utm_medium=link
#. Investigation and definition: https://doodle.com/poll/8mq4ph49ws5i5kq7?utm_source=poll&utm_medium=link
#. Final definition and plan requirement definitions: https://doodle.com/poll/3pywfmcwym2d3ev6?utm_source=poll&utm_medium=link

Brazil (Mike)
---------------------------
* Still processing ph.2. 
* Oct 29 Ph. 3

  * Deadline for submissions was 9/24
  * Received 24 certification requests, 20 have been certified
  * 130 remaining to be received
  * Will certify remaining based on order received.

* RP tests in beta include payment and DCR tests

  * 3 RPs testing right now
  * 60 RPs on certification list for phase 3 

* RP community slack channel was supposed to Sept. 27 but will be delayed a day or so. 
* There are moves to split payments into 3 separate trenches  that will require recertification across the board. Not finalized yet.
* Ralph flagged issues as blocking - #443 

  * Payments related to Oauth authorization server metadata and additional CIBA login hint, token values.
  * 5 different login token structures proposed


Canada (Gail)
------------------
No updates


FDX (Gail)
------------------
No updates


Middle East and North Africa (Ali)
-------------------------------------
Had first meeting with Dubai International Financial Center on Sept 29. They have expressed interest in cooperation with OIDF to create a working group to get more people involved (.eg. local regulators, banks).

Will have a follow up meeting with the strategy team within the DFC on how to put together the working group within the framework of the DFC academy.

How their working group and FAPI working group collaborates remains TBD

Don added advice to use experiences with the UK, Australia, and Brazil as a potential model.


Russia (Don/Dima)
--------------------
* Still awaiting response 


UK (Fiona/Ralph/Chris)
--------------------
Updated version of the Standard 319 that was up for approval in the steering group.

There is an outstanding issue around the granularity of error and status messaging.

There is pressure on the standards team to come up with a standard but this may be a regulatory issue instead.

No clarity or consensus about what’s the end point from a customer’s point of view resulting in banks saying they don't have to do that and regulators saying they can’t force banks to do that.

It’s a high level issue which local market regulators need to pay attention to.

Australia has released enhanced error handling. Will need to wait until February to know if it will be mandated.


PRs (Dave/Nat)
=================

PR 287 - Add requirement for clients to send issuer as a string
---
* Pull request #287 - Add requirement for clients to send issuer as a string

Feedback regarding wording is requested

PR 428 - Add initial version of implementation advice doc
---
Pull request #288 - Add initial version of implementation advice doc

Dave has created an initial version of the Implementation Advice Draft

Feedback requested



Issues (Dave/Nat)
=====================

#443 - Missing Discovery Metadata for login_hint types and login_hint_token type
--------------------------------------------------------------------------------
#443 - Missing Discovery Metadata for login_hint types and login_hint_token type: backchannel_endpoint_login_hint_token_values_supported

Provides a way to advertise, back channel endpoint, login token, value supported, and then registering client preference

Defines a spec level key but value structures are user/implementation specific

Brazil has 5 different token types 

The issue is asking for a placeholder that can be ecosystem specific

No precedent for a top level key with no predefined values

Taka suggested another approach where the value allow ecosystem specific values or the value points to another discovery document for ecosystem specific values 

OIDC Core has id_token_hint

Brian pointed out that CIBA Core is final so no changes are allowed, so it will require an extension or profile document

Will need to evaluate risks because it’s going to be fundamental data

Dave will update issue with notes and asked Ralph for feedback

Feedback is requested



AOB (Dave/Nat)
=================
Gails wanted to survey to see if anyone is aware of adaptations of FAPI, specifically for the insurance industry within OIDF communities or elsewhere.

A member was asked to start talking about such a topic.

Nat was contacted by the Japanese Fintech society’s insurance group but haven't heard back from them.

Brazil is looking to launch an open insurance that’s part of the wider open finance that Brazil is looking to expand.

UK has talk of open insurance also.

Anyone with any other information on the topic is welcome to talk to Gail.



The call adjourned at 15:00 UTC