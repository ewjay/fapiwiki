============================================
FAPI WG Meeting Notes (2018-06-06)
============================================
Date & Time: 2018-05-23 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call
===========
* Attending: 
   * Guest: 
* Regrets:  

Adoption of the Agenda (Nat)
==================================
* 

New Co-chair (Nat)
======================
* Dave Tonge is now a co-chair. There was not objection: i.e., the WG approved his co-chairship unanimously. 
* Dave's message. 

Implementer's Draft
=======================
* Review Results?: Ralph, Joseph, Brian 

Road map for OpenBanking -> FAPI (Ralph)
=============================================
* Delta between the OB spec and Part 2
    * https://gitlab.com/fintechlabs/fapi-conformance-suite/wikis/OB-specific-tests
* Conformance test harness
    * Evaluation of the delta

* Open Banking 

External Organizations
=========================

OpenBanking (Ralph)
----------------------
* 

ISO/TC68/SC 9 (Dave)
----------------------
* Released the first draft. Not much is changed. Part 1 and 2 are in there. 
* Unsure of the process. 

Other EU SDOs (Dave)
------------------------
* STET and Berlin Group
* Joint Workshop towards the end of June. 

Pull Requests
================
* https://bitbucket.org/openid/fapi/pull-requests/

* https://bitbucket.org/openid/fapi/pull-requests/45

Those on the call accepted the change and recommended that it be merged in

* https://bitbucket.org/openid/fapi/pull-requests/49/add-clause-requiring-as-to-check-when/diff

There was agreement to go with Nat's proposed wording. Dave to update the pull request.

* https://bitbucket.org/openid/fapi/pull-requests/55/part-2-clarify-that-servers-may-support/diff

There was agreement to merge in the change. There was some discussion about the need to have a standards based approach to "lodging intent". OpenBanking, Stet and Berlin Group have all taken different approaches and none of them are using the request object endpoint. Dave to raise an issue for this.

* https://bitbucket.org/openid/fapi/pull-requests/53

Tom advised that we should hold on this - he will get back to us on the next call.

* https://bitbucket.org/openid/fapi/pull-requests/54

We discussed this pull request and then moved into a related issue, see below.

Issues
===========
* https://bitbucket.org/openid/fapi/issues?status=new&status=open

* https://bitbucket.org/openid/fapi/issues/11/oauth-profile-should-mandate-rfc7636-pkce

We discussed this and came to the consensus that PKCE should be required for all clients in part 1, not just public clients. Joseph to create a pull request with this change.

* https://bitbucket.org/openid/fapi/issues/132/requirement-on-token-lengths-may-less-than

This issue can be closed when the related pull request is merged

* https://bitbucket.org/openid/fapi/issues/140/new-name-for-fapi

We discussed this issue and agreed to leave some comments on the issue. There was a discussion about whether the name needed to match up with FAPI at all.

* https://bitbucket.org/openid/fapi/issues/139/treatment-of-returned-scopes-divergent

Those on the call felt that the wording in FAPI was fine, even though it is more restrictive than the base standard.

* https://bitbucket.org/openid/fapi/issues/100/signing-api-response-payloads

We discussed this and agreed that Dave would try and raise the issue in the OAuth Working Group.



AOB
===========

Next Call
-----------------------
The next call is scheduled to be in the Pacific time zone. 

* The meeting was adjourned at 14:50 UTC.