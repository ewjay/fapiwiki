============================================
FAPI WG Meeting Notes (2020-01-22) 
============================================
Date & Time: 2020-01-22 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call
===========
Attending:
--------------------
Nat
Ben White (Plaidd)
Bjorn Hjelm
Daniel Fett
Joseph
Kosuke
DOn
Dima
Brian
Dave
Stuart Low
Glyn (Open Banking)

Guest
-------
Martin Toth 


Regrets: 
---------------------    
Torsten

Adoption of the Agenda (nat)
==================================
* Added Berlin Group report. 

Event
======
Swift Conference/FAPI F2F (Don)
---------------------------------
* Around Feb. 18. FAPI F2F. Don is finalizing. 
* Likely to be 17th. at Akamai office. FAPI, Lunch, eKYC. 
* FAPI and eKYC F2F. 
* Eventbrite will be sent by CoB today. 

European Identity Conference (Nat)
------------------------------------
* Due date: January 24. 
* OpenID Foundation Workshop on the 1st day. 
* May 12 Morning. 
* FAPI & eKYC F2F at the conference on 11th May. 
* Board meeting on May 11. 

JP Event (Nat)
---------------


External Organizations
=============================
Berlin Group (Daniel/Dave)
---------------------------
* Visited Bonn to discuss with the editors. 
* Introduced OAuth and OpenID Connect/FAPI/PAR/RAR. 
* Not very interested in aligning. 
* They have very complex use cases that they have not figured out. 
* Consent management
* Embeded mode. 
* It was not as positive as it could be but there are rooms for alignment a bit. 
* Global interoperability. 

Australia (Stuart/Dima)
--------------------------
* Ver. 1.1.1 has been released. Side by side with the spec analysis. 
* https://bitbucket.org/openid/fapi/src/master/cds-spec-analysis/
* A lot better than it used to be. Focus area would be to make sure that it will not break in certification. 

* Consent (Dima)
* Consent requirements: good to compare how consents are dealt with in other Jurisdiction. 

* Feb 1. deadline has been moved to July 1. 

* Certification has been under conversation but is not used in reality. Perhaps because the current CDS breaks on certification. 

* Focus of WG should be vendors breaking their products. 

* Now in political phase? FDATA is trying to talk to the Government. 

* Identify the diffs that really breaks and escalate. 

* Draft letter to be developed by the London meeting. 



Draft Status
========================
OAuth JAR (Nat)
----------------------
* Merge is bad. 
* client_id and response_type - interop. Perhapss add a note? 
    * Add a note suggesting for backward compatibility, add these and match. 

OAuth PAR (Daniel)
----------------------
* WG adopted PAR. 

OAuth RAR (Daniel)
----------------------
* Accepted as the WG item. 

Issues
========

#163 Security Model (Daniel)
----------------------------------
* https://docs.google.com/document/d/1Lo2LCV5eV7iVGbsM0C7i3pL1nWRftfqjpfFCx5Q3Pds/edit#heading=h.u85w4jb6qchc
* https://docs.google.com/spreadsheets/d/1PtG4f-Svils7wHBa7cGaZubbh-6lGifce38c_oShSss/edit#gid=550739163

WG discussed the initial text created by Daniel. 

* https://bitbucket.org/openid/fapi/issues/163/more-description-of-the-security-model
* https://docs.google.com/spreadsheets/d/1PtG4f-Svils7wHBa7cGaZubbh-6lGifce38c_oShSss/edit

They generally agreed that the attacker model is about right. 
Daniel also pointed out that there is one attack that we do not have a solution for. (PKCE chosen text attack.) 

WG members are invited to make comments on the document and the ticket. 
If it is a concrete change proposal to the document, it should go to the document itself. 
If it is a more general discussion, it should go to ticket #163. 

#277 FAPI-RW: Is disallowing signed id_tokens allowed? (i.e. always used signed+encrypted)
-----------------------------------------------------------------------------------------------
# Issue #277
* Short answer: Yes. It is the ecosystem's choice to make it stronger. 
* Signed and Encrypting still is supporting "Signed" but the language can be clearer. 
* ACTION: Propose an improved language. 

Next meeting
======================
* Next week, same time. 

AOB
==========================
* eKYC/IDA Meeting this week is cancelled. 


The meeting was adjourned at 14:58 UTC.