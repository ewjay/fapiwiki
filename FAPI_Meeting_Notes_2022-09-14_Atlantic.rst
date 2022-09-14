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
* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================

External Orgs & Liaisons (Dave/Nat)
====================================================
Secure Identity Foundation Webiner (Mike)
---------------------------------------------
* https://www.idsalliance.org/webinar/a-guide-to-securing-cloud-access-with-caep/

OIDF Workshop (Mike)
-------------------------
* Monday Nov 14 @ San Jose

Saudi Central Bank
-------------------------
* Received internal approval to join OIDF and FAPI WG. 
* Finalizing FAPI Adoption with FAPI 1.0 with PAR to ensure migration to FAPI 2.0. 

Brazil (Mike/Joseph)
----------------------
* Received CIBA specification for BR. 
* Joseph has done the review of it. Nine issues were raised in the BR issue tracker. 
* Open Finance BR anticipate 108 institutions to be re-certified towards the end of the year. 
* Open Insurance deadline pushed to Dec.  Phase 1 (66 institutions) to be finished by Dec.31. Dates are still fluid.  

SC27
--------- 


PRs (Dave/Nat)
=================
PR369 Proposal to improve PR for Issue #534 (Daniel)
------------------------------------------------------
Incorporating the remarks that Tim made. 

Issues (Dave/Nat))
=====================
* #541 HTTP Signatures (Justin)
* #538 Lifetime of authorization codes
* #522 optional ID Token signature validation for code flow {to be discussed next week)



AOB (Dave/Nat))
=================


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