===========================================
FAPI WG Agenda & Meeting Notes (2022-11-09) 
===========================================
* Date & Time: 2020-10-19T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-11-09_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Bjorn Hjelm
  * Dave Tonge
  * Dima
  * Filip Skokan
  * Joseph Heenan
  * Lukasz Jaromin
  * Mike Leszcz
  * Nat Sakimura
  * Kosuke Koiwai


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



Canada
-----------


New Zealand
-----------

Spec and Spec Process
========================


Lukas asked about the spec process and whether drafts can be referenced.

Implementer’s draft can be referenced, e.g. CIBA

IETF proposed standards can be referenced also

FAPI 2.0 is being sent to OIDF Secretary to begin Second Implementer’s Draft public review for 45 days.

Voting period is 14 days afterwards if no major comments/fixes are required..

60 days public review for final spec will follow and FAPI 2.0 Security profile will be published Spring 2023 barring any problem.


Lukas asked if any one is aware of migration problems from FAPI 1.0 to FAPI 2.0 code flow since FAPI 1.0 allows use of hybrid flow.

He reported some apps would like to get an ID Token before the code is received.

FAPI 2.0 returns ID Token but not in the front channel.

The front channel ID Token is most likely for app developers to display the UI earlier.

Lukas should create an issue to track the use case.

Dima asked about whether FAPI 2.0 and CIBA can be used together.

Would like to use PAR and CIBA.

Filip noted that CIBA core is not compatible with PAR 

* Pass signed request via request parameter and not request_uri
* But does not explicitly forbid request_uri

Need to make a new version of CIBA which aligns with FAPI 2.0


PRs
========

* PR #308 - Add login hint token type registry values to CIBA

  * Awaiting confirmation from Ralph

* PR #347  - scope and resource clarifications

  * Needs review



Issues
========
* #439 - Grant Management API Query Response expiration and issued at

  * Dima will update PR according to comments from Jacob and Brian

* #449 - Field name and type for resources

  * Related to PR #347 - will close once PR is merged

* #544 - FAPI1 vs FAPI2 blog post should be updated

  * Dave will create a drafts for review.
  * One to announce Implementer’s Draft of Security profile
  * And one for comparison of FAPI 1.0 and FAPI 2.0



The call adjourned at 15:15