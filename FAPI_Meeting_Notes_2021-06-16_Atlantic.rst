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

FIDO Plenary
-----------------------------------
* Today
* FAPI was presented.

External Organizations (Nat)
================================
IETF/OAuth
------------------------
RAR is in the WG final call. 
Please review. 

Australia (Mike L.)
----------------------
* Coordinating follow up call with CDR including Ron Deacon. 
* A lot of TPP are also data providers and are not following good security practices in how to integrate with third parties.
* RP security issues. They should also comply to FAPI.
* Some RPs are very lax in security, e.g., Many TPPs in UK are susceptible to Cross Browser Payment Initiation Attack.
* It’s more of a regulator issue.
* Standards may not be the problem but TPPs lack of conformance and adherence to standards are.
* OB’s arrangement defined by the CMA order, can give mandates to the 9 biggest banks. For everyone else, it can only provide best practice guidelines, etc.
* New CMA consultation regarding the future of OBIE, expect decision within next week or two
* Could ask banks to take responsibility and plug the hole.
* Dave and Fiona to arrange discussion within  TDA 

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
* Nat was contacted by iSPIRT who is working on IndiaStack
* They had questions regarding OIDC, FAPI, etc..
* They are considering consumer data cross border exchange with Australia, UK, and others
* Now, they are looking at Grant Management and other specs


MENA (Ali/Gail)
-----------------------
* June 22: 200 banks in the region, OB panel discussion regarding security protocols
* July 12: Virtual board meeting addressing 20 regulatory bodies in the area. 
* July 2nd week: Innovation week hosted by Dubai International Financial Center (DIFC). 

  * Security standard for Open Banking APIs.

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

* Related to rewording the security considerations when using replace on grant management
* removes the MUST on the revocation and adopts revoking relevant tokens by an out of band means.
* Merged

PR 275: Introduce backoff support for query
----------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/275
* Copy and paste from CIBA with relation to retry codes for HTTP
* There are polling in grant management, but no specific polling terminology.
* It’s questionable whether we should add standard HTTP best practices everywhere.
* It was pointed out that more context needs to be added. 

PR 274: Introduce require metadata item
-----------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/274

This helps with the transition. BR follows a similar pattern. 

ACT: Merge this PR and open a follow up one. 

PR 273: Add draft note about public clients
----------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/273
* Removes explicit requirement of confidential client management but leaves a modified version of the draft note that the spec expects confidential clients but acknowledges potential for use in public client contexts. 
* Haven’t done security threat analysis of someone impersonating a public client and utilizing grants and getting tokens without consent.
* ACT: Torsten will propose a text. 

PR 270: Compilable deployment advice updates
-----------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/270
* Nat added comments related to compliance to ISO Directive Part 2. 
* ACT: Stuart to fix the PR. 

PR 269: Compilable http signing, a lot of rejigging to get references right
-----------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/269
* Made changes to HTTP Signing to  make it compilable, needs review
* Stuart to make HTML results and distribute to authors.


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