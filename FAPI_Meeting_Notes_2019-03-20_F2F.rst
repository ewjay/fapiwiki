============================================
FAPI WG Meeting Notes (2019-03-20) 
============================================
Date & Time: 2019-03-20 09:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: Nat, Brian, TOny, Torsten, Hans, Vladimir, John, Tatsuo, Daniel Fett (yes), 
  * Sebastian Ebling (yes), Dave, Axel, 
  * Pedram Hosseyni (SEC / U Stuttgart)
  * 
* Guests: 
* Regrets:      
  *  

Adoption of the Agenda (Nat)
==================================
* Accepted as is. 

External Organizations
==========================

Berling Group (Dave)
------------------------
Formally communicated the problems. We have done everything that we could. 
They at least now know the problem and they are liable. 

STET(Torsten)
-------------------------


Open Banking (Dave)
-----------------------
Moving to full read-write FAPI profile. 

Problems with algorithm agility. 

HTTP Signing
----------------------

Payment (Tony)
------------------
EMVCo: trying to work on the authentication side. 3DS 2.0.

FDATA (Dave/Nat)
---------------------- 
 
EBA ()
------------------------

Australia (Ralph)
-----------------------------


UK OpenBanking (Joseph, Dave)
-----------------------------

Testing & Certification (Hans)
=====================================
On the way for GA on Apr. 1. 

Pricing has been available since Feb. 21 at https://openid.net/2019/02/21/openid-certification-program-expansion-and-fee-update/

Lodging Intent (Torsten)
============================


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