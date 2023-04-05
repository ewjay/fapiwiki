============================================
FAPI WG Agenda & Meeting Notes (2023-04-05) 
============================================
* Date & Time: 2023-04-05T14:00Z
* Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2023-03-15_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:02 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Filip, Nat, Brian, Chris, Dima, Dave, Kosuke, Reinaldo, Craig, Takahiko
* Regrets: Mike Leszcz, Joseph Heenan, 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Adopted as presented as draft agenda. 
  * SmartData Foundry. 


Events (Mike L)
====================================================
OpenID Foundation Workshop (Mike)
---------------------------------------
* Registration page is now open. 
    * https://openid.net/2023/03/17/registration-workshop-at-microsoft/

Events are now in the Foundation Google Calendar (Mike)
------------------------------------------------------------
* In the new website, it is going to be a single source. 

Internal Liaisons
======================
NIST SP800-63-4ipd Comments
------------------------------
* Mark is leading the discussion. Several meetings. 
* Deadlines were postponed to April 14. 
* Nat has provided a few comments pointing to FAPI as a good practice for security - security is typically not composable and has to take the protocol as a whole with an appropriate security model and analysis to go with. 
* Link to the comment sheet that OIDF is compiling: 
    * https://docs.google.com/spreadsheets/d/1JHDypzbKg8x2AMfC_z4pzDBk4waVJBp2/edit#gid=571622526

“Government-issued Digital Credentials and the Privacy Landscape” whitepaper 
----------------------------------------------------------------------------------
It is now open for comment: https://openid.net/2023/04/05/open-for-comment-privacy-landscape-whitepaper/ 
Please comment. 

External Orgs & Liaisons (Nat/Mike L.)
============================================
Open Finance Brazil (Nat/Mike)
--------------------------------
* OIDF continue to receive FAPI recertification requests as mandated by OFBR. 

Open Insurance Brazil (Nat/Mike)
--------------------------------------
* We continue to receive OP and RP cert requests. OPIN is considering mandating FAPI recertification and we are engaged in the conversation and working to clarify OPINs recent requirements. 

Saudi Arabia (Mike/Chris/Nat)
------------------------------------
* We continue to receive OP and RP cert requests from SAMA participants.
* Recertification is likely to be on FAPI2. 

SmartData Foundry (Chris)
--------------------------
A standards comparison table is being compiled. 
Volunteers to review / add content are sought. 

Currently, it includes: 

* Bahrain Open Banking Framework - Bahrain OBF
* Bank Interfaces for Standardized Payments - BISTRA
* Consumer Data Standards - CDR
* Czech Standard for Open Banking - COBS
* Financial Data Exchange API - FDX
* Open API Framework for Hong Kong
* India Stack
* Japan Open Banking Framework
* NextGenPSD2
* Open Banking In Nigeria (draft)
* API Centre standards
* Open Banking Brasil
* PolishAPI
* STET PSD2 API
* Singapore Financial Data Exchange - SGFinDex
* Slovak Banking API Standard
* SNAP
* KSA Open Banking Standard
* Open Banking Platform
* Swiss NextGen API
* UK Open Banking Standard

Also, we need to find out what is the best way of crediting individuals and the foundation of the work. 
Chris will ping Gail and Nat on this. 

Draft Updates
====================
Message Signing (Dave)
--------------------------
* Dave has sent the fixed Implementer's draft documents to Mike J. 

Grant Management (Dima)
--------------------------
* Dave is creating a submission package now. 

PRs (Dave)
===============
* Apart from one PR that we are parking until HTTP signature is settled, there is no standing PR. 
* Request/Response binding fix is waiting for IETF result next week. 


Issues (Dave)
==================
Proposed new FAPI certification test: private_key_jwt client authentication assertion where aud contains multiple values (Filip)
------------------------------------------------------------------------------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/403/proposed-new-fapi-certification-test
* related to #501
* see https://bitbucket.org/openid/fapi/issues/403/proposed-new-fapi-certification-test as well. 
* Filip is going to record the result of the discussion in the ticket. 

private_key_jwt audience requirements (Filip)
-----------------------------------------------
* https://bitbucket.org/openid/fapi/issues/581/private_key_jwt-audience-requirements
* Agreed that the PR is OK. 
* Nat to confirm with Torsten. 

FAPI2SP appears to permit response_types "id_token", "id_token token" and "none" (Dave)
----------------------------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/577/fapi2sp-appears-to-permit-response_types
* Dave to create a PR. 

FAPI CIBA (Dave)
---------------------
* https://bitbucket.org/openid/fapi/issues/580/fapi-ciba
* Discussed the changes it needs for supporting FAPI2. 
* Whether signing is required or not should be based on whether the base profile requires signing (e.g., FAPI2 Message Signing + CIBA should require it, while FAPI2 Security Profile + CIBA should not.)
* 5.2.2.6
* Assigned to Filip. 

FAPI2MS: Rejection of non-JAR/non-JARM requests (Filip)
------------------------------------------------------------
* https://bitbucket.org/openid/fapi/issues/576/fapi2ms-rejection-of-non-jar-non-jarm

Network Layer Protections restrict use of more recent TLS 1.2 cyphers
----------------------------------------------------------------------------
* Moving to TLS 1.3 removes the restrictions on the cyphers. 
* However, the certification suite does not support TLS 1.3. 
    * Nat to create an issue on the tracker regarding this. 

AOB (Nat)
=============
* none

The call adjourned at 14:59