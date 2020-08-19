============================================
FAPI WG Meeting Notes (2020-08-19) 
============================================
Date & Time: 2020-08-19 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Bjorn, Kosuke, Takahiko, Joseph, Dima, Francis, Torsten, Dave, Torsten, Mark, Tony
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* Accepted as is. 

Events 
======================



External Organizations
========================
Australia (Dima)
----------------------

* Currently, CDR (Open Banking) ecosystem has 4 banks and 2 RPs with pilot mode customers. 
* November Release of CDR will have more instruments supported, joint accounts.
* PAR to be supported (by Feb 2021)
* Roadmap for RAR not clear. CDR is planning to implement fine-grained consent so it should come eventually. 

Berlin Group (Francis Pouatcha)
---------------------------------
* Advisory board meeting this month
* Taskforce September. 


PRs for 1.0 (Dave)
====================

Please give feedback to all the standing PRs. 

PR 175 Add security consideration around sharing keys
------------------------------------------------------
We should keep focus and not overly generalize. 
Merge. 

PR 183 Mark pushed request object spec as deprecated
------------------------------------------------------

PR 187 Privacy Considerations
-------------------------------
* Issue #90
* Lively discussion on whether it is inching to legal advise. 
* Tony pointed out that having best practice here is very useful as many systems designer and coders forget about them. 
* Callers agreed that most of "shall" can safely be turned into "should". WG members are asked to give a final review and we will come to the conclusion next week. 

Issues (Dave)
==================
#304 Are duplicates of the response_type, client_id, and scope values necessary when using PAR? (Joseph)
----------------------------------------------------------------------------------------------------------
* Issue #304
* Agreed on the approach proposed in the comments. 
* Joseph is to create a PR. 

AOB
==========================
n/a

The meeting was adjourned at 15:00 UTC.