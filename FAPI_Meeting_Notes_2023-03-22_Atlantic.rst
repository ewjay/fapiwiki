============================================
FAPI WG Agenda & Meeting Notes (2023-03-22) 
============================================
* Date & Time: 2023-03-22T14:00Z
* Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2023-03-15_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:02 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Dave, Nat, Chris, Takahiko, Michael, Mike L. Dima, Daniel, Justin, Kelly, Brian, Filip, Bjorn, Lukasz, Kosuke, Gail
* Regrets: Joseph
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Adopted as presented as draft agenda. 


Events (Mike L)
====================================================
OpenID Foundation Workshop (Mike)
---------------------------------------
* Registration page is now open. 
  * https://openid.net/2023/03/17/registration-workshop-at-microsoft/

Events are now in the Foundation Google Calendar (Mike)
------------------------------------------------------------
* In the new website, it is going to be a single source. 

Internal Liaisons
======================
NIST SP800-63-4ipd Comments
------------------------------
* Mark is leading the discussion. Several meetings. 
* Deadlines were postponed to April 14. 
* Nat has provided a few comments pointing to FAPI as a good practice for security - security is typically not composable and has to take the protocol as a whole with an appropriate security model and analysis to go with. 
* Link to the comment sheet that OIDF is compiling: 
  * https://docs.google.com/spreadsheets/d/1JHDypzbKg8x2AMfC_z4pzDBk4waVJBp2/edit#gid=571622526

FAPI2 Conformance test is now available (Mike)
-------------------------------------------------
* https://openid.net/2023/03/21/fapi-2-conformance-tests-available/

External Orgs & Liaisons (Mike L.)
============================================
Saudi Arabia (Mike)
-----------------------
* KSA
  * OP Testing: https://openid.net/certification/fapi_op_testing/
  * RP Testing: https://openid.net/certification/fapi_rp_testing/

Draft Updates
====================
Message Signing (Dave)
--------------------------
* Dave has sent the fixed Implementer's draft documents to Mike J. 

Grant Management (Dima)
--------------------------
* Dima is applying the fix and is sending the draft out. 

PRs (Dave)
===============
* Apart from one PR that we are parking until HTTP signature is settled, there is no standing PR. 
* Request/Response binding fix is waiting for IETF result next week. 


Issues (Dave)
==================
Proposed new FAPI certification test: private_key_jwt client authentication assertion where aud contains multiple values (Filip)
------------------------------------------------------------------------------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/403/proposed-new-fapi-certification-test
* related to #501
* see https://bitbucket.org/openid/fapi/issues/403/proposed-new-fapi-certification-test as well. 
* Filip is going to record the result of the discussion in the ticket. 



AOB (Nat)
=============
* none

The call adjourned at 14:59