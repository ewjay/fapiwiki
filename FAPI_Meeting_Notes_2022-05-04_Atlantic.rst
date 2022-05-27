============================================
FAPI WG Meeting Notes (2022-05-04) 
============================================
* Date & Time: 2022-05-04T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-05-04_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:00 UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

  * Filip Skokan
  * Lukasz Jaromin
  * Mike Leszcz
  * Takahiko Kawasaki
  * Travis Spencer
  * David Januchowski
  * Dave Tonge
  * Michael Palage
  * Nat Sakimura
  * Joseph Heenan
  * Brian Campbell
  * Dima

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================


Events (Nat)
======================

IIW Workshop 
----------------------
Google — Monday, April 25, 2022

Workshop recordings and presentations are available on the OIDF website.

https://openid.net/workshops/openid-foundation-workshop-at-google-monday-april-25-2022/

Another workshop will take place at EIC in Berlin, May 10, Tuesday local time



Internal Liaison (Nat)
================================
Certification (Joseph/Mike)
----------------------------
Brazil asked for a new DCR test to test the subject DN field can be updated using Dynamic client management and the new subject DN works correctly.

Will require Brazil to issue some certificates that have different subjects.

This is due to banks wanting to transition away from a certain cert authority to another one that issues certificates with subjects in different formats.



FAPI 2 RP and OP tests are ongoing

Working to address Filip’s feedbacks.

Tests are available but are not on public servers yet.

Interested parties should contact Joseph.


External Organizations (Nat)
===================================

University of Stuttgart
------------------------------------
Contract is in the final signing process with the University to begin FAPI  Security Analysis

A brief overview of what has been done was presented this morning at OSW.


Canada Open Banking
------------------------------------
The group will regroup and then come back for a deeper dive into the specs, roadmap from 1.0 to 2.0, and certification.

Mike will update when a date is scheduled.

Thailand
------------------------------------
Thailand tasked one of the British departments to do a report on open banking and rollout.

FAPI was recommended to them.


Australia (Mike L.)
------------------------------------
Elections are taking place

Brazil (Mike L.)
---------------------------
Still working to finalize CIBA specification.

Timeline and requirements are not available yet.

Development on CIBA tests  will be paused until the specification is completed.

Another DCR test will be added to the conformance suite and will be available at the end of May for testing before being put into production.

Testers will be identified to test it.



Berlin Group (Daniel)
--------------------------------
Will have a coordination call with BG this week.


EU DIW ARF (Gail)
------------------
* n/a

FDX (Rifaat)
------------------

GAIN (Dima)
---------------------
* 

IETF OAuth WG (Rifaat)
-------------------------

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
Currently on pause to do internal coordination.

Mike will reach out to the team to see when they’ll be prepared to continued moving forward.


OECD (Nat)
-------------
Comments have been submitted



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


PR #326 - FAPI2Base: Disallow dpop nonces
------------------------------------------
PR #326 - FAPI2Base: Disallow dpop nonces

FAPI 2 is not requiring the use of DPoP nonces

Add note to make it clear that nonce is not required because clients are expected have good, synchronized times and are 
enforcing time validity iat/exp/nbf claims

Joseph will create another merge request for the note

iat leeway needs to be defined for acceptable values.

Mobile devices will sometimes have clocks that are intentionally changed for games, etc..

So assumption that clocks are synced is wrong

The reason to disallow nonces is to simplify implementation 

Clients and servers need to keep track of most recent nonce

Removing nonces may be deal breaker outside of banking

Need to provide justification for the exclusion of DPoP nonces

Private Key JWT will have same problems

Dave will create a new issue



PR #329 - Add a note about mtls_endpoint_aliases
------------------------------------------
PR #329 - Add a note about mtls_endpoint_aliases

Added note that Ecosystems which require people to use TLS client certificates, in cases where the protocol doesn't require it, mtls_endpoint_aliases should not be used.

Will be merged


Issues (Dave)
=====================
#469 - Add protocol version and variant identifier
---------------------------------------------------
#469 - Add protocol version and variant identifier

Generally good practice with security protocols to have the protocol version of Variant Identifier.

Discussed whether it should be done at discovery or registration

Taka suggested ecosystems define  a particular profile

Could also be part of metadata going into software statement

Might be useful in transition migrations

Should work on a migration document for FAPI 1 to FAPI 2




AOB (Nat)
=================
* none



The call adjourned at 15:59 UTC