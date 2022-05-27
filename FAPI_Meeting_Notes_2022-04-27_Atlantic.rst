============================================
FAPI WG Meeting Notes (2022-04-27) 
============================================
* Date & Time: 2022-04-27T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-27_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

  * David Januchowski
  * Filip Skokan
  * Joseph  Heenan
  * Elizabeth Garber
  * Nat Sakimura
  * Dave Tonge
  * Takahiko Kawasaki
  * Brian Campbell
  * Lukasz Jaromin
  * Dima Postnikov
  * Craig Borysowich
  * Domingos Creado
  * Chris Michael
  * Michael Palage
  * Bjorn

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================


Events (Nat)
======================

OSW 2022 (Daniel)
----------------------
May 4 - 6 @ Trondheim
In-person only

https://oauth.secworkshop.events/osw2022

Event is now sold out

EIC/OpenID Foundation Berlin Workshop (Mike)
----------------------
May 10, Tue.

https://www.kuppingercole.com/sessions/5048/1


Identiverse
----------------------
Denver, Colorado  June 21-24, 2022

https://identiverse.com/


Internal Liaison (Nat)
================================
Certification (Joseph/Mike)
----------------------------


External Organizations (Nat)
===================================
Australia (Mike L.)
------------------------------------

Brazil (Mike L.)
---------------------------

Berlin Group (Daniel)
--------------------------------

EU DIW ARF (Gail)
------------------
* n/a

FDX (Rifaat)
------------------

GAIN (Dima)
---------------------
Group is still forming

Looking at different options for trust management

* How to trust participants from different ecosystems
* How to determine the level of trust and level of participation in the network

FAPI  is used together with eKYC for identity assurance



IETF OAuth WG (Rifaat)
-------------------------
Call for adoption for the Step Up Authentication draft by Brian and Vittorio

ISO/TC68 (Nat/Dave)
----------------------
* n/a

The Middle East and North Africa (Chris)
-----------------------------------------
* n/a

Mexico (Gail)
------------------
* n/a

Nigeria (Mike)
---------------

OECD (Nat)
-------------
* n/a


UK (Chris)
--------------------
* n/a


USA (Gail)
----------------
* n/a 


Specs (Dave)
================
Grant Management (Dima)
----------------------------------------
Will work on issues at OSW and EIC

FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* N/A 

Advanced authorization (Dima)
----------------------------------

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
* N/A

JARM (Dave)
----------------------------------------
 

PRs (Dave)
=================



Issues (Dave)
=====================

493 - certification query: supply of TLS client certs & use of mtls_endpoint_aliases
--------------------------------------------------------------------------------------

#493 - certification query: supply of TLS client certs & use of mtls_endpoint_aliases

It’s about mtls_endpoint_aliases and how that works and certification

It’s problematic when used with ecosystems and PAR

In UK, banks all have MTLS protected endpoints

FAPI required MTLS sender constraining at the token endpoint

There are doubts on when mtls_endpoint_aliases should be used if MTLS is required on top of private key JWT

Client behavior is not defined

Some view that MTLS is just a transport layer and the client should not need to care

If there is a need to use MTLS and non-MTLS endpoints, there is no need to use mtls_endpoint_aliases

Problem can be solved by mtls offload proxies

Not sure how to implement the conformance test due to uncertainty

Current 3 FAPI ecosystems are requiring MTLS everywhere, will be problematic if each uses different approach for using mtls_endpoint_aliases

Should be treated as transport layer

Should FAPI 2 Advance have a use case for using MTLS everywhere and add a note on how to interpret the use of mtls_endpoint_aliases?

Joseph will summarize the issue and draft a PR with note.



495 - Certification: Requirements for alg support in RPs/OPs
-------------------------------------------------------------
#495 - Certification: Requirements for alg support in RPs/OPs

Should certification reflect support for the various algs? Doing so will allow discovery of problems with various algs but will make certification tables unwieldy. There will be a presentation problem.

If certifying for Eddsa, will have to support DPOP, private_key_jwt and OpenID

Google has  a crypto test suite with tests vectors for testing correct implementation

Could add some of those tests into the certification suite.

Should FAPI tests the JOSE specs as much as possible?

Doing so could add lots of complexity.

There is no clear line of distinction on what should be tested at which level. 

Should the certification suite be responsible for testing them?

Joseph and his team to investigate and summarize the issue.

Testing every possible combination is impossible but maybe a few select  tests.


AOB (Nat)
=================
* none



The call adjourned at 15:59 UTC