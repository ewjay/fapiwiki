============================================
FAPI WG Meeting Notes (2017-10-11)
============================================
Date & Time: 2017-10-03 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:05 UTC. 

Roll Call
===========
* Attending: Bjorn, John, Nat, Edmund, Sascha, Tom, Pam, Carla
   * Guest: 

* Regrets: Anoop

Adoption of the Agenda (Nat)
==================================
* Added: CA report, FIDO report, 

External Orgs
================
Berling Group Consultation (Nat)
----------------------------------
Since PSD2 mandates the use of international or European standards to help fintech, 
there are couple of initiatives within Europe. Open Banking is one, STET(?) in France is another, 
and the Berling Group is one of the largest so many banks will be implementing it. 

Callers agreed to start writing a formal response back to the Berlin Group on Google Doc. 
Dave volunteered to create a shared Google Doc link and send it out to the mailing list. 

Consultation links: 

1. https://www.berlin-group.org/market-consultations
2. https://docs.wixstatic.com/ugd/c2914b_6a15d20b155a4d62922c67fe5a6e3dd5.pdf?index=true

See last weeks discussions for issues. 

Open Banking (Joseph)
-------------------------
* Basic test suite has been demo-ed to them. Go live date is next Friday. 
* Everyone is in implementation mode. 
* From the policy point of view, they are concerned about Berlin group, and concerned about the legal challenges for only supporting redirect based protocol, but for the time being, they are going to push for it. 
* Open Banking is going to put comments to Berlin Group. EBA's draft has a clause around having the API to be certified by a certain body if they are going to stop the screen scraping. That body may well be ERPB (European Retail Payment Board). Open Banking has a good connection with James Whittle who chairs that group. Feedbacks will happen in multiple fronts but it is Open Banking's interest to defend the current specification, essentially FAPI, and make the case for implementing APIs in more secure ways. 
* John pointed out that it sounds like the banks have to get certified before deploying a secure authentication mechanism. 
* What is needed for the certification is not clear yet. Independent body to assess that the API is available and friendly etc. It is likely to be connected to RPB. It is still vague at the moment. 
* Nat expressed the concern about Open Banking's mandate would be extended so that it will exist beyond January. 
    * Dave informed the group that it will be expanded from CMA mandate to PSD2 so that it will exist at least till mid-2018. 
 
Draft status and plans 
===========================

Verification: non-compliant JWT audience (Nat)
------------------------------------------------
Nat reported that the group agreed to remove audience last week and Pam was going to create an issue at the Open Banking. 

CIBA progress (Dave)
-----------------------
Couple of clarification given to Axel's questions. 
Dave asked if the joint meeting with Modrna was fixed on 7th. 
John pointed out that we were but with the apparent conflict with Berlin meetings we may want to move it. 
Don was going to talk to Open Banking trustees about it and get back to us, but so far we have not heard back. 
Dave said that 6th works much better for him and he will put more comments to the issues and update the draft to get inline with the main CIBA spec. Dave asked the group to give more feedback. 

John pointed informed that Open Banking trustee has asked for FAPI / OpenID Foundation meeting, that is probably around testing and broader issues. They probably are not interested in the details. We need to figure out where our WG discussions items will fit in. Nat pointed out that it seems it is prudent to block both 6th and 7th and fine tune the topics to be discussed there. 

Events
================
Open Banking F2F (Nat)
--------------------------
* Joseph asked about the Oct. 17 event. 
* Nat replied that it is the Open Banking meeting that Ralph informed us. It is not a FAPI meeting. 

FAPI/Modrna joint F2F
-----------------------
* See CIBA section above. 

AOB
===========

Next Call (Atlantic)
-----------------------
* The meeting was adjourned at 14:30 UTC.