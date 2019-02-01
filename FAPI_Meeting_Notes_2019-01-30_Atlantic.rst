============================================
FAPI WG Meeting Notes (2019-01-30) 
============================================
Date & Time: 2019-01-02 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending:　
  * Nat, Bjorn, Brian, Daniel, Dave, Joseph, Ralph

* Guests: 
* Regrets:      
  * Torsten

Adoption of the Agenda (Dave)
==================================
* Agenda was agreed

External Organizations
==========================

STET, Berlin Group & Session Fixation in Payment Flows (Torsten)
-----------------------------------------------------------------
* Cross-browser Payment Initiation Attack is in the repo as a markdown document
* WG members to share bilaterally 
* There has been more discussion with STET


Australia (Ralph)
-----------------------------
* Dates have been pushed back

UK OpenBanking (Joseph, Dave)
-----------------------------
* Things are on track for FAPI conformance test
* There may be a delay on banks moving to the FAPI RW standard
* RP conformance tests - should be released in the next month, still need to add negative tests
* Banks need to provide account holder name, currently this will be in an API response rather than an ID Token
* App to App flows are going live
* Banks are using multiple well-known configs, with diff auth endpoints to support different brands


ISO TC68 (Dave)
-----------------------------

* The editor is asking when FAPI will move to a final draft, we discussed that when things settle around the OB implementation we should probably move to final
* Nat and Dave are feeding back to the editor
* Dave asked the WG about guidance for websockets with OAuth.
* Ralph explained that this is an area that needs more work, e.g. a lot of libraries don’t support auth headers
* There are different security implications and may need to be a different protocol - Dave to ask OAuth WG

Issues
==========================

https://bitbucket.org/openid/fapi/issues/142/standardising-lodging-intent

https://bitbucket.org/openid/fapi/issues/200/ciba-signed-authentication-request

https://bitbucket.org/openid/fapi/issues/213/requirements-on-rsa-ec-key-sizes-should

AOB
==========================
* Research Paper - Formal analysis of FAPI, this is being reviewed by Nat and will be released shortly
* ISO27002 in revision, the identity and access management section is very weak. WG members are encouraged to feedback


Next Call
==========================

* Pacific call next week. Atlantic call in 2 weeks time.