============================================
FAPI WG Meeting Notes (2020-02-26) 
============================================
Date & Time: 2020-02-16 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========


Attending:
--------------------



Guests:
--------------



Regrets: 
---------------------   


Adoption of Agenda (nat)
===========================
Adopted as is. 

AU Consent Consultation (Stuart/Dima)
========================================================

External Organizations
==================================

SWIFT
---------------

FDATA
---------------

Brazil
---------------

FAPI Evolution (Torsten)
==========================
Torsten provided the presentation: 
https://docs.google.com/presentation/d/1LyebJ8FhC1sIM9F5e9TNHRPDOYuXiilHt4wQBkvRvtc/edit#slide=id.p

* Rob: User interface issues. Many wants ROPC to keep control of the UI. 
* Ralph: consent means different so need clarification. 

Fine-grained authorization request

Consent is application-specific. More granular and complex as time goes by. 



Grant request/consent API (Torsten/Daniel/Joseph)
====================================================

Refactoring of the specs taking the security assumptions in mind. 
======================================================================

Issues and Pull requests. 
====================================================


Meeting starts at 11:00 GMT. 
Remote participation is available. 

Ask Don if we can use the room until 5 PM.


Presentation for the SWIFT Conference on the 18th (torsten)
=============================================================
OIDF sales pitch with an emphasis on FAPI (API Security) and eKYC.

Use https://docs.google.com/presentation/d/171gOhCdxp1jZBo9P16gFLXOyIGILaPEGs6L7sDctHhg/edit?usp=sharing as the base and add a few slides for Swift. 

Swift Identity APIs
----------------------
Benefits With 3SKey, SWIFT shoulders your burden to build, maintain and update a technical infrastructure. 3SKey provides a common solution for strong authentication and digital identity, which can be used on any electronic banking channel, including offline applications, web-banking, local and proprietary networks, and SWIFT. 3SKey uses industry standards and provides toolkits and APIs for easy and rapid integration in applications while ensuring maximum security. https://www.swift.com/your-needs/corporates/3skey/benefits 3SKey for Banks factsheet .pdf RESOURCE Trusted and cost-effective solution for strong authentication and digital identity. https://www.swift.com/sites/default/files/resources/swift_needs_factsheet_3skeyforbanks.pdf

Issues
========

issue #278: duplicate kids in the authorization server's jwks (Joseph)
----------------------------------------------------------------------
* Document the key selection algorithm when a duplicated kid is present. 
* FAPI certification should give a “pass” to duplicated kids. 

AOB
==========================
n/a.

The meeting was adjourned at 14:__ UTC.