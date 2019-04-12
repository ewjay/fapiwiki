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
They came back saying that it only affects if the attacker takes control of the user's computer and we replied back that it does not. 

They at least now know the problem and they are liable. 

Sending to some of the big banks in the Berlin Group seems to be a sensible way forward. 


STET(Torsten)
-------------------------
STET appreciated our contribution and decided to use OAuth with best practice instead of the generic solution in the white paper. 

Open Banking (Dave)
-----------------------
Moving to full read-write FAPI profile. 

Problems with algorithm agility: from RS256 to PS256. 
When registering a client, the algorithm value is a single value so the migration does not go smoothly. 
FAPI brought this problem of OIDC not having a sensible algorithm migration forward by recommending a newer algorithm. Even if the client could register a new value for the supported algorithm, the transition has to be coordinated. If the parameter supported multiple values like in the case of JWKS, then the transition would be smooth.  We have documented key rotation but we have not for the algorithm. RS256 to PS256 migration is a special case since it can use the same key. In other cases, keys need to be rotated as well. This really is a generic OAuth problem and needs to be considered in that frame rather than creating a point solution. If doing it in OAuth is difficult as it is expected to be, then it should be dealt with OIDC. 

There is a related problem of a client not having a way to signal if the request from the client needs to be signed. 


HTTP Signing (Tony) 
----------------------
HTTP signing is way under-specified. There are many drafts floating around. 
FAPI specification must provide a more concrete guidance, at least documented pros and cons. 

Justin's draft and others are a bit different in the sense. 

* [ACT] Tony will open an issue. 
* [ACT] Dave will create an initial draft. 

Payment (Tony)
------------------
EMVCo: trying to work on the authentication side. 3DS 2.0.

Most of 3DS is over a redirect flow, but there is a "frictionless flow" where no authentication is done. 

FDX (Nat/Hans)
--------------------
OIDF and FDX will be issuing the announcement on the liaison relationship pretty soon. 

FDX sees a similar approach to FAPI. 

FDATA (Dave/Nat)
---------------------- 
FDATA is a regulatory trade body. Gavin was saying that he can promote FAPI to Brazil, India, Australia etc. 
They are talking with Japanese fintech association. They are making a coordinated effort so it is good. 

EBA (Dave)
------------------------
Chris is in the API evaluation group. 

UK OpenBanking (Joseph, Dave)
-----------------------------
UK Open Banking is transitioning tests to OIDF provided test suite except for the OB-specific features. 

There is a need for App to app communication, where one App is acting as authentication and consent page to improve the user experience. Typically, the authorization endpoint is served by a `Universal Link <https://developer.apple.com/ios/universal-links/>`_. 

However, App to app communication seems to have payload length limit and many problems arising when an app tries to use banking app to get authorization. One of the implementations had to reduce the request just to nonce and scope. Even just trying to send JWT gets trouble. 

Testing & Certification (Hans)
=====================================
On the way for GA on Apr. 1. 

Pricing has been available since Feb. 21 at https://openid.net/2019/02/21/openid-certification-program-expansion-and-fee-update/

Tony asked if there is a testing site ("refernece banks") that he can use during development. 
Dave will send a list of them to Tony. 

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