============================================
FAPI WG Meeting Notes (2017-06-27)
============================================
Date & Time: 2017-06-27 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:07 UTC. 

Roll Call
===========
* Attending: John, Nat, Tony, Dave, Joseph, Tom, Edmund, Anoop
   * Guest: 

* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Added issues, Berlin Group, 

External Orgs
================

Berlin Group (Dave)
-------------------------------
* Dave spoke with Tom of Payment UK. 
* He made the email introduction to Nat to Tom for TC68. 
* Berling Group timeline is not advanced as UK Open Banking since they only need to go online March 2019. 
* The initial feedback is positive in the relationship, especially on testing. 

FS-ISAC (Anoop)
--------------------
* There is a call scheduled on June 29 14:00UTC with the Security & Product and services group that deals with credential based aggregation. 
* BoA, Citi, Fidelity confirmed on the call. 
* From FAPI side, Anoop, Tony, Nat, and Dave. Dave was added because there is a high level of interest to the FAPI-PSD2 relationship. 
* Agenda Plan: 
    * Intro (10 min)
    * FAPI presentation (20 min)
    * Discussion (30 min)
* Nat plans to send the slides today. 

UK Open Banking (Dave)
---------------------------
* Specs coming out in a couple of days. 
* Need to document around hybrid flow. 
    * Spec itself should have a messaging. We may be able to extract Ralph's work. 
* Detached signature on the resource response. 
    * Not yet decided if mandated. 

EBA Regulatory Technical Standards (Dave)
-------------------------------------------
* EBA's new draft allows fallback to password storing if the API is not available. 
    * Quite a lot of opposition to the amendment coming up. e.g., UK banking group, Kantara, etc.  

Others
------------
* Dave reported CAPS and NETS.eu. NETS doing a lot of work on PSD2 and OpenID Connect on strong customer authentication. 


Draft status and plans 
===========================
Issues
------------------
* #102 -- Query re `x-fapi-...` headers
  WG agreed with Joseph's proposal. 

* #101 -- JWS signature algorithms for RW
  Reasonable to add RS256 back for the case where HSM does not support PS256. 
  Nat need to check with the OIDF secretary if it is ok to add it now or wait until after the vote. 

* #100 -- Signing API response payloads
  See the ticket. 


CIBA/Decoupled profile (Dave)
-------------------------------
* Dave is writing a draft now. Hopefully, he can post it by the next call. 

Others
----------
* Ping is working with RBS for June release. 
* Nat will get more info from FR and CA. 
* Apigee seems to have shown interested but Nat has not heard back. Dave will re-engage with them. 


Events
================
July 12 @ London
-------------------------
* WG meeting is scheduled to be from 9 am to 12 pm at Microsoft Paddington Office. It does not require registration. It is a WG meeting. 
* Afternoon seminar location is TBD. Nat will post the info as soon as gets to the list. 

CIS 2017 @ Chicago
------------------------
We had 4 related sessions. 2 on Monday, 1 on Tuesday (Ralph) and 1 on Thursday afternoon. 
There were a bunch of other PSD2 sessions as well. 
Also, FAPI was highlighted in the first keynote session on Tuesday. 
The interest level is quite high. 
PSD2 and GDPR are often linked together as the other side of a coin. 
GDPR also requires data portability so while it does not mandate API, it still makes sense to do it via PSD2 APIs. 


AOB
===========
PSD2 Trust Framework
-----------------------
Question of the client on-boarding was discussed. 
PSD2 requires the clients to be registered. In the case of the OB, it will be registered to the OB CA. 
Client registration would happen through Software statement. See http://openid.net/wordpress-content/uploads/2014/04/draft-mobile-registration-01.html for more details. 

There's a little bit of info on the open banking uk directory here: http://oixuk.org/wp-content/uploads/2016/10/OpenBanking-Update-22-May-2017-v1.0.pdf - page 46

Next Call (Atlantic)
-----------------------
* July 4 is US holiday so attendance may be light but we will do the call nevertheless. 

The meeting was adjourned at 23:58 UTC.