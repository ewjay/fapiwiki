============================================
FAPI WG Meeting Notes (2018-08-01) 
============================================
Date & Time: 2018-08-01 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:04 UTC. 

Roll Call
===========
* Attending: Nat, Herik, Joseph, Ralph, Robert, Torsten, John
* Guests: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Add issue #155: Support authorization and identity federation use cases for the same client_id  

SG Data Schema (Nat/Anoop)
===============================
We are starting new Sub-group, SG Data Schema. Anoop will lead it. 
In the last week's call, Anoop explained possible approaches, e.g., taking DDA and combining it with UK Open Banking etc. Regional differences need to be evaluated.

It was also pointed out that investment trading part is pretty thin in both DDA and UK Open Banking. Considering retirement investment forms a good part of a person's portfolio, unable to deal with it effectively from Personal Finance Management software or Intelligent Finacial Agent is suboptimal that we need to cover them.

In the Open Banking seminar in Tokyo last week, Nat was approached by several banks that they are interested in working on the schema so there probably is a sizable potential participants slate in Tokyo as well. Starting with NY/London/Tokyo slate for the internationalization probably is a good start.

Implementer's Draft (Nat)
===========================
* Need to apply required change in the text to follow up the security report. 
* [ASK] Should we start the Implementer's draft public review period then? 
* Having said that ... there are 12 remaining issues on the Part 2. 
    * https://bitbucket.org/openid/fapi/issues?status=new&status=open&component=Part%202%3A%20RW%20Security
    * [ASK] Do we want to make changes to adopt them to this round or do them after? 

Issues (Nat)
=================
3 New issues were filed.  #152, #153, #154, #155

#152: request objects should have iat and exp (Joseph)
---------------------------------------------------------
* #152 

Callers felt that `exp` should be enforced and `iat` should be allowed. 
The reason for having these are not for preventing replay attack but 
to make the enforcement of nonce etc. easier. After `exp` date, 
the server can take the request objects offline though the server 
may need to keep them as evidence for legally required amount of time. 

Torsten is to create the pull request. 

#153: Add level of assurance to scope (Tom)
----------------------------------------------
* #153

It resulted in a lengthy discussion. Torsten provided his idea on what is 
required for KYC. Just having a single value `acr` is too simplistic. 
Vector of trust, while good fothe r authentication phase, would not for KYC phase either. 

There seem to be parallel works happening elsewhere. At least three were identified. 

This is an important topic that warrant the cordination among those bodies and take time, 
so it was proposed to continue working beyond the 2nd implementer's draft.  


#154: Behaviour of AS undefined if no acr claim supplied by client (Joseph)
-----------------------------------------------------------------------------
* #154

We still need more investigation on this one, but the call on Aug. 2 pointed out several things:

The client, where it was exempted, should be able to ask for a lower level authentication, e.g., single-factor authentication to improve the U/X. This kind of use-case is not covered by 5.5.1.1 of OIDC Core.
Even if the client asked for LoA 3 or something, it is at the Bank's discretion to perform a lower LoA authentication as the responsibility falls onto Banks anyways. (This is in contrast to many existing identity federations.)

Ad Hoc Call
==================
At this point, the scheduled meeting closure time has come. 
Nat proposed to do a doodle poll for the next week to schedule an extra Atlantic call next week. 
The doodle will close COB Friday EDT, and Nat will announce the date according to it. 

As the next topic is Torsten's ticket, his ability to be present will take precedence (beside at least one of the chairs.) 

Thus All the following are to be dealt with in the ad-hoc call

#155: Support authorization and identity federation use cases for the same client_id (Torsten)
---------------------------------------------------------------------------------------------------
* #155

Discussion from the list (Nat)
----------------------------------
A lengthy thread started from 
* http://lists.openid.net/pipermail/openid-specs-fapi/2018-July/000962.html

External Organizations
-------------------------- 

AOB
===========

Next Call
-----------------------
Next call in Atlantic time will be announced on Friday. 
Next Pacific call will go as scheduled. 

* The meeting was adjourned at 15:06 UTC.