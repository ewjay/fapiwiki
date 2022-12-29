===========================================
FAPI WG Agenda & Meeting Notes (2022-11-02) 
===========================================
* Date & Time: 2020-11-02T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-11-02_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Pedram Hosseyni
  * Daniel Fett
  * Rifaat Shekh-Yusef
  * Tim Würtele
  * Nat Sakimura
  * Filip Skokan
  * Joseph Heenan
  * Craig Borysowich
  * Mike  Leszcz
  * Chris Michael
  * Travis Spence
  * George Fletcher
  * Lukasz Jaromin
  * Gail Hodges
  * Kosuke Koiwai
  * Takahiko Kawasaki
  * Ali
  * Pieter Kasselman


* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================

* Events
* External Organizations
* PRs
* Issues


Events (Mike L.)
====================================================




OIDF Workshop prior to IIW Fall 2022
----------------------------------------
Monday, November 14th – OIDF Workshop prior to IIW Fall 2022

Final reminder to register for the OpenID Foundation workshop at Visa on Monday, November 14, 2022 as registration closes today. All participants, in-person and virtual, are required to register: 

https://openid.net/2022/10/24/workshop-at-visa-monday-november-14-2022/


External Orgs & Liaisons (Mike L./Chris)
============================================
Brazil 
-----------


Saudi
---------
SAMA has formerly published the Framework on the standards

Will go live at the end of December but realistically will be next year.

Will have conformance certification requirements



Canada
-----------


New Zealand
-----------

Spec and Spec Process
========================

JARM - spec vote is open until tomorrow.

Still a few votes short of quorum .

WG members are asked to vote.

https://openid.net/2022/10/13/notice-of-vote-for-proposed-final-jwt-secured-authorization-response-mode-for-oauth-2-0-jarm-specification/



PRs
========

* PR #308 - Add login hint token type registry values to CIBA

  * Awaiting confirmation from Ralph

* PR #347  - scope and resource clarifications

  * Needs review



Security Analysis
========================

Overview
----------
Modeled FAPI 2.0 (based on WIM - Web Infrastructure Model)

Formalized Security Goasl form FAPI 2.0 Attachker Model

(Tried to ) Prove Formalized Security Properties

 * Under Atacker assumptions from FAPI 2 Attacker model

Proofs are detailed, systematic mathematical proofs of security properties based on formal model of FAPI 2


Summary of Results
----------
Some of the original security goals are not met under original attacker assumptions

Incorporated changes into model after discussions 

 * Changed attacker assumptions
 * Changed security properties
 * Minor protocol change (clients are required to use AS published metadata document)

Found no violations under adapted assumptions

FAPI 2 is secured  within the formalized security properties


Security Properties
----------
Authorization - no attacker can access protected resources other than his own

Authentication - no attacker is able to log in at a client under the identity of another user

Session Integrity

 * For Authorization  - no attacker is able to force a user to use resources of the attacker
 * For Authentication - no attacker is able to force a user to be logged in under the identity of the attacker

Analysis : Only if authorization request does not leak (i.e. w/o A3a Attacker)


Attacker Model : Changes
----------
Initial Attacker model was too strong; can break all security goals

A3b attacker : Authorization response leakage

 * Breaks authorization and authentication
 * Discussed with WG on Sept 28
 * Discussed invalidating the code at the client but cannot be realistically implemented and there is no practical solution
 * Resolution was remove the A3b attacker to
 * Implementers should ensure that Authorization responses (code) are not leaked

A5 attacker - token endpoint misconfiguration

 * The attacker makes the client use a token endpoint that is not at the honest AS
 * A5 attacker is prevented by requiring server metadata
 
Model: Differences to Specifications
----------
Preventing Cuckoo’s Token attack

 * Sender constrained access token is leaked to attacker
 * Malicious AS replays access token to correct client
 * Possible mitigations

   * Clients use different DPoP keys or MTLS certificates at each AS
   * Clients send issuer identifier the access token was obtained from to the RS and RS need to verify the issuer
   * Shorter lived access token alongside refresh tokens

 * None of the recommendations are required

   * Each mitigation might “mask” some unknown attack

 * Formal model assumes that the client checks whether the requested resource is managed by the AS that issued the access token

