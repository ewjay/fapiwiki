============================================
FAPI WG Meeting Notes (2021-05-12) 
============================================
* Date & Time: 2020-05-12 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-04-07_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
* Attending: Bjorn, Dave, Nat, Ali, Brian, Daniel, Dima, Filip, Francis, Joseph, Kosuke, Lukasz, Ralph, Stuart, Takahiko, Torsten
* Regrets: Vinod Anandan (self)
* Guest: 

Adoption of Agenda (Nat)
===========================
* Adopted as is. 

Events (Nat)
======================
Brazil Workshops (Joseph)
----------------------------------
* Not open invite. Need to drop email to Joseph to get an invite. 

Identivers (Don)
---------------------
* A few presentations on FAPI. 

Open Banking World Congress (Don)
---------------------------------------------
May 11 - 13. Dave Tonge spoke. 

Site URL: https://congress.openfuture.world/speakers/?utm_campaign=OBWC21&utm_medium=email&_hsmi=122216549&_hsenc=p2ANqtz-85MvO81z4sSX-dOrIbCIC77pfdwrqN1LhYxs6JTNfFHSk6PP3ROFz2iSRjFU6OdZZ-50Pr2u0HE4KChrgo0Y_r3ALFfw&utm_content=122216549&utm_source=hs_email

Presso: https://www.linkedin.com/feed/update/urn:li:activity:6798194660650061824/?midToken=AQEYA6ePoVQTBg&midSig=37bbJEUaPKcpM1&trk=eml-email_notification_single_mentioned_you_in_this_01-notifications-1-hero~card~feed&trkEmail=eml-email_notification_single_mentioned_you_in_this_01-notifications-1-hero~card~feed-null-32hrd~kolciuly~45-null-voyagerOffline

External Organizations (Nat)
================================
Brazil (Ralph)
---------------
Sizable directed funding for certification test. 
Mandating CIBA. 

Berlin Group (Francis)
---------------------------
Nat to suggest setting up sub-committee to FAPI to deal with BG needs. 
Two co-chairs. Dave Tonge from OIDF and another from BG. 

Modrna Report (Dave/Bjorn)
=============================
Trying to move CIBA Core to final. 
There are a couple of issues that are being covered by PRs. 

* Adding text for sender constrained token and push mode. 
* New parameter for showing text on the consumption device. e.g., select a number from the following three. 

* https://bitbucket.org/openid/mobile/issues/197/clearer-binding-message-verification
* https://bitbucket.org/openid/mobile/issues/178/modes-supported
* with relevant blog post: https://ritou.medium.com/binding-message-verification-and-candidate-list-parameter-in-oidc-ciba-90ffcefa6665

Certification (Joseph)
========================
* Certs team is working on FAPI 1.0 Final test to go live at the end of this month. (Beta in one or two weeks.) 
* Directed funding from Brazil for their profile. 
* Simple Dynamic Client Registration being added. 

Docker Run (Stuart)
=====================
* Stuart Demoed the current one. 
* Discussed which files are to be processed automatically, and agreed. 

PRs (Dave)
===================
PR 266 Grant Management - Introduce replace action (Stuart)
------------------------------------------------------------
* https://bitbucket.org/openid/fapi/pull-requests/266
* Addressing issue #396, related to #407

This introduces replace action into the GM specification and attempts to include security considerations with respect to permission propagation.

* Lukasz: If it is in fact merge, wouldn’t naming it “merge” make it more self-explanatory?
* Brian: The replace action text seems okay. But the security considerations seems overreaching.
* Dave: Use cases need to be collected. 
* Ralph: Delete and Revoke have different connotations, esp. legally. In UK, the ownership of the grant rests on TPPs. TPP opinion needed. 
* Dima: There are local requirements for Replace.  
* Brian: Security concerns - not realistic to propagate the change in Grant to AT immediately. 
* Separating the PR into two seems to be reasonable? 


Issues (Dave)
=================
We had no time to discuss issues but Dave pointed out that new issue #411 should be considered re: HTTP signing. 

AOB
=======
* none