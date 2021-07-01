============================================
FAPI WG Meeting Notes (2021-06-30) 
============================================
* Date & Time: 2020-06-30 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-06-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
* Attending: Nat, Filip, Daniel, Kosuke, Stuart, Joseph, Craig Borysowich, Brian, Lukasz, Don, Travis, Gail, Takahiko, Dima, Ralph, Mark
* Regrets: Dave
* Guest: 


Adoption of Agenda (Nat)
===========================
* Added Certification. 

Events (Nat)
======================
Identiverse
------------------------------
* unofficial @identiverse
 '21 photo collection is now officially available https://flickr.com/photos/brian-d-campbell/albums/72157719477514466 #dentiverse

FAPI Workshop hosted by Curity
---------------------------------
* August 24, 2021
* https://curity.io/resources/webinars/financial-grade-apis-now-and-in-the-future

BGIN Block #3
------------------
* 6/29-7/1
* https://bgin-global.org/block_3/
* Some discussions for DID today

External Organizations (Nat)
================================
Australia (Gail/Dima)
------------------------------------
Chatted with ACCC on regulatory side. 

* Interested in exploring making use of certification. (CommonWealth and NAB completed certification)
* Doing due diligence to adopt certification. 
* Openness towards RP tests. 
* Potential for direct funding for developing AU test. 

* July 1 deadline. 19 Brands need to be compliant. (=13 legal entities) Data Holders. 

  * Some didn’t make the deadline

New Zealand (Ralph)
---------------------
* NZ standards copy the UK standards
* Lead developer, Gavin Wong did most of UK standards
* NZ and Australia are still at Implementer’s Draft 2
* Decision proposal 182 asking the ecosystem what the CDR should be doing going forward in regards to FAPI2, Grant Management, etc.
* Broad alignment towards adopting FAPI 2, Rich Authorization and Grant Management


Brazil (Gail/Joseph)
---------------------
* First wave of 26 entities engaging in certification
* July 15 deadline for 11? banks. 
* Govt contemplating RP tests as well. “Almost certainly” will be required for Phase 3 Payments (end of Sept) for TPPs. 
* BR certification is fully live. 
* Main RPs are banks. 
* Open Banking Brazil’s Adoption of Financial-grade API (FAPI) & FAPI Certification https://openid.net/2021/06/30/open-banking-brazils-adoption-of-financial-grade-api-fapi-fapi-certification/

Berlin Group 
-------------------
* Will leverage EIC and workshops to engage Berlin Group and others
* Good news for Berlin Group. We are coming forward with the setup of the joint subcommittee (FAPI / BG). The suggestion went positive through the Berlin Group Task Force approval and Bruno is preparing feedback for FAPI WG.
* Sept 13, one day before EIC, OIDF Workshop will give update on OIDF WGs

UK
--------------
* Scheduling meeting with Fiona to share aggregated learnings across UK, Australia, and Brazil. 
* Already shared with Brazil and Australia, FDX upcoming

US/FDX
--------------
* Meeting with FDX on Friday. Paperworks for reframing licensing agreement to strategic partnership.
* FDX adopting FAPI standard. 

  * Will recommend but not require FAPI certification


Middle East
-----------------
* E-mail exchanges on next steps. Directed funding for workshop and Authlete coordinating. 
* Introducing OIDF to leaders in the middle east. 
* Planning to put together a program for investigating FAPI adoption and certification.


Certification (Joseph)
==========================

* Certification Fees

  * Implementations who recently paid for FAPI ID2 certification do not need to repay for FAPI 1.0 Final certification again

* JARM certification 

  * JARM tests are available but not offered for certification
  * Might become more prominent in Brazil spec
  * Any objections to launching a certification program that includes JARM?

* Side note : certification page columns are increasing, ideas solicited for better display
* JARM to Final?

  *  Need to move process forward

* Streamlining is much appreciated. 
* Too many PDFs to sign. 

  * Allow multiple profiles to be listed in conformance document?

    * Nat, Joseph, Travis  to discuss offline

  * Discussed idea of Docusign integration

    * Pre-fill certification details for easier signing

* Combination explosion problems. Need to be clear on what’s needed for test profiles.

  * Feedback is welcome



FAPI 2.0 (Dave)
===================



PRs (Dave)
===================
This week, the WG focused on FAPI 2.0. 

PR 279: Add reference to grant management API (Dave)
----------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/279
* Approved. 
* Ralph pointed out the importance of the interoperable grant management etc. 
* Dave pointed out that it is written to FAQ  that FAPI 2.0 objectives ARE to create an interopable consent and authorisation framework that addresses management AND rich authorisation request handling.

PR 276: Add normative clause for AS to accept issuer value in aud claims
----------------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/276
* Filip pointed out the issuer URL should be substituted with the issuer identifier. 
* Multiple values to be addressed in issue #426 slated for ID2

PR 280: Add initial acknowledgements
-------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/280
* Please add your name. 

Issues (Dave)
=================
#416: RAR if scope *and* claims param not expressive enough (Travis)
----------------------------------------------------------------------------------
* Using claims parameter to describe permissions for access tokens is not standardized
* Discussion to be continued
* Milestone moved to ID2



#417: Shall require introspection of claims (Travis)
----------------------------------------------------------------------------------
This is not related to #416. 

* New statement states that the resource server can verify the validity using scope or claims that are within the token.
* Need to clarify what “claim” is referring to; JWT, simple JWT claim, or OIDC claims parameter 
* Milestone moved to ID2


AOB
=======
* Neither Dave nor Nat is available next week so it is proposed to be cancelled. 

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