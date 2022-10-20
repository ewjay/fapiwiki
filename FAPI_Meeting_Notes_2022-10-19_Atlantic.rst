===========================================
FAPI WG Agenda & Meeting Notes (2022-10-19) 
===========================================
* Date & Time: 2020-10-19T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-10-19_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Bjorn Hjelm
  * Chris Michael
  * Daniel Fett
  * Dave Tonge (Moneyhub)
  * Dima Postnikov
  * Filip Skokan (Okta)
  * Naohiro Fujie(OIDF/OIDFJ)
  * Nat Sakimura
  * Ralph Bragg
  * Takahiko Kawasaki
  * Brian Campbell (Ping Identity)
  * Craig Borysowich
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


Authenticate
-----------------------
Tuesday, October 18th – Authenticate – Seattle
o   OIDF Strategy and FAPI Panel – 1:45-2:40pm PT – Gail Hodges & Anoop Saxena

FIDO Member Plenary
-----------------------
Wednesday, October 19th – OIDF Sessions at FIDO Member Plenary

* 9:00-9:10 -- Welcome & Opening Remarks

  * Presenter: Gail Hodges - OpenID Foundation Executive Director

* 9:10-9:45 -- Shared Signals & Events: A Secure Webhooks Framework

  * Presenter:  Atul Tulshibagwale - SGNL

* 9:45-10:20 -- OpenID for Verifiable Credentials (OpenID4VC): Addressing Self-Sovereign Identity, Decentralized Identity, or User-Centric Identity

  * Presenter: Kristina Yasuda – Microsoft

* 10:20-10:55 -- "A Review of the Global Assured Identity Network (GAIN): One Year On"

  * Presenter:  Elizabeth Garber - Co-Chair GAIN Proof of Concept

* 10:55-11:30 -- OIDF Government Whitepaper Listening Session: "Citizen-Centric Identity Systems"

  * Presenter: Elizabeth Garber – Whitepaper Co-Author

* 11:30-12:05 -- OIDF Privacy Whitepaper Listening Session: “Help Design a Scalable Future for Personal Privacy”

  * Presenter: Heather Flanagan - Principal at Spherical Cow Consulting

* 12:05-12:30 -- Closing Remarks, Open Q&A and Networking

  * Presenter: Gail Hodges – OpenID Foundation Executive Director


FDX Global Summit Fall 2022
----------------------------------
October 18th – 19th – FDX Global Summit Fall 2022

Wes Dunnington & Joseph Heenan will be presenting “he journey from OAuth to FAPI: Why should I do this and what do I need to know?” (reference final agenda for date and time TBC)

OIDF Workshop prior to IIW Fall 2022
----------------------------------------
Monday, November 14th – OIDF Workshop prior to IIW Fall 2022

* Finalizing host location in the Mountain View area.
* Details including registration link will be published to the OIDF website.


External Orgs & Liaisons (Mike L./Chris)
============================================
Brazil 
-----------
No updates

Saudi
---------
Saudi Government has selected FAPI 1.0 with PAR for launch this year and will migrate to FAPI 2.0 when it is final. 

Will hold weekly meetings to support launch.

Two or three banks have been confirmed to test the certification tests.

Saudi will also deploy the third party certification model. Still in talks.

Still looking at the whole certification framework to certify functional stuff and other processes.

Not sure in what order things will proceed.


Canada
-----------
No updates

New Zealand
-----------
New Zealand to expected to pass legislation like Australia CDR later this year.


Security Analysis (Daniel)
=============================
Stuttgart Security Analysis is due to be finished by the end of this week.

Have some questions regarding DPoP.

Nonce mechanism protects against reply but there are weaker options available such as not rotating nonce after every request/response.

How should this be modeled? If nonce is not rotated after every request/response then there is replay probability. 

Assuming nonce is rotated, then there is strong protection against replay but will add text stating that for practical reasons,  weaker mechanisms such as not rotating nonce can be used.

Should put a security consideration in the final version of analysis. Daniel will double check.

Australia DSP is completing the contract for Work Package 2 of the Security Analysis, including DCM, CIBA,and signing. Awaiting delivery of Stuttgart work before awarding next contract. Will start work at the start of November for six months.

