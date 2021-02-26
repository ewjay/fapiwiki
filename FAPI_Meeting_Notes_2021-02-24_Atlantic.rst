============================================
FAPI WG Meeting Notes (2021-02-24) 
============================================
* Date & Time: 2020-02-24 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Daniel, Torsten, Takahiko, Brian, Dima, Lukaz, Joseph, DOn, Francis, Kosuke, Ralph, Brian Chris, 
* Regrets:
* Guest: 

Adoption of Agenda (Nat)
===========================


External Organizations (Nat)
================================
W3C Web Payment Interest Group (John)
--------------------------------------

Nat has been communicating with someone at FIDO and will start attending W3C group meetings soon.


Australia (Dima/Stuart)
----------------------------------

No updates

Berlin Group (Francis)
---------------------------

No updates

Brazil (Chris/Ralph)
----------------------

No updates

Canada (Ralph)
------------------

No updates

UK (Don/Ralph)
-----------------
* Talked to Fiona Hamilton on the history of OBIE and OIDF. 
* Planning to do a deeper demo of conformance suite. 

* Bill Roberts and UK Finance is working on how to change the organization of OBIE. 
* Timeline is within next 12 months.
* Some parts are to be handed over to some other orgs. It is very fluid. 
* UK Finance will be taking over the standards for Financial APIs.
* Open Energy. Energy ecosystem modeled on UK platform RAdium to be set up by July 2021. 

USA 
----------

OIDF and FDX is completing a legal agreement on use of OIDF trademarks.

Rounding up on existing liaison agreement that lays out “rules of engagement” for adoption of FAPI and self-certification test suite results as part of their certification program. Announcement to be made at their Global Summit in April.

Ralph: Some of FDX’s RFCs and extensions haven’t had much scrutiny from IETF and OIDF. There are duplications of DCRs claims of fields that have already been defined. At what point does OIDF say no to these and not certify them because they are not aligned with OIDF or haven’t been through appropriate governments or we’re concerned that could introduce certain challenges? Where does the line get drawn between consent authorization and security standards?

Don: Development and evolution of FAPI belongs to OIDF. Look to FAPI working group for how the standard and the certification program will evolve. The foundation's role is simply to protect its processes and its trademarks, but also to provide a clear working environment for its working groups. We’re going to continue to help FDX and help organize their early stage certification program.

Lukas: We need to promote FAPI in such a way such that there is an isolation of FAPI and FDX’s extensions. There will be more cooperation between FAPI and FDX and we’re going to have clear isolation in the test certification on what is FAPI and what is FDX. FDX would rather use FAPI.


Torsten: I don’t understand how the cooperation will be structured. We presented 
Grant Management to them a couple of times. There were lots of questions but no one has come back to discuss a way forward. There was no feedback. How is the cooperation going to be structured? There are occasional meetings with no follow up.

Don: The most effective way to impact development of FAPI is to join the FAPI WG. I keep inviting FDX members to join FAPI. The developer community for FDX is new to OIDC, FAPI. We hope that we can schedule a series of workshops that will provide some education for them. We haven't finalized those workshops yet. FDX members can join OIDF and contribute to standards.

Joseph: FDX WGs are well coordinated with regards to standards between their WGs.

Lukas: There may be some legal obstacles as well. FDX meeting information must be kept within FDX and may not be disseminated to outside groups. So even if there are members in FAPI and FDX, they cannot distribute the information to the FAPI WG. 

Nat: What is the current liaison setup with FDX?

Don: Currently, OIDF is working at maximum transparency. FDX members do not have the same flexibility to report discussions. OIDF is looking for practical ways to benefit from more open exchange within legal limitations of their members. We have the opportunity with the FAPI FAQ and roadmap to provide to FDX and all of its members as clear of a view as possible as to the current state of FAPI and its development and future direction. We will share the drafts with FDX members and invite them to comment and provide feedback.


Chris: When developers start building FAPI and FDX together, that will get people to start having conversations and rethinking sooner and will expose things that need change. 


Events (Nat)
======================

1st call of GOFCoE WG
------------------------


KuppingerCole Event on March 3
------------------------------------
* https://www.kuppingercole.com/events/identity-fabrics-future-proofing-iam
* March 3. 
* On FAPI 2.0 and FAPI 1.0 differences by Daniel. Mainly on FAPI 2. 

Open Identity Summit 
-----------------------------
* https://oid2021.compute.dtu.dk/
* Submission deadline: March 1. 
* June. 

Identiverse
-------------

June 21-23, 2021.
Identiverse tickets are available. 
Joseph will do a presentation on latest practices for OAuth 2.0 and OIDC on mobile.

OIDF Workshop
--------------

Don will send information to mailing list.




Adoption of the Grant Management Draft (Nat/Dima)
==================================================
* Announced the call for adoption on the 17th. 
* No objection till today, so it is now adopted. 
* Thanks the SG for taking this forward. 
* Dima would like the WG homepage updated to include the specification.


PRs (Dave)
===================
* Pull request #229 - remove Warning from Part 1/2 of FAPI 1.0

  * merged

* Pull request #241 -  HTML feedback changes

  * Merged

* Pull request #238 - contributor list
* Pull request #239

  * Declined - PR changes already in other PRs

* Pull request #242 - FAPI 1.0 Introduction simplification

  * Accepted and merged

* Pull request #243 - Add PAR and JAR to Bibliography

  * Accepted and merged


Edmund to produce HTML version for review before submission to OIDF secretary.


Issues (Dave)
===============

Lots of new Grant Management issues

Filip raised questioned about the philosophy we will pursue with Grant Management, where we assumed that the grants are fully and explicitly managed by the client. If the client does not specify a grant_id, there's automatically a new grant and grand_id being generated, which means a new concurrent grant setup. Filip proposed that this be an option where the client does not need to pass the grant ID but the AS is not going to be establish a new grant, but just return the grant ID for the grant it picked for that transaction.We should talk in the group what we want to achieve. I would like to know other people's opinion.

Dave: Can we provide a way for a client to request a new grant?  If they don't specify a client ID and they don't specify they want a new one, then the AS can at its discretion decide what to do.

Torsten: Right now, there aren't just two options.

1) Omit the grant ID and a new grant is created
2) client passes a grant ID in the parameter, then this grant ID is used.

If we want to allow the client to leave the decision of whether a new grant is being spawned to the AS, we need to have a signal from the client to the AS. We originally had an additional parameter called grant management mode that we could have used for that, but was stripped in order to simplify the specification.


Brian: It's extremely difficult to reason about what the different combinations of parameters and metadata fields actually mean, in terms of expected behavior. Simplification actually made it more difficult to understand. I’d like some improved clarity behind the reasoning.


Dave: I see downsides to just automatically creating a new grant.

Takahiko: We don't have any metadata which describes characteristics of refresh token behaviors. I suggested that we define the meta- data. There are 2 ways to control the behavior:

1) Define client metadata
2) Define request parameter

Torsten: One of the reasons why we went for the client policy approach is that most features in the OIDC and OAuth just work that way. The client specifies a policy or somehow sets up a policy that controls a lot of the behavior. And only a couple of things are controlled by parameters. iI feels more in line with the design philosophy of the ecosystem. Even though I see a lot of advantages with having parameters because then you can change behavior on a per transaction basis.


AOB (Nat)
=============


Chat Log
============