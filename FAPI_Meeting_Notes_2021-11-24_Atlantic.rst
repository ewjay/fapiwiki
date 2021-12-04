============================================
FAPI WG Meeting Notes (2021-11-24) 
============================================
* Date & Time: 2020-11-24 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Ali Adnan
  * Brian Campbell
  * Chris Michael
  * Daniel Fett
  * Dima Postnikov
  * Domingos Creado
  * Francis Pouatcha
  * Gail hodges
  * Joseph Heenan
  * Kosuke Koiwai
  * Lukasz Jaromin
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Takahiko Kawasaki

* Regrets: Dave
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Adopted as is. 

Events (Dave/Nat)
======================

OIDF virtual workshop (Mike L.)
--------------------------------
* Thursday, December 9th at 9 AM PT. 
* Link with registration details: https://openid.net/2021/10/19/registration-open-for-openid-foundation-virtual-workshop-thursday-december-9-2021/



GSMA (Gail/Bjorn)
---------------------
The second workshop is on Nov. 29 for deeper technical dive. 

Dave is presenting on behalf of FAPI WG. 

OAuth Security Workshop (Daniel)
------------------------------------
OAuth Security Workshop 2021 is coming up https://barcamps.eu/osw2021/

Nov 30 - Dec 1, 2021

Free Virtual Event 

Session proposals are still accepted are scheduling

Some OIDF Session topics:

* Browser interaction, third party cookies
* SIOP cross-device security, risk mitigation
* State of OAuth clients for modern security features


External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
n/a

Brazil (Mike L.)
---------------------------
Hosted RP workshop yesterday. Joseph walked through RP certifications. 

Close to 200 participants. 

Both Marks and Domingos participated. 

Still receiving OP certification requests and RP requests are starting to come in.

Slack channel activity is increasing.

It looks like RP Certification mandate is official for some participants using accounts or payments.

Still questions about which profiles need to be certified (e.g. private key or MTLS).

JARM is not yet required for RPs.



Berlin Group (Francis)
--------------------------------
Meeting was postponed to work on PAR.

Second workshop is pushed to the beginning of next year.         
                                                                                                                                                                                                                                                                               
Gail asked about digital wallet (cryptocurrency, digital euro) movement in EU.

It’s still in early stages and there is a lot of confusion.


FDX (Mike)
------------------
FDX and OIDF Blog posts are now public. 

The Middle East and North Africa (Ali)
---------------------------------------
MOU being developed. 

DIFC wants to speak to a bank to see if they can also be part of the MOU to bring more weight to the relationship.

Russia (Dima/Mike)
--------------------
They will get back later this week. 

UK (Chris)
--------------------
Ongoing consultation on sweeping and vRP use cases and OBIE and OpenFinance future. 

PayByLink http://lists.openid.net/pipermail/openid-specs-fapi/2021-November/002483.html

Request to pay. No interest in the market and has not taken off. 
Berlin group is also looking at something similar as a premium API. 

There is more interest in confirmation to pay but the current regulatory framework is lacking account linking to identity and causing a lot of fraud (same in PayByLink). Confirmation to Pay has made the situation worse. 

There are no concrete solutions to the problem.

One unlikely proposal is to make the receiving banks liable for the fraud so they will be inclined to implement strong KYC, but is not being considered at the moment.


Mexico (Gail)
------------------
There are some standards being drafted that are not public but do not look promising at the moment.

Might be useful for the OIDF to proactively reach out to regulators.


GAIN (Gail)
---------------
MOU agreement is being developed to clarify roles and commitments of “G5” organizations. 

Target date is likely to shift to the beginning of January

Don and Mark Haine are organizing a mega deck to explain the process, flesh out POC, roadmap, split of work between OIDF and OIX.

The roadmap will be shared with the G5 on Dec 1.

Participation agreement for POC is seeing some movement and is targeted for Jan.

eKYC interop event this week with 4 IdPs. Report will be provided at OAuth Security Workshop.


PRs (Nat)
=================
* https://bitbucket.org/openid/fapi/pull-requests/288  -  Implementation advice

  * Joseph and Nat will review

* https://bitbucket.org/openid/fapi/pull-requests/289  - Claims parameter clarification

  * Dima will resolve conflicts.

* https://bitbucket.org/openid/fapi/pull-requests/291  - Introduce notational conventions.

  * Waiting for Stuart to resolve, postponed for next week

* https://bitbucket.org/openid/fapi/pull-requests/295  - Adding another non-normative example for when AS doesn't support resource indicators

  * Waiting for Stuart and Torsten to review - 

* https://bitbucket.org/openid/fapi/pull-requests/294  - Conditions for grant ID issuance

  * If grant is not requested, grant ID should not be issued.
  * Grant ID is requested via grant management action.
  * If requested, it must be issued for all scopes.
  * Dima will consult with GM authors.

* https://bitbucket.org/openid/fapi/pull-requests/292 - Introduce additional examples and remove reference to incremental auth, progress towards

  * Merged


Issues (Dave/Nat)
=====================
* issue #458: FAPI1 Part1: not clear as to which auth flows are supported

  * PKCE is mandated by  Public client 

* Issue #459: Should JARM be mandated for code flow with PAR and PKCE?

  * Australia is transitioning to FAPI 1.0 
  * If using code flow with PAR and PKCE, is JARM still required?
  * Additional spec may face pushback from vendors and  adds additional barrier
  * JARM adds message integrity and mitigation for mix-up attacks
  * FAPI 1.0 is final so changes can’t be made
  * Another option is to stay on Hybrid flow



AOB (Nat)
=================
none


The call adjourned at 15:02 UTC