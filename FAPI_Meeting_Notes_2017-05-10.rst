============================================
FAPI WG Meeting Notes (2017-05-10)
============================================
Date & Time: 2017-05-10 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call
===========
* Attending: 

* Regrets: 

Adoption of the Agenda (Nat)
==================================
* 

External Orgs
================

Euro Retail Payments Board (Dave)
-------------------------------------
* https://www.ecb.europa.eu/paym/retpaym/euro/html/index.en.html
* Need to create a report by June. 
* Establish formal rel. with them? 
* Dave will meet with them next week. 

UK OBS (Dave)
-------------------------
* Good call on Monday with OBS and Dave, Nat, John. 
* Explained the split. 
* UK is developing their own data payload and endpoints
    * e.g. https://www.openbanking.org.uk/developers/
    * https://developer.openbanking.org.uk/open-data/api-console/
    * https://github.com/OpenBankingUK/opendata-api-spec-compiled
* UK OBS to adopt modified FAPI for the begining with the roadmap to comply later
* May 23 workshop
* OBS hoping to join FAPI, under legal check now. 

ISO/TC68 (Paul)
-------------------
* Need to send out the liaison letter to them. Paul will update the list in 48 hours time. 
* Nat will update the WG presentation so that it can be attached to the letter. 
* The liaison letter need to go out pretty soon. 

Starling Bank (Dave)
----------------------
* TOauth
* Came up with OAuth 2.0 API. 
* re: #77, #78
* Nat to send Torsten's draft to the list. 
* Dave to start using it to persuade banks. 

Mobile Connect (Dave)
-----------------------
* Mobile Connect being introduced as strong customer authentication by Banks. 
* Modrna has relationship with CPAS 
* Back Channel Authentication -- two proposals. 
    * CIBA
* Two joint workshops May 11, 12. 
* Current IPR problems with GSMA may be able to be addressed by using LC. Bjorn and Nat will talk about it next week at IIW. 

Others
------------


Part 2: WGLC Issues 
===========================
* #93: Not clear why AS needs to support signed+encrypted ID Token
* #92: Put cipher suite recommendations in the security considerations
* #91: Id mix up attack
* #89: s_hash needs to be defined more precisely
* #88: Sender constraining the code
* #87: Need create request_uri endpoint in AS
* #78: Malicious Endpoint Attack
* #77: IdP Confusion Attack
* #60: Only one method to Token Bind AT rather than two?


AOB
===========
Next Call (Pacific)
-----------------------

Meeting was adjourned at __:__ UTC.