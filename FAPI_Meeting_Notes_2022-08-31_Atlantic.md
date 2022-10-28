============================================
FAPI WG Meeting Notes (2022-08-31) 
============================================
* Date & Time: 2022-08-31T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-08-31_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Brian Campbell
  * Craig Borysowich
  * Dave Tonge
  * Dima Postnikov
  * Gail Hodges
  * George Fletcher
  * Kosuke Koiwai
  * Nat Sakimura
  * Takahiko Kawasaki
  * Tim Würtele
  * Filip Skokan
  * Lukasz Jaromin
  * Mike Leszcz



* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================
Adopted as is



Feedback to Stuttgart on open items
=======================================
Look at second phase of work to address questions by Ralph

Summary of past few weeks discussions (Dave)
------------------------------------------------

In the process of adding security considerations for various issues that have been found

May make normative changes to authorization code and access token lifetimes to limit some attacks

Tim stated security considerations are hard to interpret. How do we change our model to prevent these kinds of attacks or should these attacks be considered at all?

For Cuckoo’s token attack, we have identified possible mitigations

  * Use different DPOP keys at each AS
  * Send issuer identifier to RS


Mitigations are not mandated but are added to security considerations if such attacks are a concern. 

Treat the recommendations from security recommendations as normative requirements for proof. Specification will call out attacks and mitigations but not mandate them.

Some issues were discussed last week and are resolved.

  * Access token injection with ID Token Replay

     * Reduce access token lifetime to limit attack

Model will have to say some attacks can happen but define the problem away.

Attacker A.5 has the ability to change the token endpoint but if metadata is received from an authoritative source then the attacker no longer needs to be considered.

* #534: Authorization Request Leaks lead to CSRF

  * Put possible mitigations in security considerations

Some PRs have been merged to address attacks

* PR #363 - FAPI2SP: Add requirement for RP to use discovery
* PR #364 - FAPI2SP: Add security consideration for cuckoo's token attack
* PR #365 - FAPI2SP: Document DPoP proof leaks

Tim will review new text and use recommendations in model. 

Will review next week if clarifications are needed



Second Phase for Security Analysis from October Onwards
-----------------------------------------------------------
DSB is going through procurement process for SOW but there are questions from Ralph

* "FAPI 2.0 Advanced" should be called "FAPI 2.0 Message Signing" it seems.       

  * Yes name has been changed

* JARM is just one way of signing message in FAPI 2.0 Message Signing.     Others are JAR, JIR und HTTPSig. Should they be included in the model/analysis as well? 

  * FAPI 2 message signing uses several options for non-repudiation and is purely gears towards meeting non-repudiation goals. FAPI 2 Baseline is the security profile.
  * Can only analyze message signing if the model can somehow prove non-repudiation goals and depends on how non-repudiation is defined.
  * JARM only signs the authorization response and is not used for other messages.
  * JAR is for signing authorization request.
  * Each one is used for different parts of the protocol and are optional.
  * Which ones to use will depend on ecosystem requirements.
  * Tim will review whether the model can proof the non-repudiation properties.
  * Gail will work on how to proceed with the scope of work and leave this issue open for additional feedback.

* For Dynamic Client Registration it should be made clear whether we should look at RFC 7591 or the Australian variant, or both.   

  * There is also the OIDC DCR.
  * Joseph is working on a DCR document to formalize the optionality.
  * Security analysis can model the message signing and determine whether messages need to be signed.
  * Tim will look at all 3 variants and determine the guidance for FAPI DCR.
    
* Same for Dynamic Client Management: RFC 7592 or Australian variant, or both.

  * Need to have a proposal for proceeding forward to assess and then can articulate the differences between different specs and their impacts.
  * RFC 7592 is experimental and is not on the standards track so we may need to reconsider.
  * Will consult with Stuttgart to look at these components and their security implications to create profile choice and before performing formal analysis.
       
* As for FAPI-CIBA, should we model CIBA in addition to the normal  FAPI 2.0 flow or instead of the normal FAPI 2.0 flow. Probably the former, but this should me made clear. While FAPI 2.0 baseline was pretty close to FAPI 1.0, and hence, was easier to handle, WP2 contains several new elements from our point of view. So this will certainly require more effort (manpower and time) from our side.   In particular, I would also formally have to put both Pedram and Tim on     the project (as you know, effectively, they have both been involved     already).  I don't know exactly what RT's time schedule is, but for us it would certainly be much better to have 3 (definition) + 3 (proof) month for WP2. Would that be ok?

  * WG talked about updating CIBA so it will work with both FAPI 1 & 2 but haven’t done the analysis on what is required.
  * Need to make sure there are no contradictions between the 2 FAPI versions.
  * Is CIBA in scope for the next work package? CIBA is in the work package but will need to confirm with AU on where CIBA is within their roadmap to determine urgency.
  * Analysis on CIBA will take more time from the original 4 months to 6 months.
  * AU is looking at using JARM with FAPI 1 soon and FAPI 2 Baseline later. CIBA is not planned.
  * Gail will follow up with Stuttgart and AU

