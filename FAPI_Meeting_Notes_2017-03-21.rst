============================================
FAPI WG Meeting Notes (2017-03-21)
============================================
Date & Time: 2017-03-21 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:10 UTC. 


Roll Call
===========
* Attending: John, Nat, Edmund, Tom, Henrik, Joseph
* Regrets: Tony, ANoop, Sascha


Adoption of the Agenda (Nat)
==================================
* Adopted as presented. 

Drafts
==========

Part 1: Read Only API Security Profile
---------------------------------------------

Issue #76 - Can vs May
~~~~~~~~~~~~~~~~~~~~~~~~~~
* Accepted changes. 

Part 2: Read & Write API Security Profile
-------------------------------------------------

PoP other than Token Binding - https://tools.ietf.org/html/draft-sakimura-oauth-jpop-01
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* We need both raw and artifact version of JPOP token
* Artifact version needs to be introspected. 
* Need new claim "jty": JPOP / JPOPA (for artifact)
* Resources discovery: abstract resource identifier. 
* AT needs to include `aud`. 
* Resource server returns the header that includes Resoruce server metada URI. 
* Resource server metadata format needs to be defined. Mike had one in the past. 
    * https://tools.ietf.org/html/draft-jones-oauth-resource-metadata-01
        * it uses .well-known, which is not good. 
* Security consideration on TLS binding on the server side if the server has access to TLS info. 

Other issues in Bitbucket
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* #77, #78: Edmund created a branch for discussion. It is capturing the good practice for authentication protocols. 
* Lengthy discussion followed. While this method leaks less information to attackers, for the know attacks, enforcing JWT client authentication seems adequate. For FAPI purposes, we probably do not need it while it would make a good discussion point in the July OAuth Security workshop in Zurich. 
    * The difference in the security characteristics for including client intent in the authorization request or not is whether Authorization Server can detect badly configured client or not. 


Part 3: Open Data API
----------------------
* Skipped

Part 4: Protected Data API and Schema - Read only
--------------------------------------------------------
* Skipped

Part 5: Protected Data API and Schema - Read and Write
-----------------------------------------------------------
* Skipped

External Orgs
================

UK OBS (Dave, John)
-------------------------
* Not recorded

Others
------------
* IETF is wanting another chair for OAuth WG, who knows the administrative process. 

AOB
===========
Next Call (Atlantic)
-----------------------
* Question was raised whether we want to peg the time to UTC or to move around with Daylight saving time. 
* Opinion was split in the call. Nat will ask about it in the list as well.