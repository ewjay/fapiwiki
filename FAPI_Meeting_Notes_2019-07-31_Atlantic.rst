============================================
FAPI WG Meeting Notes (2019-07-31) 
============================================
Date & Time: 2019-07-31 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call
===========
Attending:
--------------------
#. Bjorn Hjelm (Verizon)
#. Dave.Tonge (Moneyhub)
#. Dima Postnikov
#. Joseph Heenan
#. Kosuke Koiwai (KDDI)
#. Nat Sakimura
#. Ralph Bragg
#. Stuart Low
#. Torsten Lodderstedt (yes.com)


Regrets: 
---------------------    
#. Anoop

Adoption of the Agenda (Nat)
==================================
* Adopted as is. 

External Organizations
=======================

IETF (Nat)
--------------
* Daniel presented Pushed Request Object to the OAuth WG. It was well accepted. Once we are done with the editing that applies the changes to all the current issues, we should submit it towards IETF 106. Nat will check if we need to do Implementer's Draft vote before that. 
* Justin presented XYZ. It will likely to be taken up as an experimental spec. 

ISO/TC68 (Nat)
--------------------
* Two new WG, one for eKYC and another for QR code payment is being formed under SC2. 
* FAPI may want to open a liaison with the later so that we can review the document and give feedback. 

Open Banking (Ralph)
----------------------
* Payment API is lacking reverse and refund. It needs to be dealt with. 

PSD2 (Ralph)
------------------------
* Wait and see mode in many banks. 
* App to App / App based decoupled authentication. CIBA like. Now compelled to adopt due to EBA comment. 
    * App based direct redirect Can be implemented through Intent / Redirect. 
* EBA comment can be implemented both decoupled and redirect. 
* Joseph commented that calling through HTTPS Claimed URL is mandatory. 
* Torsten said may be not. 
* Dave commented that it is the perfect timing for the deployment document as FAPI supports it. 
    * Torsten commented that the title of the document should include "implementation" as otherwise 
      developers will not notice it. 
* Joseph asked Ralph when the delta between the OB version and FAPI version of CIBA will close. 
* Ralph replied that it is upon him. It should happen soon. 

Australia (Dima/Stuart)
-------------------------
* Combination of partial adoption of OIDC suite + custom claims - some std claims (iss). 
* Most of the work is on data and metadata. 
* Perhaps we should provide feedback and letter. 
* Stuart and Dima to draft a factual statement of the problems so that FAPI or OIDF can officially comment on their spec. 

FYI: 

General feedback thread is open: https://github.com/ConsumerDataStandardsAustralia/standards/issues/79 

If you have consent decision feedback: 
https://github.com/ConsumerDataStandardsAustralia/standards/issues/77

And authorization flow:
https://github.com/ConsumerDataStandardsAustralia/standards/issues/76

Events
==============
Nothing for August. 

Pull requests and issues
==========================
PR #125 CIBA: let AS determine whether signed request is mandatory
-----------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/125/ciba-let-as-determine-whether-signed/diff
* Modified the language a little (recommended to should) and everybody in the call approved. 
* As the editor of the spec, Joseph asked to hold merging till after publishing the implementer's draft. 
  Joseph will take care of the conflicts if there will be. 

PR #115 FAPI-R/RW: Bring clauses about acr inline with usage
------------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/115/fapi-r-rw-bring-clauses-about-acr-inline/diff
* This change is to give more flexibility to the Authorization server as risk can be mitigated by non-technical measures as well. Many of the Open Banking UK banks would not be deploying SCA so does PSD2 banks. 
* It was approved pending the conflict fix. 


AOB
==========================

Next Call
-------------------------
* In the next call, `PR #131 first proposal to integrate JARM as equal option <https://bitbucket.org/openid/fapi/pull-requests/131/first-proposal-to-integrate-jarm-as-equal/diff>`_ will be taken up as the first item in issues/PRs. Experts are expected to review the PR by then to be fully prepared to discuss it. 

The meeting was adjourned at 15:00 UTC.