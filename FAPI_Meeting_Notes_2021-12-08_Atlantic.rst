============================================
FAPI WG Meeting Notes (2021-12-08) 
============================================
* Date & Time: 2020-12-08 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Ali Adnan
  * Bjorn Hjelm
  * Chris Michael
  * Daniel Fett 
  * Dima Postnikov
  * Domingos Creado
  * Don Thibeau
  * Filip Skokan
  * Francis Pouatcha
  * Gail Hodges
  * Joseph Heenan
  * Mike Leszcz
  * Nat Sakimura
  * Adrian Field
  * Jacob Ideskog
  * Kosuke Koiwai
  * Lukasz Jaromin



* Regrets: Dave
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Status of blog by Dave Tonge
* FAPI 1.0 blog
* Feedback from WG on actions for strategic taskforce

  * Revisit line items for WG
  * Confirm which areas which might have funding requirements for 2022 planning and budgeting


Events (Dave/Nat)
======================

OIDF virtual workshop (Mike L.)
--------------------------------
* Thursday, December 9th at 9 AM PT. 
* Link with registration details: https://openid.net/2021/10/19/registration-open-for-openid-foundation-virtual-workshop-thursday-december-9-2021/
* Dave will not be able to present for the OIDF workshop. 
* Joseph will replace Dave.


GSMA (Gail/Bjorn)
---------------------
The second workshop is on Nov. 29 for deeper technical dive. 

Joseph presented on behalf of FAPI WG. 

Quite a lot of questions about eKYC. 

Recording will be released when available.

OAuth Security Workshop (Daniel)
------------------------------------
OAuthSecurityWorkshop2021 

This is the zoom link we'll use for the event: https://us02web.zoom.us/j/81871097591?pwd=S3U4NTlHZythZXhKa3RkOGFMVTBCUT09

OWS zoom link: https://us02web.zoom.us/j/81871097591?pwd=S3U4NTlHZythZXhKa3RkOGFMVTBCUT09

Recordings will be in Youtube channel.


External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
Started in the certification group on what they might be able to do for FAPI 2.0 Baseline test. 

DSB and another organization may fund development and security analysis of FAPI 2.0.

Gail and Mike will reach out to DSB.

Brazil (Mike L.)
---------------------------
Increase in RP certification. 

Domingos and Marcus had real positive impact. 

Open Banking Brazil milestones are quite fluid. 

Working with Chicago Advisory Partners to extend RP community group pilot, including the Slack channel, through the first quarter of 2022. Directed funding provided to ensure greater RP participation, interoperability, and certifications.


Berlin Group (n/a)
--------------------------------
n/a

FDX (Gail)
------------------
Blog post on FAPI 1 vs. 2 to clarify the status of how OIDF considers FAPI 1.0 so as to not confuse stakeholders around 2 different versions.

Emphasize the maturity of FAPI 1.0, it’s security diligence, and that FAPI 2.0 is still in early development.

Mike Jones volunteered to draft the blog post if not done by next Monday.

Joseph pointed out that the FAPI FAQ covers much of those topics and we could possibly reorganize the content into a blog post instead of creating new content.

Gail, MikeL, and Nat will coordinate on blog post.


The Middle East and North Africa (Ali)
---------------------------------------
Received the draft MOU today.

Content is related to what was discussed:

* Putting together an entity that can promote the OIDF standards to address open banking, finance, and the relative businesses in the sector.

Will forward to Gail and Don.

Don will take a first pass.


Mexico (Gail)
------------------
Gail to help identify someone in Mexico to talk to.

Nat will look back on meeting notes to see if anyone was mentioned.




Russia (Dima/Mike)
--------------------
No updates.

MikeL will follow up.


UK (Chris)
--------------------
n/a

GAIN (Gail)
---------------
Participation agreement
~~~~~~~~~~~~~~~~~~~~~~~
It is being worked on by Gail and Tom. 

Don is now reviewing it. 

Will share with POC chairs when consensus is reached and slowly distribute it more widely for review.

G5
~~~
Consensus on MOU among the five. 

Now socializing with their boards. 

Get final version of the business principles and goals completed  and then share that with the legal stakeholders around the first week of January 2022.

Goal is to finalize by the end of January for distribution and sign up.


Roadmap (Don)
~~~~~~~~~~~~~~~~
Identifying participants for IdP and RP roles.

Emphasized the  importance of OpenID Connect for IDA for that context.

Made advances in substantive planning and guidance documents.

Also reaching out to potential participants.

Will have background and informational paper available by the end of the year.




FAPI DCR/M (Dynamic client registration and Management) (Joseph)
====================================================================
Scope and proposed TOC will be provided by Joseph to the WG list to solicit comments.


European Payments Initiative/Open Banking  (Anders)
====================================================================

The idea is to make the SEPA  payment network more useful.

Has been working for many years but has not succeeded in the last mile problem : enabling SEPA payments in e Commerce, in shops, or for person to person payments.

Created shareholder organization to solve this problem.

How does the  EMV standard fit in? It’s the only user side payment standard that has big acceptance among the whole field, from consumers, merchants, payment intermediaries, and banks.

There is a big gap between open banking payments and EMV.

It’s the same situation with W3C’s Secure Payment Confirmation, based on FIDO and WebAuthn. Also interested in getting into Open Banking.

Bank selection is a common problem for Open Banking and the W3C effort, while EMV has had a solution for 25 years.


Security Analysis Planning (Nat)
===================================================
* CIBA-FAPI Profile Security Analysis (Nat)
* 7.2. FAPI 2.0 Security Analysis (Nat)

There is formal security analysis for FAPI 1.0 but none exists fo CIBA-FAPI profile and FAPI 2.0.
Need to start planning for them.


Budget (Gail)
===============
Strategic Task Force working on strategic direction of the Foundation and related budget for 2022 to ensure clear WG objectives, tactics, and priorities,  and funding requirements.

**FAPI WG objectives:**
* Maintain & evolve standard, close gaps as requirements evolve
* Government/management entity outreach
* Avert fragmentation, encourage profile management within OIDF
* Advocate for OP/RP/TPP certification


**Tactics**
* Standard presentation - standardized presentation of OIDF work, Working groups chairs to work on initial version
* Support FAPI markets
* FAPI Whitepaper and learnings to date for governments considering open banking, open finance, or open data ($12K)
* FDX Whitepaper ($12K)
* Develop OP and RP tests for FAPI 2.0 and recertification
* Brazil Community pilot group -  3 month extension
* Vertical expansion in open Data with Open Finance



Feedback should be sent to Gail by beginning of next week


PRs (Nat)
=================
* PR #304 -  Generate html for all specs in pipeline

  * Pipeline for generating HTML versions of specs
  * Members asked to review for merge


Issues (Dave/Nat)
=====================
Skipped


AOB (Nat)
=================
none


The call adjourned at 15:02 UTC