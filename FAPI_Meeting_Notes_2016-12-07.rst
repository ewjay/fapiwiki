============================================
FAPI WG Meeting Notes (2016-12-07)
============================================
Date & Time: 2016-12-07 15:00 UTC 
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 00:00+1 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:05 UTC. 

Roll Call
=============
* Present: Nat, Sascha, Anton
* Regrets: Henrik, Dave
* Guest: none. 

Adoption of the Agenda (Nat)
===============================
* Adopted as is. 

Working Draft 02
===================

    * Financial_API_WD_001.md Financial API - Part 1: Read Only API Security Profile
    * Financial_API_WD_002.md Financial API - Part 2: Read and Write API Security Profile
    * Financial_API_WD_003.md Financial API - Part 3: Open Data API
    * Financial_API_WD_004.md Financial API - Part 4: Protected Data API and Schema - Read only
    * Financial_API_WD_005.md Financial API - Part 5: Protected Data API and Schema - Read and Write

Last call on Part 1: Read Only API Security Profile (Nat)
------------------------------------------------------------
* `Part 1: Read Only API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md 
* Nat has been working on the comments received. 

Issues (Nat)
=========================

Additional issues (#44, #45, #46, #47, #48, #49) have been posted and the callers went over them. 

#44: Read Only profile only needs GET not POST? 
------------------------------------------------------
* #44
* Comment type: technical
* Callers agreed to require only GET. 

#45: Wording around resources and resource server 
------------------------------------------------------
* #45
* Comment type: editorial
* Callers agreed to accept the proposal. 

#46: x-fapi-InteractionId
---------------------------------------------------
* #46
* Comment type: technical
* Sascha also supported the idea to stick with "-" and not camel case. 
* Callers agreed to accept the proposal. 

#47: Confusing use of `client` and `server`
---------------------------------------------------
* #47
* Comment type: editorial
* Callers agreed that it can further clarify. 
* Sascha volunteered to come up with a better wording. 

#48: Definition or description around log entry
---------------------------------------------------
* #48
* Comment type: editorial
* Nat explained that we are using "logging" without explanation. 
  Perhaps having a new clause on logging would be a good idea. 
* Needs somebody to come up with the text. 
* Having said that, since it does not impact the implementation, 
  the nature of the change is editorial so we could potentially 
  postpone it until the Final draft. 

#49: x-fapi-FinancialId
---------------------------------------------------
* #49
* Comment type: technical
* It is at best confusing. the value of `x-fapi-FianncialId` identifies the issuer 
  but it might not be a URI and thus different from the value of `iss`. 
* It is used as routing number at service bureau. The advantage of having it 
  is that it does not have to parse the payload. 
* There are some downside as well: 
    * Duplication of information; 
    * Risk of the consumer of the payload not checking the `iss` value but using the header value, 
      which is not protected. 
* The callers agreed to consult with Anoop and Brian about the needs for it. 

#32: How to communicate back the partial errors to the client (Sascha)
-----------------------------------------------------------------------
* #32
* Sascha started working on it. 

#39: 2nd WD Part 1 6.2.1 -- Comments about DDA remains (Nat)
--------------------------------------------------------------
* #39
* Has been removed. 

#40: 2nd WD: Part 1: 6.2.1: Constraint on the InteractionId string unclear (Nat)
---------------------------------------------------------------------------------
* #40
* Mandates UUID now. 

Events
=============

API Days (Nat)
-------------------
* http://www.apidays.io/
* Dec 13 & 14 @ Paris. Nat got a ticket to Paris now. 
* Two talk sessions: 
    * one in CA session (workshop on the 13th?)
    * one in Banking API session (25 min. ) on the afternoon of the 14th. 
* The one on the 13th will elaborate on Sascha's presentation @ OIDF WS this October. 
* The one on the 14th will elaborate more on the security aspects of the OAuth/OpenID/JWS/JWT as previously submit in this list. 
    * Will talk about Part 1. 
    * Will talk about Part 2's direction. 
    * Any other ideas? 
* Nat will develop the slides probably on a corroborative editing platform so that WG members can assist him. 

CA World Report (Sascha)
---------------------------------
* Sascha talked to banking customers at CA World and they were very positive about FAPI work that they now consider joining the WG. 
* Sascha observed that 
    * customers providing Apps want to use the newest and greatest technology; and 
    * the industry's skepticism against OAuth is now disappearing and they are starting to see the potential. 

Digital Finance World 2017 (Nat)
-----------------------------------
* https://digitalfinance.world/
* KuppingerColes event. 
* Mainly on Blockchain and Distributed Ledger so not so sure... 
* WG members are asked to evaluate the needs for it. 

External Orgs
==================

Implementation Entity (Nat)
-------------------------------
* Dave will send in a written report. 

ISO/TC68 (Nat)
-----------------
* On hold now for other priorities. Will resume in the new year. 

Others
---------
* Nat will be talking to 

AOB
========
shall v.s MUST (Sascha/Nat)
------------------------------
* Sascha asked for the clarification on the strength of 'shall' v.s. 'must'. 
  He wanted to be clear that those 'shall' needs to be adheared to and is not optional. 
* Nat explained that the language is defined in ISO/IEC Directive Part 2 and 
  'shall' is a requirement -- it is not optional and it really is a formal way of saying 'must'. 

Next Call (Pacific)
--------------------------
* 2016-12-14 23:00 UTC
    (15:00 PDT, 23:00 UK, 00:00 Denmark, 08:00+1 JST)
* Regrets from Anton. 

