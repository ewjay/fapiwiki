============================================
FAPI WG Meeting Notes (2022-05-18) 
============================================
* Date & Time: 2022-05-18T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-05-18_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

  * Daniel Fett
  * Dave Tonge
  * Dima Postnikov
  * Don Thibeau
  * Filip Skokan
  * Gail hodges
  * Joseph Heenan
  * Lukasz Jaromin
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Rifaat Shekh-Yusef
  * Takahiko Kawasaki
  * Torsten Lodderstedt
  * Brian Campbell
  * Dima Postnikov
  * Michael Palage
  * David Januchowski

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================


Events (Nat)
======================
EIC
---
Presentations will be available on OIDC website today




Identiverse
-----------
Denver, Colorado | June 21-24, 2022

Joseph, Torsten will have presentations

OIDF has a meeting room for the duration of Identiverse and will be available for use

Contact Mike to schedule

FAPI WG may schedule a F2F meeting, possibly during the Pacific time call



Internal Liaison (Nat)
================================
Certification (Joseph/Mike)
----------------------------
Will look at expanding the certification model

Brazil certified on staging systems last year, but didn’t work out well

Goal is to enable to certify on production systems but keys are restricted

Certification suite needs to stop publishing key information in logs

Need to be in situation where OIDF isn’t holding private keys

Test logs also contain PII information, due to request objects containing real user information

Brazil production systems don’t allow test users


Will have a Brazil hosted server where keys are stored in HSM where any banks can use to test their system

Will change the certification policy so that full detail logs won’t be needed. More terse logs stripped of HTTP 
traffic, keys, signed objects, and PII will be used.

Will present a proposal to Brazil next week.

Will help certification situation with Saudi which doesn’t want self-certification

Will allow contracted third-parties to run certification servers 

Feedback on new model should be sent to Joseph

UAE has requested a similar certification model.. Ali will try to involve the UAE in discussion.

Now is the time for the WG and organizations to bring forward proposals from the marketplace so that the board and 
EC can make informed decisions about the path forward.


External Organizations (Nat)
===================================

University of Stuttgart
-----------------------
Signed contract is in place between OIDF and the University to start FAPI 2 Security Analysis 


Australia (Mike L.)
------------------------------------

Brazil (Mike L.)
---------------------------
Brazil will publish FAPI CIBA spec next month

Will contain updates to login_hint



Berlin Group (Daniel)
--------------------------------
Will have a call next Tuesday, May 24

Will discuss PAR, OIDC, and embedded 

EU DIW ARF (Gail)
------------------
* n/a

FDX (Rifaat)
------------------

GAIN (Dima)
---------------------
* 

IETF OAuth WG (Rifaat)
-------------------------

ISO/TC68 (Nat/Dave)
----------------------
* n/a

The Middle East and North Africa (Chris)
-----------------------------------------
* n/a

Mexico (Gail)
------------------
* n/a

Nigeria (Mike)
---------------

OECD (Nat)
-------------
* n/a


UK (Chris)
--------------------
* n/a


USA (Gail)
----------------
* n/a 


Specs (Dave)
================
Grant Management (Dima)
----------------------------------------
A few PRs are needed

FAPI CIBA
----------
Discussed a refactoring of FAPI CIBA at OSW so it will work with FAPI 2


FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* N/A 

Advanced authorization (Dima)
----------------------------------

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
* Closing down remaining issues

* Would like to agreement on the naming of Advanced profile

  * Joseph received feedback that the Financial in FAPI automatically causes notions of banks despite being a general purpose high security profile

    * Related issue #479 - Change to the naming of FAPI


  * Replacing “Financial” with something else will enable wider adoption
  * Replacement suggestions : Fortified, Open Data

    * Ideally would like to retain FAPI acronym

  * Changing names at this point will add to confusion

    * Alternative is to create different profile for different industries and point to FAPI 

  * FAPI is already an established acronym
  * Consensus is to use FAPI but not define what FAPI stands for.
  * Rebranding will waste all the good will established so far
  * Focus on education of what it was and what it is now and different builds for different sectors
  * Reword introduction to remove emphasis on financial
  * Use FAPI logo with high security API tag line
  * FAPI microsite has heavy focus on banking at the moment - https://fapi.openid.net/

    * Make it clear that Open Banking is only one of the use case and not the primary use case
    * Site should focus on examples where FAPI is used (telco, energy, health)

  * Another naming issue related to the naming of Baseline and Advanced 


JARM (Dave)
----------------------------------------
Dave will get new drafts ready for public review


PRs (Dave)
=================



Issues (Dave)
=====================

#499 - Re structure FAPI2 baseline
----------------------------------
#499 - Re structure FAPI2 baseline

Restructure Baseline to link in other specs.

Separate authorization code flow from general requirements

Dima will double check


The Advanced Authorization profile spec talks about Grant Management and RAR

There is a proposal to drop Advanced Authorization profile spec because it mainly states to use Grant Management and RAR.

This can be achieved using non-normative text in Baseline

Dave will create PR

FAPI 2 Advanced is mainly about Message Signing for non-repudiation

Advanced is not a more secure profile but rather to help ecosystems achieve non-repudiation goals

Should Advanced be changed to FAPI 2 Message Signing or something similar?

Is Baseline actually needed if Advanced is renamed?

Baseline and Advanced are separated to make simplify  implementation and increase interoperability

FAPI 2 Message Signing may be too long?

* Will change :

  * Baseline => FAPI 2 Security Profile
  * Advanced => FAPI 2 Message Signing


What does it mean to be certified? We need to be clear about the profiles, specs, and technical framework. Dima 
will come up with a suggestion.

Grant management is about grant lifecycle management


#496 - clock sync and FAPI2 baseline
------------------------------------
#496 - clock sync and FAPI2 baseline

DPoP nonce is supported to get around clock sync issues

Are other parts of spec affected by clock sync issues like private key JWT

FAPI 2 targets confidential clients but does not preclude dynamically registered confidential clients or public clients that have its own keys

FAPI 2 can be used with a client on a user controlled device

WG asked for comments and feedback on this issue


AOB (Nat)
=================
* none



The call adjourned at 15:59 UTC