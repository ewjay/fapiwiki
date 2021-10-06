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

* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================


Events (Dave/Nat)
======================
OpenID Foundation Workshop moved to December (Mike L.)
---------------------------------------------------------
It was originally planned for Oct. 21 but it collides with Authenticate so it was pushed to December. 

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

Topics are mostly on Self-Sovereign Identity right now

Mike J. is coordinating with organizers to allocate the second morning to do OIDF work.


External Organizations (Dave/Nat)
===================================
ISO/TC 68 (Nat/Dave)
-----------------------------

Nat has drafted a liaison statement and have distributed it to the liaisons committee.


Australia (Dima/Joseph)
------------------------------------
N/A

Berlin Group (Nat)
--------------------------------
Nat had a call with Bruno.

OIDF-Note-Well : Nat explained that any OIDF publication is validated beforehand, therefore there is no such risk as Wijnand raised for the BerlinGroup.

And the text as proposed by the ODIF is approved as is.

Sub-Committee planning: We concurred that the workstream should be 2 phases :

Phase 1: Share approaches and identify requirement domains to elaborate
Phase 2: Build the requirements for the joint Initiative
 

Phase 1 will break down across 3 workshops:

#. Mutual presentation (ie The Berlin-Group and OIDF) on the key domains which might be beneficial for each other: 3 hours Workshop to be set during the week of Oct the 25th. 

#. To improve this first workshop, both the Berlin-Group openFinance Editor and the OIDF will share documents they have to highlight the specific areas of potential mutual interest (Action : as soon as possible)

   Investigation and definition of the areas to investigate jointly

#. Final definition and plan requirement definitions: Plan Phase 2 (ie what and when)
 

Phase 1 is targeted to end before Christmas (2021) and here are 3 doodles (one for each of the 3 phase 1 workshops) to share with the SC members :

#. Mutual Presentation WS: https://doodle.com/poll/uq6fnuwtc7zpsg2c?utm_source=poll&utm_medium=link
#. Investigation and definition: https://doodle.com/poll/8mq4ph49ws5i5kq7?utm_source=poll&utm_medium=link
#. Final definition and plan requirement definitions: https://doodle.com/poll/3pywfmcwym2d3ev6?utm_source=poll&utm_medium=link

Brazil (Mike)
---------------------------
* DCR test working well. 
* https://openid.net/2021/09/29/announcing-the-gain-poc-pre-launch-listening-tour/
* Open Banking Brazil RP Community Group Slack link: https://join.slack.com/t/openbankingbr-z4z3977/signup?x=x-p2561471170368-2534834696229-2597135141008



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

Feedback requested



Issues (Dave/Nat)
=====================
Issue 445: Condition for a token response to include a grant_id
--------------------------------------------------------------------------------
https://bitbucket.org/openid/fapi/issues/445/condition-for-a-token-response-to-include



Issue 447: grant_id is given but grant_management_action is not
--------------------------------------------------------------------------------
https://bitbucket.org/openid/fapi/issues/447/grant_id-is-given-but

Issue 449: Field name and type for resource fields
--------------------------------------------------------------------------------
https://bitbucket.org/openid/fapi/issues/449/field-name-and-type-for-resources

#443 - Missing Discovery Metadata for login_hint types and login_hint_token type
--------------------------------------------------------------------------------
#443 - Missing Discovery Metadata for login_hint types and login_hint_token type: backchannel_endpoint_login_hint_token_values_supported

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



AOB (Dave/Nat)
=================
Gails wanted to survey to see if anyone is aware of adaptations of FAPI, specifically for the insurance industry within OIDF communities or elsewhere.

A member was asked to start talking about such a topic.

Nat was contacted by the Japanese Fintech society’s insurance group but haven't heard back from them.

Brazil is looking to launch an open insurance that’s part of the wider open finance that Brazil is looking to expand.

UK has talk of open insurance also.

Anyone with any other information on the topic is welcome to talk to Gail.



The call adjourned at 15:00 UTC