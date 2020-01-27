============================================
FAPI WG Meeting Notes (2019-12-18) 
============================================
Date & Time: 2019-12-18 14:00 UTC

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
#. Danel
#. Dima
#. Joseph
#. Kosuke
#. Mark Haine
#. Robert
#. Torsten
#. Dave Tonge
#. Freddi Gaya
#. Stuart Low

Regrets: 
---------------------    

Adoption of the Agenda (nat)
==================================
* Debrief from Financial Data Summit Added. 

Event
======
Financial Data Summit (Torsten)
---------------------------------
* Meetings between UK OB, Berling Group, and OIDF on how to cooperate to achieve international standard for financial APIs
* UK OB and Berlin Group confirmed that they want to work with OIDF on a standard security profile that can be used by various initiatives within SWIFT
* UK OB and Berlin Group and STET agreed for Common Data Model. 
* Security profile is the last missing piece. 
* Vinat Markessen (sp?) from National Institute confirmed that they would like to work with OIDF also
* SWIFT
* Don Managed to get us invited to SWIFT meeting. 
* Setting up formal LS between BG and OIDF for cooperation on security profile.
* Meeting on 15th of January to talk about the scope of the potential liaison in Bonn. 
   * CfC for participation to the list. 
* Would like to incorporate the way the actual authorization data are being conveyed to FI AS. Should extend scope to have interoperable profile that can be used to authorize access to financial and other security grade profiles.
* Authorization data refers to all data that are relevant to the authorization process. (Payload to PAR, RAR, and JAR)

* Feb. 18. FAPI F2F in London.
* IETF WG has call for adoption of PAR. There is a possibility that RAR will be adopted also but there is not call for adoption yet.

#163 Security Model (Daniel)
=============================

* https://docs.google.com/document/d/1Lo2LCV5eV7iVGbsM0C7i3pL1nWRftfqjpfFCx5Q3Pds/edit#heading=h.u85w4jb6qchc
* https://docs.google.com/spreadsheets/d/1PtG4f-Svils7wHBa7cGaZubbh-6lGifce38c_oShSss/edit#gid=550739163

WG discussed the initial text created by Daniel. 

* https://bitbucket.org/openid/fapi/issues/163/more-description-of-the-security-model
* https://docs.google.com/spreadsheets/d/1PtG4f-Svils7wHBa7cGaZubbh-6lGifce38c_oShSss/edit

They generally agreed that the attacker model is about right. 
Nat has seen some attacks that are as elaborate if not more than attacker model.
In Chilean banks case, attackers servers have TLS certs that belong to bank's domains. 
It's useful to add examples of attacks to attacker model and differentiate which are unrealistic attacks.

* A6 may be unrealistic
* A4 attack of authorization responses (popular during early days of OAuth)
* A3B reading of authorization responses and returning payload to client, attacker can send anything to client. Not an attacker reading from headers or logs. Not easy to turn passive attacker into active attacker.
* Cases of malware making requests on behalf of users after they have logged in
* Want to protect against unpopular but trending attacks. In Japan, attackers are cracking OTP protected pages since they are not phishing-resistant
* What's the difference between replay and tempering? If one can intercept requests/responses, one can replay and replay potentially tempered data. Whats the difference between replay and tempering with actual request/response?
  * Replay requires a browser in the loop and is more of an CSRF attack
  * Tempering is more of an server side attack
  * Fine line between them

Daniel also pointed out that there is one attack that we do not have a solution for. (PKCE chosen text attack.) 

Might be more attacks if we do a systematic analysis of the specs.
Need to think about attacks and their mitigation.
Have to add wording that the honest endpoints are not hacked, otherwise nothing is guaranteed

Would be worth it to put scenario regarding when both DNS and TLS are attacked.
Just having TLS is not good enough since DNS is often times not protected. 

HSTS is a basic web security measure that should be enabled but is not recommended anything in FAPI specs.

Next step is to propose more concrete wording for FAPI profiles.
Take FAPI profiles and create a first draft specification with all mechanisms that we think we need and then see they would defend against attacks.

Baseline is the next Read-only spec and Baseline + non-repudiation or advanced is the RW spec


WG members are invited to make comments on the document and the ticket. 
If it is a concrete change proposal to the document, it should go to the document itself. 
If it is a more general discussion, it should go to ticket #163. 

Next meeting
======================
* The next meeting will be January 8, 2020. 

AOB
==========================


The meeting was adjourned at 14:56 UTC.