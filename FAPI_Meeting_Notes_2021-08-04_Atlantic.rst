============================================
FAPI WG Meeting Notes (2021-08-04) 
============================================
* Date & Time: 2020-08-04 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-08-04_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:04 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Nat, Dave, Joseph, Kosuke, Brian, Dima, Domingos, Ion, Daniel, Fiona, Stuart, Taka, Lukasz, Filip, Ralph, Francis, Danillo, Ali, Barry O'Donohoe. 
* Regrets:
* Guest: Mike Lesczc

Adoption of Agenda (Dave/Nat)
================================
* 

Events (Dave/Nat)
======================
EIC (Dave)
---------------------


OAuth Security Workshop (Daniel)
-------------------------------------

External Organizations (Dave/Nat)
===================================


Australia (Dima/Joseph)
------------------------------------

Data Standards Body has joined OIDF.

Mike Lescz to schedule a call with DSB team to facilitate participation in WG calls and for overall updates from DSB in 
Australia


Berlin Group (Francis)
----------------------------

Mike Lescz to consult with Tom Smedinghoff to ensure the Pros engagement process does not cause any IPR issues.

First common session with BG will be in September.


Brazil (MikeL)
---------------------

Working with Mirow to get the final phase 2 institutions certified. Deadline has been extended to  August 13.

Also confirming phase 3 institutions that need certification. Deadline is scheduled for August 31.

Lots of activity involving Payments API. Current situation is a mess and the Phase 3 deadline will likely be pushed back.

Ralph has concerns that certifications are issued for non-production systems. User experience and consent flows may not have been implemented and customers were not actually presented with any of the correct information about what they have consented to.

Ecosystem certifications are very nuanced and not easy for OIDF to do and have lots of factors involved.

There should be a separate certification for customer experience elements.

Joseph and Mirow had a call regarding working around certifying actual production systems. Questions will be raised to the Central Bank.

Need to make sure that this doesn’t cause a reputational issue for OIDF where certifications have been issued but banks do something else afterward.

Partly related to a tight timing schedule.

The Central Bank has set a firm timeline to go live for payments. OIDF has set a deadline for the 200+ bank certifications to be submitted in order to be processed in time.

The Central Bank is aware of the problem.

Certification submissions are tracked and shared with Mirow for transparency.



FDX (Don)
------------------

Still awaiting response from FDX


UK (Ralph/Chris)
--------------------

CMA has mandated Variable Recurring Payments for Implementing Sweeping.

CMA9 to implement it by January 2022.

CMA to make an announcement regarding the future state of OBIE around September.


Russia (Don/Dima)
--------------------

PRs (Dave/Nat)
=================

Pull request #283 - FAPI Grant Management ID1 Review: Editorial Fixes
Editorial fixes to be merged afterwards


Issues (Dave/Nat)
=====================


#432 FAPI2 Trust Framework structure (Dima)
---------------------------------------------------
Daniel made a new proposal on how to visualize FAPI 2 ecosystem components 

Dima - missing authorization methods at the moment

* Redirect
* Decoupled
* Embedded recommendations for Berline Group

Need to outline options of how to capture authorization (e.g. implementation advice)

The baseline/advanced profile and the other spec components gives you the toolset and the implementation advice will give guidance on how to use them.

Joseph: This might impact the certification tool. We should stay away having to implement ecosystem specific pre-launched intent mechanisms.

Implementation advice is not considered normative.

Might consider a normative document on what to use when and how to combine features.

Might consider making advanced authorization profile mandatory in addition to other solutions during the transition period.

Individual components will complicate certification while we’re trying to simplify the certification process with less optionality.

Dave : We start to define the scope of these documents and look at ways of presenting them.

Dima will review and clarify some areas and certification possibilities.



#429 FAPI Certification with Lodged Intent or RAR - User Consent vs Technical Process Certification
------------------------------------------------------------------------------------------------------
There is not much FAPI WG can do at the moment. Keep with certification team and keep on top of it.



#433 Track FAPI compliant RP libraries (Dave)
-------------------------------------------------

Daniel provided some feedback.

Security BCP may possibly overwhelm developers and might be better for them to use libraries instead.

Give the message that it’s better to develop good libraries for implementation.

RP certification is difficult to setup to execute. Orchestration process is complicated. Should provide an example.

Many libraries are simple and do not implement extensions.

Self implementations often have many mistakes. Security is not as high.



#412 FAPI 2.0 - Hard requirement to support Grant Management Requirement
--------------------------------------------------------------------------------
* #412 FAPI 2.0 - Hard requirement to support Grant Management Requirement
* #417: Shall require introspection of claims
* #416: RAR if scope *and* claims param not expressive enough

Create Pull Requests to remove reference to RAR and close issues or reassign to the new spec.

Dave and Dima to work on them.




AOB (Dave/Nat)
=================


The call adjourned at 15:01 UTC