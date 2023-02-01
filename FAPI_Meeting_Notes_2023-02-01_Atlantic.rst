===========================================
FAPI WG Agenda & Meeting Notes (2023-02-01) 
===========================================
* Date & Time: 2023-02-01T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-11-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 
* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================

Events (Mike L.)
====================================================
* 2023 OIDF Calendar. OIDF Calendar: https://openid.net/foundation/calendar-of-events/ has been updated. 
* Currently coordinating OIDF Workshops April 17 Mountain View Microsoft. 
* OIDF WS Tues May 9. Any special topics to be sent to Mike L. 

* FIDO Event next week in Taipei. 
* 

EIC Submission due Feb. 8
-----------------------------
* Need to submit one from FAPI. Joseph+Daniel probably do one. 

FIDO Taipei
------------------------------
* Feb 6 - 9
* Kosuke and Nat are going. 


Internal Liaisons
======================
Modrna WG (Nat/Joseph)
---------------------------


External Orgs & Liaisons (Mike L./Chris)
============================================
Brazil
--------------
* Recertification with Open Finance Brazil
* Certification for Insurance. 

Saudi Arabia
---------------
* Quite an active testing on KSA profile. 
* Domingos creating RP tests. 
* Another FAPI WS on next Wednesday. 
* Chris asked about the optionality on the KSA profile. Private Key JWT and MTLS? Are they mandated to both? 
* It is up to AS to choose. 
* This would cause problems. 

PRs (Dave)
===============
404 add intro and rework initial section for message signing
------------------------------------------------------------------
* Approved

Issues (Nat)
==================

Tracking: Implementers of FAPI 1.0 and FAPI 2.0
----------------------------------------------------------
* #555
* A few new implementations have been added. 

Deprecation & removal of FAPI 1 Implementer's Draft conformance certification tests/programme
--------------------------------------------------------------------------------------------------
* #570
* OBIE probably would not have problems with it. Note OB is going through change. 
    * https://www.openbanking.org.uk/news/the-obie-marks-completion-of-cma-open-banking-roadmap-on-fifth-anniversary/

Other issues
----------------
* Privacy consideration etc. is holding back the progress of the draft. 
* Nat apologized that he is going to work on it next week so that we can deal with it next week. 

AOB (Nat)
=============
n/a

The call adjourned at 14:40

Chat Transcripts
========================

.. sourcecode:: text

    Dave Tonge (Moneyhub) to Everyone	11:05 PM	1.   Roll Call (Dave/Nat)
2.   Adoption of Agenda (Dave/Nat)
3.   Second Implementer’s Drafts of Two FAPI 2.0 Specifications
4.   CFPB section 1033 Personal Financial Data Rights questions
5.   Events (Mike L.)
6.   Internal Liaisons 
7.   External Orgs & Liaisons (Mike L./Chris)
8.   Drafts Updates (Nat)
9.   PRs (Dave)
10.   Issues (Dave)
11.   AOB (Nat)

Me to Everyone	11:07 PM	FAPI Objectives for this year 
Me to Everyone	11:08 PM	https://openid.net/2023/01/08/notice-of-vote-for-proposed-second-implementers-drafts-of-two-fapi-2-0-specifications/
Taka (Authlete) to Everyone	11:11 PM	https://bitbucket.org/openid/fapi/pull-requests/402
Me to Everyone	11:12 PM	* Source: https://files.consumerfinance.gov/f/documents/cfpb_data-rights-rulemaking-1033-SBREFA_outline_2022-10.pdf 
* https://files.consumerfinance.gov/f/documents/cfpb_data-rights-rulemaking-1033-SBREFA-high-level-summary-discussion-guide_2022-10.pdf
* Draft response: https://docs.google.com/document/d/1mjmqPzfRI1l0ki9qnyaSz2YwAkH54gfG8A4lJtzA0WI/edit

Kosuke Koiwai to Everyone	11:15 PM	Im coming!
Dave Tonge (Moneyhub) to Everyone	11:18 PM	
E.g. FAPI Baseline moving to FINAL
FAPI Message signing moving to FINAL
Security Analysis of Work Package 2: FAPI Message Signing, CIBA, Dynamic Client Registration completed – (Marcus Almgren to project manage, Australia funded)
Security Analysis of Work Package 3: Grant management, Security Event Token, and other related OIDF specs: (SSF, CAEP, OIDC for IA) - (Marcus Almgren to project manage, co-funding requested from WG members
Support Public/Private Requests for Comment on formation of Open Banking/ Open Data ecosystem – CFPB, Canada, Saudi, etc. (new tech lead)
Global advocacy / support in existing and new markets, particularly expansion in Latam, Africa, Asia (new tech lead)
Publication of “Open Banking, Open Data: Ready to Cross Borders” whitepaper.  (January, Dima)
Potential Formation of Community Group adjacent to FAPI for advocacy of latest whitepaper, and evaluation of governance options for ongoing support. (Dima, Gail, others TBC 1H 2023)
Dave Tonge (Moneyhub) to Everyone	11:21 PM	grant management to final
Dave Tonge (Moneyhub) to Everyone	11:21 PM	implementation and deployment advice document
Dave Tonge (Moneyhub) to Everyone	11:22 PM	tests for fapi2 security and message signing to be completed
Dave Tonge (Moneyhub) to Everyone	11:23 PM	conformance tests for grant management
Dave Tonge (Moneyhub) to Everyone	11:23 PM	Align CIBA to FAPI2
Dave Tonge (Moneyhub) to Everyone	11:26 PM	https://bitbucket.org/openid/fapi/pull-requests/402
Dave Tonge (Moneyhub) to Everyone	11:28 PM	https://bitbucket.org/openid/fapi/issues/555/tracking-implementers-of-fapi-10-and-fapi
Dave Tonge (Moneyhub) to Everyone	11:28 PM	https://bitbucket.org/openid/fapi/issues/570/deprecation-removal-of-fapi-1-implementers
Dave Tonge (Moneyhub) to Everyone	11:37 PM	https://www.openbanking.org.uk/news/the-obie-marks-completion-of-cma-open-banking-roadmap-on-fifth-anniversary/
Me to Everyone	11:38 PM	Sorry, I will get to the ticket next week. 
Joseph Heenan (OIDF/Authlete) to Everyone	11:39 PM	Thanks Nat.