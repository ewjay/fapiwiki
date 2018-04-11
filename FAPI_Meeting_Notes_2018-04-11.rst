============================================
FAPI WG Meeting Notes (2018-04-11)
============================================
Date & Time: 2018-04-11 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: 
   * Guest: 
* Regrets:  

Adoption of the Agenda (Nat)
==================================
* 

External Organizations
=========================

ISO/TC68 (Dave)
--------------------

Open Banking (Joseph)
-------------------------
* Yolt announcement: https://www.yolt.com/blog/2018-03-15/open-banking-update-weve-officially-connected-to-three-banks
* Conformance suite is now open source. 

OpenAPI (Nat)
----------------
* There was a call with the OpenAPI Foundation last Friday. It is heading in a good direction, e.g., supporting signed JWT response, etc. Nat will send a link to it in the mail list. If you are interested, please get involved. 

Events
==========
IIW (John)
--------------
* John is going to present FAPI in the pre-IIW OpenID Workshop. 
* Please send the presentation ideas to the list to help John. 

Pull Requests
================
* https://bitbucket.org/openid/fapi/pull-requests/


Issues
===========
* https://bitbucket.org/openid/fapi/issues?status=new&status=open
* Talked about #135 at some length. It looks like a core problem is how to express the needs for "meaningful consent" at the authorization server. Unlike in the regular OAuth's case, FAPI Part 2 allows the client to be authenticated via a digital signature, so the authorization server can actually show who is requesting what to the end user. However, the actual user interface for showing that information is out of scope for OpenID Connect Core. We might want to come up with a text that expresses the need for the "meaningful consent." 



AOB
===========
* There seem to be some demands for FAL3 authentication in the US now, as a part of Fedramp program. 
* EAP WG has a draft that deals with it and it may go to the implementer's draft vote in the near future. If you are interested, please join the WG and submit your comments. 


Next Call
-----------------------
The next call is scheduled to be in the Pacific time zone. 

* The meeting was adjourned at 15:01 UTC.