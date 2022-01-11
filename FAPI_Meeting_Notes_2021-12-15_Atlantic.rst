============================================
FAPI WG Meeting Notes (2021-12-15) 
============================================
* Date & Time: 2020-12-15 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-12-15_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Adrian Field
  * Ali Adnan
  * Bjorn Hjelm
  * Brian Campbell
  * Craig Borysowich
  * Daniel Fett
  * Dima Postnikov
  * Joseph Heenan
  * Kosuke Koiwai
  * Lukasz Jaromin
  * Manuela Sedvartaite
  * Mike Leszcz
  * Nat Sakimura
  * Takahiko Kawasaki 
  * Travis Spencer
  * Ayomi Igandan
  * Bjorn Hjelm
  * Daniel Fearns
  * Filip Skokan
  * Michael Palage

* Regrets: Dave
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* 

Events (Dave/Nat)
======================

Report on OIDF virtual workshop (Mike L.)
-----------------------------------------------
Thursday, December 9th at 9 AM PT. 

Joseph present FAPI WG updates

New board members from Cisco, Okta, and Visa

Torsten updated on the GAIN POC

Workshop presentations and recordings are on the OIDF website : 
https://openid.net/workshops/oidf-virtual-workshop-thursday-december-9-2021/



External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
Started in the certification group on what they might be able to do for FAPI 2.0 Baseline test. 

Brazil (Mike L.)
---------------------------
Increase in RP certification. 


Domingos and Marcus had real positive impact. 

Open Banking Brazil milestones are quite fluid. 


Berlin Group (n/a)
--------------------------------
OIDF does not have country standing liaison rep in the BG advisory group. 

We should have one.


FDX (Gail)
------------------
Blog post on FAPI 1 v.s. 2. 

https://openid.net/2021/12/14/what-are-the-differences-between-fapi-1-0-and-fapi-2-0-and-what-do-they-mean-to-you/


The Middle East and North Africa (Ali)
---------------------------------------
Received the draft MOU today.

Gail suggested making an announcement in January 2022 instead of December 2021.


Mexico (Gail)
------------------
n/a

Russia (Dima/Mike)
--------------------
MikeL followed up with people at the Fintech association in Russia.

Shared the learning deck that Gail wrote, the workshop recordings from last week, and the blog post published yesterday.



UK (Chris)
--------------------
n/a

GAIN (Gail)
---------------
Participation agreement
~~~~~~~~~~~~~~~~~~~~~~~
It is being worked on by Gail and Tom. 

Don is now reviewing it. 

G5
~~~
Consensus on MOU among the five. 

Now socializing with their boards. 

Roadmap (Don)
~~~~~~~~~~~~~~~~
Identifying participants. 



FAPI DCR/M (Dynamic client registration and Management) (Joseph)
====================================================================
No updates

Grant Management (Dima)
=============================
Wrapping up issues and PRs

PRs (Nat)
=================

* PR #301 - Editorial fixes

  * Fixes #462 - 
  * Deleted duplicate copyright notices
  * Change Spec working group from Connect to FAPI
  * Merged

* PR #294 - Conditions for grant ID issuance

  * Fixes #445
  * Merged 

* PR #270 -  Compilable deployment advice updates

  * Skipped since Stuart was not present
  * Awaiting some resolutions for comments by Nat

* PR #297 - Clarify refresh token behaviour on replace and update.

  * Fixes #454
  * Approved and merged
  * Whole document needs a review for proper keyword capitalization
  
    * Travis will create new issue 

* PR #299 - First attempt at a pipeline

  * Every push will trigger a build pipeline to generate the HTML
  * The master branch HTML will be published to bitbucket.io
  * Currently works for FAPI 2.0 Baseline. Other docs don’t work yet.
  * Merged

* PR #300 - Remove/update various non-current documents

  * GM spec can’t be built yet. Dima/Torsten to investigate and add new instructions.
  * Will merge later after creating an associated issue for tracking.
  * Issue #463 created 


Issues (Dave/Nat)
=====================
* #455 - Impact of grant_management_action=update on AT implementation and introspection

  * Will create implementation advice which clarifies introspection response
  * Dima has created a PR awaiting review

