============================================
FAPI WG Meeting Notes (2017-03-01)
============================================
Date & Time: 2017-03-01 15:00 UTC
    (15:00 PDT, 23:00 UK, 00:00 Denmark, 08:00+1 JST)

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:10 UTC. 

Roll Call
=============
* Present: 
* Regrets:
* Guest: 

Adoption of the Agenda (Nat)
===============================
*

External Orgs
==================

UK OBS (Dave)
---------------

DK Banking Association(s) (Henrik)
------------------------------------------
* No news. 


Others
------------
* FS-ISAC DDA (Anoop)
* OFX (Anoop)
* ISO/TC68
* Figo
* JP Banking Association (Nat)

iGov Presentation (John)
============================

Modrna Presentation (John)
============================

Implementer's draft  (Nat)
========================================
Part 1: Read Only API Security Profile (Nat)
-------------------------------------------------------------

* `Part 1: Read Only API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md 

* Went through with 50 votes. Only 1 objection. 
* Now need implementations - NRI's STAR system is nearly compatible yet not quite. CA will look into it as well. 

Working Drafts
===================

Part 2: Read & Write API Security Profile (Nat & Edmund)
------------------------------------------------------------
* `Part 2: Read & Write API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md 

What shall we token bind? 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The WG group discussed what needs to be token bound. 
If the server and the client supports token binding, then it should token bind refresh token and access token. 

Question: Shall we token bind `code` as well? 

Nat asked John to provide an example of token binding messages, which are not in the token binding specs. 
John agreed. 

Would there be other options? 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Yes. We will still have mutual TLS auth available. 
Token Binding may take longer time to get implemented. 
Sascha expressed that something that can be completely application layer is easier to implement. 
Nat expressed that he needs something that API GW vendors can support. 
Sascha agreed to look into the matter and report back on the token binding support and alternatives. 

Authentication Requirement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
WG discussed what format shall be used to express the authentication requirement. 
John pointed out that iGov is coming up with vectors of trust expression. 
Nat pointed out that it would be best to align and asked John to make a presentation 
on iGov decision next week. John agreed. 

Always Request Object? 
~~~~~~~~~~~~~~~~~~~~~~~~
There can be two types of interactions with the user. 

* type 1: The client makes the "write" request (e.g., initiate payment) in the authorization request to get user authorization. This is a typical case in many of the payment schemes. 
* type 2: The client makes the "write" request to a specialized API so that the API can send the user notification and get authorization. This is something Modrna is working on. 

In type 1 case, authorization request should be signature protected: i.e, has to be a request object, otherwise it may be tampered in browser. 

In type 2 case, there is no authorization request involved but some other API calls 
(Editors note: which again may be needed to be signature protected for the recording purposes etc.)

Nat asked John to make the presentation on Modrna user questioning API next week. John agreed.  


Part 3: Open Data API
----------------------------
* Skipped

Part 4: Protected Data API and Schema - Read only (Sascha)
---------------------------------------------------------------
* Skipped

Part 5: Protected Data API and Schema - Read and Write
----------------------------------------------------------------
* Skipped


AOB
========

Next Call (Pacific)
--------------------------
* Next call is Pacific shift and is in next week. Please consult the WG calendar for the date and time. 

The meeting adjourned at 00:02 UTC.