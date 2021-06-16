============================================
FAPI WG Meeting Notes (2021-06-16) 
============================================
* Date & Time: 2020-06-16 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-06-02_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
* Attending: Nat, Mike L, Dave, Jacob, Lukasz, Chris Wood, Dima, Torsten, Francis, Takahiko, Travis, Ralph, Brian, Stuart, Fiona Hamilton, Travis, Stephane Durand, Joseph, Danillo Branco, Ali, Filip, Kosuke
* Regrets:
* Guest: 


Adoption of Agenda (Nat)
===========================
* Adding Grant Management related issues and PRs. 

Events (Nat)
======================
Identiverse (Brian/Joseph)
-----------------------------------



External Organizations (Nat)
================================
IETF/OAuth
------------------------
RAR is in the WG final call. 
Please review. 

Australia (Mike L.)
----------------------
* Coordinating follow up call with CDR. 

* RP security issues. They should also comply to FAPI. 
* Some RPs are very lax in security, e.g., Cross Browser Payment Initiation Attack. 

Brazil (Mike L.) 
------------------------
* FAPI Conformance test is underway. 
* OP test, DCR test online. 
* RP test is under development. Beta version early next week. 

Berlin Group (Francis)
---------------------------
* No major news. 

India (Nat)
---------------
* 

MENA (Ali/Gail)
-----------------------
* June 22: 200 banks in the region
* July 12: Virtual board meeting addressing 20 regulatory bodies in the area. 
* July 2nd week: Innovation week hosted by DIFC. Security standard for Open Banking. 

UK (Fiona)
--------------------
* Updating conformance tool. July release will support ver. 3.0 which includes variable recurring payment. 
* Working on 3.1.9 (Sept.) 
* RC1 of extended customer attribute. 

US/FDX (Gail)
-------------
* T&A being worked on. 

PRs (Stuart/Dave)
===================
PR 268 Minor changes to ensure xml2rfc compilation with backlink checking
---------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/268

Approved and Merged. 

PR 266: Introduce replace action
---------------------------------------
https://bitbucket.org/openid/fapi/pull-requests/266

Merged

PR 275: Introduce backoff support for query
----------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/275

There are polling in grant management. 

It was pointed out that more context needs to be added. 

PR 274: Introduce require metadata item
-----------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/274

This helps with the transition. BR follows a similar pattern. 

ACT: Merge this PR and open a follow up one. 

PR 273: Add draft note about public clients
----------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/273

ACT: Torsten will propose a text. 

PR 270: Compilable deployment advice updates
-----------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/270

ACT: Stuart to fix the PR. 

PR 
* https://bitbucket.org/openid/fapi/pull-requests/269

WG Last Call on Grant Management (Dima)
===========================================
Editors requested the start of the WG Last Call with particular reference to the following issues. 

* https://bitbucket.org/openid/fapi/issues/287/document-the-impact-of-grant-changes-on
* https://bitbucket.org/openid/fapi/issues/377/grant_id_required-client-metadata 
* https://bitbucket.org/openid/fapi/issues/316/grant-management-and-incremental 
* https://bitbucket.org/openid/fapi/issues/384/sever-metadata 
* https://bitbucket.org/openid/fapi/issues/374/grant-management-query-response 
* https://bitbucket.org/openid/fapi/issues/422/grant-create-and-access-methods 
* https://bitbucket.org/openid/fapi/issues/423/refresh-token-used-as-bearer-token-for

Dima will draft some notes to go with it and send them to the Co-chairs tomorrow. 

Issues (Dave)
=================
#412 FAPI 2.0 - Hard requirement to support Grant Management Requirement
------------------------------------------------------------------------------
The Charter issue was pointed out and need to be discussed. 
We only had two minutes for this topic and was not enough so it will be discussed in the next call. 


AOB
=======
* Next call will reserve some time for issues #412 and #416

The call adjourned at 15:02 UTC




Chat Log
----------

23:05Filip Skokan (Auth0) to Everyone
:wave: apologies for being late

23:26Don Thibeau to Everyone
I will be representing the OpenID Foundation in the June event Ali references and will reference Financial-Grade APIs and eky

23:29Takahiko Kawasaki (Authlete) to Everyone
2nd Open Banking MENA Digi-Conference (22 June 2021) https://openbanking.gmevents.ae/

23:30Travis Spencer (Curity) to Everyone
What Brazil related tests were coming on the 28th?

23:30Travis Spencer (Curity) to Everyone
DCR?

23:30Gail Hodges (OIDF, she/her) to Everyone
Sorry no one could hear me on the voiceline.

23:32Takahiko Kawasaki (Authlete) to Everyone
Open Banking Forum (12-13 July 2021) https://openbankingboardroom.com/

23:33Stuart Low to Everyone
https://bitbucket.org/openid/fapi/pull-requests/268

23:33Joseph Heenan (Authlete / OpenID Foundation) to Everyone
Travis: The Brazil Profile tests went into beta on Friday (FAPI OP and FAPI OP DCR), they're in a test/enhance/fix phase right now, and the certification program launches on 28th on the same day the tests come out of beta.

23:34Stuart Low to Everyone
https://bitbucket.org/openid/fapi/pull-requests/266

23:35Travis Spencer (Curity) to Everyone
ah, I see @josheph

23:35Ali Adnan (Authlete) to Everyone
https://www.difc.ae/events/innovation-month/

23:35Stuart Low to Everyone
https://bitbucket.org/openid/fapi/pull-requests/275

23:42Stuart Low to Everyone
https://bitbucket.org/openid/fapi/pull-requests/274

23:46Stuart Low to Everyone
https://bitbucket.org/openid/fapi/pull-requests/266

23:48Stuart Low to Everyone
https://bitbucket.org/openid/fapi/pull-requests/273

23:50Stuart Low to Everyone
https://bitbucket.org/openid/fapi/pull-requests/270

23:51Stuart Low to Everyone
https://bitbucket.org/openid/fapi/pull-requests/269

23:52Francis Pouatcha (adorsys) to Everyone
Have to drop. Bye...

23:53Dima Postnikov to Everyone
https://bitbucket.org/openid/fapi/issues/287/document-the-impact-of-grant-changes-on https://bitbucket.org/openid/fapi/issues/377/grant_id_required-client-metadata https://bitbucket.org/openid/fapi/issues/316/grant-management-and-incremental https://bitbucket.org/openid/fapi/issues/384/sever-metadata https://bitbucket.org/openid/fapi/issues/374/grant-management-query-response https://bitbucket.org/openid/fapi/issues/422/grant-create-and-access-methods https://bitbucket.org/openid/fapi/issues/423/refresh-token-used-as-bearer-token-for

23:53Ralph Bragg to Everyone
Bye

23:55Gail Hodges (OIDF, she/her) to Everyone
Bye

23:59Ralph Bragg to Everyone
https://openid.net/wg/fapi/charter/

23:59Ralph Bragg to Everyone
enable applications to utilize the data stored in the financial account,
enable applications to interact with the financial account, and 
enable users to control the security and privacy settings.