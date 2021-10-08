============================================
FAPI WG Meeting Notes (2021-10-06) 
============================================
* Date & Time: 2020-10-06 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-06_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Ali Adnan (Authlete)
  * Anthony Nadalin (it)
  * Barry O'Donohoe (Raidiam)
  * Bjorn Hjelm (Verizon)
  * Brian Campbell
  * Chris Michael
  * Daniel Fett (yes)
  * Dave Tonge
  * Dima Postnikov
  * Francis Pouatcha (adorsys)
  * Gail Hodges (OIDF, she/her)
  * Jacob Ideskog (Curity)
  * Joseph Heenan (Authlete / OpenID Foundation)
  * Mike Leszcz
  * Naohiro Fujie(OIDF/OIDFJ)
  * Nat Sakimura
  * Nick Mothershaw
  * Peter Bainbridge-Clayton
  * Sascha Preibisch (LoginID)
  * Takahiko Kawasaki (Authlete)
  * Travis Spencer (Curity)
  * Ayomi Igandan (Capco)
  * Brian Campbell
  * Chris Wood
  * Daniel Fearns
  * Domingos Creado (Authlete)
  * Edmund Jay


* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================


Events (Dave/Nat)
======================
OpenID Foundation Workshop moved to December (Mike L.)
---------------------------------------------------------
It was originally planned for Oct. 21 but it collides with Authenticate so it was pushed to December 9. 

Authenticate/FIDO (Gail)
---------------------------
Authenticate happening on Oct. 18-22. OpenID Foundation sessions are part of the plenary, Oct. 21. 

Link: https://fidoalliance.org/event/authenticate-2021-conference/


GAIN PoC Meetings
---------------------------
A few listening sessions. 

1. OIX: Oct. 14
2. FIDO: 
3. Virtual Workshop: Dec. 9. 

They are going to be announced in the blog. 


IIW
------------
October 12-14, 2021 

Some members will try to reserve evening or early morning session spots so other participants from Asia-Pac or Europe can attend.

External Organizations (Dave/Nat)
===================================
ISO/TC 68 (Nat/Dave)
-----------------------------

Nat has sent the liaison statement.


Australia (Dima/Joseph)
------------------------------------
N/A

Berlin Group (Nat)
--------------------------------
Bruno is organizing time slots for the first workshop. All interested parties may attend.

There’s a lot of parallel initiatives happening on payments and banking. BG is attempting to synchronize the data model with ISO 20022

Defining FAPIs that can be used on peer-to-peer basis agreement between banks and TPPs, requests to pay.
Working on future of payments in Europe to converge on a common standard. 

Open Banking Association is mandating all banks to stop using old interfaces and focus on digital? interfaces on Jan 1. 2022.


Brazil (Mike)
---------------------------
* RP, DCR test working well.
* Will have meeting with Brazilian team to add new DCR tests for Brazil OP certifications
* DCR certifications are on hold
* Open Banking Brazil RP Community Group Slack link: https://join.slack.com/t/openbankingbr-z4z3977/signup?x=x-p2561471170368-2534834696229-2597135141008
* Travis raised the issue about dependence of DCR tests on Brazilian infrastructure.
* Tests require integration with the Brazilian directory.
* This doesn’t prevent vendors from certifying for Brazil FAPI. Certification team has a solution for a workaround, but Travis is not satisfied with it.
* Chris is interested in this issue.



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