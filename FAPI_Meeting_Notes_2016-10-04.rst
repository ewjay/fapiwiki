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
* Present: Nat, Dave, Sascha, Anton
* Regrets: Anoop, John, Henrik

Adoption of the Agenda (Nat)
===============================
* 

Atlantic Call Report (Nat)
===============================
* Nat briefly explained the outcome of the last week's Atlantic call 
  which is recorded at [[FAPI_Meeting_Notes_2016-09-28]]

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

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Restructuring (Nat)
----------------------

Issues 
=========================

#7 Add "Open Data" data set (Dave/Anoop)
----------------------------------------------
* issue #7
* Dave suggested to consider normalising the `Category`, `Family`, 
  and `SuperFamily` with the `AccountType` and `AssetClass` from the DDA.

#20 Surrogate Identifier (Nat/Anoop)
--------------------------------------------
* issue #20
* Surrogate identifier is `user_id`, which is a user identifier 
  but not user account number etc. It is `sub` in ID Token. 
* Suggests closing this ticket and continue tracking with #22. 

#22 Replace `user_id` in DDA with `id_token` and put a NOTE (Nat/Anoop)
-------------------------------------------------------------------------
* issue #22

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

