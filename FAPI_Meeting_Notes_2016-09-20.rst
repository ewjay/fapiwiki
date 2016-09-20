============================================
FAPI WG Meeting Notes (2016-09-20)
============================================
Date & Time: 2016-09-20 23:00 UTC
      (16:00 PDT, 00:00+1d UK, 01:00+1d Denmark, 08:00+1d JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: 
* Regrets: Sascha

Adoption of the Agenda
=========================
* 

External Org Relationships 
=============================

UK Implementation Entity (Dave)
-------------------------------

Federal Reserve of Minnesota (John)
---------------------------------------
* Doing research part of ANSI group. Paul Grassi. Encouraged to join here. 

EBA Consultation (Dave)
----------------------------
* Dave has started the draft at https://docs.google.com/document/d/1V3q1avS1zO2n2YaB-Y2Z1Vf6j-DrE7OwiISRuRpvs24/edit


Actions::
    
    * Nat to draft liaison requests
    * Anoop to follow up with Intuit UK Team (Next week) 

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Review Results (John)
--------------------------------


Action:: 

    John to review and send the result to the list. 


Issues 
=========================

#29 Draft Split (Nat)
--------------------
* issue #29
* Per the result of the Atlantic call last week, the split of the draft is suggested as recorded in #29. 

#16 Client Authentication (John)
----------------------------------------
* issue #16
* Mutual Auth TLS profile not defined anywhere for token endpoint. We probably need to do ourselves. 
* Client auth JWT (secret, private key) can also be used, so it is either of them. 
   * Nat has suggested a text for this bit on #16. 
* We probably should not allow Basic auth. 
* John volunteered to craft text. 

Action:: 

    John to come up with the additional text to be applied and do a pull request. 


#28 International names for retirement savings account names (Dave/Nat)
-----------------------------------------------------------------------------
* issue #28
* Dave is looking through taxonomy and it should be solved together with Open Data. 

Action:: 

     * All members were asked to review issues on the tracker and comment if necessary. 
          * Sascha and John will review as named reviewer. 
          * Others please review as well. 
     * Questions on DDA-Cusotmer-ID. 

#30 Hanging Paragraph in 5.2 (Nat)
-----------------------------------
* issue #30 : Editorial
* disposition suggested in the ticket. 

#31 5.2 - te - More fine grained scope needed
------------------------------------------------
* issue #31 : technical
* Currently we have only one scope `FinancialInformation`. Perhaps we need more fine grained ones? 

Events
=============
Pre-IIW (John)
----------------
* Location fixed. We will have time allocated. Likely to be 20 min. 
* Sascha is in the process of preparing a presentation. It should be ready for review next week. 

Action::

    * Develop a presentation for the occasion (Lead by Sascha) in two weeks. 

Pre-IETF (Nat)
-----------------
* Not yet. 

Action::

    * Nat will get in touch with them and get back to the list. 


AOB
========

InvestmentAccout questions
------------------------------
* NRI's team is reviewing it, and feels that it may need a bit of refactoring. Will report on the analysis next week. 

Next Call
----------
* 2016-09-28 14:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 23:00 JST)

The meeting adjourned at  UTC