OIDF is looking for co-funding partners for Work package 3 to start Spring 2023,  to cover Grant Management, OIDC for IDA and SSE

Australia DSP also asked for a brief  on certification capability.



Open Data Cross Borders Whitepaper (Dima)
============================================

Dima is updating the draft after discussions and will distribute it to the list when it is ready.



PRs
========

* PR #377 - Reduced attacker model

  * Dave will review and merge

* PR #370 - Addressing issue #531 - Adding normative references clause in FAPI_2_0_Security_Profile.md

  * Dave will review and merge

* PR #376 -  FAPI2SP: Correct request_uri lifetime value in comparison table

  * Dave will review and merge

* PR #379 - FAPI2SP: Rework lower limit on request_uri expires_in

  * Dave will review and merge
 
* PR #378 - FAPI2SP: Add text about further profiling

  * Some regions may profile FAPI 2.0 Security profile to make it incompatible or weaken some options that will   * invalidate Security Analysis still believing it is secure.
  * Propose to add consideration regarding profiling.


* PR #375 - improvements to http sig wording

  * Need to address feedback before merging
  * Used fapi-2-request and fapi-2-response for signature naming convention
  * The rest is specific profiling of HTTP signature draft


* PR #308 - Add login hint token type registry values to CIBA

  * Add standard mechanism to store metadata token types
  * Need to address additional comments from Joseph before merging


* PR #347 - scope and resource clarifications

  * Taka and Filip to review 
  * Additional comments to be addressed
  * Should issue WG last call for additional comments.


Security Profile will be ready for public review once PRs are merged.

Possibly, HTTP Signature will be ready for First ID

Possibly, Grant Management will be ready for 2nd ID.


Issues
========
* #522 - optional ID Token signature validation for code flow

  * Security Analysis outcome is expected to consider the signature validation as optional
  * Joseph is using that as input to  incorporate that as part of certification tests.
  * Depending on final outcome of analysis, will need language to state signature validation requirements.
  * OIDC ID Token signature validation is optional for code flow when ID Token is returned from token endpoint. TLS server validation is used to validate the issuer.
  * Awaiting Security analysis outcome. Assigned to Filip to follow up.


* #546 - lower limit on request_uri lifetime in FAPI2 may be too short

  * Related to PR #379  - to be merged after review

* #547 - Make clear if there's items where we would expect ecosystems to make choices?

  * Related to PR #378 - to be merged after review

* #543 - Browser swap attack explained on 2022-09-28

  * Related to PR #377 - to be merged after review

* #545 - FAPI2SP vs FAPI1 table has incorrect value for request_uri lifetime

  * Related to PR #376 - to be merged after review

* #539 - Access token lifetime

  * Related to PR #374- Dima will review PR and merge.

* #544 - FAPI1 vs FAPI2 blog post should be updated

  * Update post regarding differences between FAPI 1.0 and 2.0 after public review.

* #534 - Authorization Request Leaks lead to CSRF

  * Resolved with PR #367

* #531 - Insert "2. Normative references" to comply with ISODIR2

  * Resolved with PR #370 

* #523 - Rotation of Refresh token - Compromised client highlighted by AU - CDR Independent review

  * Awaiting feedback from the Australian team but will close for now.
  * Will discuss with Australia on the coming Friday call.

* #465 - Align the chapter etc. structure to FAPI 1

  * Close due to duplicate issue

* #506 - Explict security target

  * Attacker model is for the security profile.
  * Will need a delta of the attacker model for other specs.
  * Will reassign to other CIBA spec.


* #449 - Field name and type for resources

  * Awaiting implementer feedback. Filip and Taka will review.

* #439 - Grant Management API Query Response expiration and issued at

  * Awaiting implementer feedback. Filip and Taka will review.


* #520 - Versioning for first draft of FAPI2-Advanced

  * Joseph proposed the message signing spec keep the same numbering in sync as the baseline security profile.
  * Having a different implementer’s draft number is not an issue and numbers should not be skipped


The call adjourned at 15:15