Preventing DPoP Proof replay
----------
A7 attacker able to see resource requests thus allowing replayability

Replay of DPop Proofs possible which violates authorization property

Current specs  has no effective mitigation

Formal model assume there is effective replay protection using DPoP nonces which is not mandatory by DPoP spec

Assumes RS invalidates the nonce

Assume resource request leaks after the request was processed by the RS

PR created for change in attacker model document

Further assumptions (Out of scope of FAPI 2)
----------
CSRF protection at client

 * Interaction for initiating the protocol is out of scope
 * Formal model uses a dedicated endpoint that start the flow upon receiving a request
 * Assumes that the endpoint is protected against CSRF

Session Cookie between browser and client

 * Formal model - client sets a browser cookie to establish a session
 * Assumption: protection against session hijacking

Remark : ID Token validation

 * As agreed upon : modeled client does not check ID token signature, but relies on TLS connection information
 * Result : ID token signature verification was not necessary to prove security properties (within the model)


Conclusion
----------
Some original security goals were not met under original attacker assumptions

Adapted goals and assumptions as agreed upon with FAPI WG and made minor change to protocol

Found no violations of adapted goals and assumptions

⇒ ** FAPI 2.0 security profile is secured with the limits of formal model.**


Questions/Comments
----------

* Does the model rely on anything in the ID Token? ID token is optional in FAPI 2. There is no assumption that there is an ID Token.

  * Uses subject information. Nothing in ID token affects authorization property.
  * We mentioned CSRF requirements in the security considerations of spec

* Model does not consider weak cryptography, but does it consider the TLS 1.2, 1.3 handshakes?

  * FAPI limits the 1.2 and ciphers.
  * Model abstracts away this part and assumes a secure authenticated channel.
  * Looks at core FAPI properties and rely on assumptions on security channels

* DPoP nonces are not mandated by DPoP spec and are not required to be one time use and does not provide effective replay protection
  * DPoP 11.1 discusses nonce replayability
  * Single use nonces provide same level of replay protection as jti
  * Added PR #365 for DPoP Proof replayability mitigations
  * Will discuss further at upcoming IETF meeting

* Security analysis slides will be sent to the mailing list 

  * http://lists.openid.net/pipermail/openid-specs-fapi/attachments/20221102/ef10ed6e/attachment-0001.pdf

* How do we position the security analysis so as to amplify the good aspects and make it business friendly?

  * FAPI 2.0 is secured with the current set of goals and assumptions.
  * Dave is writing a document for a blog post for review.


Can start ID2 after merging final PRs

Then it will go to Final.

The Security Analysis will be published at some future conference.

Awaiting some general feedback from WG for final publication.



PRs
========
* PR #381 -  Change attacker model to reflect formal model

  * Syncs attacker model with changes in formal analysis
  * Merged 


Issues
========
* #551 - Extra security considerations for clients as a result of formal analysis

  * Will leave for Final 

* #535 - Attackers A7/A8 break session integrity

  * Resolved by PR #381 - Change attacker model to reflect formal model

* #547 - Make clear if there's items where we would expect ecosystems to make choices?

  * Resolved by PR #378 - FAPI2SP: Add text about further profiling

* #543 - Browser swap attack explained on 2022-09-28
  * Resolved by PR #377 - reduced attacker model

* #522 - optional ID Token signature validation for code flow

  * Resolved by PR #490 

* #542 - A7 Attacker Clarification

  * Resolved by PR #381 - Change attacker model to reflect formal model

* #508 - Security goals requirements ("shalls") may need to be relaxed/reworded

  * Resolved by PR #358 - improve description of attacker model
and PR #382 - Reword to Fix Issue #508

* #549 - Network Layer Protections restrict use of more recent TLS 1.2 ciphers

  * Ciphers were added to TLS 1.2 after the referenced BCP and certification suite still only allow the 4 listed ciphers
  * Set for Final draft

* #550 - Should Network Layer Protections be made server-side enforced?

  * Server shall enforce ciphers and clients are recommended



The call adjourned at 15:15