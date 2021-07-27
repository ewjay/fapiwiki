============================================
FAPI WG Meeting Notes (2021-07-14) 
============================================
* Date & Time: 2020-07-14 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-07-14_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:04 UTC. 

Roll Call 
===========
* Attending: Nat, Bjorn, Dave, Dima, Kosuke, Takahiko, Joseph, Lukas, Ali, Danillo, Brian, Daniel, Francis, Edmund, Stuart, Ralph (at 14:30)
* Regrets: Dave
* Guest: 


Adoption of Agenda (Nat)
===========================
* Adopted as is. 

Events (Nat)
======================
n/a

External Organizations (Nat)
================================
Australia (Dima/Joseph)
------------------------------------
Mike and Gail had a meeting last week.

Joseph and Mike have a meeting scheduled with Joe .



Berlin Group (Francis)
----------------------------
OIDF response was favourably accepted and the response is being written. 

There seem to be many people who would like to join the effort. 

BG is focusing on extended and paid services that can be offered by banks that are not regulated.


Brazil (Mike L)
---------------------
Phase.2 banks are going through certification. 10 of 25 went through. 

The deadline is tomorrow and need to observe the effect. 15 more needs certification.

There are issues around Consent API that it has to bundle claims that true data collection minimization is not possible.

There’s a communications issue between Security WG designing the consent API and the User Experience group that deals with what users see when they’re giving consent. 

Resolved by grouping permissions together during consent but may not be able to request minimal permissions.

Phase 2 deadline now postponed to August 13.

Also coordinating phase 3 efforts with Mirow  via Central Bank.

The Certification team is also looking to streamline the certification process.

#429 - https://bitbucket.org/openid/fapi/issues/429/fapi-certification-with-lodged-intent-or
* Ralph raised this issue regarding what should be in scope for certification.
* Make sure the user be informed of what they consented to
* Check is very subjective
* Generic check is difficult. Ecosystem specific check may be easier but requires ecosystem specific knowledge.


US/FDX (Mike L.)
------------------
Call with FDX. Reviewed original license agreement with reworked terms. 

Gail sent back a counter proposal (structuring it to a partnership instead of license agreement ) which FDX is now reviewing. 

Lukasz: what should be improved for fast adoption is, at formal level, open channel between FDX and FAPI. 

If OIDF is recognized as an organization member, topics can be discussed more openly at FAPI WG.

Open Banking in US looks like MiData. 

https://www.whitehouse.gov/briefing-room/statements-releases/2021/07/09/fact-sheet-executive-order-on-promoting-competition-in-the-american-economy/ is the official note.

They describe it as "Encourages the Consumer Financial Protection Bureau (CFPB) to issue rules allowing customers to download their banking data and take it with them."

https://www.consumerfinance.gov/about-us/newsroom/consumer-financial-protection-bureau-releases-advance-notice-proposed-rulemaking-consumer-access-financial-records/

The opportunity: A CFPB-issued open-banking regulation will make it easier for consumers to port their banking data and will simplify the bank-switching process. This could potentially help neobanks to pick off incumbents’ customers and persuade potential users to designate them as their primary banks. Neobanks would then profit from higher value per client and higher deposit totals. Convenient data movement would benefit challenger and incumbent banks alike by letting them share their data with fintechs. Banking players could then market seamless integration with fintechs as an enhancement to the customer experience to appeal to prospects and deepen existing customer relationships.
  * Will recommend but not require FAPI certification

OIDF should submit consultation responses for standards.

Dave will start a document and share it with the mailing list for collaboration.


MENA (Ali)
-----------------
Had high-level workshop with Ali and Don. 

Attended by regulators from UAE and Gulf countries

Topic on open standards and security for Open Banking APIs

Some opportunity with Abu Dhabi central bank as well.

Setting appointment with Dubai International Financial Center and Don regarding setting up a program for educating CSO and executives about standards.


Grant Management (Dima)
==========================
Drafts have been sent to the OIDF secretary for Implementer’s Draft. Nat will check the status.

Two scoping issues were discussed: Initially, for the WG and one for the FAPI 2.0 drafts.

Most of the discussion was on FAPI 2.0 drafts on whether it should require the Grant Management draft now that it is getting queued for the public review.

Dave inquired about updating FAPI charter. Main focus of the group seems to be a subset of the whole charter.

Narrowing scope of charter is possible. Expanding the scope requires approval from all members with IPR agreement for WG.

Background Information 

* Work going on regarding future directions of Open Banking Australia. 
* There is a question regarding adopting FAPI2, Grant Management. 
* It’s not clear what the additional benefits are from migrating from FAPI 1 to FAPI2, besides GM. 
* Ralph is positioning it as an upgrade, not just a security protocol but  also authorization framework that is covered by grant management with of privacy and consent.

FAPI2 upgrades the security side but will it incorporate transaction discovery or not?

Will FAPI2 be a suite of specs with baseline, advanced, and consent profile with Grant Management instead of GM being part of baseline or advanced.

What are motivations to upgrade to FAPI2?

FAPI2 has clear security model and less optionality for better interoperability. 

* Simpler so easier for security analysis.
* There was a lack of interoperability in the consent management area during analysis of Open Banking initiatives. That’s why GM was incorporated in FAPI2.

Ralph:

* If GM is not part of FAPI2, it should be broken up into constituent parts for different profiles: baseline, advances, RAR, GM, etc..
* Will FAPI2 be a security profile, security authorization profile, security authorization and consent management protocol. 
* Will it be a family of profiles as opposed to a monolithic profile?
* Solving consistently authorization and consent management is much better path forward.

Dave: We should avoid custom implementations like we seen in current ecosystems to further interoperability. Document the use cases of what we are trying to solve with FAPI2 to check alignment in the WG.

Lukasz suggested we wait until GM matures and leave note in spec to say it’s optional now but will be mandatory in the future. The whole spec might be too much for some jurisdictions to adopt all at once. 

Ralph : 

* It’s essentially segregating the missing parts. 

  1) Standardizing the flexible means to solve authorization 
  2) Standardizing the mechanism to manage authorizations.

* Main point is to be clear on the message of what FAPI 2 is about and what it’s trying to solve to encourage adoption  and influence the outcome for the benefit of all.

Brain disagreed that GM should be part of FAPI2 Security profile.

Ralph agreed with Brian that the primary issue of communication is nomenclature. Is it a security profile, trust framework, etc…? Have to make it clear what it is.

The WG seems to agree on a family of FAPI2 profiles versus a single document.

#412 - Hard requirement to support Grant Management Requirement 
Opened for further discussion


Most of the discussion was on FAPI 2.0 drafts on whether it should require the Grant Management draft now that it is getting queued for the public review. 

#413 - 
A question was asked if FAPI 2.0 ID2 can immediately follow ID1 and the answer from the chair was "yes". 

Some argued that it should to give more reasons for Banks to move from FAPI 1.0 to 2.0, as just simplicity does not give enough reasons for it. 

The discussion will be continued in the next session as well. 

AOB
=======
None

The call adjourned at 15:03 UTC