Events & Liaisons (Joseph on behalf of Mike L.)
====================================================

Brazil
-----------------

SAMA
--------------

Nigeria
-----------------


PRs (Nat)
=================
* PR # 358  – Improve description of attacker model

  * Moved non-repudiation messages out of the attacker model into FAPI 2 Message Signing
  * Will renumber the messages that allows for non-repudiation but numbered sections are now referenced by other specs
  * Nat noted that the attacker model uses normative language that mandates other documents
  * Dave will remove normative language from attacker model
  * Also  the case of authorization says, FAPI 2  security profile shall aim to ensure that no one can access resources belonging to a user. Do resources always belong to a user?
  * Resource is something that is controlled by a resource owner.
  * Suggest to change wording to “...resources that the resource owner…”
  * Dave will file another issue to change wording

* PR #367 - Add security consideration for CSRF attack

  * Mitigation 2  - Requiring the Client to only make one authorization code grant call for each  authorization endpoint call. This will prevent attacks where the attacker is  unable to send the authorization response before the honest user does so.
  * Dave is soliciting feedback on better wording



Issues (Nat)
=====================

#541 HTTP Signatures (Justin)

#538 Lifetime of authorization codes

#522 optional ID Token signature validation for code flow {to be discussed next week)



AOB (Nat)
=================


Chat Log
=================

Gail Hodges (OIDF - she/her)
So FAPI 2.0 Spec makes recommendation for a security issue, and if implementor is concerned, the two ways to close it.
Dave Tonge
https://bitbucket.org/openid/fapi/pull-requests/365
Dave Tonge
https://bitbucket.org/openid/fapi/pull-requests/364
Dave Tonge
https://bitbucket.org/openid/fapi/pull-requests/363
Dave Tonge
https://bitbucket.org/openid/fapi/issues/534/authorization-request-leaks-lead-to-csrf
Gail Hodges (OIDF - she/her)


- "FAPI 2.0 Advanced" should be called "FAPI 2.0 Message Signing" it seems.       - JARM is just one way of signing message in FAPI 2.0 Message Signing.     Others are JAR, JIR und HTTPSig. Should they be included in the     model/analysis as well?       - For Dynamic Client Registration it should be made clear whether we     should look at RFC 7591 or the Australian variant, or both.       - Same for Dynamic Client Management: RFC 7592 or Australian variant, or     both.       - As for FAPI-CIBA, should we model CIBA in addition to the normal  FAPI     2.0 flow or instead of the normal FAPI 2.0 flow. Probably the former,     but this should me made clear.         While FAPI 2.0 baseline was pretty close to FAPI 1.0, and hence, was     easier to handle, WP2 contains several new elements from our point of     view. So this will certainly require more effort (manpower and time)     from our side.       In particular, I would also formally have to put both Pedram and Tim on     the project (as you know, effectively, they have both been involved     already).       I don't know exactly what RT's time schedule is, but for us it would     certainly be much better to have 3 (definition) + 3 (proof) month for     WP2. Would that be ok?


There is also a Brazilian DCR spec as indicated in issue #466. https://bitbucket.org/openid/fapi/issues/466/proposal-for-fapi-dcr-dcm-dynamic-client
Dave Tonge


https://bitbucket.org/openid/fapi/pull-requests/358
Dima Postnikov


Last call for feedback on “Open Banking and Open Data: Ready to Cross Borders?” https://openid.net/2022/07/29/whitepaper-open-banking-and-open-data/. If you were planning to review it, please do it this week.


Resources that ro can access?
Dave Tonge


https://bitbucket.org/openid/fapi/pull-requests/367
Nat Sakimura


https://www.terrapinn.com/exhibition/identity-week-asia/agenda.stm
Takahiko Kawasaki


OpenID Connect for Identity Assurance, explained by an implementer https://darutk.medium.com/oidc4ida-93aedffa3058



The call adjourned at 15:03 UTC