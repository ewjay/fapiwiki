============================================
FAPI WG Meeting Notes (2019-09-25) 
============================================
Date & Time: 2019-09-25 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
Attending:
--------------------
#. Nat
#. Brian
#. Dima
#. Joseph
#. Kosuke
#. Ralph
#. Stuart
#. Dave
#. Bjorn

Regrets: 
---------------------    

Adoption of the Agenda (Nat)
==================================


External Organizations
=======================

ISO/TC68/SC2/SG2 Security aspects of bar code payment (Nat)
--------------------------------------------------------------
Their first meeting is scheduled to be tomorrow. Nat did not see any WG members to be in the roaster but suggested that somebody working on CIBA may be interested to it that they can join the group through their respective National Bodies. Alternatively, FAPI WG could open a liaison with this new group but that will take some time before getting approved. 

The group's web page is here: 

* https://www.iso.org/committee/49670.html

Australia (Dima/Stuart)
--------------------------------------
New consent request is going around. Folks that are interested should weigh-in. 

* https://github.com/ConsumerDataStandardsAustralia/standards/issues/85

Certification team compiled the document listing the differences between the current FAPI specs and Australia. 

* https://docs.google.com/document/d/1_reJVmWSxIyeKm2yGFN2cAP9BcWYsT7XosNbLYk4D0Y/edit

Some changes previously noted seems to be fixed. There are changes that may cause interoperability issues however and we need to understand why they are made. For example, requiring that `iss` SHALL NOT be in the request object. The rationale seems to be save something like 20 bytes in the request object for the concern of the request object size but if the size is the concern, using request_uri is a preferred method in FAPI. In any case, we are just guessing the rationale and that is not really productive so we should clarify those in the forthcoming call. 

Related to it, Stuart asked about the `Mix-up Attack mitigation <https://openid.net/specs/openid-financial-api-part-2.html#identity-provider-idp-mix-up-attack>`_ and the relationship between `client_id` and `iss`. Nat answered the question. 

Dima also pointed out that another topic is being raised in CDR. People are asked to read it. 

* https://cdr-register.github.io/register/#client-registration


UK Open Banking (Ralph)
----------------------------
Interest on CIBA building up. 
There was a hack-a-thon at SIBOS. 



Pull Requests
=================

PR #142 Refresh Token (Joseph)
---------------------------------
Joseph proposed a new wording on the call and there was a friendly amendment on it by Brian. 
Joseph is going to make a modified PR based on it so that people can review the concrete wording. 

Issues
================

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

AOB
==========================

The meeting was adjourned at 14:58 UTC.