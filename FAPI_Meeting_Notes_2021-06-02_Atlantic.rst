============================================
FAPI WG Meeting Notes (2021-06-02) 
============================================
* Date & Time: 2020-06-02 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-04-07_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:06 UTC. 

Roll Call 
===========
* Attending: Nat, Dave, Chris Wood, Travis, Joseph, Renato, Takahiko, Taimoor Hazir (Millenium Partners), Filip, Don, Omer Khawaja, Daniel, Brian Torsten, Dima, Kosuke, Gail, Lukas, Francis, Brian. 
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* Adopted as is. 

Events (Nat)
======================
Open Identity Summit (Daniel)
--------------------------------
* 30 People attended
* Slides to be shared. 


External Organizations (Nat)
================================
Australia (Joseph)
----------------------
* Working with DSB. 
* ACCC Cyber Security Team got in touch. 

Brazil (Danillo) 
------------------------
* Little delaied with translation
* OK with Video. 
* Gail and Mike L, Joseph will help Daniello. 
* Directed funding received. Expecting 35 certifications in the first half of July. 
* Brazil test will be available on June 11. 
* It will be available in the master branch. 
* New features: encrypted request object. Not major diffs. 

Berlin Group (Francis)
---------------------------
* n/a

UK (Dave)
--------------------
* Quite sophisticated fraud going on for payment initiation. 
* 

US/FDX
-----------
* Paper work between OIDF and FDX is being finalized. 

Middle East (Gail)
-----------------------
* June 7 call
*  

Modrna Report (Dave/Bjorn)
=============================
* No additional comments in WG. 
* Getting ready for the public review for the FINAL. 

FAPI 2 Report (Dave)
=====================
* Implementers Draft Public Review started for Baseline and Security Model. 
* Quite a number of issues are coming in. 

PRs (Dave)
===================
Following PRs were discussed. 

* https://bitbucket.org/openid/fapi/pull-requests/269
* https://bitbucket.org/openid/fapi/pull-requests/270
* https://bitbucket.org/openid/fapi/pull-requests/268
* https://bitbucket.org/openid/fapi/pull-requests/267

They are to be merged. 

* https://bitbucket.org/openid/fapi/pull-requests/266

is to be continually discussed. 

Issues (Dave)
=================
416: RAR if scope *and* claims param not expressive enough (Travis)
------------------------------------------------------------------------
* #416

418: 303 should be used (Travis)
--------------------------------------
* #418

417: Shall require introspection of claims (Travis)
----------------------------------------------------------
* #417

415: Discovery Metadata for mtls (Ralph/Travis)
----------------------------------------------------------
* #415
* Callers pointed out that the support of alias would not help interoperability. The majority of FAPI implementation does not support MTLS alias endpoint.

To be discussed with Ralph.

413: FAPI2 Baseline: Sender-Constrained Authorization Code (Taka)
-----------------------------------------------------------------------
* #413
* Clarification of the language probably is needed. 
* Filip pointed out that it is used in the certification suite and removing it may not be appropriate. 


AOB
=======
* n/a

The call adjourned at 14:59 UTC