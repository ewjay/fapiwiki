============================================
FAPI WG Meeting Notes (2022-04-13) 
============================================
* Date & Time: 2022-04-13T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Nat/Dave)
======================
* Attending: 
* Regrets: Mike L. 
* Guest: 

Adoption of Agenda (Nat)
================================


Events (Nat)
======================
OpenID Foundation Mountainview Workshop (Mike)
----------------------------------------------------
* April 25 @ Google. 
* Link: https://openid.net/2022/03/22/registration-open-for-openid-foundation-workshop-at-google-monday-april-25-2022/
* Hybrid 
* Registration needed and is closing in a few days: https://openid.net/2022/03/22/registration-open-for-openid-foundation-workshop-at-google-monday-april-25-2022/



OpenID Foundation Berlin Workshop (Mike)
------------------------------------------
May 10, Tue. 

https://www.kuppingercole.com/sessions/5048/1

OSW 2022 (Daniel)
--------------------
* May 4 - 6 @ Trondheim
* In-person only
* https://oauth.secworkshop.events/osw2022

OIDF and Microsoft sponsored the event. 
 
Tickets are still available. 


Internal Liaison (Nat)
================================
n/a


External Organizations (Nat)
===================================
Australia (Gail/Mike L.)
------------------------------------
n/a

Brazil (Mike L.)
---------------------------
n/a

Berlin Group (Daniel)
--------------------------------
Follow up meeting has not happened but wrote that certain technical items. 

Regulators in Israel asked BG to a localised version of the 1st phase of OB implementation. 
(Account info)

Payment initiation hoping to align both BG and FAPI. 

Global Open Finance Technical Working Group has a plan to meet on May 5. 
Dave and Gail will be presenting on behalf of OIDF. 

Global Open Finance Technical Standards Work Group Meeting- Member Presentation: OpenID Foundation presentation on Open Banking, Open Data and Financial-grade APIs
OpenID Foundation Whitepaper on Open Banking
International movement towards Open Banking, Open Finance, and secure, consent driven access to all user data.
Financial-Grade API (FAPI) Working Group’s experience with Open Banking ecosystems internationally
Process of standards development, user experience, consent flow, security research
Attack and threat model, mathematical proofs, testing implementations
The role of conformance testing in driving out inefficiency and improving security
Selected studies in implementation (UK, Australia, Brazil). What did we learn?
Questions and comments
Member Presentation: Berlin Group
Story of Berlin Group and PSD2
Structure, Governance, standards development,
Specifications rather than implementation
From PSD2 to Open Finance - scope of thinking
Exploring relationship with FAPI
Questions and Comments

Brian.Costello@ed.ac.uk

5 May from 11:00 AM – 13:00 PM BST.


FDX (Mike L.)
------------------
* n/a

GAIN (Mike L.)
---------------------
* CG meeting is going well. 
* Speaking at EIC, Identiverse, etc. 

ISO/TC68 (Nat/Dave)
----------------------
* n/a

The Middle East and North Africa (Chris)
-----------------------------------------
* Israel: see BG. 
* Saudi: Waiting for project to officially kick off. 1st standard to come in June. Very strong regime of certification. 
* UAE etc. would be following soon. 

Mexico (Gail)
------------------
* n/a

Nigeria (Mike)
---------------
In the process to schedule a second call.

OECD (Nat)
-------------


UK (Chris)
--------------------
* Published ver. 3.1.10 -- final version to be published under CMA order. 
* What happens to OBIE, Open Finance, etc. is not known yet. 


USA (Gail)
----------------
n/a 


Specs (Nat)
================
Grant Management (Dima)
----------------------------------------
n/a


FAPI DCR/M (Dynamic client registration and Management) (Joseph)
-------------------------------------------------------------------------
* No updates in spec. 
* Brazil is using subject dn in DCR but changing CA later this year. 

Advanced authorization (Dima)
----------------------------------
n/a

FAPI 2 Attack, Baseline and Advanced (Daniel)
----------------------------------------------
* Perhaps look at the open issues at OSW. 

JARM (Brian)
----------------------------------------
* PR is being prepared. 

PRs (Dave)
=================
PR323 (Brian)
-------------------
* To be merged. 

PR315 
-------------------
* Change to a note. 
* Move to "advanced" as there is no JARM in baseline anymore. 

PR324 Remove reference to RAR in FAPI 2 baseline (Dave)
---------------------------------------------------------
* Brian asked if it is wise to push all the authorization stuff to advanced. 
* Joseph seconded. 
* Perhaps call for an additional co-editor? 

PR325 
---------------------------------------------------------

PR322 Pull-in key management clauses
---------------------------------------------------------
* Build error needs to be fixed. 
* Joseph pointed out that we technically require jwks_uri - we require OIDC discovery, and jwks_uri is required in Final: OpenID Connect Discovery 1.0 incorporating errata set 1. 
* Will continue discussing. 

PR326 FAPI2Base: Disallow dpop nonces
---------------------------------------------------------
* WG agreed to remove dpop nonces on the condition that if the FV finds it to be needed we add it back. 
* We need to have a new issue around the OIDC nonce. 

Issues (Dave)
=====================
We were not able to cover it. 



AOB (Nat)
=================
* Please review https://bitbucket.org/openid/fapi/issues/492/eddsa-in-fapi-20



The call adjourned at 15:00 UTC