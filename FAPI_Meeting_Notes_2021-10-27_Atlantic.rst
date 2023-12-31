============================================
FAPI WG Meeting Notes (2021-10-28) 
============================================
* Date & Time: 2020-10-28 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlanti20
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Ali Adnan
  * Brian Campbell
  * Chris Michael
  * Dave Tonge
  * Dima Postnikov
  * Domingos Creado
  * Edmund Jay
  * Filip Skokan
  * Francis Pouatcha
  * Gail hodges
  * Jacob Ideskog
  * Joseph Heenan
  * Lukasz Jaromin (Cloudentity)
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Takahiko Kawasaki (Authlete)
  * Travis Spencer (Curity)
  * Kosuke Koiwai

* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Adopted as is. 

Events (Dave/Nat)
======================

OIDF virtual workshop
------------------------------
* Thursday, December 9th at 9 AM PT. 
* Link with registration details: https://openid.net/2021/10/19/registration-open-for-openid-foundation-virtual-workshop-thursday-december-9-2021/

Workshop with Berlin Group
--------------------------------
* WS -1 : Monday Nov 15th 1pm-4pm (CET)

  * Need to collect reading material
  * Francis suggested using the Summary/Introductory document that the group wrote as starting point and send for feedback

* WS - 2: Wed Nov 24th (1pm to 4pm or 2pm to 5pm)
* WS - 3: Friday Dec 10th (2pm to 5pm)

TODO: Reading Materials

GSMA (Gail)
---------------------
* OIDF/GSMA Workshop is being planned towards the end of November to give them overview of OIDF projects. 
* Speakers tbd. 

External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
* Australia government has declined to proceed with the study
* Reaching out to Mark Savage if they need assistance in the assessment towards the certification. 
* AU Std Body published a paper outlining the staged approach to converge to FAPI 1.0. 

** LINK: https://github.com/ConsumerDataStandardsAustralia/standards/issues/209#issuecomment-945322753

Brazil (Gail/Joseph/Chris)
---------------------------
* Published new DCM test 1.5 w ago. 
* Some issues with the tests where instructions weren’t clear regarding client registration access tokens at the management endpoint
* Waiting for clear instructions on how to proceed as it will impact RP and OP tests
* Brazil will go live wit payments APIs on Friday
* Maybe less than half of banks are prepared
* Meeting to discuss how OIDF could discuss issues with Central Bank about moving goals



Berlin Group (Francis)
--------------------------------
* Focused on Workshop

Canada (Gail)
------------------
* n/a
* Probably a good time to reach out as the election has passed. 


FDX (Gail)
------------------
* Good conversation with Don Cardinal 
* FDX API is covering a very wide range of use-cases, e.g., checking, savings, mortgages, stocks payment, insurance, investment, etc. 
* Situation has changed from "there might be regulation" to "inevitable". 
* Some implementations of FAPI already in place in some major banks and RPs
* Large banks and large TPPs are connected via screen scraping and covering a large population. 
* ~110 millions accounts used for screen scraping.
* Currently, able to cover 30% of those users
* Certification to standards most likely 4-6 months away.
* FDX is preparing a blog post to be reviewed by OIDF. 
* Press release: https://financialdataexchange.org/FDX/News/Press-Releases/Financial_Data_Exchange_Releases_FDX_API_5.0.aspx
* Joint Whitepaper towards Govt may be possible. 
* Certification:

  * Currently focused on other areas 
  * Will get back to discuss in a couple of months on how to work together on certification



The Middle East and North Africa (Ali)
---------------------------------------
* Nov. 4 Strategy team @ DIFC Meeting. 
* Putting together a team for local WG including banks. 

Russia (Dima/Mike)
--------------------
* Fintech association Russia/OIDF meeting this Friday


UK (Chris)
--------------------
* n/a

PRs (Dave)
=================
n/a

Issues (Dave/Nat)
=====================
#443: Missing Discovery Metadata (Dave)
-----------------------------------------
Callers agreed to the approach - to add the metadata to FAPI CIBA. 


#411: HTTP Signing Scheme for FAPI 2.0 Advanced (Dave)
----------------------------------------------------------
Three options: 

* UK: Detached JWT
* BG: Draft Cavage and Draft HTTP Singing @ IETF
* DPoP: 

HTTP Signature mechanism for PoP seems controversial and not yet adopted.

For implementer’s draft, may have 3 different options and then select one as mandatory in the final draft. 

Need some implementation experience.


#455: Impact of grant_management_action=update (Dima)
-----------------------------------------------------------
This issue relates to how we represent historical updates to Scopes and resources relationship and when we query grant management APIs

There was a suggestion to Flatten the structure but it was pointed out that it might be too much change introduced to the ecosystem.

Maybe too complex for too little value.

Introducing a new structure into access tokens is too invasive for a theoretical problem.

Brian suggested that putting guards  at the data model or restricting what’s actually issued or being careful with what's issued would be sufficient to address the issue.



AOB (Nat)
=================
The FDX Blog Post (Gail)
----------------------------
WG discussed the blog post text to come and made some edits to the text.

Changed protocols to standards

Put more emphasis on security and interoperability

A modified sister blog will also be posted on OIDF website


Two Open Polls 
-----------------------
* Federation
* eKYC & IDA


The call adjourned at 15:00 UTC