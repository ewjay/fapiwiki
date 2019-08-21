============================================
FAPI WG Meeting Notes (2019-08-07) 
============================================
Date & Time: 2019-07-31 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:04 UTC. 

Roll Call
===========
Attending:
--------------------
#. Nat Sakimura
#. Dima Postnikov
#. Kosuke Koiwai 
#. Joseph Heenan
#. Dave Tonge
#. Anthony Nadalin
#. Brian Campbell
#. Torsten Lodderstedt
#. Eric Tedeschi
#. Bjorn Hjelm
#. Ralph Bragg

Regrets: 
---------------------    
#. Anoop Saxena

Adoption of the Agenda (Nat)
==================================
* Added Certification

Certification
=====================
2 Banks paid. One has not submit the result yet. 
The other has, but not yet publisheable. 
Request from Open Banking to separate FAPI Certification result. 

External Organizations
=============================
FDX
----
* Sept. 13, 14 in Detroit. 
* Presso needed. If you have one already, please send it to Bjorn and nat. 


Pull requests 
=================
#131 first proposal to integrate JARM as equal option
-----------------------------------------------------------
JOseph is doing the final review. 

#137 changed the draft to use the application/x-www-form-urlencoded encoding
-------------------------------------------------------------------------------
Related to issue #253. 
Changes the JSON POST to form encoding. 

Brian asked that posting raw JSON may be simpler. 

#134 FAPI-R/RW: client authentication restrictions apply to all endpoints
--------------------------------------------------------------------------------
Joseph will make the change to pull request. 

#130 Initial attempt at listing requirements for FAPI HTTP signing
-----------------------------------------------------------------------
Accepted as a new document. 

#129 First Cut
-----------------------

#113 FAPI-R: Clarify authorization code reuse requirements
---------------------------------------------------------------


#135 FAPI-RW: Apply cipher restrictions to < TLS 1.3
-----------------------------------------------------------
Just qualifying TLS cipher restrictions. 

Code reuse issue
-----------------------
Merged. 

#125 CIBA: let AS determine whether signed request is mandatory
------------------------------------------------------------------
Merged. 

Issues
==============
#239 FAPI part 2 should mention/require discovery? (Joseph)
--------------------------------------------------------------
In Open Banking, Discovery is mandated so there is no deployment impact in that respect. 
Two good comments from Brian and Torsten. 
Joseph will create a pull request. 

#250 certification clarification request: grant_types_supported in discovery (Joseph)
---------------------------------------------------------------------------------------
People in the call agreed that it should be advertised, but we did not get to 
the conclusion whether it should be "SHALL" or "SHOULD". 

Discussion is going to be continued on the ticket and we will come back to it in the next call. 


AOB
==========================

The meeting was adjourned at 15:09 UTC.