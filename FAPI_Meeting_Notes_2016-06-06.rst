==============================================================
Financial API (FAPI) Work Group Meeting Notes (2016-06-06)
==============================================================

.. sectnum::
   :suffix: .

.. contents:: Agenda

DATE: 2016-06-06 9:06AM - 9:50AM CDT 

LOCATION: New Orleans Marriott 3rd floor + GoToMeeting. 

Attendees:: 

 	* Nat Sakimura - Chairman, OpenID Foundation
 	* Don Thibeau - Executive Director, OpenID Foundation
 	* Rob Laurence - Innovate Identity
 	* Steve Greenberg - Independent Consultant
 	* Henrik Biering - Peercraft
 	* Nov Matake - OpenID Foundation Japan
 	* Bertrand Carlier - Solucom
 	* Mike Jones - Microsoft
 	* George Fletcher - AOL
 	* John Bradley - Ping Identity
 	* Adam Dawes - Google
 	* Brian Berliner - Symantec
 	* Tony Nadalin - Microsoft
 	* Lydia Vasquez - PayPal
 	* Dale Olds - VMWare
 	* Masanori Kusunoki- Yahoo! Japan
 	* Tom Smedinghoff - Locke Lord
 	* Doug Foiles - Intuit
 	* Mike Leszcz - OIDF & OIX


Nat Sakimura called the meeting to order at 9:06AM CST. 

This was the inaugural OpenID Foundation Financial API (FAPI) Working
Group meeting. 

NOTE WELL – IPR AGREEMENT

Reason for the IPR Agreement - to make sure that the end specification
is completely open and not encumbered by patent protected contributions.


ADOPTION OF CHARTER
=========================
* Charter link- openid.net/wg/fapi
* Nat reviewed the draft Charter.
* One thing is out of scope - web payment. Need to liaise with W3C Web Payment WG.
* Email is the primary vehicle for working group communication but
  there will still be regular monthly conference call for status checks.

The working group will schedule face-to-face meetings when convenient
adjacent to other industry events.

Nat opened the call to solicit any changes to the draft FAPI WG
Charter

Charter was adopted unanimously. 

SELECTION OF CHAIR
=====================
Nat Sakimura is the acting working group chair. 

Tony Nadalin from Microsoft and Anoop Saxena from Inuit have indicated
interest in being a co-chairs. 

The FAPI Working Group unanimously selected Nat Sakimura (NRI), Tony
Nadalin (Microsoft) and Anoop Saxena (Intuit) as co-chairs of the FAPI
Working Group. 

MEETING SCHEDULE
=====================
Global participation creates meeting scheduling issues. 

Alternating working group call schedule: 

* (2) calls a month.
* (1) US/AsiaPac time and (1) US/EU time.

The FAPI Working Group meeting schedule to be posted to the working
group webpage. 

Exact schedule is to be worked out in the mailing list. 

SPEC DEVELOPMENT STRATEGY
==============================

Roadmap
------------

	* Nat proposed that the WG should consider the UK Open Banking Standard
(OBS) schedule as it relates to the FAPI WG spec development. The
release dates proposed by OBS are: 

 	* Release 1 - January 2017
 	* Release 2 - March 2017
 	* Release 3 - March 2018
 	* Release 4 - March 2019
 	* FAPI WG should beat the deadline enough to be adopted there.

Spec Format
-----------------
* The Open Banking Standard suggests HAL, Swagger, and RAML.

* Nat recommended HAL for defining the interaction between endpoints,
  and Swagger for defining the interaction to an endpoint, for now. 
    * Swagger: http://swagger.io 
    * HAL: http://stateless.co/hal_specification.html 
    * While historically we have been using IETF language, since we need
      to consider this to be submit to ISO/TC68 at a later date, it would be
      better to use ISO language described at http://isotc.iso.org/livelink/livelink?func=ll&objId=4230456&objAction=browse&sort=subtype

Spec Language
------------------

Nat suggested that as the FAPI WG may wish to submit the spec to ISO/TC 68 as: 

* ISO/TC68 is the maintainer of ISO 20022 Payment message catalogue.
 	* https://www.iso20022.org 

the WG may want to use ISO language (shall, should, may, etc.) 
as defined by the ISO Directive Part 2 
rather than the IETF language ( RFC 2119 ). 

WG unanimously agreed on it. 

Establishing a liaison relationship with the ISO/TC68 Financial Services
----------------------------------------------------------------------------
As a corollary, we probably want to establish a liaison with ISO/TC68. 

* To be discussed further at the OIDF board meeting on June 6, 2016.
* Mike Jones made the point that submission to ISO would be down the
  road once the specification has been developed.
* Tony Nadalin asked if the plan is to get the entire spec through ISO
  or just registering the spec with ISO? Nat suggested that would be
  determined later.

Recruitment of other members
-------------------------------
Nat pointed out the needs for reaching out. 
We need members from all the continents. 

* North America
* Latin America
* Europe
* Africa
* Asia


AOB
=====
Intuit is going to contribute Durable Data API (DDA) to the FAPI Working
Group. 

 * Currently being used by US financial institutions.
 * Nat reviewed the spec - very US-centric and needs to be
   internationalized but it is a good starting point otherwise.

Nat concluded the FAPI Working Group meeting at 9:50AM CST. 
