============================================
FAPI WG Meeting Notes (2022-06-08) 
============================================
* Date & Time: 2022-06-08T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 

  * Brian Campbell 
  * Dave Tonge
  * Dima
  * Filip Skokan
  * Joseph Heenan
  * Lukasz Jaromin
  * Mike Leszcz
  * Naohiro Fujie
  * Rifaat Shekh-Yusef
  * Takahiko Kawasaki
  * Bjorn Hjelm
  * Domingos Creado
  * Kosuke Koiwai
  * Michael Palage

* Regrets: 
* Guest: 

Adoption of Agenda (Dave)
================================


Events (Dave)
======================
Identiverse (Mike)
------------------------------
* F2F FAPI meeting Wednesday 6/22 normal meeting time
* Remote attending available. 


Internal Liaison (Dave)
================================
Security Analysis
---------------------------
* Australian university awarded contract so that the second part of the security analysis can go ahead. 
* Formal definition by U. of Stutgart is scheduled to be completed by end of June

  * Technical report by end of June
  * Presentation in mid-July

* Australian University will look at Grant Management and also apply security analysis to Australian CDR standard


Certification (Joseph/Mike)
----------------------------
* Brazil – certificate issues. 





External Organizations (Nat)
===================================
Australia (Mike L.)
------------------------------------

Brazil (Mike L.)
---------------------------
Brazil CIBA spec is still in the process of being finalized.

Scheduled to be finalized next week 

Other milestones to be confirmed.

Open banking Brazil will start recertification for banks from September to December 15

Central bank is signaling annual recertifications for FAPI

There is a new test for the updating of TLS client subject DN in Dynamic Client Management endpoint. Only available for functional testing but not for generic testing due to requirement for 2 valid certificates.

Comparison rules for DN still need to be defined.

Access to Brazil sandbox is not open. Registration is only allowed for 10 countries but can be tested with specific configurations.



Open Insurance Brazil

66 institutions to be certified in September

OIDF will host a couple of outreach workshops in July and August  to introduce FAPI and conformance certification


Berlin Group (Daniel)
--------------------------------
* N/A

Canada (Gail)
-----------------


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
* JWK thumbprint was approved by IESG.
* DPoP – Brian is addressing the issues collected. After that, Rifaat will do the shepherd write-up.  

ISO/TC68 (Nat/Dave)
----------------------
* n/a

The Middle East and North Africa (Chris)
-----------------------------------------
* Meeting with Open Banking Saudi Arabia during Identiverse. 

Mexico (Gail)
------------------
* n/a

Nigeria (Mike)
---------------
* Follow-up call is scheduled for June 16.

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
Addressing "User Interface Hijack attack" in FAPI 2? (Nat)
-----------------------------------------------------------
* https://lists.openid.net/pipermail/openid-specs-fapi/2022-May/002619.html
* Provide incentives for ecosystems to adopt FAPI 2 if addressed
* Discuss on list and next call


Grant Management (Dima)
----------------------------------------
* There are now a couple of PRs and Issues. 

FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* N/A 

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
* Name change PR etc. is yet to be created. 

JARM (Dave)
----------------------------------------
* https://openid.bitbucket.io/fapi/openid-fapi-jarm.html
* Need feedback before last call for final draft.
 

PRs (Dave)
=================

To be merged
----------------

* PR #336 -  rename update to merge
  
  * Need to sync with latest revision before merge

* PR #341 – Grant Management - clarify scopes  related to #448 (one or more resource fields?)

  * Torsten had proposed some editorial text 

* PR #340 – JARM security properties - Attempt to finesse some text in JARM so as to not overstate its security properties

  * Discussed by various members
  * There was intention to use the encryption part of JARM from Australia but the text seems to over promised on the security properties of using encryption  alone
  * No protocol changes but to be honest about the security properties of JARM.
  * Would like to adjust text to reflect what security properties JARM provides by itself to give accurate representation and not do unneeded actions
  * More editorial changes like removing references that are not used. 
  * It is possible to tidy up more but perhaps it is not worth investing the time. 
  * Financial-grade text also removed to align with oncoming name change of spec
  * Dave is going to send out the last call email after merging it. 


Under discussion
----------------------

Issues (Dave)
=====================

* #501 - Clarify that authorization response encryption is not required for FAPI2 + Message signing / JARM

  * Australia is in transition to FAPI 2 and JARM will be required
  * Asked by encryption is required for JARM
  * Dima discussed with others and conclusion was

    * Encryption is not needed since there is nothing sensitive about the authorization response (only code and issuer)

      * Update JARM spec to be clear about what’s protected or not
      * Clarify in Message Signing profile that only response signing is required
      * Issue regarding nonce was raised (#502 - Is nonce required with JARM?)

  * Dima will make PR 


* Attacker model 

  * Nat raised question in mailing list - https://lists.openid.net/pipermail/openid-specs-fapi/2022-June/002624.html
  * Model allows compromised browser to a certain degree
  * Assumed front-channel redirected  can be tampered / replayed
  * Need to discuss with Daniel and  U of Stuttgart
  * Combination of PAR/PKCE removes a lot of tampering attacks

* #496 - clock sync and FAPI2 baseline

  * Added nonce back to DPoP to deal with clock skew
  * Using FAPI 2 on user controlled device will most likely use private key JWT and DPoP instead of MTLS
  * Private key JWTs will have clock skew issues also
  * Solution requires DPoP nonce at the AS or use other time sources but will be tricky since NTP isn’t done over TLS
  * Private key JWTs and DPoP proofs can be pre-computed on user controlled device
  * DPoP nonce is used to correct time skew 
  * Attack might be theoretical and may not need to be addressed for JWTs
  * Need more feedback and maybe add a note
  * WG to make decision after further discussion with Travis 


* #484 - Key management in FAPI2 Advanced

  * Do we need to specify normative text for key reuse or leave it to implementations?
  * DPoP assumes no key reuse, but there is no clear guidance
  * Will be silent regarding key reuse, will use recommendations for jjwks_uris from FAPI 1.0



AOB (Dave)
=================
* none



The call adjourned at 15:59 UTC