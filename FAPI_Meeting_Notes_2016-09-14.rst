============================================
FAPI WG Meeting Notes (2016-09-14)
============================================
Date & Time: 2016-09-14 14:00 UTC
      (07:00 PDT, 15:00 UK, 16:00 Denmark, 23:00 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: Bjorn, Nat, Dave, Henrik, Sascha, Anton, John, Nov

Adoption of the Agenda
=========================
* Adopted as is. 

External Org Relationships 
=============================

UK Implementation Entity (Dave)
-------------------------------
* Attended stakeholder meeting. Not technical but road map, as liaison. 
* CMA Implementation trustee. should happen in next couple of weeks. 
* Hard deadline of Jan 2018 for top 9 banks in UK, as in PSD2. 
* Payments UK technical people. Talked about expertiese that FAPI wg can offer. received greatfully. 
* Another meeting: for Data, more on higher level, at the type of data required for OB. 
* Informally accepted the liaison request. 
* Time is important. Maybe we can split the security section and make it reference-able. 

Action:: 

    Nat to send proposal for the split to the list. 


Federal Reserve of Minnesota (John)
---------------------------------------
* Doing research part of ANSI group. Paul Grassi. Encouraged to join here. 
* 

EBA Consultation (Dave)
----------------------------
* Dave sent a draft just before the call. 


Actions::
    
    * Nat to draft liaison requests
    * Anoop to follow up with Intuit UK Team (Next week) 

Branch issue/26 Error messages (Sascha)
=============================================
Sascha reported the current state of the issue/26 branch. 
It now has two chapters. People are encouraged to read it and give feedback. 

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Review Results (John)
--------------------------------
* John mainly on section 5 and 6: Not yet done. He will try to do it today and send it to the list. 
* See also #16 below. 

Action:: 

    John to review and send the result to the list. 


Issues 
=========================

#7 Open Data (Dave)
--------------------
* issue #7

Dave is going through the schema and taxonomy to see if it can be generalized. 
It will be done in conjunction with #28. 

#16 Client Authentication -- Do we need TLS mutual authentication? (Nat)
---------------------------------------------------------------------------
* issue #16
* Mutual Auth TLS profile not defined anywhere for token endpoint. We probably need to do ourselves. 
* Client auth JWT (secret, private key) can also be used, so it is either of them. 
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

Events
=============
Pre-IIW (John)
----------------
* Location fixed. We will have time allocated. Likely to be 20 min. 
* Sascha is in the process of preparing a presentation. It should be ready for review in two weeks. 

Action::

    * Develop a presentation for the occasion (Lead by Sascha) in two weeks. 

Pre-IETF (Nat)
-----------------
* Nat is yet to call his colleagues in Korea. He will try to do it tomorrow. 

Action::

    * Nat will get in touch with them and get back to the list. 


AOB
========
none. 

Next Call
----------
* 2016-09-20 23:00 UTC
     (16:00 PDT, 01:00+1d Denmark, 08:00+1d JST) 

The meeting adjourned at 14:50 UTC