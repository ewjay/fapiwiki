============================================
FAPI WG Meeting Notes (2022-05-11) 
============================================
* Date & Time: 2022-05-11T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-05-11_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

  * Brian Campbell
  * Dave Tonge
  * Filip Skokan
  * Kosuke Koiwai
  * Nat Sakimura
  * Ralph Bragg
  * Takahiko Kawasaki

 

* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
================================


Events (Nat)
======================
EIC
----------------------
Happening this week


Identiverse
----------------------
https://identiverse.com/

Denver, Colorado

June 21-24, 2022




OSW 2022
----------------------
May 4 - 6 @ Trondheim

Had WG meetings regarding FAPI 2.0 and Grant Management

Resolved many issues with Grant Management and will update next draft

Had discussion about RAR and it is now removed from Baseline to simplify it

Have pointers to components of FAPI 2 Framework mentioned 

Another idea was potentially changing FAPI 2 Advanced to FAPI 2.0 Message Signing since currently it only contains various mechanism to do message signing on authorization request/response, HTTP messages

Talked about stripping CIBA out to make it work with Baseline

Also Baseline will mention RAR in the introduction so it’s not normative but will reduce need for another spec

Name changes will affect Australia which has 2 ecosystems.

It’s using FAPI 2.0 Advanced 

Not being prescriptive in specs will cause fragmentation

Adopted specs should not allow picking of various components which will cause fragmentation like Australia Consumer Data Rights

OIDF needs to manage the messaging of FAPI 2.0 name change

Different ecosystems will have different options which will cause fragmentation leading to global interoperability problems.

FAPI 2.0 Baseline will only have minimum components  needed to achieve security goals and protect against the attacker model.

Ralph stated that WG needs to make global interoperability a priority rather than just certification.

Keep Baseline as is but OIDF should work with various certification bodies to agree on a single security profile.

Look at commonality used across ecosystems and create a profile suitable for interoperability.

There seems to be confusion regarding removing the Advance profile and the creation of an Advance Authorization profile.

The WG actually discussed stopping work on Advance Authorization and put pointers to RAR, Grant Management, etc. into Baseline instead. Advanced profile will remain unchanged with the possibility of a rename.

Instead of requirements in a spec, it might be better to have a named set of specs and call it the Global Interoperability Profile.

Dave will create/update issue and solicit feedback from WG.



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

PR #315 - FAPI2 iss + JARM
--------------------------
PR #315 - FAPI2 iss + JARM

Related to #478  - FAPI2 Baseline + jarm & iss draft

JARM requires all parameters to be inside the JWT

Adds note that Iss should be in the JWT

Wait for Daniel’s approval before merge


PR #333 - Link advanced profile and attacker model
--------------------------------------------------
PR #333 - Link advanced profile and attacker model

Adds attacker model and definition of non-repudiation to Advanced profile

Leave open for comments


PR #331 - Add clauses for dpop nonce
------------------------------------
PR #331 - Add clauses for dpop nonce

AS MAY use DPoP nonce and requires SHALL for clients for interoperability reasons

PR #332 - Simplify RS access token guidance
-------------------------------------------
PR #332 - Simplify RS access token guidance

Simplified the language requiring the AS to verify the entity associated with the access token has sufficient access for the resource


PR #322 - Pull in key management clauses
----------------------------------------
PR #322 - Pull in key management clauses

Related to #484 -  Key management in FAPI2 Advanced

Still work in progress

Adds Date header for HTTP message signing

Added note regarding keys since HTTP Signatures does not mention them 

RS can retrieve keys from AS, third-party, or other means.

Adds jwks_uri as requirement for discovery

Clients shall use jwks_uri or jwks

PR #335 - Add "may" clause for client credentials grant
-------------------------------------------------------
PR #335 - Add "may" clause for client credentials grant

Listing only client credentials grant but not others may cause confusion that it is the only accepted grant type

Need to add note to allow other appropriate grant types

Leave open for comments

PR #334 - Restructure FAPI2 baseline
------------------------------------
PR #334 - Restructure FAPI2 baseline

Adds client credentials and links CIBA and other grant types

Should separate the authorization flow and the generic clauses

Groups authorization code flow requirements to improve readability

Dima will double check


Issues (Dave)
=====================

#452 - When the user being authenticated is different from the user of the grant
--------------------------------------------------------------------------------
#452 - When the user being authenticated is different from the user of the grant

When an authenticated user is different from the resource owner, an error should be returned.

There was discussion about relaxing the language for use cases such as some people at a company reauthorizing some banking connection to an accounting app.In this case, the end user and grant ID doesn’t need to be exact.

Relax language to say resource owner rather than user.


#436 - Change grant_management_action "update" to "add" or "append"
-------------------------------------------------------------------
#436 - Change grant_management_action "update" to "add" or "append"

Decided to change to merge

#296 - Treatment of subject in id_token used for code detached signature
------------------------------------------------------------------------
#296 - Treatment of subject in id_token used for code detached signature

The issue no longer applies.

Closed.



AOB (Nat)
=================
* none



The call adjourned at 15:59 UTC