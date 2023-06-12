============================================
FAPI WG Agenda & Meeting Notes (2023-06-07) 
============================================
* Date & Time: 2023-06-07T14:00Z
* Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2023-05-24_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Kosuke, Nat, Brian, Takahiko, Domingos, Peter Stanley, Lukasz, Bjorn, Victor Lu, Dima
* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Added Camara Project. 


Events (Mike L)
====================================================
Identiverse (Mike L)
-----------------------
Identiverse was last week.

There were quite a few sessions on FAPI.

OAuth Security Workshop (Daniel)
-------------------------------------
* August 22-24, 2023, Royal Holloway University, London/UK
* The site https://oauth.secworkshop.events/osw2023 opened. 
* Call for papers
* Some travel information is also available. 

IETF
-------------------------------------
* July 22-28, 2023. San Francisco, USA 
* https://www.ietf.org/how/meetings/117/

External Orgs & Liaisons (Nat/Mike L.)
============================================

OFBR
-----------
Continue to process FAPI recertification requests. CIBA Squad recently sent updated OFBR CIBA spec which is still to be reviewed. Elcio Calefi joined us at Identiverse in Las Vegas last week where we had meaningful conversations regarding FAPI adoption and certification.

OPIN
---------
Phase 1 is finished for the most part. OPIN are now considering FAPI recertification requirements that will begin Q3 2023.

SAMA
------------
Phase 1 almost completed with final bank and fintechs to be certified. Coordinating call with SAMA to discuss next steps including Phase 2.

FDX
----------
Met with FDX leadership at Identiverse last week in Las Vegas to discuss updating our liaison relationship. We also discussed FAPI certification and what that may look like in the overall FDX certification stack. Joseph provided detailed update on FAPI WG efforts.

ConnectID
------------------
Ongoing conversation regarding OID adoption, certification and certification pricing.

They are using multiple specs which will require different certification. Suggesing to use a different certification implementation which can potentially combine specs.


Camara Project (Bjorn)
-------------------------
* API 
* June 1 meeting. 
* https://camaraproject.org/
* https://github.com/camaraproject

It’s a Linux project for APIs to expose telco information.

Using OIDC and other profiles as baseline.

Bjorn and Gail gave a presentation last week regarding WG projects, FAPI, Grant Management

Since consent is part of Camara project scope

Currently working on revising governance model so they can establish relationships with external organizations.

OIDF will establish a relationship once the new governance model is established.



Spec Status
====================
Grant Management 
------------------------
* Currently in public comment period


PRs (Nat)
===============
Only 2 PRs by Dave for CIBA but was skipped due to Dave being absent


Issues (Nat)
==================

* #599 - FAPI Acronym

  * Biran pointed out that website content needs to be updated
  * MikeL is working on the new site updates and issues
  * There were problems with certification listings where data was not taken from the database. The problems have been fixed.
  * Domingos will create a ticket to keep track of other issues.

* #602 - "Client" is misleading in the context of signed introspection responses

  * Clarification is needed

* #601 - Title 8.1 is redundant

  * Remove the heading title since there is no other sections 
  * Assigned to Nat

* #428 - Baseline: Clause 7.4.1 Talks about security issues with authorization requests and responses but incorrectly refers to encrypting authorization 'responses' not requests.

  * Issued opened but will not take further action

* #466 - Proposal for FAPI DCR/DCM (Dynamic Client Registration/Management) profile

  * Want to create a profile to avoid different flavors of DCR/DCM by different ecosystems
  * There seems to be interest in creating a profile
  * Will wait to discuss with Dave and Joseph on next call

* #549 -  Network Layer Protections restrict use of more recent TLS 1.2 ciphers

  * Will discuss on next call

* #487 - RS must check x-fapi-interaction-id is an UUID or IP address

  * Interaction ID was removed but is mentioned in implementation advice.
  * May need to add additional clause


* #598 - Version identifier for FAPI 2.0

  * Marked as Duplicate of  #469



AOB (Nat)
=============
Victor asked if there is any documentation regarding why FAPI profile is different from other profiles such as iGov and are they any specific industry requirements.

Nat gave a brief history of FAPI from financial specific to general purpose high security usage.

iGov also has cases and specs that can be general purpose use.

Dima asked if those use cases can be covered by FAPI

There is a possibly of basing iGov specs on FAPI
The call adjourned at 14:__