============================================
FAPI WG Meeting Notes (2018-04-03)
============================================
Date & Time: 2018-04-03 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:02 UTC. 

Roll Call
===========
* Attending: Nat, Tom
   * Guest:
* Regrets: Joseph


Adoption of the Agenda (Nat)
==================================
* Since IIW is going on, we only got two people so we decided to cancel most of the topics and talk about Tom's issue only. 

Issues
===========
#135 Confidential client needs a strong identity for the user to verify real world entity
-------------------------------------------------------------------------------------------------
It was discussed that it would be very important for the Banks to show who is asking for the money. 
The client needs to be identity proofed strongly and then authenticated strongly so that its identity can be shown to the user before the user gives consent. 

Tom felt that it is not so important in the case of read only because money will not be extracted so that it should be added to the Part 2. The user interface requirement should go into 5.2.2 and identity proofing requirement into 5.2.4. 

Then the privacy aspect of the issue, especially in view of GDPR, was discussed. The result was that these requirements, in fact, should go into Part 1, and privacy consideration (Clause 8) should also be added. 

Tom is going to work on a pull request to Part 1. 


Events
==========
IIW
-----
IIW is going on right now. 

AOB
===========

Next Call
-----------------------
The next call is scheduled to be in the Atlantic time zone. 

* The meeting was adjourned at 23:20 UTC.