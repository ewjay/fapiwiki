============================================
FAPI WG Agenda & Meeting Notes (2023-05-03) 
============================================
* Date & Time: 2023-05-03T14:00Z
* Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2023-05-03_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:02 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Nat, Joseph, Mike L. Arnaud, Daniel, Dave, Filip, Rifaat, Victor
* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Default agenda used. 


Events (Mike L)
====================================================
OpenID Foundation Workshop (Mike)
---------------------------------------
* Workshop recording was released. 

EIC Workshop
----------------
* May 9. 
* 

External Orgs & Liaisons (Nat/Mike L.)
============================================

Brazil (Mike L.)
---------------------------------
* Re-Certification going strong for Open Finance.
* Same for Open Insurance. 
* OP/RP recertification lower fee being considered. 

Saudi (Mike L.)
---------------------


Security Analysis sponsored by AU (Mike L.)
-----------------------------------------------
* WP2 is proceeding. Everything should be on track. 
* The team to brief the WG. 

FDX (Mike L.)
----------------
* FDX Conference - Joseph and Wes was there. Reconnected with Don C. 
* Follow-up call with Don C. on certification models. 

OAuth WG (Rifaat)
------------------
* DPoP was approved. It is now in RFC editor's queue. 



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