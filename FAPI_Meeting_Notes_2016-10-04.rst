============================================
FAPI WG Meeting Notes (2016-10-04)
============================================
Date & Time: 2016-10-04 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: John, Nat, Edmund, Eric, Bjorn, Henrik, Anoop
* Regrets: Dave, Anton, Sascha

Adoption of the Agenda (Nat)
===============================
* Adopted as presented. 

Atlantic Call Report (Nat)
===============================
* Nat briefly explained the outcome of the last week's Atlantic call 
  which is recorded at [[FAPI_Meeting_Notes_2016-09-28]]

External Org Relationships 
=============================

UK IE & EBA (Nat)
---------------------
* Nat reported the message from Dave that there is no progress on UK IE. He will report back by email when it progresses during the week. 
* Also, Nat reported that Dave has prepared the EBA consultation response draft and solicited the WG members to give him their feedback ASAP, as the deadline is just a week away. 

X9 (Nat)
---------
* The relationship has been established. Nat and Paul is now on their mailing list. 


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

#32: How to communicate back the partial errors to the client (Nat)
-----------------------------------------------------------------------
# issue #32
* Anoop added a suggested solution. 
* Edmund will check if it can be expressed in Swagger. 

#31 5.2 - te - More fine grained scope needed (Nat)
----------------------------------------------------
* issue #31 
* Anoop pointed out that CRUD x Resource may be OK, 
  but the meaning of e.g., "cCustomer" may not 
  be obvious. He also pointed out that FIs themselves 
  may want to use these APIs without exposing to the 
  outside. 
* Nat explained that a customer creating 
  an account at a bank using his National ID card 
  through the ATM network is an example of "create account" 
  use case. Although it is possible for the ATM 
  network to use proprietary APIs of each banks for 
  this operation, it is much more desirable to have a 
  standardized API because it will then be able to 
  re-use the program. 

#16: Client Authentication -- Do we need TLS mutual authentication? (Anoop)
-------------------------------------------------------------------------------
* issue #16
* Anoop pointed out that it is likely that banks mandates TLS client certs, 
  which gets us into the challenges that OFX had - it was for the desktop apps, which could not use mutual TLS. 
  DDA used TLS mutual auth as it was for the back end services of the Fintech companies. 
  Then, he asked what would be the position of the WG.  
* Nat explained that we have to have two ways of doing it. 
  * TLS client certs authentication
  * Another way for Mobile clients (e.g., Assertion based authn potentially Token Bound)
* For the TLS client certs, John and Brian are working on to create a new document explaining how to do 
  the TLS client auth to the token endpoint, which should be ready to be reviewed at IETF Seoul meeting. 

#12: OAuth Profile should mandate per AS redirect URI for Clients with session comparison (Nat)
---------------------------------------------------------------------------------------------------
* issue #12
* Nat replied to the comments in the ticket that we need these to avoid mix-up attacks etc. 

#33: John's Security Section Review Result (Nat)
---------------------------------------------------
* issue #33
* Nat went over the ticket. 
* WG agreed that `code` validity to be 60 seconds. 
* If `code` is PKCE bound, that limit is not needed. 

Events
=============
Pre-IIW (John)
----------------
* Sascha is developing a presentation and will be able to send the draft by the weekend.
* WG is asked to review it ASAP once received it.  

Pre-IETF (Nat)
-----------------
* Nat is going to create a ticket. Please add what you would like to talk about in it. 

AOB
========

Next Call
----------
* 2016-10-04 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)

