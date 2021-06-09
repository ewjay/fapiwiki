============================================
FAPI WG Meeting Notes (2021-06-09) 
============================================
* Date & Time: 2020-06-09 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-06-02_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:06 UTC. 

Roll Call 
===========
* Attending: Nat, Mike Leszcz, Takahiko, Jacob, Travis, Chris Wood, Rento Athaydes, Omer, Joseph, Dima, Taimoor Hazir, Stuart, Brian, Barry, Filip, Kosuke, Ali, Wesley, Torsten, Gail, Lukasz, Ralph, Vinod. 
* Regrets: Francis
* Guest: 


Adoption of Agenda (Nat)
===========================
* Adopted as presented. 

Events (Nat)
======================
Identiverse (Brian/Joseph)
-----------------------------------
* Hybrid event in Denver. 
* Joseph is going to mention FAPI in his session. 


External Organizations (Nat)
================================
Australia (Mike L.)
----------------------
* CDR

Brazil (Mike) 
------------------------
* 27 banks are part of phase 2 certifying 39 implementations by July 15. 
* A number of them joined OIDF. 
* 3rd WS coming up with a comprehensive walkthrough of the conformance suit. 
* Danillo's translation of Taka's article should be ready by then. 
* The recording will be available in Portuguese as well. 
* Test suit should be ready on Friday. 

Berlin Group (Francis)
---------------------------
* n/a

UK (Dave)
--------------------
* Phishing attack on OTP going on. 
* Dynamic Linking to the transaction. 

US/FDX (Don)
-------------
* Gail is working on the Paperwork between OIDF and FDX is being finalized. 

MENA (Gail)
-----------------------
* June 7 call with Authlete team. 

Modrna Report (Dave/Bjorn)
=============================
* 60 days public review of CIBA Core has started. 

FAPI CIBA (Dave)
======================
* two new FAPI-CIBA certifications in the last week - the second one is Finansystech in Brazil.
* We aim to start the WG last call next week. 

FAPI 2 Report (Dave)
=====================
* Implementers Draft Public Review started for Baseline and Security Model. 
* Quite a number of issues are coming in. 

Grant Management (Dima)
============================
PRs
-----------
* PR 266 https://bitbucket.org/openid/fapi/pull-requests/266
* PR 271 - Filip and Brian to review it. https://bitbucket.org/openid/fapi/pull-requests/271

Issues
-----------
* #412 - FAPI 2.0 - Hard requirement to support Grant Management Requirement
* #416 - 

PRs (Dave)
===================
Following PRs were discussed. Mostly editorial fixes for compilation.

* https://bitbucket.org/openid/fapi/pull-requests/269

  * Compilable http signing

* https://bitbucket.org/openid/fapi/pull-requests/270

  * Compilable deployment advice updates

* https://bitbucket.org/openid/fapi/pull-requests/268

  * Minor changes to ensure xml2rfc compilation with backlink checking

* https://bitbucket.org/openid/fapi/pull-requests/267

  * Add more details to grant lifecycle


They are to be merged. 

* https://bitbucket.org/openid/fapi/pull-requests/266

  * Introduce a *replace* action
  * is to be continually discussed. 

Issues (Dave)
=================
416: RAR if scope *and* claims param not expressive enough (Travis)
------------------------------------------------------------------------
* #416 - RAR if scope *and* claims param not expressive enough

Access requested via scope or authorization  details

FAPI 2 baseline, and noticed this in 2.2.1 point 7:
shall support the authorization_details parameter according to [I-D.ietf-oauth-rar] to convey the authorization clients want to obtain if the scope parameter is not expressive enough for that purpose

This should say “…to convey the authorization clients want to obtain if the scope and claims parameters are not expressive enough for that purpose”

Travis > Would like to avoid supporting RAR if claims parameter is enough to expressive authorization request.

Dave > FAPI2 is aiming for less optionality.

Travis > Claims request parameter allows clients to ask  for different claims that should be placed in an access token and are more expressive than what you can request in scopes and if f the authorization server, based on policy, can put those into an access token, it achieves the same goal so authorization_details is not needed. 
Current wording ignores prior art for claims parameter.

Brian > Claims parameter is defined in OIDC. Just because you used it for something else doesn’t make it prior art.

Filip > Claims is defined in OIDC as a way for the client to replace the request claims not for those to be conveyed to the resources.

Travis > Current language is over restrictive. 

There are no specifications precluding or including use of claims as a way to request access tokens.

Discussion to be continued.


418: 303 should be used (Travis)
--------------------------------------
* #418 - 303 status code should be used when redirecting user-agents

Suggestion is for when only status codes are used since other methods such as meta-refresh and javascript can also be used

Keep alignment with Security BCP with current language


417: Shall require introspection of claims (Travis)
----------------------------------------------------------
* #417 

Related to #416

Claims request parameter is for ID Token and UserInfo claims request and not for other uses


415: Discovery Metadata for mtls (Ralph/Travis)
----------------------------------------------------------
* #415

Would like to make explicit reference to requiring mtls alias’s to be advertised by authorisation servers

Alias is used only when host or port are different so it will be optional for most implementations

Callers pointed out that the support of alias would not help interoperability. The majority of FAPI implementation does not support MTLS alias endpoint.

To be discussed with Ralph.

413: FAPI2 Baseline: Sender-Constrained Authorization Code (Taka)
-----------------------------------------------------------------------
* #413
* Clarification of the language probably is needed. 
* Filip pointed out that it is used in the certification suite and removing it may not be appropriate. 
* Dave suggested removing the wording
* Might need to consider the same issue in Security Tokens BCP
* To be continued 


AOB
=======
* n/a

The call adjourned at 14:59 UTC