============================================
FAPI WG Meeting Notes (2019-10-16) 
============================================
Date & Time: 2019-10-16 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
Attending:
--------------------
#. Bjorn
#. Dima
#. Nat
#. Brian
#. Kosuke
#. Joseph
#. Stuart
#. Freddi

Regrets: Dave
---------------------    

Adoption of the Agenda (Joseph)
==================================



OpenBanking CIBA
================

Freddi shared that OpenBanking has published new draft specifications that align with FAPI-CIBA, links for these were shared and Joseph emailed them to the working group mailing list:

http://lists.openid.net/pipermail/openid-specs-fapi/2019-October/001566.html

Pull Requests
=================

https://bitbucket.org/openid/fapi/pull-requests/144 - looks to be awaiting updates from Torsten

Issues
================

https://bitbucket.org/openid/fapi/issues/271/rename-and-adjust-fapi-profiles - waiting for Nat to send note to list

https://bitbucket.org/openid/fapi/issues/255/certification-clarification-request - Joseph to propose text to add clause to FAPI-v1 to emphasise clients should check

https://bitbucket.org/openid/fapi/issues/252/question-about-accessing-userinfo-endpoint - close, point at connect bug tracker

https://bitbucket.org/openid/fapi/issues/251/refresh-token-expiry-time - discussed and suggested raising it at the connect group

https://bitbucket.org/openid/fapi/issues/250/certification-clarification-request - discussed but no clear consensus on should vs must

https://bitbucket.org/openid/fapi/issues/249/certification-clarification-request - discussed but no clear consensus on should vs must


https://bitbucket.org/openid/fapi/issues/245/fapi-ciba-client-authentication-at - close as spec seems to be clear enough


https://bitbucket.org/openid/fapi/issues/242/missing-bibliography-reference-to-fapili - Stuart agreed to produce a merge request for this

https://bitbucket.org/openid/fapi/issues/236/charset-not-needed-for-application-json - charset is not required; Brian agreed to propose a change


AOB
==========================

Stuart asked about the status of the lodging intent document; various members pointed out Torsten's latest work on the subject:

https://tools.ietf.org/html/draft-lodderstedt-oauth-rar-01

https://medium.com/oauth-2/rich-oauth-2-0-authorization-requests-87870e263ecb

https://medium.com/oauth-2/transaction-authorization-or-why-we-need-to-re-think-oauth-scopes-2326e2038948

There was discussion about whether FAPI-CIBA should move to referencing RAR (instead of the lodging intent document) but it was felt to be too early to do this but we should review the situation in a few months.




The meeting was adjourned at 14:56 UTC.