============================================
FAPI WG Meeting Notes (2022-01-12) 
============================================
* Date & Time: 2022-01-12 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-01-12_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Ali Adnan
  * Ali Brian Campbel
  * Ali Chris Michael
  * Ali Daniel Fett
  * Ali Dima Postnikov
  * Ali Don Thibeau
  * Ali Filip Skokan
  * Ali Joseph Heenan
  * Ali Kosuke Koiwai
  * Ali Lukasz Jaromin
  * Ali Michael Palage
  * Ali Mike Leszcz
  * Ali Nat Sakimura
  * Ali Rifaat Shekh-Yusef
  * Ali Takahiko Kawasaki
  * Ali Adrian Field
  * Ali Srivathsan Morkonda
  * Ali Stephane Mouy
  * Ali Stuart Low

* Regrets: Dave
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* 

Events (Dave/Nat)
======================

Identiverse
------------
Meeting with organizers to follow up on OIDF submissions as well as OIDF sponsorship of Identiverse.



EIC
----

The EIC closing date for proposals Feb 28 - https://www.kuppingercole.com/events/eic2022/callforspeakers


External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
Mike Leszcz was in contact with the CDR team to coordinate a call for next week to get an update briefing from the CDR regarding their FAPI efforts, including a transition to FAPI 2.0. Will also share OIDF updates. 

Possibly might give an update during next week’s call depending on timing of the call.


Brazil (Mike L.)
---------------------------
Continue to receive RP certifications (Currently 19 organisations certified.)

Extended RP community group to  the end of March to encourage RP certifications.

Mike and Joseph was in meeting with Central bank to get an update regarding  CIBA requirements.

Will require CIBA certifications probably at the end of Q1 or during Q2.

Certification team will add  OP and RP CIBA tests for Brazil.


Berlin Group (Dave)
--------------------------------
* Dave to follow up. 

FDX (Mike)
------------------
* n/a 

The Middle East and North Africa (Ali)
---------------------------------------
Waiting for the green light to sign the MOU.

Pending announcement by the central bank of UAE to issue new licenses to challenger banks.

Might be worthwhile to have that information mentioned in the press release preceding the MOU.

Will hear from them next week regarding the signing of the MOU between the OIDF and DFC.

There should be agreed parts on the MOU to have both sides appoint people to discuss next steps.

Will follow Brazil footsteps by using informational workshops about relevant standards and developing a community approach.
 

Mexico (Gail)
------------------
n/a

NIST (Gail)
--------------
NIST IR 8389 is now available for comments. 

See http://lists.openid.net/pipermail/openid-specs-fapi/2022-January/002514.html for more details. 

NIST Page: https://csrc.nist.gov/publications/detail/nistir/8389/draft?utm_campaign=Daily%20News&utm_medium=email&_hsmi=199892597&_hsenc=p2ANqtz-8e00EUjDiF3cjokSiAHdV2blyRoL4PdEUljePvkXfNQO4YqwPt-MachArLcSSoeen1_Y8lc3UlnOD734uGAZX1BPYbUg&utm_content=199892597&utm_source=hs_email

Russia (Dima/Mike)
--------------------
* Bank of Russia is looking at the security profile right now. 
* Dima and Mike is following up. 

UK (Chris)
--------------------
90-days reauthentication requirements are being removed.

The deadline will be March or May

It will be the job of TPP to make sure the consent of the Customer is there.

Europe is potentially planning to extend the time from 90 days to 180 or similar.

Customer has to effectively go back to the bank to reauthenticate. This is a friction point which might cause drop off.

It will be up to TPP to make sure that customers are actually using the services and dosn’t need to involve the bank

FData is writing a paper to feed back into the European consultation.

People with questions or concerns should reach out to ghela.boskovich _at_ fdata.global. She’s coordinating response to European regulators.

GAIN (Mike)
---------------
Participation agreement
~~~~~~~~~~~~~~~~~~~~~~~
It is under review. 

G5
~~~
Consensus on MOU among the five. 
Now socializing with their boards. 

