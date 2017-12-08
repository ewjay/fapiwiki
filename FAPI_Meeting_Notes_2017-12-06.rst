============================================
FAPI WG Meeting Notes (2017-12-06)
============================================
Date & Time: 2017-12-06 17:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 17:__ UTC. 

Roll Call
===========
* Attending: Brian, Dave, Don, Pam, Bjorn, John, Chris & Gavin (Open Banking)
   * Guest: 
* Regrets: Anoop, Tony

Adoption of the Agenda (Dave)
==================================
* Agenda adopted

Open Banking IE Topics (Chris & Gavin)
================================

Decision 088: authorizing multiple intent-ids at once
--------------------------------------------------------
* https://openbanking.atlassian.net/wiki/spaces/WOR/pages/24805559/088

Decision 089: Partial acceptance of intents 
---------------------------------------------------
* https://openbanking.atlassian.net/wiki/spaces/WOR/pages/28934198/089

Decision 090: how tokens issued from the authorization grant are managed
-------------------------------------------------------------------------------
* https://openbanking.atlassian.net/wiki/spaces/WOR/pages/28934212/090

We discussed these 3 issues length and there was a general consensus that passing multiple intent ids was OK, but there should be a limit to the number (maybe 10?). Chris made the point that this feature isn't for bulk payments, but rather for scenarios that could involve 3 different payments, e.g. a deposit, a payment on delivery and a regular monthly payment. John made the point that this is essentially similar to scopes, and that a decision would need to be made on whether the user could only accept some of the intents and how that information would be communicated back to the client.

On decision 90, Pam volunteered to create a worked example and share it with the list, for further feedback.


AOB
===========
* John brough upp with issue of Strong Customer Authentication (SCA) not being phishing-resistant (https://medium.com/@davidgtonge/not-so-strong-customer-authentication-692abf022f92) 

There was a discussion that it would be useful to create some guidelines on what good SCA looks like. This could be helpful for the industry and is closely linked to the FAPI profile.

Next Call
-----------------------
The next call is scheduled to be in the Pacific time zone. 

* The meeting was adjourned at 16:10 GMT.