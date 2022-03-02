============================================
FAPI WG Meeting Notes (2022-03-02) 
============================================
* Date & Time: 2022-03-02T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-02-02_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Nat)
======================
* Attending: 
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================
* Move the NIST response and white paper topic to the front. 

Draft NISTIR8389 Cybersecurity Considerations for Open Banking Technology and Emerging Standards
==================================================================================================
* Link: https://csrc.nist.gov/publications/detail/nistir/8389/draft
* Commentary link : https://docs.google.com/document/d/10GTmFGtyZO96CpigzvZ1kyl5rIqVqsjwfR9IMAay3yk/edit#
* Due: March 3

Whitepaper link: https://docs.google.com/document/d/18i1f-lYd7VgAyw_2vYZChlFcSZwG_yK_epF7wAJkBaw/edit

Please comment on the link above, especially the last two pages. 

The whitepaper will be kept as a draft for some more time but the NSIT response will be sent tomorrow. 


Events (Nat)
======================
n/a

Internal Liaison (Nat)
================================
AB/Connect WG (Nat)
---------------------

The FedCM is just addressing a niche problem. 
It is addressing Account chooser and thrid party logout is going to be broken. 

PrivacyCG wants to prevent navigational tracking. 
They said that FedCM will solve it, This will break 
the redirect based protocols e.g., SAML, OAuth, OpenID and thus FAPI. 


Interested parties probably should raise voices of concern. 

Links: 

* W3C Federated ID CG:https://www.w3.org/community/fed-id/
* W3C Privacy CG: https://www.w3.org/community/privacycg/
* https://privacysandbox.com/open-web/#the-privacy-sandbox-timeline
* https://github.com/fedidcg/meetings/blob/main/2022/2022-02-14-notes.md
* https://github.com/whatwg/html/issues/6364

IIW Side Event is being planned for this. 

Other WGs 
-------------------------


External Organizations (Nat)
===================================
Australia (Gail/Mike L.)
------------------------------------
* Working with DSB and U.Stuttgart to start formal security analysis. Hopefully the work will start at the end of this week. 

Brazil (Mike L.)
---------------------------
* RP certifications coming in. 
* CIBA certification requirements coming. 
* Chicago advisory group, Radium, setting up RP community group. 
* Hopeing to create a knowledgebase. 
* Carnival week. 

Berlin Group (Dave)
--------------------------------
* n/a

FDX (Mike L.)
------------------
* n/a

GAIN (Elizabeth/Mike L.)
--------------------------
* Finalized participation agreement. 
* Elizabeth has sent out a link to the agreement. 
* project paper link: 
* PoC web page is going 
* Kick-off call is tomorrow. 
GAIN POC Online Meeting Venue and Schedule
Weekly Thursday Call @ 7 pm UTC
Location: https://meet.goto.com/520132557

First POC call tomorrow, Thursday, March 3rd. The meeting is on the OIDF Google calendar.

The Middle East and North Africa (Chris)
------------------------------------------
* Israel: 
    * Central bank of Israel is announcing open banking / finance regulations and releasing first. 
    * Closely aligned with Berlin Bank Standards. 
    * 15 banks. 
    * First phase is account information. 
* Saudi Arabia
    * They are interested in opening dialogue with OIDF. 
    * Following UK model.
    * Quite innovative around conformance certification model - realtime automated certification. 

Nigeria (Mike)
---------------
* Having a call after eKYC call to better understand the USSD requirements. 

UK (Chris)
--------------------
* n/a

USA (Gail)
----------------
* n/a 

NIST.IR.8389-draft - https://nvlpubs.nist.gov/nistpubs/ir/2022/NIST.IR.8389-draft.pdf

We will discuss it as an independent topic below. 


Specs
================
FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/466/proposal-for-fapi-dcr-dcm-dynamic-client
* Joseph to work on it but is currently preoccupied with FAPI 2.0 tests. 
* Nat pointed out that now that additional ecosystems are coming in, it is important to get at least something out as a guidance. 

Grant Management (Dima)
----------------------------------------
* n/a 

JARM
----------------------------------------
* Need to move forward to get it finalized. 

PRs (Dave)
=================
All the PRs are Dave's apart from the initial draft still being worked on by Dima, and Dave had to leave the meeting today early, we skipped the discussion. 

Issues (Dave)
=====================
Following new issues were discussed and opened. 

* #473 FAPI2 JWS alg choices are much wider than FAPI1
* #470 Are unsigned id_tokens permitted in FAPI2 baseline?
* #471 Resolve '?' in FAPI1 vs FAPI2 differences table
* #474 "shall use the authorization code grant described in [RFC6749]" could be clearer
* #477 FAPI2 + dpop nonces


AOB (Nat)
=================
n/a


The call adjourned at 15:02 UTC