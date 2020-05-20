============================================
FAPI WG Meeting Notes (2020-05-20) 
============================================
Date & Time: 2020-05-20 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call 
===========
Attending:
--------------------
Nat, Mark, Dave, Don, Kosuke, Joseph, Lukasz, Dima, Barry, Brian, Bjorn. 

Adoption of Agenda (Nat)
===========================
* Adopted as event

Events
===============
OIDF Workshop
--------------------
* Workshop tomorrow. Link: https://openid.net/2020/04/27/openid-foundation-virtual-workshop-may-21-2020/
* Nat intend to use the slides that Daniel used for OB/OIDF workshop + alpha on FAPI 1.0. 
* Slides: https://docs.google.com/presentation/d/1VbUZNOXbRfSnaZ1-aiI5Sx8hS6_rNvY6MS0nP6-HNy4/edit?usp=sharing
* Comments are welcome. 

External Organizations
=====================

Australia (Stuart/Dima)
-------------------------
Open Banking Australia Goes live July 1. 
Everyone busy preparing for it. 
Don to send out the response to the Farrel enquiry, whose deadline is May 21. 

* https://docs.google.com/document/d/1cPPN3wbJFGM9vv-w4Au1rOv3BZeT8Y01xHqe9z5TixI/edit#heading=h.fgy35k6wtl8z

ISO
-----
ISO/IEC 29184 Privacy notice and consent is getting published shortly. 
For those who are interested in User Consent, please refer to it. 

Pull Requests
================

Multiple issuers PR
--------------------
Dave sent out an enquiry to the OAuth WG to solicit wider community comment. 
We will wait until more feedback to come in before accepting the PR.  

Issues (Nat)
=============
During the call, two new issues were filed:

* #292: PKCE inconsistencies between Part 1 and Part 2
* #293: PKCE & Nonce Security Considerations

Taking the FAPI 1.0 Final (Nat)
==================================
Pending several issues, we should now consider moving Part 1 and 2 to the Final. 
The issues are: 

* Clean up re: public clients
* Changing the JAR reference to RFC number
* #292
* #293

We could consider FAPI-CIBA to Final as well, but we have to prove the interoperability of the independent implementations before that. Authlete, MoneyHub, Ozone Bank have implementations. The latter two should get the certification and then we can do the interop testings. 

Nat proposed the target date for submitting the drafts to the 60-days public review to be at the end of June. 
Dave commented that is reasonable, and everyone in the call agreed. 

AOB
==========================




The meeting was adjourned at 14:40 UTC.