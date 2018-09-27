============================================
FAPI WG Meeting Notes (2018-09-26) 
============================================
Date & Time: 2018-09-26 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: Nat, Bjorn, Brian, Joseph, Robert, Torsten, Dave, Ralph, John
* Guests: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Added European Commision, Berlin, Astralia

CIBA Progress Report (Brian/Dave)
=====================================
* Distributed all the tickets. 
* to be completed by the next call. 
* Needs a few more week. 
* In general, we reached agreement on the direction. 
* Still issues coming in though. 
* End user identifier needs to be disucssed as a part of CIBA FAPI Profile. 

Test Harness (Joseph)
======================
* There have been discussions between Don, OB, and OIDF 
* OB signed on for updates for conformance Part 2 implementers draft for AS and RP side
* There will be a presentation regarding the certification roadmap at the pre-IIW OIDF workshop 
* Edmund working on Java supplementary tests for OIDC Basic profile

Q : How do we make sure OIDF is moving things to take over OB handover?
A : Might be addressed in workshop with the certification roadmap


External Organizations
==========================

Berlin Group (Torsten)
--------------------------
* https://nisp.online/
* Multi-level SCA for multi-person authorization. 
* Open Banking is also working on something similar so it may be an opportunity. 
* NexGen PSD2 conf in Nov and Dec? It is likely to be a marketing event but could ask "right questions". 
* Torsten met with editor of Berlin Group specification
* Explained security issue regarding initiating of payments within authorization process which will allow attacker to mount session fixation attack to make someone else pay another's bills
* OAuth session fixation countermeasures ineffective because action happens before countermeasures become effective
* Straight solution is to initiate the payment using the payment access token and nothing else, but will require significant changes to BG api, 
* Editor reluctant to change due to irrelevance and may be considered "premium" service
* Will have follow up discussion on Oct 12 for Next Gen Task Force Advisory board
* Also discussed w/contacts in German banks, which will implement payment using access token, which may help to influence BG spec
* Should make a blog post to spread the issue via social media, since the problem eoesn't just apply to BG, Australians might be in same boat.
* Consumer groups might be interested also
* A document to explain different attack vectors/models that FAPI Parts 1 & 2 protects against might be useful.
* Banks might not be fully aware of problem so we need to do more educational reach out on risks involving protocols
* Torsten added additional security checks in SCA model and references


Open Banking UK (Ralph)
---------------------------
* No new updates
* OB working on supporting services for PSD2 compliance
* Doing workshops with vendors to drum up support for standardization of security profile

Australia (Ralph)
-------------------
* 4 major banks + other banks. 
* Collaborating through git. Some decisions are unilateral.
* There is concern regarding consent and authorization since person in charge of decision may not be expert in field.
* Data 61. 
* Australian Competion Consumer Commission  conformance certification onboarding. (Acts as federation/security provider, policy information point for lists of accretions, certification and directory services)
* Aggressive timelines may not be reachable
* Conformance bodies keen to reuse certification frameworks, standards, toolset, and external bodies to make sure they have secure stable standard. Only one available is OB conformance testing suite harness based on OIDC and FAPI rewrites
* As part of FAPI blog post, it should respond to not just BG challenges but also to publicly stated directions by other standards bodies.
* Another round of consultations and validations in November
* Legislative instruments allow government to to compel providers of certain services  to provide APIs is being baked into legislation now. Start with banking and will move to telco and energy. Similar to data portability.
 

Security Profile Comparison (Dave)
-------------------------------------
* Trying to finish it in a few days. 
* Freddie Guyera did line by line comparison of changes in R/RW/OB. Will be shared with Dave.


European Commission (Nat)
-----------------------------
* Nat will be in Brussels for presentation of OIDC, FAPI so they can be leverage for KYC token, account onboarding
* Welcome ideas for presentation
* Objective is to transfer KYC related attributes from one entity to another so receiving entity can onboard the subject using transferred attributes, KYC federation
* Can use OIDC by using extra claims in ID token or userinfo
* Blockchain groups also interested, but the key is the source of identity claims.
* Trust framework and sources for IDP must be considered
* Torsten has presentation for EIC on Youtube which can provide some ideas.





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

AOB
===========


Next Call
-----------------------
Next Pacific call will go as scheduled. 

* The meeting was adjourned at 15:03 UTC.