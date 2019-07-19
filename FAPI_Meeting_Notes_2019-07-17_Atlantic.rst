============================================
FAPI WG Meeting Notes (2019-07-17) 
============================================
Date & Time: 2019-07-17 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:06 UTC. 

Roll Call
===========
* Attending: 
    *　Nat、Bjorn, Dave, Brian, Dima, Joseph, Kosuke, Wesley, Torsten
* Regrets:      
  * 

Adoption of the Agenda (Nat)
==================================
* Added Additional Documents. 

External Organizations
=======================

Open Banking (Dave)
----------------------
* Open Banking was using defined scheme for HTTP signing using detached JWS signatures in header with base64 encoding.
* None of the banks can support it. 
* HSBC - First bankers to implement fallback mechanism instead of fully API driven. Has interface to allow screen scraping to work in presence of SCA.
* TPP identification must be behind mutual TLS endpoint or some other way of signing with eiDAS cert.
* One way of doing it : Online banking interface running proxy that requires mutual TLS handshake
* Screen scraping as it was done is no longer allowed or legal for payment accounts
* LLoyds also implementing this. There is no unintended access with API and access/refresh tokens. Access is  available for 90 days.
* Fallback mechanism does not have this.  Customer needs to be present on each interaction and requires some sort of strong customer authentication(SCA).
* Why are they not issuing access/refresh tokens as credential for screen scraping?
* It's more work.
* Banks had to apply for exemptions not to build these mechanisms. Need to provide good interface based on redirect. Some banks struggled with creating good user experience based on redirect.
* Failure to support OAuth redirect properly is part of reason for the need to rely on fallback.
* The amount of PSPs (TPP/ASPSP) with eiDAS certs are still really small.

PSD2
------------------------
* https://developer.hsbc.com/#/welcome

Australia (Dima/Joseph)
-------------------------
* Regulators released some decisions. 
* Some are good, like proposing FAPI but also there are concerning things. 
* Variations around authorization flow. 
* Good thing: they came back to redirect model but to a different version of redirect. Not using CIBA, but an usable version of decoupled.
* It's a web based redirect that captures usernames with separate decoupled authentication.
* OTP version might cause problems going forward. CIBA is in future but considers it not ready yet.
* Decided not to do Consent api (Intent api in UK)
* There are proposals for using the draft version FAPI WG has been proposing but regulators decided not to use it.
* Banks complained. They see consent API as important for future.
* There are 2 different orgs looking after security profile and APIs but not org groups of Directory
* Directory implementation is biggest, but looks less than developed
* They descoped a lot of requirements of OB, instead of using standards, went with own way/implementation
* Adoption will be challenge
* Dynamic client registration removed and used API extension
* OB registration is a profile of OIDC Dynamic Registration but not all required yet. The payload is signed JWT instead of plain JSON and has extra claims.
* API access is more important for deployments but so is standardization


Events
==============
IETF
----------
Next week. Nat and Brian will be there. 

Fin/Sum
----------
* The first week of September in Tokyo. 
* https://finsum.jp/
* Bill Roberts from CMA UK and Gavin LittleJohn from FData UK will present panel discussion

OpenID Summit Tokyo 
--------------------------
* 2020-01-24

New Documents (Dave)
==========================
JARM was previously accepted and became an implementer's Draft. 
Other documents are coming in, namely: 

* Lodging Intent / Push Request Object
* Implementation Advice
* HTTP Signing

Out of which the last two are new. 

* Implementation Advice is not going to be a normative technical specification but will be a general guidance document. 
* `Deloyment Advice Doc <https://bitbucket.org/josephheenan/fapi/src/edce6adee86b16f5fed2ef71ce8a86f4f01dc181/Financial_API_Deployment.md>`_
* The document has a structure that is good as a starting point. There was no objection for Nat to ask the list to accept the document as a workgroup item. 

#. Public clients not permitted
#. Replacing screen scraping with APIs

* Nat would like to add "communication between apps and backend"
* Nat will send call for adoption to list

* Doc is not a spec and is more about documenting expertise /whitepaper/tech report/advice/ living doc
* If it's just a standing doc, will just adopt it and announce to the list unless there are objections
* No guidance in OIDF process for these docs
* Joseph would like this doc to go through sign/off process
* Will use working draft process


HTTP Signing was much more controversial. It was suggested that first, we focus on the Requirement: 

* `HTTP Signing Doc <https://bitbucket.org/josephheenan/fapi/src/http-signing/Financial_API_HTTP_Signing.md>`_
* Why we need it; 
* What it needs to fulfill (non-repudiation or replay). 
* Starting listing requirements as applies to FAPI for protecting HTTP request during transit
* What to sign (e.g. sign request uri, method, headers or entire request)
* It will be generic api request/response independent of use of access tokens, not OAuth related
* It will may list alternatives methods in Annex or another doc
* But need agreement on requirements first, need to confine doc first to avoid getting out of hand
* Nat would like to add HTTP signing requirements to title before accepting as work item
* Nat will announce to list and will adopt if no objections

Pull requests and issues
==========================

AOB
==========================

Next Call
-------------------------
* We will talk about the pull request by Torsten re: making JARM a parallel option in Part 2. 
* Also, we will dedicate half of the call for the issues. 

The meeting was adjourned at 15:28 UTC.