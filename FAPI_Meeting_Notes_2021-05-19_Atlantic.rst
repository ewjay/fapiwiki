============================================
FAPI WG Meeting Notes (2021-05-19) 
============================================
* Date & Time: 2020-05-19 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-04-07_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Dave, Bjorn, Don, Kosuke, Joseph, Takahiko, Daniel, Lukasz, Torsten, Brian, Dima, Craig Borysowich, Ralph
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
Adopted as is. 

Events (Nat)
======================
OpenID Workshop @ Brazil (Don)
--------------------------------
Ralph was the catalyst for OpenID Foundation workshop in Brazil. 
It was attended by hundreds of attendees, indicative of needs for tech info. 

Ralph also negotiated directed funding to the foundation to build 
conformance suite for Brazil. 

This is the first of the three workshop. 

Similar efforts in the Middle East. Authlete is arranging it there. 

These should help with expanding the diversity. 




External Organizations (Nat)
================================
Australia (Dima)
----------------------
* Number of consultation going on. 

Brazil (Dave/Danillo) 
------------------------
* Daniello Branco from Open Banking. 

Berlin Group (Francis)
---------------------------
* A couple of consultation (mostly business) 

UK (Dave)
--------------------
* Different RPs trying status check at different OPs (Banks) creating fake lodging intent. 
* Banks are asking for some headers to signal that it is an automated check. 
* Australia has not found the same yet but it could. 
* Dave will create an issue in the tracker. 

US/FDX
-----------
* Lukasz reported on FDX and Grant Management: 
* Initial scope was narrowed to consent authorization and grant removal. 
* This is a good direction and now it sounds like it can adopt OIDF Grant Management. 
* Torsten -- 
* Vote for RFC closes this week for the adoption of FAPI and the certification. Positive development. 

Modrna Report (Dave/Bjorn)
=============================
A good discussion resulted in PRs. 
By next week, all the remaining issues should be finalized. 
After that, they will do the final review and go for the last call for the WG. 

Joseph suggested starting WG last call sooner. 

Bjorn agreed. Perhaps it can start at the next call on the next Tuesday. 

Takahiko asked its relationship with the FAPI CIBA profile. 

Dave replied that most changes are on the push mode, which is not used by FAPI CIBA. 

Feature extensions are more explicit and may break not really behaving clients. 

Certification (Joseph)
========================
Joseph reported that 

* FAPI final test is progressing. 
* Discussion with Brazil is also continuing for Brazil profile. 

Daniello asked about ... 

Joseph replied that he is talking with miro. 

Daniello offered some help wrt it. 


Docker Run (Dave)
=====================
* Stuart volunteered to fix the problem with ipr=none. 


PRs (Dave)
===================
267: Add more details to grant lifecycle (Dima)
--------------------------------------------------


266: Introduce replace action (Stuart)
--------------------------------------------------


Issues (Dave)
=================
Issue #411: HTTP Signing (Dave)
-------------------------------------
* #411
* Dave explained the advantage of referring the HTTP signing as it is a standard track document. 
* https://codimd.ietf.org/s/notes-ietf-interim-2021-oauth-10-oauth has the recording of the recent OAuth meeting on the subject

Other Issues
----------------

AOB
=======
*

The call adjourned at 15:00 UTC