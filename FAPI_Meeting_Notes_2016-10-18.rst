============================================
FAPI WG Meeting Notes (2016-10-04)
============================================
Date & Time: 2016-10-18 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: John, Nat, Anoop, Edmund, Henrik, Sascha, Brian C. 
* Regrets: Dave, 

Adoption of the Agenda (Nat)
===============================
* Added **Pre-IIW Presentation (Sascha) 

Atlantic Call Report (Nat)
===============================
* Please refer to [[FAPI_Meeting_Notes_2016-10-12]]
* There is API Days in Paris on 13, 14 December. The organizer will be in IIW so we may want to connect with him. 
    * Dave is supposed to introduce him to John and Sascha
    * There currently is a FUD that "OAuth is no good for financial APIs", so we need to find somebody to be there to present.

External Org Relationships 
=============================

UK Implementation Entity (Dave)
-------------------------------
There has been an update from the UK Implementation Entity:
http://www.paymentsuk.org.uk/sites/default/files/Implementation%20Entity%20Steering%20Group%20-%20Oct%202016%20Update%20to%20CMA.pdf

Key points from a FAPI perspective:
 - The trustee has been appointed
 - Working groups and advisory boards are being convened
 - There is a push to ensure the API standards developed comply with PSD2 (and the RTS)

I haven't had any more specific feedback apart from the general communication linked above.

I hope to have more information before the call next week. 

Others
----------------
* OFX (): Anoop to follow up for the meeting on Friday after. 
* FIGO (Anton): http://docs.figo.io/  
* Apigee: https://openbank.apigee.com/home : Got email introduction from Dave. Not heard back yet. 
* DDA (Brian C./Anoop): 

OFX (Anoop)
-------------
* Anoop and Don will have meeting on the Friday the week after. Anoop will follow up on the details with Don. 

Apigee (Nat)
-------------
* Dave made an introduction to Nat over email. 
* Nat responded to it but is yet to hear back. 

FS-ISAC (Brian C./Anoop)
--------------------------
* Aggregation work group has re-convened but there is no firm direction yet. 
* Brian will introduce the progress of this group. 



Action::

    * Anton to get in touch with FIGO. 
    * Nat and John will try to get in touch with Apigee as well. 


Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Restructuring (Nat)
----------------------
* No new progress as both Nat and Edmund was busy working on the ISO meeting preparation. 
* Hopefully we can show the progress in the next call. 

Issues 
=========================

#32: How to communicate back the partial errors to the client (Anoop)
-----------------------------------------------------------------------
# issue #32
* Anoop added a suggested solution. 

Action::

    * Edmund to check how to express it in Swagger. 

Events
=============
Pre-IIW Presentation Review (Sascha)
-------------------------------------
* We went over the Slides. Couple of points were made. 
    * Should be updated with #33. 
    * Should add some names for the external org (EU EBA, UK IE, US X9, etc.)
    * DDA-InteractionId should be changed to x-fapi-requestid
* Sascha will send the slides out to the list once these changes are applied. 

Pre-IIW (John)
----------------
* https://www.eventbrite.com/e/openid-foundation-workshop-tickets-27312519481
* Now sold out (130). Expect 50 - 100 people. 
* Will check if there is remote access / webinar. 

Pre-IETF (Nat)
-----------------
* John has made a room request. Waiting for the response. 

AOB
========

Next Call
----------
* No call next week due to ISO and IIW. 
* 2016-11-02 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)

