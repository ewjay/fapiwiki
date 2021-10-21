============================================
FAPI WG Meeting Notes (2021-10-13) 
============================================
* Date & Time: 2020-10-13 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Amirhossein Najmi
  * Ayomi Igandan
  * Brian Campbell
  * Chris Michael
  * Daniel Fett (yes)
  * Danillo Branco
  * Dave Tonge
  * Dima Postnikov
  * Edmund Jay
  * Francis Pouatcha (adorsys)
  * Gail Hodges (OIDF, she/her)
  * Joseph Heenan (Authlete / OpenID Foundation)
  * Kelley Burgin (MITRE)
  * Kosuke Koiwai
  * Lukasz Jaromin (Cloudentity)
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Ralph Bragg
  * Stuart Low (Biza.io)
  * Takahiko Kawasaki (Authlete)
  * Yaron Zehavi
  
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

FAPI WG presenter needed for WG update.

Authenticate/FIDO (Gail)
---------------------------
Authenticate happening on Oct. 18-22. OpenID Foundation sessions are part of the plenary, Oct. 21. 

Remote attendance pass code is available 

FYI information on 10/21 OIDF sessions http://autheneticatecon.comautheneticatecon.com...20Auth!FIDO21.

3 sessions at FIDO: https://openid.net/2021/10/11/announcing-openid-foundation-sessions-at-the-fido-member-plenary-on-thursday-october-21-2021/

* GAIN PoC
* Mobile Driver’s License
* Shared Signals and Events

Link: https://fidoalliance.org/event/authenticate-2021-conference/

code is 20Auth!FIDO21 to access plenary sessions on 10/21 remotely.

Free to attend plenary remotely, there are fees for in person attendance, at member rates using the same code. ($450 for plenary 2 days).


External Organizations (Dave/Nat)
===================================

Brazil (Mike)
---------------------------
Central Bank has requested additional OP DCR tests to support Phase 3 rollout.

Had call with Brazil team to understand requirements.

Received $50,000 directed funding from Brazil for development and recertification of some Phase 3 banks which have already certified.

RP community Slack channel is up and running. Activity is light and will continue to promote it.

Filipe Skokan has joined the certification team to support this effort.

MikeL will send information to the mailing list on how to participate.

The Certification suite did not have support for RFC7592 which is mandatory for Brazil profile.

Banks registered with OP but forgot access tokens.

Central Bank is serious about interoperability and is compelling recertifications for Phase 3 DCR and Phase 2 functional APIs.



Australia (Dima/Joseph)
------------------------------------
AAAC decided not to work with OIDF to perform assessment of their current implementation and necessary improvements.

Have provided clarifications for certifications and potential  leverage of OIDF certification capabilities to support their mission.


Berlin Group (Nat)
--------------------------------
Bruno is working on setting up appointments for the three workshops.

Advisory board would like the 3rd workshop to be in late February.

First 2 sessions will focus on finding common ground on how to approach the Berlin Group.

Community will look at results to decide how to move forward.

Dave will forward workshop Doodle to the list.

Appointments will be available soon and workshops will likely be around mid-Nov to mid-Dec



Canada (Gail)
------------------
No updates


FDX (Gail)
------------------
Don Cardinal will be attending and speaking at Authenticate and FIDO conference.

Hope to connect and continue the conversation.

They have issues with NDA and desire for control.

Gail has provided certification models to WG and Executive Committee and will update Board members at Authenticate.

Models with complete outsourcing with no control measures lack support from the Board.

WG would like to retain development of security profile and certification suite.



Middle East and North Africa (Ali)
-------------------------------------
No updates


Russia (Don/Dima)
--------------------
No updates


UK (Fiona/Ralph/Chris)
--------------------
No updates

PRs (Dave/Nat)
=================

* https://bitbucket.org/openid/fapi/pull-requests/286

  * Fix for typo
  * Merged

* https://bitbucket.org/openid/fapi/pull-requests/287

  * Issuer ID will be sent as a string not as an item in an array.
  * Merged


Issues (Dave/Nat)
=====================
#443 - Missing Discovery Metadata for login_hint types ... (Ralph)
--------------------------------------------------------------------------------
#443 - Missing Discovery Metadata for login_hint types

Brazil mandates use of CIBA for different regulatory scenarios

Credit propositioning - consumer asking broker, who delegates to other agents that will request access to consumers data. 
Will have different token type. Important for bank to collect information on such requests. Consumer may have to provide consent N times.

3-4 different IID token  types depending on banks API offerings for payments

* Opaque
* CPF
* Emails
* Phone numbers, etc.

Brazil payments infrastructure has concert of DICT, which contains different keys that can be used to identify someone for making payments. Banks need to provide support for some not all of the keys.

There is a mechanism for banks to advertise which token types they support. Allows RPs to filter which OPs they can support.

These uses cases are critical to enabling CIBA in the real world.

Brian : Registering keys is not enough, needs to define possible values and their meaning

Brazil specification defines keys but not standard values

First standardize the key and then specify process for registering values

Still needs more work to be complete

Login type will contain domain specific subject ID and other attributes about the subject

CIBA is mandated for credit propositioning but not payments

This could be applied to other use cases such as UK’s supported Bank permissions 

Is it better to have a better placeholder?

Need description of how it would be used

May used different ways to denote what keys mean to different ecosystems

Making it more generic requires more context and descriptions other than key name

Ralph to make a pull request to the FAPI CIBA spec


#445 - Condition for a token response to include a grant_id (Dima)
--------------------------------------------------------------------------------
#445 - Condition for a token response to include a grant_id

Taka noted that Grant IDs should not be issued to public clients due to security reasons

Stuart commented whether there should be a parameter to  force return of Grant IDs from token endpoint

It might be needed in migration scenarios

Members are asked to review issue and provide feedback


#452 - When the user being authenticated is different from the user of the grant
------------------------------------------------------------------------------------------
#452 - When the user being authenticated is different from the user of the grant

Doesn’t have an error behavior defined

Joseph gave example of user authorizing an app to use a business account to access the business’s account data and needing 
to reauthorize when the connection expires but the original authorizing user is not available.

The use cases might be more complicated

One option is to not mention this scenario and let providers decide

Rather than define something that is limiting 

Feedback is requested


AOB (Dave)
=================

The call adjourned at 15:00 UTC