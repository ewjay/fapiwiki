============================================
FAPI WG Meeting Notes (2022-04-20) 
============================================
* Date & Time: 2022-04-20T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

  * Chris Michael
  * Daniel Fett
  * Dave Tonge
  * Dima Postnikov
  * Filip Skokan
  * Joseph Heenan
  * Mike Leszcz
  * Nat Sakimura
  * Takahiko Kawasaki
  * Bjorn Hjelm (Verizon)
  * Brian Campbell
  * Lukasz Jaromin
  * Rifaat Shekh-Yusef
  * Srivathsan Morko

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================


Events (Nat)
======================
OpenID Foundation Mountainview Workshop (Mike)
----------------------------------------------------
April 25 @ Google. 

Link: https://openid.net/2022/03/22/registration-open-for-openid-foundation-workshop-at-google-monday-april-25-2022/

Hybrid 

Registration needed and is closing in a few days: https://openid.net/2022/03/22/registration-open-for-openid-foundation-workshop-at-google-monday-april-25-2022/

FAPI Presentation Deck needed. 

OpenID Foundation Berlin Workshop (Mike)
------------------------------------------
May 10, Tue. 

https://www.kuppingercole.com/sessions/5048/1

OSW 2022 (Daniel)
--------------------
May 4 - 6 @ Trondheim

In-person only

https://oauth.secworkshop.events/osw2022

OIDF and Microsoft sponsored the event. 
 
Tickets are still available. 


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
Mike and Joseph had a meeting with Open Insurance (OPIN) regarding certification, fees, testing process, submissions, and payment process.

Will have 68 institutions to certify between June and August and will use the Brazil conformance tests.



Berlin Group (Daniel)
--------------------------------
Follow up meeting has not happened but wrote that they would like to discuss some FAPI technical items.

Regulators in Israel asked BG for a localized version of OB standards for their 1st phase open banking implementation. (Account info)

Looking to align second phase Payment initiation with both BG and FAPI.

Global Open Finance Technical Working Group is planning a meeting on May 5. Dave and Gail will be presenting on behalf of OIDF.

Meeting Agenda:

* Global Open Finance Technical Standards Work Group Meeting- Member Presentation: 
* OpenID Foundation presentation on Open Banking, Open Data and Financial-grade APIs
* OpenID Foundation Whitepaper on Open Banking 
* International movement towards Open Banking, Open Finance, and secure, consent driven access to all user data. 
* Financial-Grade API (FAPI) Working Group’s experience with Open Banking ecosystems internationally 
* Process of standards development, user experience, consent flow, security research Attack and threat model, mathematical proofs, testing implementations 
* The role of conformance testing in driving out inefficiency and improving security 
* Selected studies in implementation (UK, Australia, Brazil). 
* What did we learn? 
* Questions and comments 
* Member Presentation: Berlin Group Story of Berlin Group and PSD2 Structure, Governance, standards development, 
* Specifications rather than implementation From PSD2 to Open Finance - scope of thinking 
* Exploring relationship with FAPI Questions and Comments

Interested parties can contact Brian.Costello@ed.ac.uk for more information.

5 May from 11:00 AM – 13:00 PM BST.

EU DIW ARF (Gail)
------------------
Architecture Reference Framework

OIDF (Torsten, Gail, others) has created a response to the call for contributions and sent it out.


FDX (Mike L.)
------------------
* n/a

GAIN (Mike L.)
---------------------
CG meeting is going well. Next one is tomorrow.

  * Discussions on how participants can discover each other.

Speaking at Identity Week London Now, EIC, Identiverse, etc.

ISO/TC68 (Nat/Dave)
----------------------
* n/a

The Middle East and North Africa (Chris)
-----------------------------------------
Israel: see BG.

Saudi: 

  * Work is progressing on the localized standard.
  * Waiting for the project to officially kick off. 
  * 1st standard to come in June. 
  * Very strong regime of certification.

Bahrain is updating their standards 

UAE, Oman, Qatar,  etc. would be following soon.

Mexico (Gail)
------------------
* n/a

Nigeria (Mike)
---------------
In the process to schedule a second call.

OECD (Nat)
-------------
Call for contribution for privacy enhancing technology by April 27.

Nat has created an outline of the white paper for the privacy aspect of technology.

Due to confidentiality requirements, contact Nat for details and/or provide feedback.


UK (Chris)
--------------------
* Published ver. 3.1.10 -- final version to be published under CMA order. 
* What happens to OBIE, Open Finance, etc. is not known yet. 


USA (Gail)
----------------
n/a 


FAPI Presnetation Deck (Nat)
================================
Will include recent developments, certification

Nat will create a new draft and share with the group.

