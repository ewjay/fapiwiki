============================================
FAPI WG Meeting Notes (2020-10-28) 
============================================
* Date & Time: 2020-10-28 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call 
===========
* Attending: 



* Regrets: Daniel
* Guest: 

Adoption of Agenda (Nat)
===========================

* Events
* External organizations
* PRs
* Issues

1.   Roll Call
2.   Adoption of Agenda (Nat)
3.   Events

4.   External Organizations
4.1.   Berlin Group (Francis)
4.2.   ETSI (Dave)
4.3.   Australia (Stuart)
4.4.   European Commission (Mark/Torsten)
4.5.   UK (Ralph)
5.   Drafts
5.1.   FAPI 2.0 (Daniel)
5.2.   HTTP Signing (Dave)
6.   PRs (Dave/Nat)
7.   Issues (Dave/Nat)
8.   AOB


Events 
======================

OBIE Webinar (Chris)
-----------------------
9:30 tomorrow on alternative registration. 

Launch Event for variable payment 
------------------------------------

 

External Organizations
========================
Berlin Group (Francis)
------------------------



ETSI (Dave)
---------------------




Australia (Stuart)
------------------------
Consent revocation proposal adds a lot of complexity. 
There is no standards to built upon. 

* https://github.com/ConsumerDataStandardsAustralia/standards-maintenance/issues/247


* Big 4 banks and recipients going into Phase 2 of consumer data sharing

  * Includes new products
  * Tweaks to information security profile
  * Joint accounts
  * Still finalizing consultation, looks very complex

    * No existing technical standards available to achieve goals

      * Intermediaries
      * Cascading consents (communicating consents via third parties)
  * OAC conformance testing

    * Joseph has CDR version of test on production and certification
  * Joseph still finalizing Australian response letter

      * Still don’t know where to send it
      * Might be better to do open letter and CC the chair


European Commission (Mark/Torsten)
------------------------------------
* 


UK (Ralph)
---------------------

* No updates

PRs (Dave/Nat)
=====================


* issue #330 - potentially misleading language WRT JWT ATs - language is confusing

    - Suggested removing "opaque"
    - Intent is tat AT is not to be consumed by clients
    - remove "opaque" and reword note, make it similiar to RFC 6749 language that AT is usually opaque to clients
    - No PR yet



* issue #317 

    - Reassigned to Dave








AOB
==========================


The meeting was adjourned at 15:00 UTC.