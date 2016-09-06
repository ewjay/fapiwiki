============================================
FAPI WG Meeting Notes (2016-08-31)
============================================
Date & Time: 2016-08-31 14:00 UTC
             (07:00 PDT, 16:00 Denmark, 23:00 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Nat Sakimura, Dave Tonge, Brian J. Costello, Sascha Preibisch, Anton Tabrosky, Henrik Biering, Tony Nadalin
* Regrets from Luis Saiz

Adoption of the Agenda
=========================
* Agenda was adopted unchanged. 


Error report coding (Sascha)
================================
* Sacha reported the error report coding scheme using numbers. 
* The draft is available to see in the repo as a new branch: issues/26
* Dave asked if there is structure, and Sascha replied that it is using CA scheme and yes. 

External Org Relationships 
=============================

UK Groups (Dave)
------------------------------------
OBDG is still in an early stage. 
Legal mandates by CMA is on the implementation of  
Open and common API standards. 
It started to have meetings - stakeholder steering meeting next week. 

Dave advised to establish a liaison with them. 
The WG decided to ask for one. 

Dave was elected as the liaison officer to the Implementation entity. 
He will lead crafting the liaison letter, working with Board's liaison committee. 

Henrik is still working on to get to the the right connection at the Dansk Bank. 
He has contacted Vice president of the bank. 
Apparently, the division involved is in the Northern Ireland. 
He will re-initiate the action once FAPI WG has established 
the liaison. 

action:: 

    Dave to craft the liaison letter and send it to LC via Nat. 
     

EBA (Dave)
-------------------
EBA has a draft regulatory technical standards. It requires API access, not by screen scraping. 
They have not mandated a specific standard, though it refers to ISO 20022. 

Dave recommended the WG to respond to EBA Consultation as 
EBA text confusing authentication and authorization and 
clarification would be good. 

The Deadline is Oct. 14. 

Brian of Yodlee, who has been acting in data.gov.uk and Fintech field commented 
that responsible screen scraping should not be prohibited as a fall back for smaller 
financial institutions. 

The WG agreed that there probably is no need to mention screen scraping in the response. 

Need team to write response:: 

    Leader: Dave  


TC68, X9 (Nat)
----------------
Nat needs to create the liaison letter, which he has not yet. 
For X9, Paul Grassi volunteered to be the liaison officer. 

Dansk Bank (Henrik)
----------------------------
* Will wait until LS in place. 

Other action items
--------------------

    * Nat to draft liaison requests
    * Anoop to follow up with Intuit UK Team (Next week) 

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_ now available.  

WD Structure (Nat)
----------------------
1st WD is structured after ISO Directive Part 2 so that it could potentially be submit to 
ISO/TC68 at a later date. 

Main sections are divided into three sections: 

* Getting Tokens (profiling RFC6749)
* Using Tokens (profiling RFC6750)
* APIs. 

Currently APIs for the protected resource is following the DDA, while 
the security profile is much enhanced. Also, only a little bit of 
Open Data APIs are there (see the next section). 

Open Data (Nat --> Dave)
------------------------------
Open Data section of the 1st WD is quite light. 
DDA has not much text for it, and Nat created some initial text 
but much more is needed. What is being discussed in UK should 
be good to put in. 

It was also pointed out that maybe we need to look at W3C web credential specs. 


New & Open Issues (Nat)
=========================
* issue #28 - International names for retirement savings account names

Dave presented the issue. The WG agreed to the needs. 
Nat commented that at the end of the day, we probably need to 
have country specific instruments but it would be good to have 
the "class" that encompasses them. 

Action:: 


     * Concrete proposal to fix #28 needed. 
     * All members were asked to review issues on the tracker and comment if necessary. 
          * Sascha and John will review as named reviewer. 
          * Others please review as well. 
     * Questions on DDA-Cusotmer-ID. 


AOB
========

Coming up events
---------------------
There is a pre-IIW workshops. Neither Nat nor Tony would be available as 
they are in Abu Dhabi at the time and no VoIP is allowed there, 
but Sascha kindly agreed to lead the sessions on FAPI. 


Action::

    * Develop a presentation for the occasion (Lead by Sascha)

Next Call
----------
* 2016-09-06 23:00 UTC (16:00 PDT, 01:00+1d Denmark, 08:00+1d JST) 

The meeting adjourned at 14:50 UTC