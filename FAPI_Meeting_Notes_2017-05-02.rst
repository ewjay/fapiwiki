============================================
FAPI WG Meeting Notes (2017-05-02)
============================================
Date & Time: 2017-05-02 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 15:10 UTC. 


Roll Call
===========
* Attending: Nat, Dave, Edmund, Joseph, Tom, Anoop
* Regrets: 


Adoption of the Agenda (Anoop)
==================================
* Adopted as is. 


Issues 
========
* Issue #87 - Need create request_uri endpoint in AS
    * No objections from the callers. 
    * Nat will draft the chapter. 
* Issue #88 - Client ID in the front channel
    * John suggested from Ping implementation experience that having `client_id` in the front channel is 
      useful in filtering the request in the case of using `request_uri`. 
    * Dave agreed and no objections were found. 
    * OpenID Connect actually mandates it but OAuth JAR does not. So, FAPI should mandate it. 


External Orgs
================

FS-ISAC (Anoop)
-----------------
* May 18, 19. One hour allocated for how to extend OAuth 2.0 to support a couple of use cases. 
    * partner ID --> ID Token
    * token binding
* Discussion on DDA in relation to other standards e.g., FAPI, OBS, OFX. 
    * We should at least inform them of the current status in UK etc. 
* 40 members getting together in two locations. Virginia and San Francisco. 
* Top 10 banks and some fintech are participating in the form of a roundtable. 
* They are only concerned with read only so FTC etc. does not come into the picture. 
* Dave will send some material to the list. 
* Primary product to "sell" to them is the Part 1: RO security profile. 
* Anoop will create a presentation and send it to the list for review. 

UK OBS (Nat)
-------------------------
* Joint seminar with UK OBS on May 22. 
* Expect some news in a couple days. 

ISO/TC68 (Nat)
-------------------
* Finally sent out our liaison request. 
* 4 weeks ballot starting. 



AOB
===========
Part 2 completion timeline 
------------------------------
* Edmund is working on the security consideration and the corresponding lines in the introduction. 
* Nat will work on the request object endpoint chapter this week. 
* Content-wise, it should be complete by the end of the week. 

Next Call (Atlantic)
-----------------------
* Please refer to the group calendar for the exact call time. 

The meeting was adjourned at 23:50 UTC