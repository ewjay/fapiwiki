============================================
FAPI WG Meeting Notes (2017-01-18)
============================================
Date & Time: 2017-01-18 15:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 00:00+1 JST)

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:05 UTC. 

Roll Call
=============
* Present: Nat, Dave, Bjorn, John
* Regrets: Henrik
* Guest: 

Adoption of the Agenda (Nat)
===============================
* Adopt. 


External Orgs
==================

UK OBIE (Dave)
----------------
* Re-branding as Open Banking Service
* Data dictionary: a lot of work on Open Product data - on the schema level. ISO 20022 schema. 
* Moving to transactional data after that. 
    * HSBC API as an example. https://developer.hsbc.com/
* Dave is getting confirmation for joining the security WG. Nothing suggests that using FAPI profile would not be impossible. Only the discussion to this date is the establishment of a new certificate authority and the registry and nothing firm have been decided on the OAuth side. Thus, hopefully, they can adopt ours. 
* Much of the work currently are done in a closed environment. Dave et al are arguing that a lot has to come out in the open, and it is believed that it will be so shortly. 
* Registry WGs are meeting with software vendors for information but the steering group is trying to put a brake on it. It seems they are trying to offer too much before scopes are settled down. 
* Also, it is now clear that OBIE will match the requirements of PSD2. Before there was a question mark but it is clear now. 
* They are creating a certificate authority and online registry. Registration and accreditation process. 
* Accreditation process being discussed: No info public available now. On the PSD2, EBA currently has a consultation with the account service providers and PISP. The competent authority in the member states. UK FCA. Details of the registry are still not clear. 
* Service catalog: discovery API. 
* John pointed out that we should stick with OpenID Connect discovery as much as possible. GSMA tried to centralize it but it was a complete failure and they are now having to re-work everything using Connect's distributed discovery capability and client registration. GSMA's centralized approach collapsed pretty quickly under its own weight.
* GSMA is now trying to use the software statement for client registration. The advantage of the software statement is that it can include constrained registration information whereas the certificate can only provide who they are. For references, see Modrna list and draft specs. 
* Timewise, for transactional APIs, they are aiming to provide an alpha API at the end of May, beta by the end of July, then testing phase follows. It is a very demanding schedule. Under PSD2, while it starts in January 2018, the technical standards does not apply at least a year but in UK OBS, January 2018 is seen as a hard deadline where Banks will have financial consequences if they do not have it ready. 60 people are now employed (funded by banks) by the IE so they will probably deliver it. The concern is that it is not going to be very well thought about specs. 

JP Fintech Association (Nat)
-----------------------------
* On Dec. 27, JP Financial Services Authority published a paper: 
    http://www.fsa.go.jp/singi/singi_kinyu/tosin/20161227-1/01.pdf
* A lot of this deals with Financial API. 
* Perhaps because of this, JP Fintech Association called Nat to meet with them to review the status of FAPI. 
* They have asked Nat to go to JP Banking Association with them in the new year. 

Implementer's draft Part 1 (Nat)
==================================
* Public review has been started. 
* Details can be found at: http://openid.net/2016/12/19/public-review-period-for-financial-api-part-1-read-only-api-security-profile-started/

The relevant dates are as follows.

Public review period: 2016-12-19 to 2017-02-02 (45 days)
Implementer’s Draft vote announcement: 2017-01-20
Implementer’s Draft voting period: 2017-02-03 to 2017-02-10 (7 days)*

    * Note: Pre-voting before the start of the formal voting will be allowed.



Working Drafts
===================

    * Financial_API_WD_001.md Financial API - Part 1: Read Only API Security Profile
    * Financial_API_WD_002.md Financial API - Part 2: Read and Write API Security Profile
    * Financial_API_WD_003.md Financial API - Part 3: Open Data API
    * Financial_API_WD_004.md Financial API - Part 4: Protected Data API and Schema - Read only
    * Financial_API_WD_005.md Financial API - Part 5: Protected Data API and Schema - Read and Write

Part 2: Read & Write API Security Profile (Nat)
------------------------------------------------------------
* `Part 2: Read & Write API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md 

* Current plan is to just to include a proof-of-possession token into the spec, so there are not too many things to do. 6 weeks should be an ample time to draft. 

* Timelines: 
    * End of February: Draft completion
    * March: Start public review
    * End of April: Vote. 

Part 5: Read & Write (Transactional) API (Bjorn)
---------------------------------------------------
* Bjorn asked about the difference between the transactional API and the user questioning API that Modrna is making. 
* John believe that they are different and John will look into it. 
* User questioning API: Phone companies sell the user consent. When someone wants user consent, the phone companies are going to push the consent request to the users through out-of-band communication to collect the consent and have the consent signed by some meaningful key. Some similarity to Contract Exchange work. Orange is very keen on it. 
* There is another group who wants a more traditional way of doing it as part of authentication. 
* Nat pointed out that while general "questioning" is not so much of the interest for FAPI, payment is. We probably need a joint call to align the two group. 
 
Issues (Nat)
=========================

#60: Only one method to Token Bind AT rather than two? (Nat)
----------------------------------------------------------------
* issue #60
* Part 2

For access tokens, The token bind spec. gives two options: referred token bind id, generated token bind key. 

John pointed out that it is not possible to mandate one way or another, as it is client environment specific. Some operation systems would provide the best security but it is not available in all OSs. Doing it at the application level gives most flexibility but least secure. 

From the server side, it looks exactly the same. 

So, this ticket probably is invalid. 

As far as the token binding spec is concerned, a new draft is being worked out which should go to WGLC and go to IESG subsequently. 

Dave also asked about the legacy platform supports. 

John pointed out that Chrome, IE, iOS, Android (Chronet library) supports them. Chronet library can go back to quite old versions of iOS and Android, though you have to include the Chronet HTTP library. There is a plan to include the supports in AppAuth. 

Nat pointed out that we probably need to do a hands-on or something and provide it throght Youtbe etc. so that developers will be able to take advantage of it. Perhaps we can try to do it in conjunction with EIC. 

#61: Fund Availability API
----------------------------
* issue #61
* Part 4

In PSD2, PISP asks AISP whether the fund is available for the payment and the answer will be yes or no. 
Nat asked Dave if there is something envisioned already for this functionality. 

Dave pointed out that it is definitely within the scope where IE is working on but cannot remember off the top of his head. 


Others
----------

Events
=============

CIS (John)
----------------------
* Submission was closed on Jan. 6 and FAPI did not submit anything but presumably there will be OpenID Foundation track so we can do something there. 

EIC
---------------
* Need to start thinking about what we can do --> homework for everyone. 
* Perhaps some kind of hands on for token binding. 
 
OB
========

Next Call (Pacific)
--------------------------
* 2017-01-24 23:00 UTC
    (15:00 PDT, 23:00 UK, 00:00 Denmark, 08:00+1 JST)