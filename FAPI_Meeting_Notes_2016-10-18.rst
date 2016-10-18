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
* Present: John, Nat, Anoop, Edmund, Henrik, Sascha, Brian C. 
* Regrets: Dave, 

Adoption of the Agenda (Nat)
===============================
* Added **Pre-IIW Presentation (Sascha) 

Atlantic Call Report (Nat)
===============================
* Please refer to [[FAPI_Meeting_Notes_2016-10-12]]
* There is API Days in Paris on 13, 14 December. The organizer will be in IIW so we may want to connect with him. 
    * Dave is supposed to introduce him to John and Sascha
    * There currently is a FUD that "OAuth is no good for financial APIs", so we need to find somebody to be there to present.

External Org Relationships 
=============================

UK Implementation Entity (Dave)
-------------------------------
There has been an update from the UK Implementation Entity:
http://www.paymentsuk.org.uk/sites/default/files/Implementation%20Entity%20Steering%20Group%20-%20Oct%202016%20Update%20to%20CMA.pdf

Key points from a FAPI perspective:
 - The trustee has been appointed
 - Working groups and advisory boards are being convened
 - There is a push to ensure the API standards developed comply with PSD2 (and the RTS)

I haven't had any more specific feedback apart from the general communication linked above.

I hope to have more information before the call next week. 

Others
----------------
* OFX: Anoop to follow up for the meeting on Friday after. 
* FIGO: http://docs.figo.io/ (Anton) 
* Apigee: https://openbank.apigee.com/home : Got email introduction from Dave. Not heard back yet. 


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
Pre-IIW Presentation Review (Sascha)
-------------------------------------

Pre-IIW (John)
----------------
* https://www.eventbrite.com/e/openid-foundation-workshop-tickets-27312519481
* Now sold out (130). Expect 50 - 100 people. 
* Will check if there is remote access / webinar. 

Pre-IETF (Nat)
-----------------
* John has made a room request. Waiting for the response. 

AOB
========

Next Call
----------
* No call next week due to ISO and IIW. 
* 2016-11-02 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)

