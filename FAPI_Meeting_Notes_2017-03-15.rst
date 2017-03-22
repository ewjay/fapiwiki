============================================
FAPI WG Meeting Notes (2017-03-15)
============================================
Date & Time: 2017-03-15 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: Nat, John, Tom, Bjorn, Joseph, Dave. 
* Regrets: Henrik
* Guest: 

Adoption of the Agenda (Dave)
===============================
* Adopted as is

Drafts
===================
Part 1: Read Only API Security Profile (Dave)
-------------------------------------------------------------
* `Part 1: Read Only API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md 

`Can vs May <https://bitbucket.org/openid/fapi/issues/76/meaning-of-can>`
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* Sacha has opened a pull request
* Consensus to change "can" to "may" 

Part 2: Read & Write API Security Profile (John, Nat & Dave)
------------------------------------------------------------
* `Part 2: Read & Write API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md 

PoP other than Token Binding
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* WG discussed new draft for `JWT Pop Token Usage <https://tools.ietf.org/html/draft-sakimura-oauth-jpop-01>`
* Discussion around the use of "Common Name" rather than "Distinguished Name"
* Dave to circulate with UK Open Banking for feedback
* WG discussed whether there should be "mandatory to implement" sections of the spec
* WG decided that it was important that the client only need to support a small number of PoP methods - even if AS supported many
* WG discussed how access tokens would be presented - Bearer vs Jpop. Draft to be reviewed to ensure this is clear. Feedback requested on feasibility of support within time constraints.

Hybrid flow mandated?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* WG discussed Issue #72
* WG agreed that where possible the implementation must support token binding and if not supported must require hybrid flow 
* Draft to be adjusted
* 

Part 3: Open Data API
----------------------------
* N/A

Part 4: Protected Data API and Schema - Read only
---------------------------------------------------------------
* N/A

Part 5: Protected Data API and Schema - Read and Write
----------------------------------------------------------------
* N/A

External Orgs
==================

UK OBS (Dave)
------------------
* FAPI Spec is in strong consideration
* Need to work closely to ensure that the spec balances security requirements and real world implementation issues

Others
------------

Followings were not discussed. 

* No other external orgs were discussed

AOB
========

Next Call (Atlantic)
--------------------------
* Next call is Pacific shift and is in next week. 
  
The meeting adjourned at 15:01 UTC.