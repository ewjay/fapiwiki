============================================
FAPI WG Meeting Notes (2019-06-05) 
============================================
Date & Time: 2019-06-05 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:06 UTC. 

Roll Call
===========
* Attending: 
    * Nat Sakimura (NRI)
    * Joseph Heenan (FintechLabs)
    * Bjorn Hjelm (Verizon)
    * Brian Campbell (Ping)
    * Dave Tonge (Moneyhub)
* Regrets:      
  * 

Adoption of the Agenda (Nat)
==================================
* 

External Organizations
==========================

ISO/TC 68
-----------

Testing & Certification
=========================
* Two more certifications for FAPI coming thorogh. 
* One passed properly but no papers yet. 
* The other certification has some discussion over how strict the error responses are. 
* Whetehr 'acr' claim is mandatory is another issue. 

Draft Status (Nat/Dave)
=============================

CIBA FAPI Profile (Dave)
----------------------------

TR Lodging Intent Pattern & Transaction Authorization with OAuth (Torsten)
---------------------------------------------------------------------------

Events
=============

Identiverse
---------------------
* Nat, Bjorn, Brian are going to be there. 
* Joseph is not going to be there. 


Issues
===========
We have discussed several issues in this call: 

#223 Need of a customer unique/immutable identity as part of ID Token
-------------------------------------------------------------------------
In essence, the issue is pointing out that there are use cases where 
there has to be a persistent identifier for the PFM clients. 

This is a classic login mixup vulnerability. 

Alice and Bob are sharing a browser and in one session, Alice was using the client while in the next session, it was Bob so that Bob's data is concatenated to Alices, and potentially leaking Alice's information is being leaked to Bob. 

Nat is going to follow it up. 

#219 JARM: expires_in should be a number
-----------------------------------------------
Brian created a pull request for this but there are some left over. 
The issue was taken by Brain. 

#218 LoA3 requirement in part2 may be too much
-------------------------------------------------------
Currently, none of the UK Banks comply to the LoA3 requirements. 
This is related to #201. 
Dave pointed out this is related to #201 and that this is a policy issue and not technical issue so it should be left out of FAPI. 

Nat pointed out that this is also related to #223. 
There are several cases.

* Case 1: Payment where the client does not care anything but the authorization by the bank for the payment. 
* Case 2: The client is concatenating data it is obtaining to the previously acquired data. (#223 case)
In this case, the client may want to have some assurance that the `sub` is stable. 
* Case 3: The client is allowing access to the data it has acquired based on the identity that the bank provided. In this case, the client may want to have strong authentication being performed by the bank. 

Dave then pointed out that even in Case 3, it is up to the ecosystem to decide and the spec should not be prescriptive. 

Nat pointed out that stating X.1254 LoA 3 is not really prescriptive that it is just saying to meet the security level appropriate to "high risk" scenario that the ecosystem agrees to. X.1254 LoA is a measurement scale that each ecosystem should establish the "equivalence" to each level by going through the individual requirements (i.e., enrollment, credential management, and entity authentication) and the sentence mentioning LoA3 is saying all these and while he is OK with rephrasing it, he is not for removing it.  

Joseph volunteered to come up with wordings. 


AOB
==========================


Next Call
-------------------------
* Atlantic "Spec" call next week. 

The meeting was adjourned at 14:03 UTC.