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
* Attending: 
* Regrets: 


Adoption of the Agenda (Nat)
==================================
* 

JPoP @ IETF report (Nat)
==========================
* issue #75
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

Issues 
========
* #79
* #81
* #72, #73, #74, #80, #82, #83

External Orgs
================

UK OBS (Dave)
-------------------------
* 

ISO/TC68 (Nat)
-------------------

Others
------------
* 

AOB
===========
Next Call (Pacific)
-----------------------