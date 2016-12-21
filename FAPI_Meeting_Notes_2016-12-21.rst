============================================
FAPI WG Meeting Notes (2016-12-21)
============================================
Date & Time: 2016-12-21 15:00 UTC 
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 00:00+1 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:05 UTC. 

Roll Call
=============
* Present: Dave, Sascha, Nat, Henrik, John
* Regrets: Anton (as it is the last day for him at DT) <-- Thanks from the WG. 
* Guest: 

Adoption of the Agenda (Nat)
===============================
* Adopted. 

Implementer's draft Part 1 (Nat)
==================================
* Public review has been started. 
* Details can be found at: http://openid.net/2016/12/19/public-review-period-for-financial-api-part-1-read-only-api-security-profile-started/

Working Draft 02
===================

    * Financial_API_WD_001.md Financial API - Part 1: Read Only API Security Profile
    * Financial_API_WD_002.md Financial API - Part 2: Read and Write API Security Profile
    * Financial_API_WD_003.md Financial API - Part 3: Open Data API
    * Financial_API_WD_004.md Financial API - Part 4: Protected Data API and Schema - Read only
    * Financial_API_WD_005.md Financial API - Part 5: Protected Data API and Schema - Read and Write

Part 2: Read & Write API Security Profile (Nat)
------------------------------------------------------------
* `Part 2: Read & Write API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md 

* There were long discussion around the various forms of attack esp. the session hijacking, lead by John. 
* Nat also pointed out that he outlined some of the security issues that needs to be addressed in his Paris presentation: http://www.slideshare.net/nat_sakimura/financial-grade-oauth-openid-connect
* Dave pointed out that UK Open Banking IE needs it at the latest by May so we need to execute quite quickly. 
* Nat volunteered to take the first crack at it so that WG members can start filing the issues and giving pull requests. 


Issues (Nat)
=========================
* Several new editorial issues have been filed for Part 1. Since they are all editorial, they can be applied before the vote. 

Events
=============

API Days Report (Nat)
-------------------
* http://www.apidays.io/
* Dec 13 & 14 @ Paris. Nat got a ticket to Paris now. 
* Slides for session 1: As distributed before. 
* Slides for session 2: http://www.slideshare.net/nat_sakimura/financial-grade-oauth-openid-connect
* Connected with Figo. 
* Connected with Open Bank Project
* The myth that OAuth 2.0 not suitable to Banking API cleared. 

Digital Finance World 2017 (Nat)
-----------------------------------
* https://digitalfinance.world/
* KuppingerColes event. 
* Mainly on Blockchain and Distributed Ledger so not so sure... 
* WG members are asked to evaluate the needs for it. 

External Orgs
==================

Implementation Entity (Dave)
-------------------------------
* Dave sent the current status report in http://lists.openid.net/pipermail/openid-specs-fapi/2016-December/000212.html
* IE is still dealing with governance process and still closed. 
* For open data schema, they are using ISO 20022 dictionary and converting it into JSON. 
* HSBC (one of the 9 banks involved with the IE) has launched their beta
   API for open data: https://developer.hsbc.com/swagger-index.html
* It may help connecting with Berkeley, who is very much involved in OIX, our sister organization. 

ISO/TC68 (Nat)
-----------------
* On hold now for other priorities. Will resume in the new year. 

X9 (Nat)
--------------
* For now, Nat is put as the liaison officer for X9, but he would like Paul to take over. 


AOB
========

Next Call (Pacific)
--------------------------
* 2016-12-27 23:00 UTC 
    (15:00 PDT, 23:00 UK, 00:00 Denmark, 08:00+1 JST)
** PLEASE NOTE THE NEW TIME: It is one hour earlier. 

Cancelling Jan. 4 Call (Atlantic)
----------------------------------
* Due to Japanese new years holiday. 


