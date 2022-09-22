===========================================
FAPI WG Agenda & Meeting Notes (2022-09-14) 
===========================================
* Date & Time: 2020-09-14T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-07-10_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Brian Campbell
  * Daniel Fett
  * Dave Tonge
  * Dima Postnikov
  * Filip Skokan
  * Jonik
  * Joseph Heenan
  * Justin Richer
  * Lukasz Jaromin
  * Mike Leszcz
  * Nat Sakimura
  * Pieter Kasselman
  * Ralph Bragg
  * Takahiko Kawasaki
  * Ali Adnan
  * Bjorn Hjelm
  * Dima Postnikov
  * Domingos Creado
  * Kosuke Koiwai
  * Rifaat Shekh-Yusef

* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
Adopted as is. 

External Orgs & Liaisons (Dave/Nat)
====================================================
Secure Identity Foundation Webiner (Mike)
---------------------------------------------
For those interested in the CAEP (Continuous Access and Evaluation Profile) topic, the Foundation and the Identity Defined Security Alliance (IDSE) are hosting a joint webinar on October 5th with Atul from the SSE WG presenting. 

Registration is required: 

https://www.idsalliance.org/webinar/a-guide-to-securing-cloud-access-with-caep/

OIDF Workshop (Mike)
-------------------------
Monday Nov 14 @ San Jose

Mike will send the Registration link to the mailing list when it’s ready

Saudi Central Bank
-------------------------
* Received internal approval to join OIDF and FAPI WG. 
* Finalizing FAPI Adoption with FAPI 1.0 with PAR to ensure migration to FAPI 2.0. 
* Now in the process of responding to various proposed certification models by Saudi.


Brazil (Mike/Joseph)
----------------------
* Received CIBA specification for BR. 
* Joseph has done the review of it. Nine issues were raised in the BR issue tracker. 
* Open Finance BR anticipate 108 institutions to be re-certified towards the end of the year. 
* Open Insurance deadline pushed to Dec.  

  * Phase 1 (66 institutions) to be finished by Dec.31. 
  * Dates are still fluid.  

ISO SC27 (Nat)
-------------------
SC27 meeting is in 2 weeks.

Nat is sending out the liaison statement imminently. 

Please send the text to be sent ASAP if you have one regarding our activities. 


PRs (Dave/Nat)
=================

* PR #369 Proposal to improve PR for Issue #534 (Daniel)

  * Related to #534 - Authorization Request Leaks lead to CSRF
  * PR to another PR.  Changed order of sentences and points out that this is an issue only with redirect based flows.
  * Incorporating the remarks that Tim made.
  * Ralph asked what is the conformance program expecting from the 3  potential mitigations?
  * There are no checks planned since they are not normative.
  * Some of the attacks require a strong attacker model and mitigations across all ecosystems may be too complex for normative text to be added.
  * Proposed mitigation #3 for reduced authorization code lifetime is filed as #538 - Lifetime of authorization codes

* PR # 368 - Add mentions of Authorization Code Binding to DPoP key

  * The word “may” discourages usage but is permitted. “Should” is suggested. 
  * The original intent was to raise the possibility of such a binding. Will change to a note and remove normative language. 
  * The AS is required to support it but not the client.
  * Joseph will update.

* PR #358 - Improve description of attacker model

  * Changed wording from “access resources belonging to a user” to “access protected resources”
  * Changed “obtain and use an access token belonging to a user” to “obtain and use an access token”
  * Suggested to change “to access protected resources that they should not have access to”
  * Support for non-repudiation

    * PAR - yes
    * Response to PAR - no
    * Authorization request front channel - Implied via PAR
    * Authorization Response - JARM
    * ID Token content, introspection responses - yes
    * Userinfo - out of scope for OAuth but it’s a protected resource and it’s covered under the signing responses for resource servers.

  * Dave will update.

* PR #308 - Add login hint token type registry values to CIBA

  * Added the backchannel_endpoint_login_hint_token_types_supported and backchannel_endpoint_login_hint_token_types to discovery metadata
  * Might need to make a FAPI 1 CIBA and FAPI 2 CIBA

* PR #369 Proposal to improve PR for Issue #534 (Daniel)

  * Incorporating the remarks that Tim made. 

Issues (Dave/Nat))
=====================
* #541 HTTP Signatures (Justin)

  * Suggested to split sections into “requests from the client to the RS” and “responses from the RS to the client” and make requirements more explicit
  * Made some recommendations for what is required in the signature
  * Don’t sign the date header 
  * Better to sign the created parameter.

* #538 Lifetime of authorization codes

  * This is a issue for one of the mitigations for #534 - Authorization Request Leaks lead to CSRF
  * Shorter authorization code lifetimes reduce the attack surface. 
  * WG is in favor to change lifetime to 60 seconds. Will align with the OAuth WG discussion outcome.

* #522 optional ID Token signature validation for code flow {to be discussed next week)



AOB (Dave/Nat))
=================


Cross device flows and threats and mitigations (Peter Kasselman)
----------------
Discussion in IETF Vienna regarding Cross device flows and threats and mitigations.

Created a document with Daniel and Filip that described the attacks and mitigations.