* #461 - FAPI2-Baseline - has the time come to recommend/require TLS 1.3?

  * Recommend FAPI 2.0 to use TLS 1.3
  * Danile posted link https://caniuse.com/tls1-3  on browser support of TLS 1.3
  * There are endpoints that don’t talk to browsers which may not support TLS 1.3
  * Need to also survey support among programming platforms like Java, .NET, PHP, Ruby, Operating Systems,  Web servers (Apache, Nginx, Tomcat), toolkits (OpenSSL)  etc..
  * No pressure to move away from TLS 1.2 yet. FAPI WG is not influential enough to create such pressure.
  * Setting up secure TLS 1.2 is difficult
  * Should reach out to other communities to find out their recommendations for TLS version for better understanding
  * FAPI 1.0 refers to BCP195 and further constrain options if not using TLS 1.3
  * Certification checks for BCP195 conformance are difficult
  * Craig posted link https://csrc.nist.gov/publications/detail/sp/800-52/rev-2/final
  * Recommending 1.3 would be useful but requiring support of it would be OK, but requiring only support of it would be premature.
  * Should follow link from Craig and state a target date for transition to TLS 1.3
  * Nat will summarize discussion in issue
  * Needs further discussion

* #460 - FAPI2-Baseline TLS restrictions are written as prose

  * Related to #461


AOB (Nat)
=================
Next Meeting (Nat)
-------------------------
* We are cancelling Dec 22 and 29 meetings. 
* The next meeting will be on January 5. 


The call adjourned at 14:55 UTC

Chat Log
-----------
23:04Me to Everyone
1. Roll Call (Dave/Nat) 
2. Adoption of Agenda (Dave/Nat) 
3. Events (Dave/Nat) 
3.1. Report on OIDF virtual workshop (Mike L.) 
4. External Organizations (Dave/Nat) 
4.1. Australia (Gail/Dima/Joseph) 
4.2. Brazil (Mike L.) 
4.3. Berlin Group (n/a) 
4.4. FDX (Gail) 
4.5. The Middle East and North Africa (Ali) 
4.6. Mexico (Gail) 
4.7. Russia (Dima/Mike) 
4.8. UK (Chris) 
4.9. GAIN (Gail) 
4.9.1. Participation agreement 
4.9.2. G5 
4.9.3. Roadmap (Don) 
5. FAPI DCR/M (Dynamic client registration and Management) (Joseph) 
6. Grant Management (Dima) 
7. PRs (Nat) 
8. Issues (Dave/Nat) 
9. AOB (Nat) 
9.1. Next Meeting (Nat)

23:05Mike Leszcz to Everyone
https://openid.net/workshops/oidf-virtual-workshop-thursday-december-9-2021/

23:08Mike Leszcz to Everyone
https://openid.net/2021/12/14/what-are-the-differences-between-fapi-1-0-and-fapi-2-0-and-what-do-they-mean-to-you/

23:12Joseph Heenan (Authlete / OpenID Foundation) to Everyone
https://bitbucket.org/openid/fapi/pull-requests/301

23:17Me to Everyone
https://bitbucket.org/openid/fapi/pull-requests/297

23:22Joseph Heenan (Authlete / OpenID Foundation) to Everyone
https://bitbucket.org/openid/fapi/pull-requests/299

23:24Joseph Heenan (Authlete / OpenID Foundation) to Everyone
https://bitbucket.org/openid/fapi/pull-requests/300

23:29Joseph Heenan (Authlete / OpenID Foundation) to Everyone
https://bitbucket.org/openid/fapi/src/master/FAPI_1.0/openid-financial-api-part-1-1_0.md

23:33Me to Everyone
https://bitbucket.org/openid/fapi/issues/461/fapi2-baseline-has-the-time-come-to

23:35Daniel Fett (yes) to Everyone
https://caniuse.com/tls1-3

23:45Craig Borysowich to Everyone
https://csrc.nist.gov/publications/detail/sp/800-52/rev-2/final

23:50Brian Campbell (Ping Identity) to Everyone
^

23:53Brian Campbell (Ping Identity) to Everyone
+2

23:53Lukasz Jaromin (Cloudentity) to Everyone
+1