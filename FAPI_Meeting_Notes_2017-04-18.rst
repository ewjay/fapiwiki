============================================
FAPI WG Meeting Notes (2017-04-18)
============================================
Date & Time: 2017-04-18 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 15:10 UTC. 


Roll Call
===========
* Attending:  
* Regrets: Nat


Adoption of the Agenda (Anoop)
==================================
* Adopted with the addition of the following:
    * Action items necessary to finalize read/write spec

MTLS @ IETF report (John)
==========================
* issue #75

Issues 
========

`#83 - Support for GET <../issues/83>`_
-------------------------------------------------------------
* Awaiting pull request from Pam

`#82 - Strict Access Control to logs <../issues/82>`_
-------------------------------------------------------------
* Awaiting pull request from Pam

`#81 - Identify user associated to the access token <../issues/81>`_
-------------------------------------------------------------
* Will replace 'user' with 'entity'
* Awaiting pull request

`#79 - Part 1: issues with x-fapi-customer-last-logged-time header <../issues/79>`_
-------------------------------------------------------------
* Nat will merge pull request from Joseph

`#78 - Malicious Endpoint Attack <../issues/78>`_
-------------------------------------------------------------
* Having a signed request object in Hybrid flow will mitigate this attack

`#77 - IdP Confusion Attack <../issues/77>`_
-------------------------------------------------------------
* Having a signed request object in Hybrid flow and unique redirect_uri per client_id will mitigate this attack

`#75 - Support other method of HoK than TOKB <../issues/75>`_
-------------------------------------------------------------
* JPOP will be merged with client certificate authentication at Token endpoint by Brian
* Waiting for merged spec to become work item in OAuth WG
* Meanwhile, we can put links in the annex and then update the reference point once the spec is approved

`#72 - Spec not clear as to which auth flows are supported <../issues/72>`_
-------------------------------------------------------------
* Dave will create pull request before next call

`#61 - Fund availability API <../issues/61>`_
-------------------------------------------------------------
* Discussion is going towards waiting for implementation entities to do it first
* Put on hold


Action Items Necessary to Finalize Read/Write Spec 
===================================================
* There seems to be not much in the sections regarding accessing resources and security considerations
* For Security Considerations, if server supports pure bearer and mutual TLS bound token, it should not support both on same endpoint

* In UK, some FIs send payment information via reference uri. Is it possible to merge this with request_uri and remove additional endpoint by requiring support and request_uri with encryption?
* For now, will keep options open

* Is AS and Client sections complete? Nat will do another pass



External Orgs
================

FS-ISAC (Anoop)
-----------------

UK OBS (Dave)
-------------------------

ISO/TC68 (Nat)
-------------------


Others
------------
* 

AOB
===========
Next Call (Atlantic)
-----------------------

The meeting was adjourned at 23:58 UTC