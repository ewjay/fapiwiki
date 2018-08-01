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
* Attending: 
* Guests: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Adopted as is. 

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
3 New issues were filed.  #152, #153, #154

#152: request objects should have iat and exp (Joseph)
---------------------------------------------------------

#153: Add level of assurance to scope (Tom)
----------------------------------------------

#154: Behaviour of AS undefined if no acr claim supplied by client (Joseph)
-----------------------------------------------------------------------------

Discussion from the list (Nat)
===============================
A lengthy thread started from 
* http://lists.openid.net/pipermail/openid-specs-fapi/2018-July/000962.html

External Organization
========================
OBIE (Ralph)
-------------

FS-ISAC (Nat/Anoop)
------------------
Not much is happening until the end of August or sometime in September. 

OFX (Nat/Anoop)
------------
There is now a bank who seeks using OAuth as an authorization method in combination with OFX, so there is going to be a spec around it. OFX has bill payment and stock trading capability so it is a read-write spec. 

Nat asked if they have considered FAPI. 

Anoop replied that it has not been introduced to them but it can be. 

Callers agreed that it would be a good idea to have a single OAuth profile rather than diverting. 

ISO/TC68/SC9 (Dave)
--------------------
Dave reported that ISO/TC68/SC9 is in the process of re-drafting their technical specification (TS) proposal. 
Dave feels that it would be a good idea for FAPI part to stay in OIDF for the time being - until they are ready to go with IS (International Standard), considering that there are still potential changes to FAPI and of the conformance suite. Dave will get back to the SC9 to discuss it. 

AOB
===========

Next Call
-----------------------
Next call will be an Atlantic Call. 

* The meeting was adjourned at 23:46 UTC.