Mike will provide information about FAPI 2.0 conformance tests to Nat


Certification (Joseph)
=======================
Requirements from new ecosystems are being considered.

* Ecosystems can’t use the certification program in production because it will result in published PII .
* Some ecosystems want third parties to run the tests.

Feedback/opinions regarding these issues should be directed to Joseph.



Java ECDSA Vulnerability (Nat)
==================================
Java ECDSA vulnerability has been announced.

Nat has sent information regarding it to the mailing list : https://lists.openid.net/pipermail/openid-specs-fapi/2022-April/002594.html

Joseph asked if certification tests should be developed to test this vulnerability.

Tests should be created if they’re easy.

Certification suite provides infrastructure for general testing of libraries, issuers, and consumers as a whole. 

Joseph will consult with the certification team and eventually the EC board.


Specs (Dave)
================
Grant Management (Dima)
----------------------------------------
Working on issues


FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
Joseph has started work on the draft and may have a version available by the next meeting 

Advanced authorization (Dima)
----------------------------------
Will address issues in person

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
Perhaps look at the open issues at OSW. 

JARM (Brian)
----------------------------------------
Merged outstanding PR

Closed last remaining issue 

It’s ready for the next step in draft process

Only editorial changes have been made since the last draft.

Nat will contact Mike Jones for the next step

Can probably go straight to Final

Dave will start WG last call
 

PRs (Dave)
=================

* PR #328 - editorial: consistent case

  * Merged

* PR #326 - FAPI2Base: Disallow dpop nonces

  * Related issue #477 - fapi2 + dpop nonces
  * WG decided to disallow nonces in FAPI DPoP
  * Will merge if no objections

* PR #324 - Remove reference to RAR in FAPI 2 baseline

  * Related issue #480 - FAPI 2 Baseline: shall support authorization details if scope is not expressive enough needs enhancement to cover standard oidc claims.
  * RAR will be moved to Advanced Authorization spec
  * Will merge if no objections

* PR #327 - Allow use of EdDSA (Ed25519)

  * Linked to #492. 
  * There was general support for EdDSA to be added as an option. 
  * Support for EdDSA was introduced in Nimbus JOSE+JWT 6.0. Note that for EdDSA you need to include the optional Tink dependency in your project. For Nimbus JOSE+JWT 6.0 that would be
  * Joseph expressed concern from the point of view of the interoperability guarantee that certification currently markets itself. 

  * There are no requirements for signature algorithms at the moment (ID tokens, private key JWT, DPoP, etc..)
  * Do we need to tighten the specs?
  * Previously, not much issue with library support of PS256, ES256. But EdDSA may not have the same support.
  * Might be worthwhile to add EdDSA as an option in light of Java vulnerability, but not require it
  * Adding it does not mean all RPs and OPs must support all of them
  * But we should make sure a certified RP will always work with a certified OP
  * OPs can choose supported algorithms, RPs need to support chosen algorithms of the OP.
  * Tests can issue failures for RPs that don’t support all of them?? This will be considered as a separate issue

* Will merge if no objections

* PR #325 - Add Scope and terms

  * Brian stated that the goal should be obtaining OAuth tokens for HTTP access. OIDC and ID Tokens should not be mentioned.
  * Text regarding no support for public clients should be moved out of the Scope section and into the Intro.
  * Dave will update text


Issues (Dave)
=====================


#494 FAPI1Adv: Apparent inconsistency in RP tests compared to OP tests
--------------------------------------------------------------------------

In the FAPI1Adv RP tests, we have a test for clause 5.2.3-10 in FAPI1-base:


.. sourcecode:: text

        shall verify that the scope received in the token response is either an exact match or contains a subset of the scope sent in the authorization request
    

The test includes an extra random scope in the token endpoint response, and expects the client to fail.

In the FAPI1Adv OP tests, we don’t appear to do any checks on the scope returned by the token endpoint, i.e. we don’t seem to be failing OPs if they decide to return extra unrequested scopes.

The FAPI1Adv spec did not require scope to be returned from the token endpoint

A Brazil bank returned token with additional scope to RPs causing clients to fail 

The conformance test should 

1) Update OP to check for scope at the token endpoint
2) Remove the RP test

Conformance suite only tests FAPI 1 Advanced but not baseline. Carryover from baseline to Advanced does not seem to make sense, but we cannot change the specs.

WG decided to delete the RP test.

If this really needs to be fixed, we can do an FAPI 1.1.

Accumulate FAPI 1 issues and decide how to handle them.



AOB (Nat)
=================
* Please review https://bitbucket.org/openid/fapi/issues/492/eddsa-in-fapi-20



The call adjourned at 15:__ UTC