============================================
FAPI WG Meeting Notes (2018-01-23)
============================================
Date & Time: 2018-01-23 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:05 UTC. 

Roll Call
===========
* Attending: Nat, Dave, Edmund, Joseph, Bjorn, Tom
   * Guest: 
* Regrets: John, Anoop

Adoption of the Agenda (Nat)
==================================
* OAuth Question on the client id added. 


Upcoming Events
======================
Open Banking (Don)
---------------------
Workshop https://www.eventbrite.co.uk/e/openid-foundationopen-banking-implementation-entity-workshop-tickets-42005257857

Remote participation may be available

API Days (Nat)
-----------------
Nat will be attending to do presentation about FAPI and OpenBanking

Informal FAPI meeting
----------------------------
Monday afternoon in London. Location TBD. 
Nat will send out a message asking who is going to attend. 

Issues
=============
#129 TLS cipher restrictions should be relaxed for the authorise endpoint
-----------------------------------------------------------------------------
What is currently in the pull request seem to be a good text. 
If there is no objection, we should adopt it. 

ASK: Adopted the pull request. 

#127 CIBA: security issues
---------------------------------
Text for the security consideration was proposed. 
When the text is added, the ticket should be closed. 

Tom wanted it to be a requirement. 
Dave is going to put it as the requirement. 

Dave also has submitted it to be dealt at the OAuth security workshop in March. 

DISPOSITION: Adopted the proposed text. 

#116 CIBA - authentication methods and proof of possession
--------------------------------------------------------------
New text was provided. 
https://bitbucket.org/openid/fapi/diff/Financial_API_WD_CIBA.md?diff1=6ef7ed915782&diff2=cf71704c2d24aa59c06acc5a9294d9ab6876fb15&at=master

DISPOSITION: To close the ticket. 

#110 more definition of s_hash
-------------------------------------
Brian wants the behavior of the AS when `state` is not in the request to be specified. 
Nat suggested that `s_hash` must not be in the ID Token if the request did not have `state` specified. 

DISPOSITION: Proposal accepted. Nat to make a pull request. 

#114 Require state
------------------------
Linked to #110. 
Nat proposed to require `state` in pure OAuth, while making it optional for OIDC. 

DISPOSITION: Adopted the direction. 


#128 redirect_uri in url query vs request object
---------------------------------------------------
Pull request: 
https://bitbucket.org/openid/fapi/pull-requests/42/part-2-require-redirect_uri-to-be-inside/diff

zzz: client_id
---------------
Test suite always sends client id in the body. 


Implementer's Draft (Edmund)
--------------------------------
Waiting for the issues to be cleared. 


AOB
===========


Next Call (Atlantic)
-----------------------
The next call is scheduled to be in the Atlantic time zone. 

* The meeting was adjourned at 23:55 UTC.