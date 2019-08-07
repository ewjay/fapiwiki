============================================
FAPI WG Meeting Notes (2019-08-07) 
============================================
Date & Time: 2019-07-31 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
Attending:
--------------------
#. Nat Sakimura
#. Dima Postnikov
#. Rob Otto
#. Stuart Low
#. Torsten Lodderstedt 
#. Erick B Tedeschi
#. Joseph Heenan
#. Dave Tonge
#. Anthony Nadalin

Regrets: 
---------------------    
#. Anoop Saxena

Adoption of the Agenda (Nat)
==================================
* Added External Organizations

External Organizations
=============================
Australia
----------------
The callers discussed for about a half an hour on the diffs between FAPI etc. and the Australian standard draft CDS. 
The outcome of the discussion was that we probably need to understand the reason for the deviations. 
As the next step, we decided to send a private email to the chair and other relevant people as the WG to them asking for the reasons for the deviations. 
Nat will create a google document for the draft letter and interested WG members are invited to comment on it. 
Please ping Nat to join the editing group. 

Pull requests 
=================
PR #131 first proposal to integrate JARM as equal option (Torsten)
---------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/131/first-proposal-to-integrate-jarm-as-equal/diff

Some concerns were raised for this pull request. Two of the main ones were: 

#. `code` being returned in the query parameter may not be desirable from security point of view; 
#. Too many optionalities in the response type. This causes multiplied number of test cases. 

For 1., Nat pointed out that ID Token leakage is a privacy issue but Authorization code leakage in our case is not a big problem as Authorization code in our case is sender constrained as there is no public client. 

For 2., Torsten agreed to reduce the optionality. 

There is a conflict right now and this also needs to be fixed. 

Torsten will fix the PR and ping the WG for the final review. 


PR #115 FAPI-R/RW: Bring clauses about acr inline with usage (Joseph)
--------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/115/fapi-r-rw-bring-clauses-about-acr-inline/diff

Everybody in the call agreed that this is good to go. Nat will merge the PR right after the call. 

PR #133 fapi-ciba: clarifications prior to id1 vote (Joseph)
------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/133/fapi-ciba-clarifications-prior-to-id1-vote/diff

The PR was approved and will be merged in right after the call. 

AOB
==========================
FAPI CIBA Implementer's Draft
-------------------------------
Pre-vote is starting but the official vote will only start next week. 

Next Call
-------------------------
* We will deal with: 

PR #134 FAPI-RW: Apply cipher restrictions to < TLS 1.3
* https://bitbucket.org/openid/fapi/pull-requests/134/

PR #129 First cut of an advice document
* https://bitbucket.org/openid/fapi/pull-requests/129/

PR #113 FAPI-R: Clarify authorization code reuse requirements
* https://bitbucket.org/openid/fapi/pull-requests/113/

and others. 

The meeting was adjourned at 15:02 UTC.