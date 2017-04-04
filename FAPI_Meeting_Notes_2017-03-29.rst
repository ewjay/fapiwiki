============================================
FAPI WG Meeting Notes (2017-03-29)
============================================
Date & Time: 2017-03-29 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:10 UTC. 


Roll Call
===========
* Attending: Nat, Bjorn, Dave, Joseph, Sasha, Henrik 

* Regrets: John, Tony, Anoop

Adoption of the Agenda (Nat)
==================================
* Adopted as is

JPoP @ IETF report (Nat)
==========================
* issue #75 - Support other method of HoK than TOKB


* Reviewed in the Monday session. 
* Great desire to do only one way. 
* AdHoc F2F among people interested on Tuesday
* Just go with x5t#s256 cnf method
    * This means we do not need Signature Method anymore. 
* Merge with X.509 client authentication draft
    * Brian Campbell is working on it right now to be reviewed in Friday session. 
* Basically, what the token endpoint would be doing is: 
    * Get the content of SSL_CLIENT_CERT, which is a PEM version of the client cert. 
    * Convert it to DER and take sha256. 
    * Associate it with the access token. (Format is proprietary to the authorization server and the resource) 
    * Return the access token. 
* Then, the client just sends the access token like bearer token but over the client cert authenticated channel. 
* Upon receipt of it, the resource gets SSL_CLIENT_CERT and calculates x5t#s256 and compares it with the x5t#s256 that is associated with the access token. 
* We could have done it with SSL_CLIENT_M_SERIAL and SSL_CLIENT_I_DN but this will not be applicable when self issued certificates are to be used e.g., the mobile applications. x5t#s256 will be more robust. 
* Q. Would we get a push back from OBS that we do not use DN?
    DN can be spoofed.
* Q. What about using public key hash instead of client certificate hash? Public key hash won't change even if the certificate changes.
    May not be so easy to just extract the public key from the cert. Certificate has a validation path that can be used for non-repudiation.

Issues 
========

#79 - Part 1: issues with x-fapi-customer-last-logged-time header
-------------------------------------------------------------
* Issue #79
* There is some confusion in regards to the "time" part of the header name.
* Some want it to end with 'date' instead.
* Some want to drop the 'customer' part.
* The group decided to use x-fapi-auth-date.
* The suggestion will be sent to the mailing list for feedback.


#81 - Identify user associated to the access token
-------------------------------------------------------------
* Issue #81 
* The word 'user' may be too specific.
* In some places, it could be the 'subject', 'principal', or 'entity' of the Access Token
* Will try to replace with 'entity' to see it will work


#72 - Spec not clear as to which auth flows are supported
-------------------------------------------------------------
* Issue #72
* Need to be more explicit
* Nat said Hybrid flow but John said that Hybrid may not be  used in some cases
* Dave will create new text to clarify


#73 - Spec says Authorization Server shall support both public and confidential clients
-------------------------------------------------------------
* Issue #73
* Nat has already made changes to that support for both is optional
* Issue is closed

#74 - Write spec should only support confidential clients
-------------------------------------------------------------
* Issue #74
* It depends on use case
    * It can be a private API used by the FI's own clients
    * It can be public API used by third parties
* Dave will create text to be inserted into Introduction to highlight use cases.


#80 - Token Response
-------------------------------------------------------------
* Issue #80
* The text is not clear whether the response must conform to RFC 6749
* It's agreed that the response MUST conform to RFC 6749
* Pam will create new text for pull request

#82 - Strict Access Control to logs
-------------------------------------------------------------
* Issue #82
* It's confusing whether the word 'should' means 'MUST'
* It is only recommendation language.
* PAM will create alternative text and create pull request

#83 - Support for GET
-------------------------------------------------------------
* Issue #83
* It points to the whole RFC2616 spec and not a specific section
* It is confusing whether read only requests can only support the GET verb
* The intention is that GET verb MUST be supported and others MAY be supported
* Pam will add text suggestion and create pull request




External Orgs
================

UK OBS (Dave)
-------------------------
* UK is working through use cases
* Not sure if OpenID Connect will be anointed standard in FAPI. Need to decide how strongly we should fight for this.
* OpenID is not the only solution.
* Not all authorization requests are based on identity, so identity is not that critical in some calls.
* Assertions regarding the authentication context and all parties involved in the request for the access token are much more critical for a high assurance framework
* Need to make the point that the assertions are absolute for accountability and risk mitigation
* For the Read/Write profile, we need to explicitly require c_hash and at_hash in ID Token
* Nat is also suggesting to add a s_hash for 'state' parameter hash
* Discussion to be continued in mailing list

ISO/TC68 (Nat)
-------------------
* Nat is crafting the liaison request to TC 68 
* Nat will be meeting to Ograssi to fine tune the request for the Brazil meeting
* Nat will also be meeting with the Secretariat of TC 68 when he gets back to Japan
* If FAPI gets adopted by TC68, that FAPI specs will get an ISO number

Others
------------
* No other issues

AOB
===========
Next Call (Pacific)
-----------------------