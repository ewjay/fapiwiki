============================================
FAPI WG Meeting Notes (2017-02-01)
============================================
Date & Time: 2017-02-01 15:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 00:00+1 JST)

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at ______ UTC. 

Roll Call
=============
* Present: 
* Regrets: 
* Guest: 

Adoption of the Agenda (Nat)
===============================


Implementer's draft Part 1 voting preparation (Nat)
====================================================
* Pre-voting possible. Please vote. 


Working Drafts
===================


Part 1: Read Only API Security Profile (Nat & Edmund)
-------------------------------------------------------------

* `Part 1: Read Only API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md 

Some issues reported last week (still within the public review period that ends on Feb. 2.) 

* #62: Scope is not specific enough
* #63: It does not state that x-fapi-customer-id is an http header parameter
* #64: "non monotonically increasing" does not cover all cases
* #65: user-agent header requirement is not a security feature
* #66: CustomerId == sub == x-fapi-customer-id: Should standardize as sub
* #67: CustomerId is not defined.
* #68: Privacy consideration should be talking about more specifics
* #69: Notes like this are strange “NOTE: Providing access to Javascript clients or not has different security properites.;”

Part 2: Read & Write API Security Profile (Nat & Edmund)
------------------------------------------------------------
* `Part 2: Read & Write API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md 

* Nat and Edmund have been adding previously identified requirements onto the drafts. 
* For request objects, it is currently referring the section 6 of OIDC, but if OAuth JAR emerges as RFC, we should use it instead. Nat is currently working on SECDIR comments in IETF for OAuth JAR and will be discussed at IESG on Feb. 3. 

Other Parts
-------------
    * Financial_API_WD_003.md Financial API - Part 3: Open Data API
    * Financial_API_WD_004.md Financial API - Part 4: Protected Data API and Schema - Read only
    * Financial_API_WD_005.md Financial API - Part 5: Protected Data API and Schema - Read and Write

External Orgs
==================

UK EBS (Dave)
-----------------

Denmark Banking Association(s) (Henrik)
------------------------------------------

Others
------------
* FS-ISAC DDA (Anoop)
* OFX (Anoop)
* JP Banking Association (Nat)
* Figo

AOB
========

Next Call (Atlantic)
--------------------------
* 2017-02-07 23:00 UTC
    (15:00 PDT, 23:00 UK, 00:00 Denmark, 08:00+1 JST)

The meeting adjourned at _______ UTC.