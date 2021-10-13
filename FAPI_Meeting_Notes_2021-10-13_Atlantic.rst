============================================
FAPI WG Meeting Notes (2021-10-13) 
============================================
* Date & Time: 2020-10-13 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 


* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================


Events (Dave/Nat)
======================
OpenID Foundation Workshop moved to December (Mike L.)
---------------------------------------------------------
It was originally planned for Oct. 21 but it collides with Authenticate so it was pushed to December 9th. 

Registration info will be available at openid.net in a few days. 

Authenticate/FIDO (Gail)
---------------------------
Authenticate happening on Oct. 18-22. OpenID Foundation sessions are part of the plenary, Oct. 21. 

Remote attendance pass code is available 

FYI information on 10/21 OIDF sessions http://autheneticatecon.comautheneticatecon.com...20Auth!FIDO21.

3 sessions at FIDO: https://openid.net/2021/10/11/announcing-openid-foundation-sessions-at-the-fido-member-plenary-on-thursday-october-21-2021/

Link: https://fidoalliance.org/event/authenticate-2021-conference/

code is 20Auth!FIDO21 to access plenary sessions on 10/21 remotely.


External Organizations (Dave/Nat)
===================================

Brazil (Mike)
---------------------------



Australia (Dima/Joseph)
------------------------------------
N/A

Berlin Group (Nat)
--------------------------------


Canada (Gail)
------------------
No updates


FDX (Gail)
------------------
No updates


Middle East and North Africa (Ali)
-------------------------------------
DIFC is connecting us with ... 


Russia (Don/Dima)
--------------------
* Still awaiting response 


UK (Fiona/Ralph/Chris)
--------------------
Ver 3.1.9 was approved last week. It only contains minor changes. 

Status and error messages: requirements not clear. Need to watch out for regulators as it may cause issues for Banks implementing useful responses. 


PRs (Dave/Nat)
=================

PR 287 - Add requirement for clients to send issuer as a string
---------------------------------------------------------------------------------------

* Pull request #287 - Add requirement for clients to send issuer as a string

Feedback regarding wording is requested

PR 428 - Add initial version of implementation advice doc
-----------------------------------------------------------------------------------
Pull request #288 - Add initial version of implementation advice doc

Dave has created an initial version of the Implementation Advice Draft

Move text regarding x-fapi headers to the advice document.

Feedback requested



Issues (Dave/Nat)
=====================
Issue 445: Condition for a token response to include a grant_id
--------------------------------------------------------------------------------
https://bitbucket.org/openid/fapi/issues/445/condition-for-a-token-response-to-include

Clarification on when AS should return a Grant ID.

Grant ID should not be issued when Grant Mangement function is not used.

Current wording does not preclude sending Grant ID when GM function is not used.

Dima to provide feedback.


Issue 447: grant_id is given but grant_management_action is not
--------------------------------------------------------------------------------
https://bitbucket.org/openid/fapi/issues/447/grant_id-is-given-but

Clarify when authorization request includes a Grant ID but does not include a grant management action.

Authors and Taka will have call next week.


Issue 449: Field name and type for resource fields
--------------------------------------------------------------------------------
https://bitbucket.org/openid/fapi/issues/449/field-name-and-type-for-resources

Clarification is needed on field name and structure/type

Published HTML was not updated in time for implementer’s draft version.

#437 also requires clarification

Will discuss next week



#415 - Discovery Metadata for mtls
--------------------------------------------------------------------------------
Underlying specs are clear that if you’re using MTLS for sender constraint tokens, you must use the alias URL

Need feedback from Ralph


#443 - Missing Discovery Metadata for login_hint types and login_hint_token type backchannel_endpoint_login_hint_token_values_supported
--------------------------------------------------------------------------------
https://bitbucket.org/openid/fapi/issues/443/

Provides a way to advertise, back channel endpoint, login token, value supported, and then registering client preference

Defines a spec level key but value structures are user/implementation specific

Brazil has 5 different token types 

The issue is asking for a placeholder that can be ecosystem specific

No precedent for a top level key with no predefined values

Taka suggested another approach where the value allow ecosystem specific values or the value points to another discovery document for ecosystem specific values 

OIDC Core has id_token_hint

Brian pointed out that CIBA Core is final so no changes are allowed, so it will require an extension or profile document

Will need to evaluate risks because it’s going to be fundamental data

Dave will update issue with notes and asked Ralph for feedback

Feedback is requested

Having a placeholder for values and registration is OK.

The use case for this is not clear.


AOB (Dave/Nat)
=================
Gail asked for feedback on licensing options for FDX:

* In house Certification Only
* License with restrictions
* License no Restriction

.. image:: https://bitbucket.org/repo/K7gLBb/images/2208548758-certlicensing.png
   :alt: certlicensing.png


The call adjourned at 15:00 UTC