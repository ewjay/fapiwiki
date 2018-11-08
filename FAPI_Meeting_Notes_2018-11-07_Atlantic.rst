============================================
FAPI WG Meeting Notes (2018-11-07) 
============================================
Date & Time: 2018-11-07 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call
===========
* Attending:　
    * Nat
    * Bjorn Hjelm
    * Dave Tonge
    * Joseph Heenan
    * Ralph Bragg

* Guests: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Added Issues. 

CIBA Progress Report (Brian/Dave/Bjorn)
=====================================
* It is expected that the split will be complete next Tuesday. 
* Reviewers needed. 
* FAPI profile work can start once the split is finished.

External Organizations
==========================

Australia (Ralph)
-------------------
* They are supporting ID Token but that is not linked to account number, etc., making the linking hard. 
* Luke Pacowell(sp?) will take over security profile.
* Some spec issues : a) forced to have single set of client credentials for each associated business that you're dealing with. Haven't decoupled individual from underlying organization. Not sure how they're going to handle identity with this approach. Things are progressing. Will include first/last name in ID Token but will not have identifier in customer records, so there no way to tie ID Token and customer record together.
* Have asked them to join pacific calls.
* Pacific calls are have started talking about data schema. Will ask OB to contribute functional specs to OpendID foundation.

UK Open Banking (Ralph)
-----------------------------
* Specs have been decoupled from OpenBanking Directory
* OB Security profile will undergo FAPI rewrite, new version will go live end of year
* Variable repeat payments will not be included. There are lots of desire to get spec done but no commitments to implement functionality. Therefore use cases such as sweeping, auto funds transfers between accounts cannot be delivered. There is no regulatory obligation to implement such functionality. Lots of TPP questioning overall usablity/effectiveness  of OB series of functional APIs.
* Chris is working on functional spec, but there is no buy-in from ASPs to do it
* TPPs may negotiate w/banks to create extended APIs for for needed functionality, but APIs will be delivered under contract, which is frustrating because banks may decided not to use OB centralized identity/KYC/Credentials, etc..
* May end up that some banks continue to use trust frameworks and security model for all TPP activity, not will need to see what happens.
* OB KYC is for B2B transactions to provide highly assured developer/business owner credentials and associated linkages to validated companies. Allows B2B KYC. Allows orgs to establish relationships quickly among banks and TPPs or any organization. But there is no commmitment from ASPs to use it outside of OB banking.
* Any work regarding customer kyc? - TPPs are calling out issue with fraud risk
* Sample scenario : TPP issues loan for customer data containing great credit/transfers. TPP have good case for getting some customer or account information into payload, but it is still optional for ASPs. Anything more may end up in an optional spec where banks are allowed to sell customer identity. No requirement to deliver it.
* Torsten mentioned KYC at IIW and EC is starting to look at KYC. Submitted Torsten's PDF doc to Australians. * Identity is a valuable commodity.  OB is well placed to standardize it and facilitate PSU identity being shared through a common broker/hub. Infrastructure is there. Hoping APIs can reach out to ASPs and bring them to table to build ecosystem.

Issues
==================
Following issues were discussed. For the details, see the tickets. 

* #110: more definition of s_hash - Reopened due to having to register s_hash in JWT IANA. Should be put into Part 2 IANA Considerations. 
* #180: Behaviour of AS when presented with a non-uuid x-fapi-interaction-id is not clearly defined. ID only needs to be unique and does not need to be a UUID. May relax client requirement for discussions.
* #182: 128 bits of entropy cannot give probability of guessing below 2^-160. There are other ways than entropy to reduce probability (e.g. blacklisting/rate limiting). Will add more explanation.
* #183: Poor section title: 5.2.2.1 returning authenticated user's identifier Authorization server. Suggested title accepted => "Authorization server returning authenticated user's identifier"
* #184: Privacy implications of oauth-mtls due to tls 1.2 sending client certs unencrypted. Will add privacy considerations. 
* #185: PKCE or Part2 mechanisms? Will delete "or the mechanisms in.." part.
* #186: BCP for OAuth 2.0 for Native Apps clause wording could be improved.  Will add condition "if native app".
* #187: Part 1 client requirements for state/nonce aren't reflected as authorization server requirements. Will be breaking change, so it will go into the next draft version.
* #188: Broken link in FAPI part 1 ID2. Will look into fixing the link.

Next Call
-----------------------
Next Pacific call will go as scheduled. 

* The meeting was adjourned at 15:02 UTC.