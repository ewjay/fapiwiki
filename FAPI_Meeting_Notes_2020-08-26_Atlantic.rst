============================================
FAPI WG Meeting Notes (2020-08-26) 
============================================
Date & Time: 2020-08-26 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Anoop, Joseph, Daniel, Chris, Don, Brian, Kosuke, Ralph, Torsten,  Dima, Dave, Stuart, Tony, Mark. 
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* +1 event. 
* #306

Events 
======================
FDX (Don)
----------
* Sept. 21st. 
* US FDX Developers Conference Keynote on global interoperability by Nat Sakimura
* Stuart Low will be presenting his view on the evolution of FAPI
* Increasing cross over on the members, e.g., Authelete, ForgeRock, Ozone, Ping, etc. 

OIDF Workshop (Don)
---------------------
* OIDF Workshop on October 25. 


External Organizations
========================
Australia (Dima/Stuart)
------------------------
n/a

Berlin Group (Francis)
------------------------
n/a

European Commission (Mark/Torsten)
------------------------------------
Preparing comment for public consultation on eIDAS regulation. 

ETSI (Ralph)
-------------
n/a

UK (Chris/Ralph)
---------------------
Main topic: the likelihood of EBA mandating eIDAS certs to be revoked on hard Brexit. 
FCA looking at a potential alternative, which is the fall back to the previous model. 

CMA9 and others going through FAPI certification: 

Firms are interested in the timing of FAPI 2.0 and differences. 
Nat gave his view on the roadmap. 

Daniel noted that the payload signature is a roadblock. 

ACT: Will deal with it in the next call. 


PRs for 1.0 (Dave)
====================
PR 188 Clarify that duplicate parameters requirement doesn't apply to PAR
---------------------------------------------------------------------------
Accepted. 

PR 189 FAPI-RW: Require PKCE when using PAR
---------------------------------------------
It is generally agreed. 
However, Stuart and Dima noted that there could be impacts to AU. 
Stuart will talk with the AU lead tomorrow. 


PR 182 Add non-normative examples of various objects
-----------------------------------------------------------
Joseph re-generated examples using example.com etc. instead of real domains. 

ACT: ALL: Please provide independent checks. 

PR 187 Privacy Considerations
-------------------------------
Torsten asked several questions on the PR. 

1. He does not want a document behind a paywall to be referred. 

Nat and Dave noted that they are not normatively referred - i.e., they are not necessary to comply with this document. At the same time, they provide valuable advice to implementers if they are interested in it. It would be a disservice to readers if we did not have any references. Joseph also asked if there is any credible and internationally vetted document and there seems to be none. 

2. He believes the statement "The authorization request should request only the claims that are needed for the purpose of the processing of PII to adhere to the collection minimization principle" belongs to OpenID Connect Core and not here. 

etc. 

Since we have run out of time, callers agreed to engage in the PR and try to close it by the next call. 

Issues (Dave)
==================
* #306 : We will deal with it as the first item next week. 

AOB
==========================
n/a

The meeting was adjourned at 15:04 UTC.