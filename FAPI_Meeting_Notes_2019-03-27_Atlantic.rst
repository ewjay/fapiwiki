============================================
FAPI WG Meeting Notes (2019-03-27) 
============================================
Date & Time: 2019-03-27 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending:　
  * Bjorn,  Dave, Joseph, Torsten

* Guests: 
* Regrets:      

Adoption of the Agenda (Dave)
==================================
* Agenda was agreed


Update from Face to Face at OSW & External Organisations
========================================================
 - Discussion around external organisations 

HTTP Signing & JSON Canonicalisation
=====================================

 - Anders, Daniel, Tony, Torsten discussed at a side meeting at IETF
 - https://tools.ietf.org/html/draft-rundgren-json-canonicalization-scheme-05
 - https://tools.ietf.org/html/draft-rundgren-signed-http-requests-00
 - Discuss whether FAPI could be a home for this spec 

Sender Constraining
===================

 - Daniel, John and Torsten writing a draft for sender-constraining in a token bound like way but without token binding.
 - Using application level signatures
 - New header that carries a JWT that contains the target url, the method, 

FDX - FAPI Update
=================
 - Dave explained about the schema and the history from durable data API

FAPI Conformance Test Suite
===========================

 - Not looked at JARM yet
 - Joseph asked about implementation - (Connect2Id & OpenID Provider)
 - Action to raise ticket about whether JARM is well integrated with part 2
 - Launch on 1st April for FAPI testing 

Update on Lodging Intent
========================

 - Torsten to update draft with this other approach
 - Change name to rich authorisation data




Issues
==========================

https://bitbucket.org/openid/fapi/issues/163/more-description-of-the-security-model
Security BCP assumes passive attackers, whereas FAPI assumes otherwise. 



Next Call
==========================

* Pacific call next week. Atlantic call in 2 weeks time.