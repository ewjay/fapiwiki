===========================================
FAPI WG Meeting Notes (2019-04-16) 
===========================================
Date & Time: 2019-04-16 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862


.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 23:08 UTC. 

Roll Call (Anoop)
=====================
* Attending: Anoop, Nat, Edmund  
* Guests: 
* Regrets: 

Adoption of the Agenda (Anoop)
==================================
* Adopted as is. 


External Organizations (Anoop)
==============================
OBIE: The use of sub and the token refresh (Anoop)
-----------------------------------------------------
Currently, Open Banking UK is filling ID Token's `sub` with the intent ID, which is of course ephemeral. 
Anoop had a question on the impact of this onto the access token refresh. 

A user may have multiple accounts at a bank and at the time of the user re-authentication, he may choose another account then he has used previously, which results in a new access token that is associated with a different account. If ASPSP can accept `id_token_hint` this problem can be mitigated somewhat but Anoop was not sure of the status. 

Nat suggested Anoop create a ticket on this issue on the FAPI issues tracker. 

STET and FAPI (Anoop)
-----------------------
Intuit has started working on the STET integration and asked STET. 
It is good to see that they are moving to OAuth rather than a proprietary one but the course is not clear if they are moving to FAPI was they start the Read & Write API. (Currently, they seem to be doing Read Only.) 

Anoop believes that we should be pushing STET more towards the direction. 
He will get in touch with Dave Tonge and Torsten Lodderstedt on this issue. 

AMEX (Anoop)
--------------
AMEX is using OAuth 1.0a HMAC Token right now. 
Anoop is trying to pursuade them to switch to FAPI and asked Nat 
what are the advantages of FAPI over OAuth 1.0a HMAC Token. 

Nat pointed out several of them randomly as: 

1. FAPI has a formal security proof so it is future unknown attack proof while OAuth 1.0a HMAC Token is not. 
2. FAPI MTLS has bindings to TLS Channels while OAuth 1.0a HMAC is purely application layer. 
3. FAPI is public key crypto based so it has "non-repudiation" property while OAuth 1.0a HMAC does not. 
4. OAuth 1.0a is obsoleted long time ago. 
5. FAPI has a conformance test suite including many negative tests to test the security of the implementations. 


Data Schema Comparison (Anoop)
===============================
Anoop has been comparing data schema between FDX (DDA) and UK Open Banking, STET, and Berlin Group. 

FDX's schema covers wide range of financial instruments and data while OBIE, STET, Berlin Group schema seem to be limited to basinc accounts. This is especially true for investemnts. Fortunately, in the U.S., since banks has been supproting OFX that also has a lot more data fields, FDX fields are getting filled. 

It was agreed that we should identify the gap and start proposing the possible remedy for them before everyone gets fragmented. 

Next Call
-----------------------
Next call will be an Atlantic Call. 
Next Pacific call will be in two weeks. 

* The meeting was adjourned at 23:48 UTC.