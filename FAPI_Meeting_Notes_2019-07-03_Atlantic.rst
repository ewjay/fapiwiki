============================================
FAPI WG Meeting Notes (2019-07-03) 
============================================
Date & Time: 2019-07-03 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:06 UTC. 

Roll Call
===========
* Attending: 
    * Nat Sakimura
    * Freddi Gyara
    * Brian Campbell
    * Joseph Heenan
    * Kosuke Koiwai (KDDI)
    * Anoop Saxena (Intit)
    * Bjorn Hjelm (Verizon)
    * Dima Postnikov
* Regrets:      
  * Dave Tonge

Adoption of the Agenda (Nat)
==================================
* Adopted as is. 

Draft Status (Nat/Dave)
=======================
FAPI CIBA profile (Nat)
-----------------------------
FAPI CiBA profile has gone into the implementer's Draft public review period. 
The announcement can be found at: https://openid.net/2019/07/01/public-review-period-for-fapi-client-initiated-backchannel-authentication-ciba-profile-started/

The relevant dates are: 

* Implementer’s Draft public review period: Tuesday, July 2, 2019 to Friday, August 16, 2019 (45 days)
* Implementer’s Draft vote announcement: Friday, August 2, 2019
* Implementer’s Draft voting period: Friday, August 16, 2019 to Friday, August 23, 2019 (7 days)

So, it will hopefully be the 1st Implementer's Draft by the end of August. 

OAuth JAR (Nat)
-----------------------
* IETF JWSReq lacking one posistive vote. One of directors dropped off. 
* John Bradley is looking into it. Once it has enough votes, will go to publication.
* Then will need to refactor FAPI Part 2 to refer to the RFC and eliminate duplicate parameters.


OAuth MTLS (Brian)
------------------------
* MTLS client authentication RFC status : awaiting second AD review due to changeover of ADs. In waiting queue of AD to move it along.


sub issue #223 (Anoop)
================================
* #223 - Need of a customer unique/immutable identity as part of ID Token
* Anoop: user has multiple logins at bank, after add the first bank account, user will be asked to reauthenticate after token expires. User doesn't know which username and password to use at website. It's difficult to validate without receiving an account number. By the time, banks get account number, it will be too late to identify username and password.
* Hoping to get a id after authentication which uniquely identifies login at bank.
* When using screen scrape, Fintech app has username and password to match but in this case doesn't have it.
* User may have reauthenticated using a different account and it's too late to inform user of wrong account.
* In past, used sub to identify unique subject that is logging in. Got overloaded with Consent ID which changes every time. Don't have identifier when token is returned identifying which authentication it is for.
* Current set of APIs and responses don't fulfill needs of account aggregators.
* As of 3.1.1 of APIS, parties endpoint allows getting some information regarding parties associated with account. Isn't mandatory endpoint. No clear legal requirement for it. FCA indicated that they expected this to be part of APIs but did not state so  in  any formal publication.
* Closest OIDC can provide is sending ID Token as login hint token. Don't think any banks doing it at the moment.
* The way it's solved in US is added custom attribute in Oauth token response which banks are willing to share.
* Apps get token together with ID Token. Can send ID Token back to AS in id_token_hint field, so user can be shown which login user used in last login.
* RP has to have way to communicate that back to AS so bank can prefill user name. 
* Promote use and support of id_token_hint.
* Recommentation is to promote use id_token hint. Anoop will look to see if this will solve the problem.
* Assumption is that ephemeral subjects can be correlated and checked. No requirement in OIDC for AS to trackback in this manner. Need to provide some guidance but still optional for banks to implement.
* Promote that this pattern  is needed in account aggregator and personal financial manager use cases.
* Given situation, law is minimal required must implement features. Given situation, people may opt to use screen scraping. PSD2 does not specify replacement for screen scraping.
* Can promote proper pattern for screen scraping uses.
* Anoop mentioned token expiry, in UK, it may be the consent expiry. When making authorization request, if passing same Consent ID, banks are not allowed to let user select different account.
* Intent ID is tied back to user, passed as claim in request so banks can identify.
* For OB, have temporary solution. 
* Pointed out in section on reauthentication in the CEGs.
* Intent ID is local solution, promote use of id_token_hint instead. In OB, sub is filled with intent ID or unique ID for PSU.
* Brian concerned about specifics and feasibility of trackbacking of sub to user. This behavior is application specific. Not specified by protocol. There is text that either makes assumption or is strict about that assumption in terms of processing of id_token hint
* OIDC  3.1.2.2 (4)  Authorization Server MUST only send a positive response if the End-User identified by that sub value has an active session with the Authorization Server or has been Authenticated as a result of the request
* In absence of application specific context, and understanding of sub, might be problematic. Might not change existing implementations.
* For now, for OB, promote this usage pattern.
* FAPI part 2 does not mentioned anything about sub. If it's general pattern for banks, it's better to give guidance and document the problem and make it known in implementation guide.
* PSD2 says user must perform strong reauthentication every 90 days. OB gives guidance that when presenting previous Consent ID, banks should not ask user to do anything other than strong authentication and return back to TPP.
* Hoping once banks do proper app to app authentication, problem will disappear.
* Banks should perform risk evaluation and perform reauthentication when needed but not strictly every 90 days.




Event Report
==============
Nat and Dave were present. Nat was involved with board so did not attend much sessions. Dave not present at meeting to give report. Will revisit at next meeting.


AOB
==========================

Next Call
-------------------------
* Atlantic call next week. 

The meeting was adjourned at 15:28 UTC.