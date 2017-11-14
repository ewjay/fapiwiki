============================================
FAPI WG Meeting Notes (2017-11-06)
============================================
Date & Time: 2017-11-06 09:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:05 UTC. 

Roll Call
===========
* Attending: Nat, John, Ralph, Tom, Taka, Joseph, Betren (Ubisecure), Chris Michael, Dave, Bjorn, Anders
   * Guest: Don
* Regrets: Tony

Adoption of the Agenda (Nat)
==================================
* Added Conformance Suite Progress

Conformance Suite Progress (Ralph/Joseph)
===========================================
Test suite will be available as of 8th of December for the Open Banking profile ver.1 Implementer's draft. 
It needs a clear statement of what this does/does not cover. 
CMA9 test the Conformance Suite. 

Subset will be available for Live proofing by the end of November. 
Where it will be hosted is a good question. Moving to OpenID Foundation is preferable from the OBIE perspective. 
Hosting is trivial. It will be provided as a Docker image. 
A catch is that the certificate will not be live until Jan 13 so it will not be a "complete test" until then. 

The suite is not using the existing python code but is written in Java and doing continuous integration using Jenkins. This was pretty much the only way to achieve the rigour required for the banking and to meet the deadline.

When to hand suite over to OIDF - better before end 2017 to increase wider adoption. 

Difference between shall and should? How to display in results - if fail should, then need to have a mitigating reason - suite should require user to add this. 

Naming: FAPI conformance suite (ver 1 based on Open Banking Profile and implementers draft)

Take offline how this is handed over and funded ongoing - OIDF to take on post 13 Jan - tbc. 
 

Next steps (Nat)
==================
The desire to do another round of implementer's draft on the Part 1 was expressed so that the unnumberd lists will be converted to numbered lists. This is desirable as the conformance suite is using these numbers. It was agreed to start the process in a few weeks. 

Sec Profile to remain implementers draft till well into 2018 - till all 4 CMA9 vendors have had 6 months to address and implement all known waiver items. It will also allow time for clarifications during implementation. 


CIBA FAPI profile (Dave)
=========================
All the issues listed in the tracker was dealt with. The results are recorded in the tracker. 

Dave T should talk to Mike Kelly (Curl)

Headers - we should register x-FAPI for headers with IETF so we can keep the x-. i.e., we are not going to change x-fapi- to fapi-. 

Creation of the response to Berling Group Consultation (Chris)
===============================================================
Based on the comments OB is creating, the group discussed the issues around the Berling Group consulation. 

signHTTP is an individual draft and not on standard track. 

User password grant is deprecated in spec and for backwards compatibility only

Assumes all you need is eIDAS - no concept of onboarding 

Section 4.6 conflated stuff  - too complex

Decoupled - caution as issues for bank fraud systems and also UX for customers. OAuth2/Oidc have established standards. We should look to build and adopt standards for this rather than just saying yes without standards. Should adopt appropriate standards which are supported and maintained by a credible global body. 

Embedded - if this is mandated for banks will have impact for banks to innovate (eg fraud detection) and safety of customer. 
This comes from some TPPs wanting to control entire UX - inc authN - however, under psd2 they don’t hold the liability. 

Table of facts - which mechanisms support SCA, dynamic linking, non-repudiation would be good. 

Banks should have an option to NOT implement embedded and pass through as soon as they implement SCA. 

Caveat: SCA doesn’t mean phishing resistant

Authorisation server and resource servers are jumbled together. 

eIDAS certs should only be used for onboarding and not every single api interaction, as they are too coarse / not the right solution. 

Redirect simpler and easier to implement for both TPP and ASPSP. Embedded also precludes W3C standard. 

Onboarding - link to dynamic client registration spec

GDPR issue for embedded and also for not having authorization held by ASPSP 

OBIE should talk to ICO about embedded and risk of this for GDPR


AOB
===========

Next Call (Pacific)
-----------------------
The next call is scheduled to be on the Pacific time zone. 

* The meeting was adjourned at 15:00 UTC.