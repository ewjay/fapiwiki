============================================
FAPI WG Meeting Notes (2017-03-07)
============================================
Date & Time: 2017-03-07 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:10 UTC. 

Roll Call
=============
* Present: Nat, Tom, Brian, Edmund, John, Henrik. 
* Regrets:
* Guest: 

Adoption of the Agenda (Nat)
===============================
* Added FS-ISAC
* Moved External Orgs as the first item. 


External Orgs
==================

FS-ISAC DDA (Brian)
----------------------
* FS-ISAC had a call. Feedback on DDA 2.0 that extends to tax, qtip, etc. 
* Banks are also interested in the consent flow. 

* Banks supporting DDA: Wells Fargo, Fidelity, Citi, 
* OFX: Chase


UK OBS (Nat/John)
------------------
* Need to come up with some spec in one to two weeks. 
* The solution needs to be implementable by the major vendors. 
* Bunch of change requests to be discussed in WD section of the agenda. 

Others
------------

Followings were not discussed. 

* OFX (Anoop)
* ISO/TC68
* Figo
* JP Banking Association (Nat)

Drafts
===================
Part 1: Read Only API Security Profile (Nat)
-------------------------------------------------------------
* `Part 1: Read Only API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md 

Not mandating public client support
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Change SHALL to SHOULD. 
* Make PKCE conditional. 
* Nat to make the changes today. 

Part 2: Read & Write API Security Profile (Nat & Edmund)
------------------------------------------------------------
* `Part 2: Read & Write API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md 

PoP other than Token Binding
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* WG decided to mandate PoP but allow two different methods: 
    * Token Binding
    * Sender constraint via Client Cert. 

* Client cert sender constraint should allow following verification methods: 
    * jku
    * x5u
    * x5t
    * dn <-- needs to be defined. All the others are defined in RFC8700. 

* Nat will come up with a draft and send it over to the list, and post it to IETF on Friday. 


Part 3: Open Data API
----------------------------
* N/A

Part 4: Protected Data API and Schema - Read only (Sascha)
---------------------------------------------------------------
* N/A

Part 5: Protected Data API and Schema - Read and Write
----------------------------------------------------------------
* This seems to be a priority. 
* Passing payment info in request object to have the user consent. 
* Gather example schema in the document so that we can abstract them later. 

AOB
========

Next Call (Atlantic)
--------------------------
* Next call is Atlantic shift and is in next week. 
  Nat is unable to make it. Perhaps John or Dave to set up a call. 
* Consider twice a week call until UK requirements are met? 

The meeting adjourned at ????? UTC.