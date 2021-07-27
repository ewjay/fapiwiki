============================================
FAPI WG Meeting Notes (2021-07-21) 
============================================
* Date & Time: 2020-07-21 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-07-21_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:04 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Nat, Dave, Don, Kosuke, Alik, Takahiko, Dima, Chris Michael, Filip, Brian, Daniel, Francis, Domgos, Danillo, Joseph, CHris Wood, Edmund
* Regrets: Dave
* Guest: 


Adoption of Agenda (Dave/Nat)
================================
* Nat

Events (Dave/Nat)
======================
n/a

External Organizations (Dave/Nat)
===================================
Australia (Dima/Joseph)
------------------------------------
n/a

Berlin Group (Francis)
----------------------------
* A letter received from Bruno @ BG. 
* IPR checks with OIDF Counsel needed. 
* Probably a good idea to invite them to Sept. 13 Workshop in Munich prior to EIC. 
* https://www.kuppingercole.com/events/eic2021
* https://www.kuppingercole.com/sessions/4592


Brazil ()
---------------------
* Chris M.: 9 profiles. Banks are picking and choosing a few of them. It will be not good for RPs. 
* Clarification for the fee structure would be good. 
* One fee for 9 profiles but how much weeks are allowed between profiles?

  * Joseph to investigate improvements to fees page
 
* PAR is recommended. (Four PAR profiles...)

  * Private Key +PAR
  * MTLS + PAR
  * Private Key + PAR +JARM
  * MTLS + PAR + JARM

* Not sure how many banks will support JARM. It’s optional in Brazil and FAPI specs
* Might lead to confusion and fragmentation

Brazil Phase 2 deadline has been extended to August 13, 2021. We still have 16 certifications to process as part of Phase 2 and expect those no later than Friday, August 6, 2021. 

The phase 3 deadline has been confirmed for August 31, 2021. Phase 3 banks are required to have certification requests to the Foundation no later than Monday, August 16, 2021. We are starting to receive inquiries from Phase 3 banks. We are in the process of confirming the banks and number of certifications with the Mirow team for Phase 3. 

The central bank and the Security Working Group as still considering requiring RP certifications in BR. There is strong support thus far. These certifications would not be required until later this year. 
CIBA is going to be required but not until Q4 2021. The exact milestones are being confirmed

* Phase two is delayed until 13th August. 
* Phase three is at the end of August for 400 banks. 

* RP certifications is hard. 

  * Not as mature as OP testing. 
  * But is recommended as it leads to less interoperability problems. 
  * Need to make lessen barriers to certification.
  * Client implementation is the main difficulty. 
  * Also concerned about CIBA.

* Workshop for TPPs may be needed. They are very concerned. 
* Summary of RP implementation experience may be helpful.
* Certification is for a deployment, not just software.
* Awaiting confirmation for RP certification requirement before finalizing plans for RP workshop for TPPs
* Unless it’s mandated, justification for building RP tests may be lacking
* If it’s difficult, central bank may lower mandatory standards


FDX (Don)
------------------
* Expected to adopt FAPI in the next Summit. 

MENA (Ali)
-----------------
* Did a panel last week - Educate key players in the region. 
* Having meeting with Mr Jeffery at DIFC to put together a program at the DIFC academy for education banks and institutions regarding standards .
* Saudis put together a fund to advance international eKYC standards


UK (Ralph/Chris)
--------------------
* 

Russia (Don/Dima)
--------------------
* Russia: Russian Federation: Open API standards https://openbankingrussia.ru/open-api-standards/
* Live ecosystem with FAPI 1.0 I-D2. 
* Some certification programme. 

Ukraina (Francis)
--------------------
* The Ukrainian centralbank is looking for support to educate and introduce open banking in the Ukraine. 
* Need speakers for the opennbanking conference taking palce in september 2021.

GOFTS WG (Nat)
--------------------
* Had the 3rd Meeting. 
* FAPI 2.0 Attacker Model mentioned. A potential expansion of the scope was pointed out, e.g., risk metrics regarding the spoofed IP Address. 

Grant Management (Dima)
==========================
* Issue #412 - FAPI 2.0 - (Hard requirement to support Grant Management Requirement) is created.

PRs (Dave/Nat)
=================
Pull Request #282 & Pull Request #283  - Lots of editorial fixes for Grant Management 

GM Authors to review and merge


Issues (Dave/Nat)
=====================

# 431 - FAPI 2.0 Baseline Attacker model not referenced.

* Editorial . Use Bitbucket URL

#430 - Add "Scope" clause to FAPI 2.0

* Assigned to Daniel

#429 - FAPI Certification with Lodged Intent or RAR - User Consent vs Technical Process Certification.

* Chris to provide comment 
* Will leave issue open

#412 - FAPI 2.0 - Hard requirement to support Grant Management Requirement

* Dave to email list for feedback


AOB (Dave/Nat)
=================
None

The call adjourned at 15:03 UTC