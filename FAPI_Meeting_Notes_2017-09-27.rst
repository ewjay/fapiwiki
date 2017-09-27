============================================
FAPI WG Meeting Notes (2017-09-27)
============================================
Date & Time: 2017-09-27 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:07 UTC. 

Roll Call
===========
* Attending: Bjorn, Nat, Brian, Dave, Joseph, Ralph, Tom
   * Guest: 

* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Added two items. 

External Orgs
================

Open Banking (Dave, Pam)
-------------------------
* Dave asked for removing `x-` from the headers two weeks ago. Still waiting for the feedback. 
   * Perhaps we should create a version without `x-` etc. and link it to the WG homepage so that people will look at it instead. 
* Dynamic client reg. missing jwt guidance on how exactly to validate request and software statement jwt. 



Draft status and plans 
===========================

Streamlining the OBUK Implementer's Draft (Pam)
----------------------------------------------------
* Several open issues: Guidance of JWT validations etc. 
* It will be circulated for comment to the Open Banking after taking a snapshot. 
* The WG participants are expected to review them before taking the snapshot. 

Verification: non-compliant JWT audience (Pam)
------------------------------------------------
A Lively discussion on this topic. 
One clear consensus item was that it is a bad idea to have the software ignore `aud` value. 
Options are: 

1. Omit `aud`
1. Use logical `aud` (of Open Banking)
1. Use logical `aud` and the `client_id`


Pending pull requests (Joseph)
---------------------------------
Joseph gave an overview of the 5 pending pull requests. All seems to be non-contentious and thus will be merged. 


Events
================
Open Banking F2F (Ralph)
--------------------------
* One is planned on Oct. 17 in London. 

FAPI/Modrna joint F2F
-----------------------
* Date fixed on Nov. 7. 

AOB
===========


Next Call (Atlantic)
-----------------------
* The meeting was adjourned at 14:__ UTC.