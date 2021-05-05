============================================
FAPI WG Meeting Notes (2021-05-05) 
============================================
* Date & Time: 2020-05-05 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-04-07_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
* Attending: Nat, Dave, Kosuke, Daniel, Joseph, Brian, Chris Wood, Lukas Jaromin, Francis Pouatcha, Torsten, Dima. 

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* Adopted as is. 

External Organizations (Nat)
================================
Brazil (Joseph)
---------------
Mike L. is setting up a meeting with the Brazilian Government as well as Workshop. The meeting schedule should be set by next week. 

There is a draft version of the security profile. 
https://github.com/OpenBanking-Brasil/specs-seguranca/blob/main/open-banking-brasil-financial-api-1_ID1.md
It is near final. Not much controversial but it is still using the structured scope. 

It is using `acr` etc. and ID Token as a detached signature: Almost the copy of UK Open Banking. 
There is only one difference. Ralph could explain in the next call. 


Berlin Group (Francis)
---------------------------
Nat to suggest setting up sub-committee to FAPI to deal with BG needs. 
Two co-chairs. Dave Tonge from OIDF and another from BG. 

UK Open Saving and Pension (Dave)
-------------------------------------
Pension dashboard slated to use UMA. 
Putting FAPI over it could be useful. 
Chris Wood wrote a `blog post <https://blog.axway.com/industries/banking-insurance/the-pensions-dashboard>`_ on it. It also deals with CIBA. 

General
-----------------
UK NCSC provides advice for security. 

FDX (Lukasz)
-----------------
Lukasz is working on the consent management at FDX. 
Dima has a slide deck that can be used to explain Grant Management. 
The link will be shared with edit permission to Lukasz. 

Internal Liaison
====================
Modrna WG (Bjorn)
---------------------
CIBA Core is proposed to bring to the final publication. 



Events (Nat)
======================

OpenID Foundation Workshop (Nat)
---------------------------------------
April 29. 

Site URL: https://openid.net/2021/03/01/registration-open-for-openid-foundation-virtual-workshop-april-29-2021/

Tickets: https://www.eventbrite.com/e/openid-foundation-virtual-workshop-tickets-143831524963

Open Banking World Congress (Don)
---------------------------------------------
May 11 - 13. Dave Tonge will be speaking. 

Site URL: https://congress.openfuture.world/speakers/?utm_campaign=OBWC21&utm_medium=email&_hsmi=122216549&_hsenc=p2ANqtz-85MvO81z4sSX-dOrIbCIC77pfdwrqN1LhYxs6JTNfFHSk6PP3ROFz2iSRjFU6OdZZ-50Pr2u0HE4KChrgo0Y_r3ALFfw&utm_content=122216549&utm_source=hs_email


FAPI 2.0  (Dave/Daniel)
======================================================
Torsten prepared the package and send it to Mike J. 

PRs (Dave)
===================
None. 


Issues (Nat)
=================
Issue #407 Grant Management Lifecycle (Dima/Ralph)
----------------------------------------------------------------
* #407
* https://bitbucket.org/openid/fapi/issues/407/grant-management-lifecycle

Currently, it is possible to have a scenario where the request and granting was completed but the response did not get delivered. 

Long discussion. 

AOB
=======
* none