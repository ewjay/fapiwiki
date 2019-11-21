============================================
FAPI WG Meeting Notes (2019-11-20) 
============================================
Date & Time: 2019-11:20 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
Attending:
--------------------
#. Bjorn
#. Nat
#. Craig Borysowich (Payments Canada)
#. Dima Postnikov
#. Joseph
#. Kosuke
#. Stuart Low
#. Rob Otto 

Regrets: Dave
---------------------    

Adoption of the Agenda (nat)
==================================


External Organizations
=========================

Open Banking (Joseph)
----------------------
Open Banking shared a new roadmap consultation mainly focused to wrap up functional spec. 
e.g., 9 CMA banks should be made available the sweeping service. 
CMA 9 must pass the functional test. 

ISO
-------------
Nat started to explore getting PAS Submitter status. 

IETF
-------------
HTTP Signing (Joseph)
~~~~~~~~~~~~~~~~~~~~~~~~
Justin's slide https://datatracker.ietf.org/meeting/106/materials/slides-106-secdispatch-http-signing

It was discussed in the Dispatch group. 
Advised to do it in HTTP group. 

Annabel has split Justin's PoP spec. into HTTP bit and OAuth Token presentation bit. 

It looks like some evolution of Cavage may happen but it still is in the early days. 

OAuth WG (Joseph)
~~~~~~~~~~~~~~~~~~~~~~~~~
Tomorrow 8AM UTC. 

BoF Transactional OAuth
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
https://www.youtube.com/watch?v=q096sY6L9-E

Exploring whether Justin's or Torsten's spec to be adopted. 

Australia (Stuart)
----------------------
Analysis of the current draft needs to be done. 

Joseph has been talking with the EY team on testing. 
EY + Data 61 to drawing the testing plan. 
Data 61 wants to start an independent test. 

Others
--------------

Pull Requests
=================

https://bitbucket.org/openid/fapi/pull-requests/

Issues
================

https://bitbucket.org/openid/fapi/issues/

#255: certification clarification request: location of discovery document
----------------------------------------------------------------------------
Joseph is going to create a pull request. 

#207: RS256 vs PS256 (again)
--------------------------------------
Nat need to create a pull request. 

#236
---------------
Closed with pull request #145

#216 TLS_ECDHE_ECDSA cipher suites
-----------------------------------------
Pending Dave's email intraction with crypto experts. 

#232: Part 1: Complete the privacy consideration section
-------------------------------------------------------------
Nat to write the text. 

#240: FAPI-R: length/entropy of authorization code / refresh token / client_secret
-----------------------------------------------------------------------------------
Waiting for Dave's text. 

#242: Missing Bibliography Reference to FAPILI
--------------------------------------------------
Around Xmas time by Stuart. 

#273: Security considerations re large access tokens
------------------------------------------------------
To be recorded in the implementer's advice document. 
Concrete text is needed. 






AOB
==========================




The meeting was adjourned at 14:56 UTC.