============================================
FAPI WG Meeting Notes (2020-09-02) 
============================================
Date & Time: 2020-09-02 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Mark, Daniel, Joseph, Torsten, Takahiko, Dima, Brian, Tony, Kosuke, Dave, Francis, Bjorn, Chris, Freddi 
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* Message Signing

Events 
======================

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
Consultation response to be dealt with in eKYC WG. 
To submit tomorrow. 

ETSI (Ralph)
-------------
n/a

FDX (Anoop)
-------------------
n/a

UK (Chris/Ralph)
---------------------
Chris reported: 


Issues (Anoop)
==================

* #306 (Anoop)

#309 Decision on message signing for FAPI 2 Advanced (Daniel)
---------------------------------------------------------------
* #309 

Agreement on having control objectives. 
However, there is no agreement on what needs to be written as the control measure. 

Almost 40 minutes of the call time was spent on the discussion on whether we should recommend detached JWS or something else. 
This is to be continued next week. 

Takahiko asked if there is any documentation on pros and cons of various approaches. 
Joseph pointed to https://bitbucket.org/openid/fapi/src/master/Financial_API_HTTP_Signing.md . 

Takahiko volunteered to review it. 


PRs for 1.0 (Dave)
====================

PR 189 FAPI-RW: Require PKCE when using PAR (Stuart)
------------------------------------------------------
Feedback from Stuart on AU impact after his talk with AU lead. 


PR 182 Add non-normative examples of various objects
-----------------------------------------------------------

Last ACTion: ALL: Please provide independent checks. 

It should be ready to be merged in a few days. 

PR 187 Privacy Considerations
-------------------------------
1. Agreed to make it advise to implementers and not a statement of limitations. 
1. Agreed to remove general bit and only deal with FAPI specific topics if there is any. 
1. Agreed to remove all ISO references with "shall" or "should" keywords. 
1. Agreed to have no "shall" in this section. 


AOB
==========================
n/a

The meeting was adjourned at 15:03 UTC.