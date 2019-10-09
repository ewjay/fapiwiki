============================================
FAPI WG Meeting Notes (2019-10-09) 
============================================
Date & Time: 2019-10-09 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
Attending:
--------------------
#. Bjorn
#. Dve
#. Nat
#. Brian
#. Kosuke
#. Torsten
Joseph

Regrets: 
---------------------    

Adoption of the Agenda (Nat)
==================================


Planning for HTTP Signature Session (Dave)
===========================================
* Anders, Manu, John, Mike Jones, Annabel, Ralph need to be there for the special call. 
A doodle poll to be created. 

Issues
================

#271: Rename and adjust FAPI profiles (Torsten)
-------------------------------------------------



#270 JARM (Joseph)
--------------------
In the non-openid cases where scope does not include openid, "nonce" does not make sense. 
However, just requiring "state" is likely to be understating what the clients need to be doing to thwart CSRF etc. 
Callers agreed that requiring PKCE may be a better way to go. 
Folks should comment on the ticket of their opinions. 


#263 Refresh Token (Joseph)
-----------------------------
See PR #142

#251 refresh token expiry time (Joseph)
---------------------------------------------
There seem to be two ways of returning it and UK and Australia are going to a different direction. 
It may be interesting to find out what is the current majority practice by taking a survey at IIW. 

Pull Requests
=================

PR #142 Refresh Token (Joseph)
---------------------------------
Joseph proposed a new wording on the call and there was a friendly amendment on it by Brian. 
Joseph is going to make a modified PR based on it so that people can review the concrete wording. 



AOB
==========================

The meeting was adjourned at 14:58 UTC.