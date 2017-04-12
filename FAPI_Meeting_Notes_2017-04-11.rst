============================================
FAPI WG Meeting Notes (2017-04-11)
============================================
Date & Time: 2017-04-11 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:10 UTC. 


Roll Call
===========
* Attending: John, Nat, Bjorn, Henrik, Joseph, Ralph, Sascha, Tom 

* Regrets: Dave, Tony, Anoop

Adoption of the Agenda (Nat)
==================================
* Adopted as is

Issues 
========

`#81 - Identify user associated to the access token <../issues/81>`_
----------------------------------------------------
Since Tom was not on the call last time, Nat asked Tom to explain his position. 
The point he made was that at least in the US, only a human being is allowed to authorize the transaction. 
Thus, the use of the term "user" instead of "entity" seemed more appropriate. 

Nat and John pointed out that it is true for the authorization step but 
this ticket is talking about the resource access step. 
In the resource access step, only the client and the resource is 
involved and it may well suffice to find out the account holder, 
which may well be a corporation and not human being, 
so expressing it as "user" would be confusing. 

Nat asked the group if they can come up with a better wording than "entity". 
Otherwise, the change from "user" to "entity" will be made in the next iteration. 


`#82 - Strict Access Control to logs <../issues/82>`_
-------------------------------------------------------------
* Clarified that 'should' = 'SHOULD' in ISO language

`#83 - Support for GET <../issues/83>`_
-------------------------------------------------------------
* Sasha stated that the current text is straight forward
* It was decided that the text will remain unchanged but the reference to
  RFC 2616 will be changed to section 4.3.2 of RFC 7231 
* Sasha will create pull request




External Orgs
================

UK OBS (Ralph)
-------------------------
* OBS has agreed to rebase security requirements of APIs on
  OpenID Connect, using signed JWTs for non-repudiation and provisions for
  non-repudiation services for communication authorizations in the request
* Hoping to leverage FAPI profile for read and read/write
* Need to draft OB profile based on FAPI and initially ratify it in UK Competition Markets Authority 
  and UK banks.
* View/desire exists to change management/maintenance of profile from Open Banking Implementation Entity to OIDF
* OB will be joining the OIDF
* How can we fast track/accelerate development of read/write profile?
  Need discussions among WG, reuse existing specs as appropriate instead of reinventing
  Need to align on a common security/trust framework instead of a specific API
  Should still document existing APIs being used so it can be publicly available    
  Contributions can be easily submitted to the WG after submitting IPR

* Ralph gave overview/history of PSD 1/2 
  There are mandates for a common API for the following services by 2018/01/01 :
   a) Account Information
   b) Transaction history information
   c) Payment services

* KYC laws require banks to verify identity of account holder
  This makes banks an authority for verifying identity
  Some banks opposed to identity attestation services
  If major banks offer ID services, most will follow
  ID services is very valuable for other industries(medical) / services
  Providing identity information is optional in FAPI
  There are no provisions in PSD2 for standardizing account creation APIs so use case 
  of creating a new account to transfer money by unauthorized party seems unlikely
  Also parties using API must be designated by a national financial authority
   

ISO/TC68 (Nat)
-------------------
Nat and Paul have written a liaison statement and is submitting it to the secretariat of TC 68 in 
time for the Rio de Janeiro meeting.


Starling Bank (Dave)
----------------------
Dave was absent for update.


Others
------------
* 

AOB
===========
Next Call (Pacific)
-----------------------