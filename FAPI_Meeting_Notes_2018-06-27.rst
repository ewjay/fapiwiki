============================================
FAPI WG Meeting Notes (2018-06-27)
============================================
Date & Time: 2018-06-20 15:30 EDT

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:40 UTC. 



This is a note from the Ad Hoc Meeting and still being written. 

Roll Call
===========
* Present: Nat (NRI), Chris(OBIE), Joseph(FintecLabs), MBJ(MS), Ralph(OBIE), Brian(Ping), Rob(Ping), Mike Andre, Mark , Michael Eagan (T-Mobile), John (Yubico)
* Observers: Shibata-san, Shinzaki-san (NRI Secure Technology) 

Adoption of the agenda (Nat)
=============================

CIBA Spec
============

Categorization of the specs
---------------------------------

The group discussed and agreed that there are legitimate case of starting with QR code as a part of discovery and do the usual redirect flow instead of CIBA. 

Thus, the group agreed that it would be creating two set of specs: 

* CIBA Core + CIBA FAPI profile
* Discovery standard

CIBA Core + CIBA FAPI profile is time critical while the Discovery is not, thus the group will first work on the former. 

CIBA Core Issues (Brian)
-------------------------
Brian explained the problems existing in the CIBA Core right now per his email. 
To sum up, there are many inconsistencies and cannot be reliably implemented. E.g., 

* Endpoint needs to be fixed. 
* Client authenticaiton 

There was an observation by John that much of the inconsistency actually stems from the symmetric authentication needs. If these parts were separated out and if the core just talks about the asymmetric authenticaiton, it will become much simpler and more consistent. 

The group agreed to remove the symmetric option from this document, I.e., move to another MODRNA specific document. 

Structured Login Token (Ralph)
-----------------------------------------

Structured Login Token that indicates the identifier type is desired. 
   Login_hint_token

Reason for login hint token was to blind the RP. 

There are cases where you are required to share a static identifier. 

CIBA Core states Login hint MUST be validated. This actually does not work. 

JSON Login Hint

ID Token Hint : No Validation. One can if wanted. 

Extend the login token hint to allow multiple types. 

Pull the construct from MODRNA Discovery to CIBA, generalize. 

JWT in JWT. 

{
 - type:
 - value: 
}

Login hint token subject type in the Server Metadata: IANA registry
 First define in CIBA.