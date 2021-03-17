============================================
FAPI WG Meeting Notes (2021-03-17) 
============================================
* Date & Time: 2020-03-17 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Don, Sngeetha Radhakrisknan (Microfocus), Kosuke Kowai, Ralph, Joseph, Barry, Dima, Taka, Francis, Lukasz Jaromin (cloudentity), Brian, Stuart, Chris Michael (Ozone), Vinod, Bjorn
* Regrets: Dave
* Guest: Fiona Hamilton (Open Banking)

Adoption of Agenda (Nat)
===========================
* Adopted as is. 

Finalization of FAPI 1.0 (Nat)
===============================
* Published On March 12. 

External Organizations (Nat)
================================
W3C Web Payment Interest Group (John)
--------------------------------------


Australia (Dima/Stuart)
----------------------------------
* FAPI WS planning undersay. It will be announced by next week. The first one will be 20th of April. 
* Dima is getting his organization's implementation to get certified including PAR, which will be the first. 

Berlin Group (Francis)
---------------------------
* Francis is drafting a letter to be sent from BG to an official application to OIDF. 

Brazil (Chris/Ralph)
----------------------
* Formal acceptance of FAPI Advanced and certification. 
* Dynamic scope, not PAR. 
* 830 banks registered (440 or so is under one cooperative)
* No news of RP testing though they are looking at. Chris believes it will be a year two thing. 

* There is no link. Redirect Mandatory, CIBA optional. 
* Security profile is not existent. 
* Working document: https://openbanking-brasil.github.io/areadesenvolvedor-fase2/#financial-grade-api-fapi
* It is not yet in a usable form. It is still a fork of AU. 
* Standard Body: Open Banking Brazil. MIRO is the consulting party. 
* Central bank made this happen. 

Canada (Ralph)
------------------
N/A

UK (Don/Ralph)
-----------------
* Meetings being scheduled. 
* Recurring payments standard (optional) will be announced next week. 
* Consultation from CMA on the next steps of OBIE. 
* Approval from the eKYC WG to extend the customer attribute. 
* OBIE job will be transitioned Fiona. 

USA (Joseph)
--------------
* FDX security committee is finalizing the review of FAPI 1.0 for approval. 
* Joseph will be giving updates on FAPI in April in their FDX Global Summit. 

Events (Nat)
======================
GOFCOE/GOFTS (Don)
-------------------------
* A bit of grey area between adoption and official announcement. 
* We still lack the central reference to look at. GOFCOE could create a library that could work as a global reference point. 

FIN/SUM 2021 (Nat)
----------------------------



PRs (Nat)
===================
247: Grant Management Refactoring & Clarification (Torsten)
---------------------------------------------------------------

249: Grant Management Refactoring Alternative (Torsten)
---------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/249

247 and 249 are two approaches on one issue. 
People's preference seems to be 249 so it will be merged into it. 

Taka compiled a table on the use-cases. 
It was compiled with an assumption that a new grant_id will be issued from the token endpoint as the response. 
Torsten pointed out that he was assuming that the same grant_id as in the request is being returned from the token endpoint. Ralph agreed. 

Lukasz: Two use-cases. Single grant gets updated. In AU - there will be concurrent grant_ids. If in the later case, no one is expecting the grant to be updated. 

Dima pointed out that something like refresh token exchange could happen, but in that case they will not exist in parallel. 

Replacing the grant_id seems reasonable but no parallel grant_id based on a single baseline grant. 

Stuart 



251: Grant Management: Use cases section added (Dima)
---------------------------------------------------------------


Issues (Nat)
===============
Skipped. 

AOB (Nat)
=============


Chat Log
============
Joseph Heenan (Authlete / OpenID Foundation) to Everyone
https://openbanking-brasil.github.io/areadesenvolvedor-fase2/#financial-grade-api-fapi

23:22Don Thibeau to Everyone
https://openid.net/2021/03/12/fapi-1-0-part-1-and-part-2-are-now-final-specifications/

23:23Don Thibeau to Everyone
https://openid.net/2021/03/16/standards-adoption-and-the-adoption-of-standards-financial-grade-api-fapi-1-0-final-specifications-published/

23:45Me to Everyone
https://bitbucket.org/openid/fapi/pull-requests/249

23:46Chris Michael to Everyone
apologies I have to drop off now

23:49Me to Everyone
Thanks for joining > @Chris.

23:56Fiona Hamilton Open Banking to Everyone
Sorry got to drop off. Thanks

0:01Vinod (self) to Everyone
Apologies I have to drop off, thanks !

0:01Barry ODonohoe (Raidiam) to Everyone
I also need to drop - bye for now