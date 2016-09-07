============================================
FAPI WG Meeting Notes (2016-09-06)
============================================
Date & Time: 2016-09-06 23:00 UTC
             (16:00 PDT, 01:00+1d Denmark, 08:00+1d JST) 
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:05 UTC. 

Roll Call
=============
* Present: John, Nat, Edmund, Brian
* Regrets: Sascha, Anton

Adoption of the Agenda
=========================
* As Sascha sent regrets, and it is a late night shift for Europe, 
  we decided to skip Error coding and detailed Europe related updates. 

External Org Relationships 
=============================

UK Implementation Body (Nat)
-----------------------------
* Nat reported that we have go ahead for sending LS to the body. 
* Nat has asked Dave to send it out as the liaison officer. 
* Brian reported that UK Implementation body meeting is tomorrow, so hopefully we can make it in time. 

TC68, X9 (Nat)
----------------
* No progress as Nat has been in vacation. He will re-initiate it once he gets back later this week.

Actions::
    
    * Nat to draft liaison requests
    * Anoop to follow up with Intuit UK Team (Next week) 

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Open Data and DDA
------------------------------
Brian asked why we are basing our draft on DDA and not OFX. Nat replied that it was an Intuit recommendation and since DDA had JSON version, we picked it up. Brian noted that what is important is the data type extensibility and as both has it, it is fine. Nat noted that he was involved in OFX 1.0 back in 95 or 96, reviewing it for the applicability for Japanese financial market, having been approached by Microsoft. 

Actions::

    * John to review (mainly) section 5 and 6, especially on the security details. 
    * Brian agreed to review the doc as well. 

New & Open Issues (Nat)
=========================
* No new issues
* Though we have agreed that these issues needs to be fixed, we need concrete text to apply. Please send pull requests. 

Action:: 

     * Concrete proposal to fix #28 needed. 
     * All members were asked to review issues on the tracker and comment if necessary. 
          * Sascha and John will review as named reviewer. 
          * Others please review as well. 
     * Questions on DDA-Cusotmer-ID. 

Events
=============
Pre-IIW
----------------
Pre-IIW event will be at VMWare. We have 5 hours to cover all the working group. 
The format is not yet finalized but if we follow the previous patterns, the WG 
will have 20 minutes to present, and any substantial work has to be deferred to 
IIW itself. 

Action::

    * Develop a presentation for the occasion (Lead by Sascha)

Pre-IETF
-----------------
Nat will ask his Korean counterparts for the possibility of having one. 

AOB
========
John got contacted by the Federal Reserve of Minnesota. 
He will have a call tomorrow. 
Apparently FR governors are active now on fintech, aggregation, etc. 
Perhaps they are developing their internal position. 
They were in W3C web authentication WG as well.

Brian pointed out that Federal Reserves are not so much into 
the technical details and the FDIC subcommittee usually takes care of the tech. 
They take care of the prudential regulation - level playing fields, safety, soundness, and stability. 
`OCC <https://en.wikipedia.org/wiki/Office_of_the_Comptroller_of_the_Currency>`_ published report on innovation (June) perhaps the inquiry is related to this one. 

Nat pointed out that just like we will be developing our response to ECB, 
we may need to develop one in the US as well. 

John will report back about the call in the next meeting. 
He will see if they can be involved in the WG work as well. 

Next Call
----------
* 2016-09-13 14:00 UTC
      (07:00 PDT, 15:00 UK, 16:00 Denmark, 23:00 JST)

The meeting adjourned at 23:35 UTC