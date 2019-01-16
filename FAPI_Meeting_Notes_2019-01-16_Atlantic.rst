============================================
FAPI WG Meeting Notes (2019-01-16) 
============================================
Date & Time: 2019-01-16 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:09 UTC. 

Roll Call
===========
* Attending:　
    * Nat, Brian, Daniel, Dave, John, Joseph, Torsten, Bjorn, Freddi, Chris

* Guests: 
* Regrets: 

Adoption of the Agenda (Dave)
==================================
* Adopted as proposed. 

Security Whitepaper (Torsten)
================================
* https://bitbucket.org/openid/fapi/src/a12ba4dd3694573310d927d8ae234ec5d4c817e3/TR-Cross_browser_payment_initiation_attack.md?at=master
* 

External Organizations
==========================

STET, Berlin Group  (Torsten)
--------------------------------
* No news. 
* Dave will also try to get in touch with them once the TR is complete with figures. 


Australia (Ralph)
-----------------------------

UK OpenBanking (Freddi)
-----------------------------
* Progressing with ver. 4. 


ISO/TC 68 (Dave)
-----------------------------
* Draft sent out a week ago. He will meet with the editor next week. 
* Feedback sought. 

Issues
==========================

# 204 CIBA Binding Messages (Dave)
------------------------------------
* https://bitbucket.org/openid/fapi/issues/204/ciba-binding-messages
Examples should be added. No concrete proposal yet. 
Assigned to Dave and taken off-line with Freddi. 

#205: Add requirement for Client to verify state matches session (Torsten)
-------------------------------------------------------------------------------
* #205
* Torsten still work. 

#206: CIBA - Add reference to the relevant clauses in FAPI RW (Dave)
-------------------------------------------------------------------------------
* #206
* text in the spec that explicitly refers to 5.2.2 in FAPI1 and FAPI2 is sufficient and I propose we close this 

#207: RS256 vs PS256 (again)
-----------------------------------------
* #207
* Lengthy discussion around it. Recommending not to use RS256 seems to be fine. People tend to use it for both signature and encryption once it is allowed. 
* Also, John pointed out that moving from RS256 to PS256 should not require complete re-registration of the client as keys are going to be the same, but Brian pointed out that there is no way to do so in the spec. 
* Chris pointed out that OBIE is trying to come up a method that smooths it. 

#208: Part 2 should limit allowed JWE algorithms (Joseph)
-------------------------------------------------------------
* #208
* PKCS 1.5 banning is only written in the context of signature. We should do so for encryption. 

AOB
==========================
Ozone reference bank experience (Chris)
------------------------------------------
* There seems to be some portion of the spec that should be softened from SHALL to SHOULD. 
* One of them is the parameter duplication: John and Nat should probably press harder for OAuth JAR. 
* Chris/Freddi/Joseph to come up with the concrete set of those issues for the next Atlantic call. 

Next Call
---------------
* Pacific call next week. Atlantic call in 2 weeks time.

The meeting adjourned at 15:05.