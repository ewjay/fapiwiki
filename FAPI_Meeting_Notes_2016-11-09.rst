============================================
FAPI WG Meeting Notes (2016-11-09)
============================================
Date & Time: 2016-11-09 14:00 UTC
(06:00 PDT, 14:00 UK, 15:00 Denmark, 23:00 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: Anton, Nat, Bjorn, Dave, John
* Regrets: Sascha, Henrik

Adoption of the Agenda (Nat)
===============================
* Adopted. 

Approval of the minutes
=========================
* [[FAPI_Meeting_Notes_2016-10-18]] Approved. 

External Org Relationships 
=============================
API Days (Nat)
-------------------
* http://www.apidays.io/
* There are two tracks that are of interest to us. 
    * The STATE OF API SECURITY : OAUTH, JSON WEB TOKENS, OPEN ID Connect, UMA; 
    * BANKING APIS and PSD2 (Payment Service Delivery)
* If we want to do both, we have to have two persons. 
    * We should find out who is going to be doing OAuth, JWT, OpenID Connect and UMA. 
    * Should contact Sascha to see if he knows the CA guy. 
* The organizers: Fabnoble and OAuth.io: We should try to access them in any case. 

* Copy DOn. 

UK Implementation Entity (Dave)
-------------------------------
* Dave has joined the Data work stream. Their scope is very wide. They are currently a closed group but Dave will give the FAPI WG information as soon as it becomes available. 
* Dave also is requesting to join the security WG. He expects to join them either directly through their invitation or through FDATA. It would be really good if we can coordinate our draft with them. 

Figo (Anton)
----------------
* Anton contacted them by email and presented WG. They are interested in our work to see how we can align. 
* Anton has provided answers to their question and waiting for the feedback. 

Apigee (Nat)
-------------
* Dave made an introduction to Nat over email and they have contacted us back. 
* They are willing to work with us. The contact person, Saravanakumar Rajagopal, will introduce their chief architect, Greg Brail, to us shortly. 

EBA (Dave)
-------------
* EBA comments were published at: https://www.eba.europa.eu/regulation-and-policy/payment-services-and-electronic-money/regulatory-technical-standards-on-strong-customer-authentication-and-secure-communication-under-psd2
* Dave got a comment on it that s/he was pleased see our comment. 

Working Draft 02
===================

Restructuring (Nat)
----------------------------
* Restructured document is available at: the repo as
    * Financial_API_WD_001.md Financial API - Part 1: Read Only API Security Profile
    * Financial_API_WD_002.md Financial API - Part 2: Read and Write API Security Profile
    * Financial_API_WD_003.md Financial API - Part 3: Open Data API
    * Financial_API_WD_004.md Financial API - Part 4: Protected Data API and Schema - Read only
    * Financial_API_WD_005.md Financial API - Part 5: Protected Data API and Schema - Read and Write

* Part 1 is the most complete one and we need the close review by the WG. 
* Once that is ready, then we can move the Part 1 towards the Implementors draft vote. 
* For implementor's vote, we need to have 45 days review period, which can be concurrent with 
  the announcement of the vote. 
* NOTE: For the final vote, we need two or more interoperable implementations to support the spec. 

Dave asked about the appearance of "DDA" as it may be confusing. 
Since Anoop agreed to remove those references, we are going to remove it per #34. 

Issues 
=========================

* No new issues. 

Events
=============

Pre-IETF (Nat/John)
--------------------
* Karen will give us answer on the room allocation today but it is probably too late for organizing a workshop. 
* We could still have a meeting there though. 

AOB
========

Change of Atlantic Call timing 
-------------------------------
* The WG decided to move the call time one hour later (from UTC perspective) to match the end of the end of the daylight saving time in Europe and the US. 
   * Next Atlantic call will be 2016-11-23 15:00 UTC. 

Next Call (Pacific)
--------------------------
* 2016-11-16 23:00 UTC
    (16:00 PDT, 23:00 UK, 01:00+1 Denmark, 09:00+1 JST)

