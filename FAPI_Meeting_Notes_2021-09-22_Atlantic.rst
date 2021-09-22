============================================
FAPI WG Meeting Notes (2021-09-22) 
============================================
* Date & Time: 2020-09-22 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-09-08_Atlantic

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


External Organizations (Dave/Nat)
===================================
ISO/TC 68 (Nat/Dave)
-----------------------------
* Need to send a liaison report. 

Australia (Dima/Joseph)
------------------------------------


Berlin Group (Francis/Mike.L)
--------------------------------
No updates

Brazil (Mike)
---------------------------
OIDF received $65K in directed funding from Mirow.
* $15K  for RP DCR test
* $50K for RP community group pilot in Brazil

Working with the certification team to identify and document Phase 3 milestones.

Will go live on October 29.

The draft will be shared and confirmed by the end of this week.

Mike L. will share details of RP community group.

Two Brazilian RPs are helping test the certification suite.


Canada (Gail)
------------------
 

FDX (Mike)
------------------
Mile, Gail, and Don will have a call with FDX on September 9.

Will provide details next week.


Middle East and North Africa (Ali)
-------------------------------------


Russia (Don/Dima)
--------------------



UK (Fiona/Ralph/Chris)
--------------------
Chris commented that there are quite a few emerging Open Banking markets around the world. 

A tracker to document the efforts and differences would be helpful.

Don, Nat, and Gail are working on  a board resolution to promote international interoperability and certification.

Global Open Finance Center of Excellence and their International Standards Forum can be a resource as an international library for open finance/banking standards.

Don and Nat have been working with Gavin LittleJohn in that effort.



PRs (Dave/Nat)
=================
n/a

Issues (Dave/Nat)
=====================

#426: FAPI 2 - Multiple audience values in client authentication assertions
--------------------

Various specs and endpoints are increasing the audience values.

Clients are sending multiple audience values in order to get things to work

Could potentially be a security and interoperability problem.

Need to improve interoperability

Brian: arbitrary restrictions of specs that use other specs makes interoperability more difficult
Going forward, using Issuer ID would be more interoperable but limiting to single value is problematic. Current deployments already use multiple values. Limiting to RP to use Issuer ID is acceptable but limiting server to accept only the Issuer ID is breaking previously working deployments.

Curren text says the AS shall accept issuer and should accept endpoint URL

The “Should accept endpoint URL” could cause problems in migration from FAPI 1.0 to FAPI 2.0 due to many clients currently sending the token endpoint as the audience value.

Conformance suite needs a test to check whether AS accepts Issuer as audience.

FAPI 2.0 test must check that AS accepts Issuer only due to RP and AS requirements.

WG agreed on tightening the current text to limit the value to a string.


#282: FAPI 2.0: x-fapi-* headers
--------------------
Two issues:
1. Do we need to add the headers in security profile
1. Do we continue using x-prefix for header names even though it’s deprecated

x-fapi-interaction-id  header is used for audit so it should be in the security profile.

Keeping x-prefix would not break existing clients

X-fapi-auth-date and x-fapi-customer-ip-address may be deprecated.

Consider using forward-for header

IP address may be considered as PII in some jurisdictions.

X-fapi-auth-date adds complexity for clients due to the information may not be easily available for clients.

Headers are only defined and used  in the Resources server section

Dave will update issue:
* Keep x-fapi-interaction-id and drop the others.

Headers cannot be validated.

Dima asked if there is an alternate way to indicate whether the current request is user attended or not.



AOB (Dave/Nat)
=================


* Please vote for Grant Management 1st Implementer's Draft: https://openid.net/foundation/members/polls/246 


The call adjourned at 15:__ UTC