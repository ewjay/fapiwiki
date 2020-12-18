============================================
FAPI WG Meeting Notes (2020-12-16) 
============================================
* Date & Time: 2020-12-16 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Dave, Don, Takahiko, Daniel, Joseph, Brian, Kosuke, Torsten, Lukasz Jaromin, Stuart, Ralph
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* Adopted as is. 

Events (Nat)
======================

* IIF meetings 
* Don - Looking in 2021 to identify opportunities for pilots and proof of concepts with FAPI & eKYC.
* Hoping to get more conversation between eKYC WG and Global Legal Entity Identifier Foundation. Use IIF to promote adoption of FAPI and eKYC.

* OIDF to focus on redesign of listing of self-certified conformance implementations of FAPI and OIDC. Members are welcome to contribute ideas, requirements and designs.

* Also soliciting wishlist or Ideas for regional workshops.
* Hope to have a set of workshops in Australia and also for FDX.
* FDX is also working through formalities of adopting FAPI as a normative requirement for their conformance testing.





External Organizations (Nat)
================================

Financial Data and Technology Association
-------------------------------------------------------
* Setting up a new organization called Global Open Finance Center of Excellence in early 2021.
* There is a proposal for OIDF to be a founding member.
* OIDF has 3 interest areas, one of which is participation and leadership of group of groups - group of representatives of various standards, organizations from around the world that would try and look for efficiencies and Interoperability across regional efforts.
* The effort is being led by Kevin Littlejohn through the Global Open Finance Center of Excellence, which is related to the University of Edinburgh.
* The organization has appears to have funding, and is hiring personnel to create a library of APIs in the open finance world
* They may also be a licensee of OIDF's listing of organizations that are in conformance to FAPI and OIDC..


Germany
------------
Francis is at OBIE and was asked for a white paper on FAPI and conformance suite testing benefits.

OIDF
-------
* In 2021, the focus of the Foundation wants to turn to organizations, banks, and other service providers that are very new to family. 
* Whitepapers and presentations developed by members are really helpful and can be used to help educate people that are new to FAPI and OIDC.
* The Foundation needs to  help educate that cohort of people that are new to this area.


FAPI 1.0 Status (Nat)
===========================
PRs (Dave)
---------------
Pull request #214 - editorial 


Issues (Dave)
---------------
#350 - Crypto recommendations

* Add reference to RFC 8725
* Daniel to create PR

#310 - Hanging paragraphs

* Won’t fix until we create ISO doc.



Voting (Nat)
---------------

Certification (Joseph)
-------------------------
* Chris sent an email stating that a vendor who previously passed FAPI conformance is now failing.
* 4 new tests were added

1) Passing valid PKCE and require that it not be rejected
2) Required to accept IP v6 addresses in the X-IP headers
3) Required to send scope when it’s sent in the other order - tests usually send openid_accounts, and the banks are required to accept accounts_openid
4) When using  private_key_jwt authentication, request object can be accepted as client authentication

* What is the process for introducing new tests in the post draft version?
* Raise a ticket with WG and add if no one objects.

* OIDF will take priority to make it clear that results of conformance testing are for a specific revision of the drafts or suite version. Also give people a place to address concerns so OIDF can react in effective ways.

* A certification should come with a revision number, date, and expiration to be more useful. Otherwise, FAPI and OIDC certified labels can be used indefinitely. A change to the certification process and T&Cs are necessary. 
* Section 3D of certification T&C states certified logos can be used indefinitely.
* Feedback is welcome.

* Security is not a fixed target so certifications need to be current to be conformant. FAPI certified is a security attestation and not an interoperability attestation.

* A subgroup for certification conformance was suggested.
* Create a document to list issues and requirements is necessary.
* Certification revocation process should also be documented.
* Nat will send out a call for participation and leadership of the subgroup.



Drafts
===========
FAPI 2.0 (Daniel)
-------------------
* Now ready to move to next stage. 


HTTP Signing (Dave)
----------------------
* No updates.

Grant Management (Torsten/Dima/Stuart)
---------------------------------------
* Need more time until early 2021.


Issues (Dave/Nat)
=====================
* Please review #348 

AOB
==========================


The meeting was adjourned at 15:00 UTC.