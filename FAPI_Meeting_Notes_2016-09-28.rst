============================================
FAPI WG Meeting Notes (2016-09-28)
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
* Present: Nat, Dave, Sascha, Anton
* Regrets: Anoop, John, Henrik

Adoption of the Agenda (Nat)
===============================
* Added Branch issue/26

Pacific Call Report (Nat)
===============================
* Nat briefly explained the outcome of the last week's Pacific call 
  which is recorded at [[FAPI_Meeting_Notes_2016-09-20]]

External Org Relationships 
=============================

UK Implementation Entity (Dave)
-------------------------------
* They have not appointed IE trustee yet. 
* Also, Security WG, Data WG, which are in the formation. 
* Because of it, they cannot yet formalize the relationship but they are working towards it. 
* Dave expects that it will be done in next week or two. 

EBA Consultation (Dave)
----------------------------
* Dave has started the draft at https://docs.google.com/document/d/1V3q1avS1zO2n2YaB-Y2Z1Vf6j-DrE7OwiISRuRpvs24/edit
* Nearly done the first draft
* Q7 and Q4
* Dave will send the draft and questions to the WG at the close of the day UK. 

Action:: 

    WG members are invited for collaborative editing. 
    Dave to send out the final draft to the WG for review when it is ready. 

    
OFX (Nat)
--------------------
* Nat reported to the group that OFX and OIDF started to hold quasi-regular meeting to discuss their alignment. 
* Nat told them that it would be good at least to have the same OAuth profile. 
* Dave pointed out that even if the data schemas are different, having the uniform Authorization and security 
  profile is worthwhile and that is one of the reason for the split of the drafts. 
* Don, the ED of OIDF, will have the F2F meeting with them on Oct. 28. 

FIGO API (Anton)
-------------------
* FIGO is a German based fintech company offering banking services provider. 
* Offers APIs for certain banking activities, account overview, transaction history, etc. 
* API documentation: http://docs.figo.io/
* The group discussed on whether we should start talking to them. 
* Nat, as an expert, expressed that it is better to involve relevant parties so it would be good to talk to them. 
  There are other parties that we also want to talk to, such as Open Banking Project. 
* The group decided to take it to the list to find out how we should approach it. 

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Security Review Results (Nat)
--------------------------------
* John and Nat had a call earlier today to discuss about section 5 and 6. 
* The result is recorded in issue #33. 
* Nat briefly explained the result. 
* Sascha pointed out that 15 seconds for the `code` validity could be too short for some clients, especially mobile, 
  that he things 60 seconds are more appropriate. 
* Sascha is going to add comments to the ticket. 


Branch Issue/26 (Sascha)
------------------------------
* Error code section is more-or-less complete and Sascha created the pull request, 
  which Nat accepted and merged to the master. 

Issues 
=========================

#32: How to communicate back the partial errors to the client (Nat)
----------------------------------------------------------------------------
# issue #32
* Sascha pointed out that it is not "error". It is the normal case, and 
  it should be handled accordingly. He will update the ticket with his comments. 

#28 International names for retirement savings account names (Dave/Nat)
-----------------------------------------------------------------------------
* issue #28
* no update this week as Dave was busy preparing for EBA consultation and Nat's 
  team member fell sick and could not update him yesterday. 


#31 5.2 - te - More fine grained scope needed (Nat)
----------------------------------------------------
* issue #31 

Callers discussed it briefly on it. 
Sacha pointed out that users would certainly want to know whether the client is doing read only or write. 
Callers agreed. 
Dave pointed out that some people say that the scope should be URI while they use just strings. 
Nat pointed out that strings are fine, and the problem with the scope is its unstructured nature. 
People agreed to update the issue ticket with their comments/ideas. 

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
* Nat has just started contacting them. Still working on what is possible. 

AOB
========

Next Call
----------
* 2016-10-04 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)

The meeting adjourned at 14:59 UTC.