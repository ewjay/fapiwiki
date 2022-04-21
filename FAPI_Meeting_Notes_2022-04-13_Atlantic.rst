============================================
FAPI WG Meeting Notes (2022-04-13) 
============================================
* Date & Time: 2022-04-13T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

  * Brian Campbell
  * Chris Michael
  * Daniel Fett
  * Dave Tonge
  * Dima Postnikov
  * Domingos Creado
  * Don Thibeau
  * Filip Skokan
  * George Fletcher
  * Joseph Heenan
  * Kosuke Koiwai
  * Nat Sakimura
  * Ralph Bragg
  * Takahiko Kawasaki
  * Brian Campbell
  * Lukasz Jaromin
  * Michael Palage

* Regrets: Mike L. 
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

Presentation slots are still available.


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
n/a

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
Will have the 3rd ministerial meeting in December.

A lot of accumulated cyber issues.

Call for contribution for privacy enhancing technology by April 27.


UK (Chris)
--------------------
Published ver. 3.1.10 -- final version to be published under CMA order. 

What happens to OBIE, Open Finance, etc. is not known yet. 

Starting to look at FAPI2

  * Need incentive/rationale to uprade

USA (Gail)
----------------
n/a 


Specs (Nat)
================
Grant Management (Dima)
----------------------------------------
Dima working on issues



FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
No updates in spec. 

Brazil is using subject dn in DCR but changing CA later this year. 

When clients switch certs and they change the subject DN to an invalid subject DN, they will lose control of the client until it’s manually recovered.

Need to consider possible solutions (2 phase commit?). 

May want a conformance check to cover this scenario

Ralph discussed some workarounds using non-explicit string matching with certain attributes in the DN (RDN component matching)

Another option is to NOT bind the management token to the client as TLS client authentication

* Token endpoint authentication mechanism remains exact string match
* Binding of management token as a credential is done on the components of the RDN
* There are no specs that require binding of registration management tokens

A certain PKI provider has unreliable OCSP connections. Many banks plan to switch soon. Brazil PKI providers all use a slightly different DN.

Need to have a dedicated session for this problem.


Advanced authorization (Dima)
----------------------------------
Working on issues

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
* Perhaps look at the open issues at OSW. 

JARM (Brian)
----------------------------------------
* PR is being prepared. 

PRs (Dave)
=================

* PR #323 - JARM: fix broken references (Brian)

  * Fixes some hanging references in JARM spec
  * To be merged. 

* PR #315  - FAPI2 iss + JARM

  * Change to a note. 
  * Move to "advanced" as there is no JARM in baseline anymore. 

* PR #324 - Remove reference to RAR in FAPI 2 baseline (Dave)

  * Brian asked if it is wise to push all the authorization stuff to advanced. WG needs to put in effort to finish it.
  * Joseph seconded. 
  * Perhaps call for an additional co-editor? 

* PR #325 - Add Scope and terms

  * Joseph noted that we should mention that public clients are not supported in the scope.
  * Dave will update


* PR #322 Pull-in key management clauses

  * Related to #484 - Key management in FAPI2 Advanced
  * Build error needs to be fixed. 
  * Joseph pointed out that we technically require jwks_uri - we require OIDC discovery, and jwks_uri is required in   Final: OpenID Connect Discovery 1.0 incorporating errata set 1. 
  * Will continue discussing. 

* PR #326 - FAPI2Base: Disallow dpop nonces

  * Related to #477 - FAPI2 + dpop nonces
  * WG agreed to remove dpop nonces on the condition that if the FV finds it to be needed we add it back. 
  * We need to have a new issue around the OIDC nonce. 

* PR #327 - Allow use of EdDSA (Ed25519) (out of time, consider for next meeting)

  * Linked to #492 - EdDSA in FAPI 2.0
  * There was general support for EdDSA to be added as an option.
  * Support for EdDSA was introduced in Nimbus JOSE+JWT 6.0. Note that for EdDSA you need to include the optional Tink dependency in your project. For Nimbus JOSE+JWT 6.0 that would be
  * Joseph expressed concern from the point of view of the interoperability guarantee that certification currently markets itself.


Issues (Dave)
=====================
We were not able to cover it. 



AOB (Nat)
=================
* Please review https://bitbucket.org/openid/fapi/issues/492/eddsa-in-fapi-20



The call adjourned at 15:00 UTC