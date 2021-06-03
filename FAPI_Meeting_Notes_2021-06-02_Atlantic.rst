============================================
FAPI WG Meeting Notes (2021-06-02) 
============================================
* Date & Time: 2020-06-02 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-06-02_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:06 UTC. 

Roll Call 
===========
* Attending: Nat, Dave, Chris Wood, Travis, Joseph, Renato, Takahiko, Taimoor Hazir (Millenium Partners), Filip, Don, Omer Khawaja (Millenium Partners), Daniel, Brian, Torsten, Dima, Kosuke, Gail, Lukas, Francis. 
* Regrets: 
* Guest: 

Taimoor introduced himself and Omer as it was their first call. 

They are helping Authlete in the EMEA region. 

Involved with organization strategy, Open Banking events, and other areas.

Adoption of Agenda (Nat)
===========================
* Adopted as is. 

Events (Nat)
======================
Virtual Open Identity Summit (Daniel)
--------------------------------
* FAPI and FAPI2
* 30 People attended
* Slides to be shared. 


External Organizations (Nat)
================================
Australia (Joseph)
----------------------
* Working with DSB to send out special offers for people who attended. 
* Joe (Oatley?) from ACCC Cyber Security Team got in touch. 
* Will set up a meeting.

Brazil (Danillo) 
------------------------
* Little delayed with translation
* OK with Video. 
* Gail and Mike L, Joseph will help Daniello. 
* Directed funding received for Brazil specific versions of security tests. 
* Expecting 35 certifications in the first half of July. 
* Brazil test will be available on June 11. 
* It will be available in the master branch as a test variant. 
* New features (No major diffs): 

  * encrypted request object
  * structured scopes 

Berlin Group (Francis)
---------------------------
* n/a

UK (Dave)
--------------------
* Not FAPI related but there is quite sophisticated fraud going on for payment initiation APIs in UK using social engineered, banking credentials.
* Found that banks have different fraud engines and controls for payment initiation journeys versus the online banking journeys.
* Happening across banks and a lot of compromised accounts
* There is an issue for FAPI2 regarding headers that we need to look at, such as what potential (fraud) information might need to be shared between a TPP and a bank
* Dave will share reports


US/FDX (Don)
-------------
* Paper work between OIDF and FDX is being finalized. 

Middle East (Gail)
-----------------------
* June 7 call
*  

Modrna Report (Dave/Bjorn)
=============================
* No additional comments in WG. 
* Getting ready for the public review for the FINAL. 

FAPI 2 Report (Dave)
=====================
* Implementers Draft Public Review started for Baseline and Security Model. 
* Quite a number of issues are coming in. 

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