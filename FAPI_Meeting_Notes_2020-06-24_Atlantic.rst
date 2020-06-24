============================================
FAPI WG Meeting Notes (2020-06-24) 
============================================
Date & Time: 2020-06-24 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
* Attending: Nat, Don, Bjorn, Mark, Kosuke, Francis, Adam, Joseph, Dave, Dima, Chris, Ralph, Barry, Glyn
* Regrets: 

Adoption of Agenda (Nat)
===========================
* 

Events
===============
Identiverse 
----------------
* 

OIDF+FDX Workshop (Don)
-------------------------
* Still waiting for date. 

IMF Institute of International Finance (Don)
---------------------------------------------
* APAC time zone meeting is also being considered. 

EU FinTech lab on digital identities (Mark)
-----------------------------------------------
* 18th. Mark will be attending it. 

EC DGConnect (Mark)
------------------------------
* 29th 14:30 CET. Nat has a conflict. He will respond to the thread. 

OSW2020 (Daniel)
---------------------
* FDX is interested in presenting. 

SIOP Info Exchange (Nat)
--------------------------
SIOP Info Exchange meeting is to happen on the 25th of June at 2 PM UTC. Registration page TBD. 

External Organizations
========================

Australia (Stuart/Dima)
-------------------------
Going live next week. Limited rollout. 

UK (Chris)
------------------
* OBIE Steering Committee today. Hopefully, confirm the crisis implementation period ending in June. 
* CMA 9 to go through the Certification: FAPI, Functional, CX. 

OAuth JAR (Nat)
=======================
* PRs https://bitbucket.org/Nat/oauth-jwsreq/pull-requests/
* What should be done for the case the value is not `true`. 
* invalid_request
* default value is false. 


PRs for 1.0 (Dave)
====================
* 

Multiple issuers (Joseph)
=================================
Chased OBIE for their implementation status. 
Waiting for their answer. 
Francis commented on FAPI ML. 
Relevant ticket: https://bitbucket.org/openid/fapi/issues/255/certification-clarification-request


FAPI 2.0 (Daniel)
========================
PR https://bitbucket.org/openid/fapi/pull-requests/163/add-clarification-on-mix-up-mitigation/diff
is adding issuer to the authorization response to mitigate Mix-up attack. 

Brian pointed out that adding those parameters that are not in the core specification to a profile like this is problematic. Daniel and Brian agreed to start a mail thread in OAuth WG. 

AOB
==========================

The meeting was adjourned at 14:59 UTC.