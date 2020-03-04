============================================
FAPI WG Meeting Notes (2020-03-04) 
============================================
Date & Time: 2020-02-16 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
Attending:
--------------------
#. Nat
#. Pedram
#. Daniel
#. Kosuke
#. Dima
#. Brian
#. Joseph
#. Bjorn
#. Barry ODonohoe


Guests:
--------------
n/a

Regrets: 
---------------------   
#. Dave Tonge
#. Tony Nadalin
#. Anoop Saxena

Adoption of Agenda (nat)
===========================
Adopted as is. 

AU Consent Consultation (Dima)
========================================
Nat posted the proposal to the consultation GitHub repository. 
It was acknowledged and the consultation was closed. 

The next step is for Data 61 to come up with the response. 

In the meantime, we should work on the Grant request API so that we will be ready to submit in time. 

Grant request/consent API (Daniel/Dima)
====================================================
No updates. 

Quite a bit of detail to be worked out. 
Stewart and Dima discussed to hold another dedicated call. 
Dima will send the document. 

Refactoring of the specs taking the security assumptions in mind (Daniel)
==========================================================================
* FAPI 2.0 drafts consists of attacker model and security profiles. 

https://bitbucket.org/openid/fapi/src/master/FAPI_2_0_Attacker_Model.md

* Baseline profile document has a diff table between 1.0 and 2.0. 

https://bitbucket.org/openid/fapi/src/master/FAPI_2_0_Baseline_Profile.md

WG members are invited to comment on it. 

* Advanced profile has non-repudiation feature. 

This property has not been proved. Dima has contacted Pedram and U. Stuttgart for it. 

There is a lot of open issues which pertain to 2.0 rather than 1.0. 

Joseph voiced concern about requiring mTLS on Baseline. 

There is a virtual interim OAuth 10:00 AM Central US Time on this coming Monday to discuss these issues. 


Pull requests. 
==================
n/a

Issues
========
Dealt with #90, #279, #281, #275, #280, #274, #276, #163. 
See issues for more details. 

AOB
==========================
* Joseph pointed out that only 5/70 or so banks have certified against OIDF test suite and 11 for now obsolete OBIE. As the result, there are fair amount of interoperability issues, esp. on App2App. To sort it out, joint workshop etc. is being proposed. 


The meeting was adjourned at 14:59 UTC.