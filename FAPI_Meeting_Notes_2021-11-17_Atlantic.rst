============================================
FAPI WG Meeting Notes (2021-11-17) 
============================================
* Date & Time: 2020-11-17 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-10-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * AF
  * Ali Adnan
  * Bjorn Hjelm
  * Brian Campbell
  * Chris Michael
  * Daniel Fett
  * Dave Tonge
  * Dima Postnikov
  * Domingos Creado
  * Don Thibeau
  * Francis Pouatcha
  * Joseph Heenan
  * Kosuke Koiwai
  * Lukasz Jaromin
  * Michael Palage
  * Mike Leszcz
  * Naohiro Fujie
  * Nat Sakimura
  * Stuart Low
  * Takahiko Kawasaki
  * Torsten Lodderstedt


* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Adopted as is. 

Events (Dave/Nat)
======================

OIDF virtual workshop (Mike L.)
--------------------------------
* Thursday, December 9th at 9 AM PT. 
* Link with registration details: https://openid.net/2021/10/19/registration-open-for-openid-foundation-virtual-workshop-thursday-december-9-2021/

Workshop with Berlin Group (Dave)
-----------------------------------
* WS -1 : Monday Nov 15th 1pm-4pm (CET)

  * Presented each other

    * Two areas to work on

      * Potential roadmap moving towards FAPI2, PAR, RAR
      * Embedded mode, still regulatory requirement in EU

* WS - 2: Wed Nov 24th (1pm to 4pm or 2pm to 5pm)
* WS - 3: Friday Dec 10th (2pm to 5pm)

Task force Advisory meeting yesterday

Will send feedback 

Will need more time to consider adopting FAPI 2.0 and PAR

Dave will perform analysis of needed changes to PAR, RAR for BG

BG supports non- pre-registration of redirect_uris, need migration path forward to PAR    


GSMA (Gail/Bjorn)
---------------------
The second workshop is on Nov. 29 for deeper technical dive. 

Will present updates on FAPI, MODRNA,, eKYC, Shared Signals and Events WG and Grant Management

Mike will create Workshop page on website for presentations and recordings.

OAuth Security Workshop (Daniel)
------------------------------------
OAuth Security Workshop 2021 is coming up https://barcamps.eu/osw2021/

Nov 30 - Dec 1, 2021

Free Virtual Event 

Session proposals are still accepted are scheduling

Nat will notify Connect WG members of requirement to pre-register 

Session topics:

* Browser interaction, third party cookies
* SIOP cross-device security, risk mitigation
* State of OAuth clients for modern security features


External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
n/a

Brazil (Mike L.)
---------------------------
OP certification still coming in. 

Two new members were added to certification team.

Slack channel for TPP/RP is becoming quite active. Membership discount is helping there.

Anticipate RP certifications to be forthcoming.

Chris asked if there is any plan for RP functional test -> No.

Functional tests are outside of certification scope.


Berlin Group (Francis)
--------------------------------
See Events. 

In addition, Francis will depart from Advisory boardis trying to find an editor from Berlin group to join FAPI WG. A colleague will also take over in the FAPI WG.

Canada (Mike)
------------------
Probably will be a month or two as new government has just been set up. 

FDX (Mike)
------------------
Blog post is coming up today or tomorrow. 

OIDF will follow with blog on OIDF website


The Middle East and North Africa (Ali)
---------------------------------------
Met with the strategy team last week. Want an MOU in place between DIFC and OIDF to outline the relationship.

Suggested an event in December to announce the partnership and start publicizing importance of standards (FAPI, CIBA) for open banking.

Also want to establish a OIDF MENA for banks, regulatory bodies, fintechs, possibliy funded non-profit.

Need to work on MOU.

Ali received OIDF Chapter policies from Gail and will structure the relationship, funding  accordingly and will inform DIFC of details.


Russia (Dima/Mike)
--------------------

Dima to follow up.


UK (Chris)
--------------------
CMA published an updated timetable for VRP. 


CMA9 was to have implemented sweeping use cases by January 

New deadline is to have testing finished with TPPs by June.

Will publish a decision in January about the future of OBIE.

Looks to align with FCA and PSR, regulators to define a roadmap for finance.

Expectation is that more RPS will start to be implemented more widely by next year’s end.


PRs (Dave)
=================
Introduce requirement for TLS, closes #446 (Stuart)
------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/293

Long discussion on how to recommend cypher suite etc. 
Both OIDC Core and TLS BCP is stale in this regard and there is even a proposal on https over QUIC which does not use TLS. 

Result: Use the following text -

Communication with the Grant Management API MUST use the "https" scheme.

This avoids references to other documents that can be outdated and the statement itself will not be outdated. 

Merged. 

grant_id is given but grant_management_action is not specified (Dima)
------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/290

Clarifies several scenarios where grant id is provided for create actions when it doesn’t make sense..

AS will return invalid request.

Merged

Introduce notational conventions. Closes #438 (Stuart)
------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/291

As it is envisioned to go to IETF eventually, we will use IETF style. 

Stuart will make corrections.

Introduce additional examples and remove reference to incremental auth, progress towards #441 (Stuart)
--------------------------------------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/292

Since incremental auth draft expired, it should be removed as an example.

Items will be directly transferred.


Issues (Dave/Nat)
=====================
What should the claims field hold?
----------------------------------------
* #450

Clarify that the definition of consented claims is up to the implementation when special scopes are used.

Dima will update PR.




AOB (Nat)
=================
none


The call adjourned at 15:00 UTC