============================================
FAPI WG Meeting Notes (2020-01-29) 
============================================
Date & Time: 2020-01-29 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call
===========
Attending:
--------------------
#. Nat
#. Torsten
#. Dima
#. Kosuke
#. Joseph
#. Dave
#. Mark
#. Ralph
#. Stuart
#. Bjorn

Guest
-------


Regrets: 
---------------------    

Agenda Bashing (nat)
==================================
* Consent Management and Grant Management API (Torsten)
* Event 
* Issues

Consent Management and Grant Management API (Torsten)
========================================================
* https://docs.google.com/document/d/1VkrkiFSoUwdKaW3aOI4zq0YeFr7tdbuyfjeswCSLNLI/edit

The "grant API" is provided by AS. 
User can revoke the grant. 
User I/F hosted by TPP can revoke the grant. 
Grant info is jointly owned by client and the user (recipient and holder). 

Grant lifecycle. "Invalidate", "Suspend" etc. may also be needed before being deleted. 
Renewing grant needed. 

To bring back an expired grant, a new authorization request using the existing grant id will do. 

Next Steps
------------
* Continue with the google doc till Feb. 18. 
* Add grant lifecycle diagram. (Ralph) 
* Add Intermediary use-case. 
* Get the doc into markdown and put it in the FAPI repo. 

Event
======
Swift Conference/FAPI F2F (Torsten)
-------------------------------------
If you are attending the F2F, please register via the following link: 

* FAPI: https://www.eventbrite.com/e/oidf-financial-grade-api-fapi-ftf-working-group-meeting-in-london-tickets-90772558165
* eKYC-IDA: https://www.eventbrite.com/e/oidf-ekyc-ida-ftf-working-group-meeting-in-london-tickets-90776191031
 
Link to the OIDF IPR Agreement and Contribution Agreement: https://openid.net/intellectual-property/

* Nat needs to catch up with Don re: Swift conference on getting explicit FAPI topic. 
* It is proposed in the WG call to use Torsten's slide [1] in the meeting.  

[1] https://docs.google.com/presentation/d/1LyebJ8FhC1sIM9F5e9TNHRPDOYuXiilHt4wQBkvRvtc/edit

Issues
========
#undef: duplicated KeyID (Joseph)
------------------------------------
This came out of Connect WG. 
For interop reasons, this was added to FAPI test suit. 
Ralph mentioned that the same question came out in Open Banking. 
Joseph will create a ticket referring to the Connect WG ticket. 


External Organizations
=============================

Australia (Stuart)
--------------------------
Stuart solicited people to the way in on the ticket re: 
CDS ticket based on CDR analysis. 

* https://github.com/ConsumerDataStandardsAustralia/standards-maintenance/issues/101


Next meeting
======================
* Next week, same time. 

AOB
==========================
n/a.

The meeting was adjourned at 14:58 UTC.