============================================
FAPI WG Meeting Notes (2021-06-23) 
============================================
* Date & Time: 2020-06-16 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-06-23_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
* Attending: 

  * Ali Adnan 
  * Anthony Nadalin (it)
  * Barry O'Donohoe (Raidiam)
  * Danillo Branco
  * Dave Tonge
  * David Chadwick (VCL)
  * Dima Postnikov
  * Gail Hodges (OIDF, she/her)
  * Jacob Ideskog (Curity)
  * Joseph Heenan (Authlete / OpenID Foundation)
  * Jules
  * Nat Sakimura
  * Ralph Bragg
  * Stuart Low (Biza.io)
  * Torsten Lodderstedt
  * Chris Wood (Axway)
  * Mike Lescz

* Regrets:
* Guest: 


Adoption of Agenda (Nat)
===========================
* PRs
* Issues
* Grant Management
* Events
* External Organizations


Events
======================


External Organizations (Nat)
================================
IETF/OAuth
------------------------

Australia (Mike L.)
----------------------
Been in contact with CDR team including Rob Deacon.

Call schedule for Monday June 28 with Mike L, Gail, Rob Deacon and Joe Otway from CDR.

Will give update in next call.




Brazil (Mike L.) 
------------------------
Hosted 3rd workshop in Brazil yesterday

300 participants

2 sessions in parallel (English, Portuguese)

Brazil OP test will be online upcoming Monday 6/28

Phase 2 banks can start submitting certifications starting 6/28

All banks to submit certification requests by July 5 in order to be processed by 7/15 Phase 2 deadline

Certification team on track to process certifications

* 26 Banks w/39 FAPI deployments

A number of banks joined the OIDF

Taka Kawasaki wrote a FAPI implementer’s guide that’s posted on the OIDF website - https://openid.net/2021/04/14/guest-blog-financial-grade-api-fapi-explained-by-an-implementer-updated/

Portuguese translation provided by Danillo Branco to assist with Open Banking rollout in Brazil



Berlin Group (Francis)
---------------------------



MENA (Ali/Gail)
-----------------------
Ali spoke at a Fintech Digit Connect event yesterday as part of a panel discussion

About 200 banks around the region

Topic about fragmented region

Most of the attendees in on the panel agreed that there needs to be some type of a regulatory body across the region, that 
would set some standards in place, especially around security, open banking APIs

Certification process could help

Had a meeting with the Head of Business at the Dubai International Financial Center.

Take initiative to work with OIDF in creating working groups where banks can be invited to learn more about such standards

Ali will put together plans on how this can be accomplished




UK (Fiona)
--------------------


US/FDX (Gail)
-------------
Did internal review of the data license agreement for certification listing data with Don Thibeau and Wes Dunnington last week

FAPI adoption has increased significantly since initial agreement

Take closer look before proceeding

Gail Hodges is going to make some recommended changes to the license agreement, do an internal review, including Tom Smedinghoff and then we'll re-engage with the FDX 



Conformance Suite Update
======================================

FAPI 1.0 Final Advanced tests went into production a week and half ago

Had first 2 certifications (Filip and Authlete)

RP Final test also went into production 

Mike will make announcement

Added Brazil profile test built on top of Final tests

Extra restriction from Brazil security profile

* Mandatory refresh tokens
* Pre-lodge intent mechanism
* Destructive scope
* Requirements on access token lifetime
* Encrypted request objects

Brazil RP test might go to into production today

Also test for Brazil DCR (Dynamic client registration)

Will develop a Brazil version of the FAPI CIBA OP and RP tests slated for November



PRs (Stuart/Dave)
===================

Pull request #277 - Remove sender-constrained codes clause
------------------------------------------------------------
Pull request #277 - Remove sender-constrained codes clause

Agreed to remove the language


Pull request #278 - Add additional clause about redirects
------------------------------------------------------------
Pull request #278 - Add additional clause about redirects

Adds normative clause to send 303  status code when redirecting the user agent using status codes

Merged



Pull request #276 - Add normative clause for AS to accept issuer value in aud claims
------------------------------------------------------------
Pull request #276 - Add normative clause for AS to accept issuer value in aud claims

Adds  more interoperability

Torsten asked whether this allow multiple values. Would like it to be single value.

“in addition to other allowed values” is very ambiguous

Using Issuer value provides more interoperability versus using specific endpoint values

Torsten proposed to use the  Issuer identifier value only. Need corresponding clause in RP clause.

Might add complexity to implementations that support normal OIDC

Joseph suggested also allowing the URL to which the assertion is sent to as opposed to listing all endpoint URLS

Suggested allowing the following values:

* Issuer
* Token Endpoint URL
* URL that assertion is being sent to

Ralph asked out that whether  retaining backwards compatibility is an objective of FAPI 2.0

FAPI 2.0 may not be implemented by new software but will most likely be built on top of existing software.

Taka suggested recording the discussion regarding simplicity, interoperability, security so that we can address those discussion points.

Dave will sent a message to the list with the discussion points and a proposal


Grant Management (Dima)
===========================================
There are 2 or 3 issues left that are waiting for Brian and Taka to confirm that they have been addressed.

Will close them and generate HTMLs for implementers draft

Jacob brought up discussion about whether to include the authorization details in the original implementers draft or add that to the ID2 and did not see an issue for that

Dima pointed that it’s #412 FAPI 2.0 - Hard requirement to support Grant Management Requirement

Multi-party consent (#420) is also moved to 2nd draft

Dave asked if there are any objections to moving Grant Mangement towards implementer’s draft. 
There were none.


Issues (Dave)
=================

#415 - Discovery Metadata for mtls
------------------------------------------------------------
#415 - Discovery Metadata for mtls

Moved milestone to ID2


#416 & #417
------------------------------------------------------------
#416 & #417

Will revisit next call



#412 - Hard requirement to support Grant Management Requirement
------------------------------------------------------------
#412 - Hard requirement to support Grant Management Requirement

Add note that there is work on Grant Management
Jacob asked that Grant Management be mentioned that it will be in ID2

Charter of FAPI needs to discussed in relations to the goals of FAPI 2.0



AOB
=======


The call adjourned at 15:02 UTC