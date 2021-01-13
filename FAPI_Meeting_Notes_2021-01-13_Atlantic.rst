============================================
FAPI WG Meeting Notes (2021-01-13) 
============================================
* Date & Time: 2020-01-13 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: 
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* 

FAPI 1.0 Updates (Nat)
===================================
Final Title confirmation (Nat)
--------------------------------
* FAPI - Part 1: Baseline profile 1.0 OR FAPI 1.0 - Part 1: Baseline profile? 
* In the latter case, what would JARM, Grant Management etc. going to be? 


FAPI 2.0 Updates (Daniel)
===========================
x-fapi-* headers


Reports from Subgroups
==========================


Other Drafts
===============
Grant Management (Dima)
----------------------------
* Probably able to report next week. 


HTTP Signing (Dave)
----------------------
* DPoP style HTTP signing. 
* GNAP drafts have 6 signing mechanisms, and one of them is very similar. 


Events (Nat)
======================
OBIE (Chris)
-----------------
Parties endpoint / eKYC 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Extension to OIDC to enable eKYC data etc. that they can monetize. 
There is some momentum. 
Sandbox till the end of Feb. 

A few workshops. 

Variable payment workshops
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
To result in the final standard by the end of March. 

Podcast on Jan 26. (Torsten)
--------------------------------



External Organizations (Nat)
================================

Financial Data and Technology Association
-------------------------------------------------------
* Setting up a new organization called Global Open Finance Center of Excellence in early 2021.
* There is a proposal for OIDF to be a founding member.
* OIDF has 3 interest areas, one of which is participation and leadership of group of groups - group of representatives of various standards, organizations from around the world that would try and look for efficiencies and Interoperability across regional efforts.
* The effort is being led by Kevin Littlejohn through the Global Open Finance Center of Excellence, which is related to the University of Edinburgh.
* The organization has appears to have funding, and is hiring personnel to create a library of APIs in the open finance world
* They may also be a licensee of OIDF's listing of organizations that are in conformance to FAPI and OIDC..


Berlin Group (Francis)
----------------------
Please review the whitepaper: https://bitbucket.org/openid/fapi/issues/353/fapi-for-berlin-group-openfinance

* https://docs.google.com/document/d/1e5M5aLgNgiu4kkPIt3BjSHBt2mZL9DkcQ7bfL4Zqdgw/edit#heading=h.vppi3bf35d6g

Open Finance will be open to everybody. They are trying to change the governance model. 
It used to be financed by Deutche ... 
Now moving to open market model. 

UK
-----
See above. 

Issues
===========
#282: FAPI 2.0: x-fapi-* headers (Dave)
------------------------------------------
Dave asked if these are really needed as it would impact the Advanced profile signature. 

Francis pointed out that IP address etc. are needed by criminal investigators so they need to be there though their effectiveness as far as security is concerned is unknown. 

Ralph pointed out they need to be there but it does not have to be in the header. 
Also, he pointed out that it may not be accurate. 
However, they are needed. 






AOB
==========================


The meeting was adjourned at 15:00 UTC.