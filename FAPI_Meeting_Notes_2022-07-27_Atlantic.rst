============================================
FAPI WG Meeting Notes (2022-07-27) 
============================================
* Date & Time: 2022-06-29T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-07-27_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Chris Michael
  * Dave Tonge
  * Gail Hodges
  * Giuseppe De Marco
  * Joseph Heenan
  * Mike Leszcz
  * Nat Sakimura
  * Torsten Lodderstedt
  * Dima
  * Takahiko Kawasa


* Regrets: 

* Guest: 

Adoption of Agenda (Nat)
================================

* Events and External Organizaions
* Whitepaper proposal by Chris
* PR & Issues
* Security Analysis Issues


Events & Liaisons (Joseph on behalf of Mike L.)
====================================================

Events happening in parallel to FAPI WG meeting
-----------------------------------------------
* OAuth WG side meetings
* Blockchain governance discussing central backed digital currencies and financial internet


FIDO 
-----------------------------------------------
* Asked OIDF to speak at Authenticate and plenary about FAPI 
* Authenticate Oct 17-19 Seattle (FIDO) followed by the plenary for members 20-22. 
* https://authenticatecon.com

FedID conference
-----------------------------------------------
* Gail will speak about mDL and digital identity standards
* Sept 7 
* https://events.afcea.org/FedID22/Public/enter.aspx


American Association of Motor Administration Conference
-----------------------------------------------
* Sep 13-15. https://www.aamva.org/events-education/conferences-meetings/conferences/2022-annual-international-conference
* Gail will speak about mDL and issuance



External Orgs & Liaisons
====================================================
Brazil
-----------------
NA

SAMA
-----------------
Will start consultation regarding which version of FAPI to use

Chris has drafted a paper to provide general guidance for markets to avoid fragmentation.

There are 3 or 4 markets in MENA region and 3 or 4 in Latin America looking to start open banking.

The goal is to recommend ecosystems to use FAPI 2 and encourage regulators to strongly enforce conformance or certification.

It proposes that ecosystems and standards bodies adopt FAPI 1 Advanced  with PAR for now and move to FAPI 2 when it is ready.

Chris inquired about whether the paper can be published by OIDF on the website or as a note pointed to by OIDF and the process for doing so.

Torsten is concerned that the paper recommends FAPI 1 with PAR for now since it is more complex than FAPI 2 mainly due to the reason that FAPI 2 is not finalized. FAPI 2 Baseline has been stable for a long time.

Chris : The main concern is that banks are reluctant to adopt specifications that are still drafts, especially for regulated ecosystems and mandates.

Torsten : FAPI 2 is much simpler using PAR, PKCE and MTLS which are all published standards and Baseline is stable.Why isn’t Baseline finalized?

Waiting for Security analysis to complete before publishing FAPI 2 Baseline.

There are precedents for adopting non-final specs. E.g. FAPI 1 references JARM, OP-UK required draft-cavage-http-signatures which was not on the standards track.

SAMA is issuing lots of mandates and is not comfortable with draft specs.

Security analysis is expected to be done by Sept 30.

Torsten : We should aim to widely recommend FAPI 2 instead and work with SAMA regarding FAPI 1.

Chris - The paper's summary recommends that ecosystems move to FAPI 2 as soon as it’s ready so it is only temporary.

We can use a softer tone and adjust the message for different markets.

This paper attempts to recommend a smooth migration path to FAPI 2 for ecosystems that must use finalized specs.

Gail suggested sending the paper attached to a letter from the OIDF to SAMA.

SAMA also would like to finalize the certification model. They would like to be the certifying body.

FAPI 2 certification tests have been developed and are being beta-tested currently.

Gail and the chairs will review the document and decide how to forward it to SAMA.



Global Open Finance Center of Excellence
-----------------
UK based GOFCoE may potentially be migrated to OIDF to form a Community Group adjacent to FAPI WG comprised of academics and gov.


Nigeria
-----------------
NA


PRs (Nat)
=================




Issues (Nat)
=====================


525 - Decide on what to do for A. Cuckoo’s Token Attack
--------------------------------------------------------
#525 - Decide on what to do for A. Cuckoo’s Token Attack

Add security  consideration for this attack. Requires a malicious AS which is unlikely to happen in many regulated ecosystems, but may be a problem for open ecosystems.

FAPI 1 has text regarding this attack.

Bad AS could advertise endpoints for honest RS. Assumes that the trust anchor for the ecosystem fails.

Mostly affects clients that support dynamic registration so we should put some security consideration around that.

526 - Decide on B. Access Token Injection with ID Token Replay
--------------------------------------------------------
#526 - Decide on B. Access Token Injection with ID Token Replay

The security analysis https://arxiv.org/pdf/1901.11520.pdf recommends ID Token from the Token Endpoint to include the hash of the access token for FAPI 1.0.

What should we do for FAPI 2? FAPI 2 does not require ID Token which acted as a detached signature.

We need to decide whether we want to rely on server authentication or use a model where all communication is authenticated at the message level. FAPI 2 relies on server authentication so if we need to introduce it on the application level, we will need to reintroduce all the signed request and response of FAPI 1.

Need to decide whether we modify the attacker model or cope with the attack.

528 - PKCE Chosen Challenge Attack
--------------------------------------------------------
#528 - PKCE Chosen Challenge Attack

Out of time to discuss 



AOB (Nat)
=================

The call adjourned at 15:03 UTC