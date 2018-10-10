============================================
FAPI WG Meeting Notes (2018-10-10) 
============================================
Date & Time: 2018-09-26 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:04 UTC. 

Roll Call
===========
* Attending:　
    * Nat Sakimura, 
    * Bjorn Hjelm, 
    * Brian Campbell, 
    * Daniel Fett, 
    * Joseph Heenan, 
    * Freddi Gyara, 
    * Chris Michael, 
    * Ralph Bragg
    * Barry ODonohue, 
    * Dave Tonge 
* Guests: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================


Implementer's Draft Voting (Nat)
======================================
* Voting has started. Right now, there are 27 votes recorded. 
* Quaram is 56 so we need 29 more ovtes. 
* Members are encouraged to ask people around to vote. 

CIBA Progress Report (Brian/Dave)
=====================================
* Number of issues. 
* Splitting of the draft is underway. Hopefully, soonish. (Plan to do it by next Tuesday)
* Outstanding work needs to be done around subject identification in login token hint. 
    * secevent - conceptually same to structured identifier. 

Test Harness (Joseph)
======================
* https://openbanking.atlassian.net/wiki/spaces/DZ/pages/126321042/Open+Banking+Security+Profile+Conformance


External Organizations
==========================

Berlin Group (Torsten)
--------------------------



Open Banking UK (Ralph)
---------------------------
* CMA 9 banks are building against v.3 of the spec, which is enabling PSD2 compliance. 
* Putting together detailed proposition on standards to be developed, including the OpenID, funtional APIs, test harness. 
* In parallel, talking with other markets, e.g., Australia, Ireland, 
European Banks, South Africa (Regulatory mandate), 


Australia (Ralph)
-------------------
* Security profile: Security WG has not yet been formed. The position paper was published, FAPI Read. 
* How to construct consent model. Scope access to resources with a configurable period of time. 
* Identity is mandated by Open Banking ACCC initiative. Banks need to provide via resource. 
* Comments sought at https://github.com/ConsumerDataStandardsAustralia/standards/issues/26
    * Decision 23 and 26 is particulary of interest. 
 

Security Profile Comparison (Dave)
-------------------------------------
* No progress for now, as CIBA is a priority. 

European Commission (Nat)
-----------------------------
* Oct. 28 - 1 day workshop. Vendor presentations for KYC and Identity proofing. 
* OIDF made a presentation about OIDC and FAPI. Some interest from EC on the situation with Berlin Group. 
  Nat will follow up. 

Issues (Nat)
=================
Part 2 Related Issues
----------------------------
* https://bitbucket.org/openid/fapi/issues?status=new&status=open&component=Part%202%3A%20RW%20Security

Issues #171, #172, #173 were dealt with. Please refer to the tickets for the details. 

We were not able to reach part 1 issues and CIBA related issues by the end of the call. 
These are going to be dealt with in the mailing list, etc. 

* Part 1 Related Issues:  https://bitbucket.org/openid/fapi/issues?status=new&status=open&component=Part%201%3A%20RO%20Security

* CIBA Related Issues : https://bitbucket.org/openid/fapi/issues?status=new&status=open&component=CIBA

Pull Requrests
=================
Note: As a general guideline, during the implementer's voting period, only the editorial or previously agreed item that were mis-represented in the draft can be applied. 

PR #77 was mereged. 

AOB
===========
Events
------------
* ISO/TC68/SC9 Singapore meeting coming up: Dave will send the dates to the list. 
* ISO/TC307 (Privacy by design for consumer goods) London meeting on Nov.1,2. Perhaps beer-bof or something can be planned. 

Next Call
-----------------------
Next Pacific call will go as scheduled. 

* The meeting was adjourned at 14:57 UTC.