Roadmap (Don)
~~~~~~~~~~~~~~~~
Identifying participants. 35 participants. 

NIST IR 8389  
===================
See http://lists.openid.net/pipermail/openid-specs-fapi/2022-January/002514.html for more details. 

NIST Page: https://csrc.nist.gov/publications/detail/nistir/8389/draft?utm_campaign=Daily%20News&utm_medium=email&_hsmi=199892597&_hsenc=p2ANqtz-8e00EUjDiF3cjokSiAHdV2blyRoL4PdEUljePvkXfNQO4YqwPt-MachArLcSSoeen1_Y8lc3UlnOD734uGAZX1BPYbUg&utm_content=199892597&utm_source=hs_email

Nat to share the Google docs version of it. 

Comments are due March 3, 2022.

The OIDF EC sees not call to action but might take advantage of the chance to educate the NIST community and community at large about FAPI an it’s adoption and roadmap.

FAPI is mentioned in one but doesn’t have much more information.

The document seems to provide an overview of what’s happening in their jurisdiction and does not have concrete cybersecurity considerations for open banking.

The document is lacking details on API security. OIDF can provide more information in this regard.

Mike and Gail will take the lead in drafting an open response and come up with an action plan. Initial effort will be in the WG.


Specs
================
FAPI DCR/M (Dynamic client registration and Management) (Joseph)
------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/466/proposal-for-fapi-dcr-dcm-dynamic-client

Create a FAPI profile for dynamic client registration and dynamic client management, RFC7591, and RFC7592
Australia, UK, and Brazil produced their own profiles. 

WG should create some generic requirements on secured DCR/DM for future ecosystems.

Need to be mindful of markets that have single directory, multi directories, and those that don’t (Bahrain), and private systems that use FAPI

The term directory has different meanings depending on market. 

Small markets  with small amount of banks and third parties don’t need directories. They’re just doing open banking as a single regulator. Only need lists of firms, IDs, and certs.

Directories are used in multi-markets or multi-sector requirements, overall regulations, Open Finance, and multiple regulators.

Joseph will create initial draft for discussion and adoption.


Grant Management (Dima)
----------------------------------------
* Next week. 

PRs (Dave/Nat)
=================

* PR #269 - Compilable http signing, a lot of rejigging to get references right
There are some small issues that need to be resolved before merging.


Issues (Dave/Nat)
=====================
* #466 - Proposal for FAPI DCR/DCM (Dynamic Client Registration/Management) profile

  * Joseph to create initial draft.

* #400 - create bitbucket pipeline for converting markdown files into html

  * Pipeline done.
  * Closed

* #465 - Align the chapter etc. structure to FAPI 1

  * FAPI 2.0’s document structure is completely different from FAPI 1.0. They should have a similar structure to make it easier for comparison, migration, and send off to TC68

* #456 - Proposal - should we remove support for refresh token rotation from FAPI 2.0 (one of the drafts)

  * There is no consensus regarding refresh tokens and will need further discussion.



AOB (Nat)
=================
The following was mentioned: 

FDIC, FinCEN Announces Tech Sprint Focused on Digital Identity Proofing The FDIC and the Financial Crimes Enforcement Network yesterday announced a “tech sprint” to develop solutions for banks and regulators to help measure the effectiveness of digital identity proofing—the process used to collect, validate and verify information about a person. The agencies are asking participants—including banks, nonprofits, academic institutions, private sector firms and members of the public—to consider “what is a scalable, cost-efficient, risk-based solution to measure the effectiveness of digital identity proofing to ensure that individuals who remotely (i.e., not in person) present themselves for financial activities are who they claim to be?” ‌ Registration for the tech sprint will open by the end of January, and interested parties have will until mid-February to apply. The FDIC’s tech lab, FDITECH, and FinCEN will evaluate the submissions and select participants to further develop their proposed solutions and make short presentations to a panel of expert judges. Those presentations will take place in mid-March. https://www.fdic.gov/fditech/techsprints/measuring-effectiveness.html



The call adjourned at 15:00 UTC