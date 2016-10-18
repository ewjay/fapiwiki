============================================
FAPI WG Meeting Notes (2016-10-04)
============================================
Date & Time: 2016-10-18 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: 
* Regrets: 

Adoption of the Agenda (Nat)
===============================
* 

Atlantic Call Report (Nat)
===============================
* Nat briefly explained the outcome of the last week's Atlantic call 
  which is recorded at [[FAPI_Meeting_Notes_2016-10-04]]

External Org Relationships 
=============================

UK Implementation Entity (Dave)
-------------------------------
* They have appointed trustee but not yet announced. 

Others
----------------
* OFX: 
* FIGO: http://docs.figo.io/ (Anton) 
* Apigee: https://openbank.apigee.com/home


Action::

    * Anton to get in touch with FIGO. 
    * Dave will get in touch with Apigee, who is in the API Days conference today. 
    * Nat and John will try to get in touch with Apigee as well. 


Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Restructuring (Nat)
----------------------
* 5 parts decomposition (Security Profile for Read Only, Security Profile for Read Write, 
  Open Data API, Read Only API, Read Write API.) 
* Nat also suggested that we may want to separate out the Data APIs into e.g., industries. 
* Anoop pointed out that such decomposition might not be easy since a bank may have to return 
  all the account types and transactions anyways. There are two options: 
  1. Get the list of accounts and then do another call to get the transactions; 
  2. Get the list of accounts with transactions, where a flag is set in the accounts list. 
* Anoop will send the details by creating a new ticket. 

Issues 
=========================

#7 Add "Open Data" data set (Nat/Anoop)
----------------------------------------------
* issue #7
* Anoop asked for the examples use of such. 
* Nat pointed out that there are example schema in 
  the section 7.3 of the current spec. (though without Swagger representation), 
  and explained the use case that the user searches for the closest 
  ATM from the banking app. 

#32: How to communicate back the partial errors to the client (Anoop)
-----------------------------------------------------------------------
# issue #32
* Anoop added a suggested solution. 
* Edmund will check if it can be expressed in Swagger. 

#31 5.2 - te - More fine grained scope needed (Nat)
----------------------------------------------------
* issue #31 

Events
=============
Pre-IIW (John)
----------------
* https://www.eventbrite.com/e/openid-foundation-workshop-tickets-27312519481
* Now sold out. 
* Sascha is developing a presentation and will be able to send the draft by the weekend.
* WG is asked to review it ASAP once received it.  

Pre-IETF (Nat)
-----------------
* Room Assignment? 

AOB
========

Next Call
----------
* No call next week due to ISO and IIW. 
* 2016-11-02 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)

