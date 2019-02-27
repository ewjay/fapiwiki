============================================
FAPI WG Meeting Notes (2019-02-13) 
============================================
Date & Time: 2019-02-13 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: 
  * 
* Guests: 
* Regrets:      
  *  

Adoption of the Agenda (Nat)
==================================
* Accepted as is. 

External Organizations
==========================

ECB (Chris/Ralph/Dave)
------------------------


STET, Berlin Group & Session Fixation in Payment Flows (Torsten)
-----------------------------------------------------------------
 

Australia (Ralph)
-----------------------------


UK OpenBanking (Joseph, Dave)
-----------------------------

ISO/TC68 (Dave)
-----------------------------

IETF:OAuth JAR (John)
-----------------------
* OAuth JAR Status

Draft Status (Nat/Dave)
===========================
CIBA FAPI Profile (Dave)
---------------------------


TR Cross-Browser Payment Initiation Attack (Daniel/Torsten)
-------------------------------------------------------------
* TR-Cross_browser_payment_initiation_attack.md
* Need to re-order chapters. 

TR Lodging Intent Pattern (Torsten)
-------------------------------------------
* Financial_API_Lodging_Intent.md

Events
=========
RSA
------------

OAuth Security Workshop
-----------------------------

IETF
-------------

Issues
==========================

#216: TLS_ECDHE_ECDSA cipher suites
------------------------------------
* https://bitbucket.org/openid/fapi/issues/216/tls_ecdhe_ecdsa-cipher-suites

Need to dig in why BCP195 is recommending only these four cipher suites. 

#215: Financial_API_Lodging_Intent should be an informational document
---------------------------------------------------------------------------
* #215
* Torsten seems to be wanting it to be a standard. Since we are lacking both Torsten and Dave from this call, the discussion was postponed to the next call. 

#214: restricting 'aud' in request object to a single value (Joseph)
--------------------------------------------------------------------------
* #214
* This has come up when writing a test suit. 
* Although Joseph argues that there is no case where multiple `aud` is justifiably useful, there may actually be in the Open Banking so we need to at least check the current configuration and assess the impact of the change. 


AOB
==========================

Next Call
-------------------------
* Pacific call next week. Nat will not be able to join. 
* Atlantic call in 2 weeks time.

The meeting was adjourned at 14:45 UTC.