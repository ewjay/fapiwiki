============================================
FAPI WG Meeting Notes (2016-09-20)
============================================
Date & Time: 2016-09-28 14:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 23:00 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: 
* Regrets:
* Guest: 

Adoption of the Agenda (Nat)
===============================
* 

Pacific Call Report (Nat)
===============================

External Org Relationships 
=============================

UK Implementation Entity (Dave)
-------------------------------


EBA Consultation (Dave)
----------------------------
* Dave has started the draft at https://docs.google.com/document/d/1V3q1avS1zO2n2YaB-Y2Z1Vf6j-DrE7OwiISRuRpvs24/edit


Action:: 

    WG members are invited for collaborative editing. 
    Dave to send out the final draft to the WG for review when it is ready. 

    
OFX (Nat)
--------------------

 

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Review Results (Nat)
--------------------------------
* #33


Issues 
=========================

#16 Client Authentication (John)
----------------------------------------
* issue #16
* Mutual Auth TLS profile not defined anywhere for token endpoint. We probably need to do ourselves. 
* Client auth JWT (secret, private key) can also be used, so it is either of them. 
   * Nat has suggested a text for this bit on #16. 
* We probably should not allow Basic auth only. 
* John volunteered to craft text. 

Action:: 

    John to come up with the additional text to be applied and do a pull request. 

#29 Draft Split (Nat)
--------------------
* issue #29
* Per the result of the Atlantic call last week, the split of the draft is suggested as recorded in #29. 
* The call participants agreed that 5 parts structure as below would be good. 
  * part 1: Read Only API Security
  * part 2: Open Data API
  * part 3: Protected Resource Data API
  * part 4: Read Write API Security
  * part 5: Read Write Data API
* Incorporate branch issue/26 into the current master branch, and then do the split. 
* During the time, we can continue reviewing the current WD esp. on the Read only security 
  so that we can go quickly to the implementer's draft vote on the part 1. 

#28 International names for retirement savings account names (Dave/Nat)
-----------------------------------------------------------------------------
* issue #28
* Dave pointed out that this is a tricky area where we have to cover vast array of products. 
   * e.g., while trying to come up with a strawman Dave started wondering whether it would make sense to have 
     interest in a single field as they now seem to depends on the account balance. 
* Nat pointed out that it is easier with the concrete account data as it can talk about the "currently applicable interest rate" but when it comes to "open data", it would be difficult. 
* NRI's team is also looking through the investment account data and they started feeling that some refactoring is needed. 
* Nat wanted to have a separate call for DDA-Customer-ID with Anoop. 

#30 Hanging Paragraph in 5.2 (Nat)
-----------------------------------
* issue #30 : Editorial
* disposition suggested in the ticket. 

#31 5.2 - te - More fine grained scope needed (Nat)
----------------------------------------------------
* issue #31 : technical
* Currently we have only one scope `FinancialInformation`. 
* Nat suggested that perhaps we need more fine grained ones? 
* Dave pointed out that he has use cases for just asking for account balance and separately the transactions details. They are two clear different scopes. 
* Nat pointed out that from the collection minimization point of view, it would also be good to have sub-scopes. 
* It is not suggesting to ditch the current scope, but is just suggesting that we need to have more granular ways to specify the access target. 

Events
=============
Pre-IIW (John)
----------------
* Location fixed (VM Ware). We will have time allocated. Likely to be 20 min. 
* Sascha is in the process of preparing a presentation. It should be ready for review next week. 
* John will see Don tomorrow to ask for the est. of time and agenda. 

Action::

    * Develop a presentation for the occasion (Lead by Sascha) in two weeks. 

Pre-IETF (Nat)
-----------------
* Not yet. 

Action::

    * Nat will get in touch with them and get back to the list. 


AOB
========

How to communicate back the partial errors to the client (Anoop) 
-------------------------------------------------------------------
While implementing DDA, Anoop et al. came across a new use case.

Sometimes, when banks are returning data, some of the sub-system may not be available temporarily and results in partial results. 

For example, the Bank's credit card system may be on maintenance mode and the bank may not be able to return data on credit card while it can return everything else. It is just a temporary error. 

We have not defined anything on this. Bank needs to communicate it back to the client. e.g., yesterday I returned 5 accounts but today I am returning only 3. However do not delete the 2 as it is only temporarily unavailable. When we come back, I might be able to return them.

Anoop can come up with suggested text. 

Action:: 

    Nat to create a ticket and assign it to Anoop.  


Next Call
----------
* 2016-09-28 14:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 23:00 JST)

The meeting adjourned at 23:55 UTC.