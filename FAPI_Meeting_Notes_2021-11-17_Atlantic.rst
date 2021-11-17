============================================
FAPI WG Meeting Notes (2021-11-17) 
============================================
* Date & Time: 2020-11-17 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlantic
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
* Adopted as is. 

Events (Dave/Nat)
======================

OIDF virtual workshop (Mike L.)
--------------------------------
* Thursday, December 9th at 9 AM PT. 
* Link with registration details: https://openid.net/2021/10/19/registration-open-for-openid-foundation-virtual-workshop-thursday-december-9-2021/

Workshop with Berlin Group (Dave)
-----------------------------------
* WS -1 : Monday Nov 15th 1pm-4pm (CET)

  * Presented each other
  * Potential roadmap
  * Embeded mode

* WS - 2: Wed Nov 24th (1pm to 4pm or 2pm to 5pm)
* WS - 3: Friday Dec 10th (2pm to 5pm)

Reading Materials will be sent by Dave - target Close of Business Day today. 

Share general summary of FAPI and then converging points with FAPI 2.0

BG redirect approach is not complete, would be ideal to replace with FAPI

GSMA (Gail/Bjorn)
---------------------
The second workshop is on Nov. 29 for deeper technical dive. 

OAuth Security Workshop (Daniel)
------------------------------------
OAuth Security Workshop 2021 is coming up https://barcamps.eu/osw2021/

External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
n/a

Brazil (Mike L.)
---------------------------
OP certification coming in. 
Slack channel for TPP/RP is becoming quite active. 
Membership discount is helping there. 

Chris asked if there is any plan for RP functional test -> No. 

Berlin Group (Francis)
--------------------------------
See Events. 

In addition, Francis is trying to find an editor from Berlin group to join FAPI WG. 


Canada (Mike)
------------------
Probably will be a month or two as new government has just been set up. 

FDX (Mike)
------------------
Blog post is coming up today or tomorrow. 

The Middle East and North Africa (Ali)
---------------------------------------


Russia (Dima/Mike)
--------------------

UK (Chris)
--------------------
CMA published an updated timetable for VRP. 
January to implement was delayed for six months. 


PRs (Dave)
=================
Introduce requirement for TLS, closes #446 (Stuart)
------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/293

Long discussion on how to recommend cypher suite etc. 
Both OIDC Core and TLS BCP is stale in this regard and there is even a proposal on https over QUIC which does not use TLS. 

Result: Use the following text -

The PAR endpoint URL MUST use the "https" scheme.

Merged. 

grant_id is given but grant_management_action is not specified (Dima)
------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/290

Introduce notational conventions. Closes #438 (Stuart)
------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/291

As it is envisioned to go to IETF eventually, we will use IETF style. 

Introduce additional examples and remove reference to incremental auth, progress towards #441 (Stuart)
--------------------------------------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/292



Issues (Dave/Nat)
=====================
What should the claims field hold?
----------------------------------------
* #450




AOB (Nat)
=================
none


The call adjourned at 15:00 UTC