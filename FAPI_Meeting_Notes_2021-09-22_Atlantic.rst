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

  * Ali Adnan (Authlete)
  * Anthony Nadalin (it)
  * Ayomi Igandan (Capco)
  * Barry O'Donohoe (Raidiam)
  * Bjorn Hjelm (Verizon)
  * Brian Campbell (Ping Identity)
  * Chris Michael
  * Daniel Fett (yes)
  * Danillo Branco (Finansystech)
  * Dave Tonge
  * Dima Postnikov
  * Don Thibeau
  * Edmund Jay
  * Francis Pouatcha (adorsys)
  * Gail Hodges (OIDF, she/her)
  * Joseph Heenan (Authlete / OpenID Foundation)
  * Kosuke Koiwai
  * Lukasz Jaromin (Cloudentity)
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Takahiko Kawasaki (Authlete)
  * Torsten Lodderstedt
  * Travis Spencer

* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================


Events (Dave/Nat)
======================
EIC (Nat/Don)
--------------------------
* Link to OIDF workshop at EIC recording: https://kc-live.com/#agenda-item.html?id=1032
* https://openid.net/2021/09/20/global-assured-identity-network-white-paper/

As the White Paper has been published by the International Institute of Finance and featured in Dave Birch's Forbes article.Or as the KuppingerCole blog puts it, "A Iot to Venture, More to Global Assured Identity Network” 

I've working with the 5 organizations referenced in the White Paper to explore their interest in taking the baton passed from GAIN co authors. Just as the White Paper seeks to build on what’s built, the next phase seems best led by those organizations that are doing the building. Brad Carr of the International Institute of Finance plans to host an initial call with representatives from the OpenID Foundation, Open Identity Exchange, Cloud Signature Consortium and Global Legal Entity Identifier Foundation to explore collaboration related to the Global Assured Identity Network. The White Paper is closely aligned with the IIF’s Open Digital Trust Initiative, the OpenID Foundation co leads. 

As you know, Gail Hodges is working with GAIN Co Authors Donna Beatty and Torsten Lodderstedt to move the GAIN Technical Proof of Concept under the auspices of the OpenID Foundation. Just as the proof of the pudding is in the eating, the proof of the paper is in the PoC. For more see the OIDF Blog

MENA (Don)
---------------------------



Authenticate/FIDO (Gail)
---------------------------
Authenticate happening on Oct. 18-22. 

Link: https://fidoalliance.org/event/authenticate-2021-conference/

Terms would be member pricing of $750 for Authenticate conference, $450 for plenary, or $1k for both.

It may also be possible to have a room for workshop/breakout. 

If you would be able to attend and would like to have a breakout f2f meeting, please speak up and contact Gail within the next few days. 


External Organizations (Dave/Nat)
===================================
ISO/TC 68 (Nat/Dave)
-----------------------------
* Nat will summarize TC 68’s activities and will forward to the WG
* Need to send a liaison report. 
* We are going to include FAPI 1.0 Final, FAPI 2.0 and Grant Managemen Implementer's Drafts, but if there are any other things notable to mention, please ping Nat. 

Australia (Dima/Joseph)
------------------------------------
OIDF to work on assessment for AAAC. They have provided direct funding for assessing :

* Migration from 1.0 to 2.0.
* Gaps relative to paper by OIDF in 2019 and 
* Any agreements or divergent views from recommendations in their 88 paper and decision 182
* Outlook of interoperability and future
* Other OIDF standards that may fit
* Mark Haine has agreed to help draft the paper
* MikeL will schedule call with CDR Team and ACCC to review updated outline

Berlin Group (Francis/Mike.L)
--------------------------------
* Ball is on their court. 
* Nat and Don is going to have a meeting with their leadership soon. 

Brazil (Mike)
---------------------------
* Still processing ph.2. 
* Oct 29 Ph. 3
* On track for RP test. 
* Adding payment and DCR to RP tests
* On track to launch RP community slack channel on Sept. 27. 


Canada (Gail)
------------------
* Reached out to FDATA. 
* Election happening: both parties want to move towards open banking. 
* Will look to connect with government players and intermediaries such as FDX


FDX (Gail)
------------------
Had a follow up conversation with Don Cardinal and team before EIC.

Licensing questions regarding certification program. Three options

a) Don’t pursue licensing at this time due. Premature time. Continue as is.
b) Avoid forking of specifications and code. May entail auditing of certification program to maintain integrity, certified trust mark, etc...
c) Fully license..

Voice of the room was to avoid forking and have WG control of specifications to maintain interoperability. This only 
applies to security profile and not functional requirements.

* Gail will draft document of key facts for WG and EC

Will provide details next week.

Mike Palage asked about registering the expired “OpenID Certified” trademark. Discussion to be take offline.


Middle East and North Africa (Ali)
-------------------------------------
Don, Ali, and Gail working on setting up workshops with emphasis on FAPI and eKYC in the Middle East. 

Details to follow. 

Initially, it will be in Dubai and could extend to Saudi and Bahrain. It will be around the region.

Scheduled call with Dubai International Financial Center on Sept 29.


Russia (Don/Dima)
--------------------
* Pinging them as of now. 


UK (Fiona/Ralph/Chris)
--------------------


PRs (Dave/Nat)
=================
n/a

Issues (Dave/Nat)
=====================
HTTP Signing (Dave)
----------------------------
* 411 
* There is a desire for it from Norway for non-repudiation. 
* https://bitbucket.org/openid/fapi/src/master/FAPI_2_0_Advanced_Profile.md

  * Currently Uses signed request objects via PAR, signed response via JARM and OIDC

* https://bitbucket.org/openid/fapi/src/master/Financial_API_Simple_HTTP_Message_Integrity_Protocol.md
* Dave provided two options: HTTP Signing and DPOP based one. 
* Travis pointed out the issue of DPOP being sensitive to clock synchronization and very little of message is actually signed.
* Dave and Brian’s DPoP based version adds the ability to sign the body digest but not headers
* Francis pointed out that a non-repudiation signing mechanism that doesn’t allow extensions would not be widely accepted due to Regional legislations that may not be interoperable.
* Need to define the goal of non-repudiation. Legal non-repudiation or just packet non-repudiation.
* Joseph pointed out that HTTP Signing is also used for transport security due to TLS removal beyond endpoints
* For increased interoperability, limiting to a single choice is best



AOB (Dave/Nat)
=================




The call adjourned at 15:__ UTC