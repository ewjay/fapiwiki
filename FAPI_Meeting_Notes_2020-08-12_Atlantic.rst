============================================
FAPI WG Meeting Notes (2020-08-12) 
============================================
Date & Time: 2020-08-12 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Mark, Don, Daniel, Takahiko, Dima, Kosuke, Dave, Chris, Francis, Joseph, Bjorn, Brian
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* 

Events (Don)
======================
FDX Event
--------------

External Organizations
========================
Berlin Group (Francis Pouatcha)
---------------------------------
Embedded approach. 

Chris is sceptical on BG adopting FAPI. 
However, he believes that it can be shown that the BG model can be implemented with FAPI. 

UK (Chris)
-------------
1. CMA9 on track for certification
1. eIDAS


PRs for 1.0 (Dave)
====================

Please give feedback to all the standing PRs. 

PR 183 Mark pushed request object spec as deprecated
-----------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/183

Callers agreed on the approach. 

PR 175 Add security consideration around sharing keys
------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/175

Approved. 

PR 182 Add non-normative examples of various objects
------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/182

PR 186 Add clauses requiring AS to be sure of/show client identity
---------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/186

Add it to privacy considerations. 
Close this PR after verified the privacy consideration text. 

PR 187 Created a sensible privacy considerations clause for dealing with issue #90
------------------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/187

Nat proposed multi-steps approach: 

1) to examine the structure and discuss on issue #90; 
2) if it looks good, then accept the PR; 
3) start creating issues to deal with text within each sub-clauses; 
4) discuss the text on the issues; 
5) create PRs for those issues; 




AOB
==========================
n/a

The meeting was adjourned at 14:59 UTC.