https://docs.google.com/document/d/1Cka4ZZvi4z-nf55UbW4nmtgzlfAZSLLR4CRkvv3xVKc/edit?usp=sharing

Peter requested interested parties to review and provide feedback.

Also in what form the final document should be and whether it is valuable enough to continue pursuing the issue.




The call adjourned at 15:00 UTC


Chat Log
============

* Mike Leszcz to Everyone	11:00 PM	Hello all. I'm going to start recording for note taking. Thank you.
* Me to Everyone	11:03 PM	1.   Roll Call (Nat)
* 2.   Adoption of Agenda (Dave/Nat)
* 3.   Events & Liaisons (Dave/Nat)
* 4.   External Orgs & Liaisons (Dave/Nat)
* 5.   PRs (Dave/Nat)
* 6.   Issues (Dave/Nat))
* 7.   AOB (Dave/Nat))
* Mike Leszcz to Everyone	11:04 PM	https://www.idsalliance.org/webinar/a-guide-to-securing-cloud-access-with-caep/
* Dave Tonge to Everyone	11:13 PM	https://bitbucket.org/openid/fapi/pull-requests/369
* Pieter Kasselman (Microsoft) to Me	11:15 PM	Hi Nat, if there is a minute at the end of the call, I would like to ask participants to review an early draft of the cross-device threats and mitigations document that was created over the summer.
* Dave Tonge to Everyone	11:15 PM	https://bitbucket.org/openid/fapi/pull-requests/368
* Me to Pieter Kasselman (Microsoft)	11:17 PM	Sure. 
* Pieter Kasselman (Microsoft) to Me	11:17 PM	You may recall cross device flows was a topic at IETF 113, IETF 114, OSW and Identiverse. and this is an attempt to capture all the feedback and thoughts we gathered from everyone.
* Pieter Kasselman (Microsoft) to Me	11:17 PM	The document is here: https://docs.google.com/document/d/1Cka4ZZvi4z-nf55UbW4nmtgzlfAZSLLR4CRkvv3xVKc/edit?usp=sharing
* Pieter Kasselman (Microsoft) to Me	11:17 PM	Thanks Nat.
* Dave Tonge to Everyone	11:19 PM	https://bitbucket.org/openid/fapi/issues/538/lifetime-of-authorization-codes
* Daniel Fett (yes.com) to Everyone	11:24 PM	+1 for Note
* Dave Tonge to Everyone	11:30 PM	https://bitbucket.org/openid/fapi/pull-requests/358
* Ralph Bragg to Organizer(s) only	11:30 PM	Joseph - if it is a MAY, how would RPs certify that they CAN use this correctly? Seperate profile? Option on conformance?
* Ralph Bragg to Everyone	11:30 PM	Joseph - if it is a MAY, how would RPs certify that they CAN use this correctly? Seperate profile? Option on conformance?
* Dave Tonge to Everyone	11:31 PM	https://bitbucket.org/openid/fapi/commits/b21f2db1bd9215d50fef99848307acd6197853f7
* Joseph Heenan (OIDF/Authlete) to Organizer(s) only	11:31 PM	Ralph: My intention at this stage would be just to verify that the value is correct **iff** the client supplies a value.
* Joseph Heenan (OIDF/Authlete) to Everyone	11:31 PM	Ralph: My intention at this stage would be just to verify that the value is correct **iff** the client supplies a value.
* 
* 
* Justin Richer to Everyone	11:33 PM	"cannot access protected resources that they do not have access to."
* Justin Richer to Everyone	11:33 PM	or "would not have access to."
* Dave Tonge to Everyone	11:37 PM	https://bitbucket.org/openid/fapi/pull-requests/308
* Dave Tonge to Everyone	11:40 PM	https://bitbucket.org/openid/fapi/issues/541/http-signatures
* Dave Tonge to Everyone	11:44 PM	https://bitbucket.org/openid/fapi/issues/538/lifetime-of-authorization-codes
* Joseph Heenan (OIDF/Authlete) to Everyone	11:48 PM	Dave: maybe https://bitbucket.org/openid/fapi/issues/539/access-token-lifetime
* Dave Tonge to Everyone	11:49 PM	ok, lets see if we have time
* Filip Skokan (Okta) to Everyone	11:49 PM	https://bitbucket.org/openid/fapi/issues/522/optional-id-token-signature-validation-for
* Pieter Kasselman (Microsoft) to Me	11:49 PM	https://docs.google.com/document/d/1Cka4ZZvi4z-nf55UbW4nmtgzlfAZSLLR4CRkvv3xVKc/edit?usp=sharing
* Pieter Kasselman (Microsoft) to Everyone	11:49 PM	https://docs.google.com/document/d/1Cka4ZZvi4z-nf55UbW4nmtgzlfAZSLLR4CRkvv3xVKc/edit?usp=sharing
* Joseph Heenan (OIDF/Authlete) to Everyone	11:53 PM	Pieter: The IETF RAR draft mentions CIBA, so it's probably okay to do so
* Joseph Heenan (OIDF/Authlete) to Everyone	11:57 PM	https://arxiv.org/abs/1901.11520 is the doc Nat is referring to I think