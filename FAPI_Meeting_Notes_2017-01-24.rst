============================================
FAPI WG Meeting Notes (2017-01-24)
============================================
Date & Time: 2017-01-24 23:00 UTC 
    (15:00 PDT, 23:00 UK, 00:00 Denmark, 08:00+1 JST)

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:05 UTC. 

Roll Call
=============
* Present: Nat, Anoop, Edmund, Henrik
* Regrets: Tony, John, Sascha
* Guest: 

Adoption of the Agenda (Nat)
===============================
* Adopted ammended: 
    * Skipping Events as we are missing John. 
    * New use case discussion added. 

Implementer's draft Part 1 voting preparation (Nat)
====================================================
* Voting announcement has been made. 
* Details can be found at: http://openid.net/2017/01/20/notice-of-vote-for-implementers-draft-of-financial-api-part-1-read-only-api-security-profile/
* Please prepare for voting: 
    * check if you can login etc. 

Working Drafts
===================

    * Financial_API_WD_001.md Financial API - Part 1: Read Only API Security Profile
    * Financial_API_WD_002.md Financial API - Part 2: Read and Write API Security Profile
    * Financial_API_WD_003.md Financial API - Part 3: Open Data API
    * Financial_API_WD_004.md Financial API - Part 4: Protected Data API and Schema - Read only
    * Financial_API_WD_005.md Financial API - Part 5: Protected Data API and Schema - Read and Write

Part 1: Read Only API Security Profile (Nat & Edmund)
-------------------------------------------------------------
* Edmund applied all the editorial bug fixes collected during the review period. 
* Edmund is also working on the Pandoc HTML template and .docx template so that 
  it will look more like OIDF specs for HTML and ISO specs for .docx. 

Part 2: Read & Write API Security Profile (Nat & Edmund)
------------------------------------------------------------
* `Part 2: Read & Write API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md 

* Nat has started to add previously identified requirements onto the drafts. 
* For request objects, it is currently referring the section 6 of OIDC, but if OAuth JAR emerges as RFC, we should use it instead. Nat is currently working on SECDIR comments in IETF for OAuth JAR and will be discussed at IESG on Feb. 3. 

Issues (Nat)
=========================

* No new issues. 


External Orgs
==================

FS-ISAC DDA (Anoop)
--------------------
* For sometime, banks were meeting within themselves to work out the charter. Now they are reconvening the working group and intuit is going to provide the status and advise on how to plug-in OpenID. 

    * Nat will follow up with Bob Blakley at Citi. 
         * Citi participant at DDA: Clint Stephan, Security Group. 
    * Tony will follow up with EMV. 

OFX (Anoop)
------------------
* As FS-ISAC started moving along, OFX should also be aligned with them. 

JP Banking Association (Nat)
-----------------------------
* Nat and JP Fintech Association visited the JP Banking Association. 
* JP Banking association is in the process of creation of their API recommendations. The secretariat believes that it should adopt a standard created by experts so adopting FAPI Part 1 and Part 2 seems to be the course. 
* For the data schema part, they were pessimistic on the possibility of them being able to come up with a single schema, let alone adopting DDA etc., but Fintech Association advised that they should at least try to. From the point of view of a fintehc company operating worldwide, each countries creating their own schema means they have to prepare for over 200 schemas and that is bad enough. If each countries start to have multiple schemas, that will multiply the "badness". 

New Use Cases Discussion (Anoop) 
==========================================
* Some use-cases where OAuth has shortcomings were identified. 

#. Left-out session problems
#. Adding two accounts from the same bank to a Fintech software
 
Nat is going to try to document them by the EOD tomorrow based on 
Anoop's description and post it to the list after Anoop's review. 

AOB
========

Next Call (Atlantic)
--------------------------
* 2017-01-31 15:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 00:00+1 JST)

The meeting adjourned at 23:59 UTC.