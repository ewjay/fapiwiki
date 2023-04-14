============================================
FAPI WG Agenda & Meeting Notes (2023-04-12) 
============================================
* Date & Time: 2023-04-12T14:00Z
* Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2023-03-15_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:02 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Mike, Nat, Justin, Daniel, Dave, Amaud, Takahiko, Joseph, Victor, Brian, Filip, Dima, Michael, Chris, Bjorn
* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Default agenda used. 


Events (Mike L)
====================================================
OpenID Foundation Workshop (Mike)
---------------------------------------
* Registration page is now open. 
    * https://openid.net/2023/03/17/registration-workshop-at-microsoft/
* Last day to register is 4/12/2023.
* Virtual attendance available. Registration is required.

External Orgs & Liaisons (Nat/Mike L.)
============================================

IETF HTTP Signatures (Justin)
--------------------------------
Had discussion with Dennis, researcher who raised issues with signing signature values.

Changed text in advice and examples to address concerns. 

Impact on FAPI : Instead of advising applications to just sign the signature value on the request when making the response, it is recommended to functionally sign everything that needs to be signed as part of the request as its own individual item. 

There is no transitive protection when signing the signature.

Draft is moving forward with new revision in the next couple of weeks.

FAPI HTTP signing draft needs to make corresponding changes.


IETF DPoP (Brian)
--------------------------------
Draft is in the final stages of IESG review and will be discussed in the telechat tomorrow.

New Attack (Nat)
--------------------------------
Nat has a report from a security researcher identifying a new kind of attack when using dynamic discovery and logout. 

Nat will share information privately. 

Joseph and Daniel have been informed and feel that there is no concern at the moment.

Contact Nat for details of the attack.


Open Finance Brazil (Nat/Mike)
--------------------------------
* OIDF continue to receive FAPI recertification requests as mandated by OFBR. 
* Had call with CIBA squad - 

  * Still finalizing CIBA spec
  * Will provide additional feedback and work to the OIDF
  * CIBA certification tests have started but awaiting final draft to finalize them


Open Insurance Brazil (Nat/Mike)
--------------------------------------
* We continue to receive OP and RP cert requests. OPIN is considering mandating FAPI recertification and we are engaged in the conversation and working to clarify OPINs recent requirements. 


Nigeria (Mike)
------------------------------------
* No updates so far.
* Mike will follow up.


Security Analysis Work Package 2
------------------------------------
Marcus from the certification team is helping coordinate and keep it on track


Saudi Arabia (Mike/Chris/Nat)
------------------------------------
* We continue to receive OP and RP cert requests from SAMA participants.
* Recertification is likely to be on FAPI2. 

Australia
------------------------------------
Looking at different options for packaging multiple certification together to support that ecosystem


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


PRs (Dave)
===============
* None


Issues (Dave)
==================
Some issues from Work Package 2 researchers

* #596 - Non Repudiation

  * Related to #594  - Value of JARM for non-repudiation

  #. Have some question as to what the intuitions regarding ‘non-repudiation’ means in regards to FAPI 2 HTTP message signing. Would like to capture the intuition in the security properties rather than the technical meaning.
  #. For a client using PAR+JAR, lack of signature on actual authorization request can have unintended consequences, e.g. client sent a PAR but never sent actual authorization request.

  * The authorization request with the artifact  doesn’t have any signature on it.
  * If HTTP request proof is desired, you should use HTTP signing.
  * Client is sending authorization code with client authentication to the token endpoint so it would be difficult to repudiate the fact that it sent an authorization request.
  * There are only 2 business requirements for such uses cases : 

    #. Resource server responses 
    #. Payments

  * If making decisions based on resource responses, HTTP signing is sufficient.
  * There are use cases for forwarding responses for tax purposes so need proof that the response hasn’t been tempered.
  * Need to be mindful that typical Openbanking APIs only return a set of transactions.Need to link the response to a non-repudiated website that the transactions belong to a specific user.
  * The exact non-repudiation properties will depend on the context.
  * Security researchers need the exact meaning for analysis.
  * Non-repudiation property of whether a particular transaction happened or not is unknown.
Need to add more security considerations.
  * JAR + PAR for a particular message exchange proves the client made the request but not whether the authorization proceeded further.
  * The consensus is that non-repudiation is for a particular message exchange but not an entire flow. Will add security considerations.

* #595 - Using OIDC Federation and FAPI together

  * Certification team received inquiries regarding using Federation with FAPI.
  * The Federation spec requires support for RS256 algorithm but FAPI disallows it.
  * The intent is that RS256 is the default if the ecosystem does not specify any.
  * Federation spec has been updated to not require RS256.
  * Dave will look into compatibility of using Federation and FAPI.
  * Security model does not look at registration at all. So the model will need to be updated if new functionality is added.
  * Just analyzing registration by itself should be sufficient.
  * DCR was analyzed in OIDC.
  * DCR for UK and AU is slightly different. Should effort be put into merging and standardizing them. Federation can be used for similar problems.

* #594 - Value of JARM for non-repudiation

  * JARM provides message integrity and earlier attack detection. It might be worthwhile to mention other benefits. 
  * However it is not required for a secure profile. However, recommending to use HTTP message signing without detailed explanations will cause confusion. 
  * Recommending JARM in the security profile will add optionality.
  * Will try to add explanations.


AOB (Nat)
=============
* Call next week is cancelled. 

The call adjourned at 14:59