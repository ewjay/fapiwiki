============================================
FAPI WG Meeting Notes (2018-01-17)
============================================
Date & Time: 2018-01-17 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: Nat, Bjorn, Brian, Charles Marais, Hubert Mariotte, Ralph, Torsten, Dave, Joseph
   * Guest: 
* Regrets: Anoop, Tony

Adoption of the Agenda (Nat)
==================================
* Adding Berlin Group status 

User Questioning API (Charles)
================================
Charles explained User Questioning. 

In it, the client sends the questions to the users to the user questioning API, which is an OAuth protected resource. 
Typically, it is hosted by an MNO. 
Then, the MNO sends the question to the user's handset. How the user is authenticated is out of scope. 
After being authenticated, the user is shown the question and answers to it. 
MNO then creates a token that represents the answer and sends it back to the initiator of the question. 

On the other hand, CIBA is specifically on the authentication and does not have the capability to ask questions. 
They could potentially be combined. 

From the PSD2 point of view, the "decoupled" authentication is a priority and FAPI WG will be concentrating on CIBA. There are use-cases that need user questioning and we may come back to it later. 


Open Banking IE Topics (Chris & Gavin)
========================================
Jan 13 Cut-over
------------------
* Managed Roll-out. Only limited number of people can access it. 
* Banks has not completed the test against test harness yet. One of the implementations from a vendor seems to have basic OAuth and OpenID Connect issues. 
* There is a question on the Part_1_5.2.2-15 where it says the list of scopes **shall** be returned. RFC6749 only requires it to be the case when the list of scopes was not the same as the one asked so another vendor was interpreting that it is implicitly returned. This issue will be raised to the issues list this afternoon and needs the discussion of the full WG. One of the reason pointed out for making it a "shall" was that since in Part 1, the authorization request is not protected so it could have been tampered by the time it arrived the authorization server. If that is the case, there will be a discrepancy between what AS has allowed and what the Client thinks it was allowed. 

Test Suite 
---------------------
* It is there. Banks should run it. 
* Mutual TLS negative test is not yet live but will be put online next week. 
* There is a sunset for the development work coming up for the test suite at the end of the month. 

Decision 090 Examples (Pam)
-----------------------------------
* Postponed. 


Berlin Group
======================
Torsten reported on the progress on the negotiation with Berlin Group. 
He seemed to have managed to put OAuth as the fourth SCA mode (other three are embedded, decoupled, redirect), though it is Vanilla OAuth + MTLS + PKCE. 
For the signature, they are using https://datatracker.ietf.org/doc/draft-cavage-http-signatures/, 
which is an individual draft written by an Oracle guy. 
(STET is also using the same.) 

Nat is going to send the link to OB's way, which uses JWS in detached mode. 


New Issues
==============
Skipped this item due to the time constraint. 
We will continue discussing the issue on the list and the issues themselves. 


Strong Customer Authentication Guidelines (John)
=====================================================
* Skipped

Events 
================
Open Banking Workshop (Ralph)
--------------------------------
There is an Open Banking Workshop on Jan. 30, 2018 in London. 
Unfortunately, Nat cannot be there due to the conflict with API Days Paris where he is speaking, but he will try to dial in. 

FAPI WG F2F @ London (Nat)
-----------------------------
There will be an informal FAPI WG F2F in London on Jan 29. 

API Days Paris (Nat)
----------------------
Main API Days event will happen on the January 30 and 31 in Paris. 
Nat will be there. 

AOB
===========

Next Call
-----------------------
The next call is scheduled to be in the Pacific time zone. 

* The meeting was adjourned at 15:03 GMT.