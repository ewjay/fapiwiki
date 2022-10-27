===========================================
FAPI WG Agenda & Meeting Notes (2022-10-12) 
===========================================
* Date & Time: 2020-10-12T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-10-12_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Brian Campbell
  * Chris Michael
  * Daniel Fett
  * Filip Skokan (Okta)
  * Gail hodges
  * Joseph Heenan (OIDF/Authlete)
  * Kosuke Koiwai
  * Mike Leszcz
  * Nat Sakimura
  * Pieter Kasselman (Microsoft)
  * Ralph Bragg
  * Bjorn Hjelm
  * Craig Borysowich
  * Dima Postnikov
  * Justin Richer
  * Matt L
  * Michael Palage
  * Takahiko Kawasaki


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

OIDF Strategy and FAPI Panel – 1:45-2:40pm PT – Gail Hodges & Anoop Saxena

Link to the OIDF sessions at Authenticare and FIDO Plenary: 

https://openid.net/2022/10/05/announcing-openid-foundation-sessions-at-authenticate-2022-and-the-fido-member-plenary/

FIDO Member Plenary
-----------------------
Wednesday, October 19th – OIDF Sessions at FIDO Member Plenary

9:00-9:10 -- Welcome & Opening Remarks

    Presenter: Gail Hodges - OpenID Foundation Executive Director

9:10-9:45 -- Shared Signals & Events: A Secure Webhooks Framework

    Presenter:  Atul Tulshibagwale - SGNL

9:45-10:20 -- OpenID for Verifiable Credentials (OpenID4VC): Addressing Self-Sovereign Identity, Decentralized Identity, or User-Centric Identity

    Presenter: Kristina Yasuda – Microsoft

10:20-10:55 -- "A Review of the Global Assured Identity Network (GAIN): One Year On"

    Presenter:  Elizabeth Garber - Co-Chair GAIN Proof of Concept

10:55-11:30 -- OIDF Government Whitepaper Listening Session: "Citizen-Centric Identity Systems"

    Presenter: Elizabeth Garber – Whitepaper Co-Author

11:30-12:05 -- OIDF Privacy Whitepaper Listening Session: “Help Design a Scalable Future for Personal Privacy”

    Presenter: Heather Flanagan - Principal at Spherical Cow Consulting

12:05-12:30 -- Closing Remarks, Open Q&A and Networking

    Presenter: Gail Hodges – OpenID Foundation Executive Director


FDX Global Summit Fall 2022
----------------------------------
October 18th – 19th – FDX Global Summit Fall 2022

Wes Dunnington & Joseph Heenan will be presenting “The journey from OAuth to FAPI: Why should I do this and what do I need to know?” (reference final agenda for date and time TBC)

OIDF Workshop prior to IIW Fall 2022
----------------------------------------
Monday, November 14th – OIDF Workshop prior to IIW Fall 2022

* Finalizing host location in the Mountain View area.
* Details including registration link will be published to the OIDF website.


External Orgs & Liaisons (Mike L./Chris)
============================================
Brazil 
-----------
OPIN will require 66 institutions to certify for OP and RP.

Two have already certified.
 
Open Finance - FAPI recertifications are increasing.


SAMA/Saudi
---------
Scheduling a follow up call to discuss certification options.

Canada
-----------
Working through due diligence.

New Zealand
-----------
No updates


Security Analysis (Daniel)
=============================
After discussions, it is concluded that we cannot defend against the attacker model that can see authorization responses.

Will remove Attacker A3B which can read arbitrary responses since protocol security is not ensured.

There are few circumstances where an attacker can see responses and also launch an attack which requires phishing/CRSF at the same time.

This is a general problem for redirect-based protocols. 

Will need to document this in security considerations..





PRs
========

* PR #376 - FAPI2SP: Correct request_uri lifetime value in comparison table

  * Corrects error in the comparison table
  * Changed to match 600 seconds in normative text
  * Brian suggested since this is not normative, it is better to say “limited lifetime” instead of actual value to prevent getting out of sync
  * Joseph will update

* PR #368 - Add mentions of Authorization Code Binding to DPoP key

  * Joseph resolved merge conflict
  * Will be merged

* PR #347 - scope and resource clarifications

  * Waiting for an update after previous discussion

* PR #370 - Addressing issue #531 - Adding normative references clause in FAPI_2_0_Security_Profile.md

  * Normative section will be duplicated
  * Will lead to sync issues
  * Would like ID-draft to be similar to the final as much as possible
  * Will update PR to reference the actual section instead

* PR #308 - Add login hint token type registry values to CIBA

  * Dave updated PR to address Ralph’s comments
  * Will need to update reference numbers in certification test suite



Issues
========
* #547 - Make clear if there's items where we would expect ecosystems to make choices?

  * Specs leave some choices up to ecosystems to decide
  * State that the spec expects ecosystems to make such choices and should make them clear for their use cases
  * E.g. MTLS token binding to certificate, refresh tokens
  * Should also point out in text that if security assumptions are changed, then security is not guaranteed
  * Daniel suggested to also highlight the reasons to use a specific profile of the spec as is, with certain options reduced.
  * Joseph suggested to avoid enumerating the options that ecosystems must make since there are many 
  * Assigned to Joseph

* #546 - lower limit on request_uri lifetime in FAPI2 may be too short

  * Brazil is seeing problems where request_uris expire before being able to use them
  * Round trips on mobile devices with bad connections and required user interactions can exceed the 5 seconds minimum
  * Brian suggested to not specify the lower bound and just use the upper bound of 600 seconds
  * AS can choose the appropriate time limit but RPs may not be able to meet the time limit
  * The current range limit allows AS to pick from 5 - 600 seconds which should suffice to satisfy most use cases so increasing the lower bound may not resolve an actual problem
  * Increase the lower bound to 30 seconds and provide note on how to pick a time value that is appropriate for the client and environment
  * Nat suggested to change the SHALL to SHOULD 
  * WG agreed to change to SHOULD
  * Assigned to Joseph

* #544 - FAPI1 vs FAPI2 blog post should be updated

  * WG members to provide text suggestions

* #543 - Browser swap attack explained on 2022-09-28

  * Attacker model to remove A3 model and add security considerations
  * Create another issue for the attacker model

* #539 - Access token lifetime

  * Need to update wording to address Dima’s comment

* #548 - Proposed new FAPI1-Adv test: consistent sub from different authorisations for same client

  * Some Brazil banks are not returning subs consistently between authorizations
  * There is OIDC test to detect this condition but not for FAPI
  * Add a test before Brazil recertification begins
  * WG to chime in 



The call adjourned at 15:15