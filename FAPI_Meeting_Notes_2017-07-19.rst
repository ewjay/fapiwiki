============================================
FAPI WG Meeting Notes (2017-07-19)
============================================
Date & Time: 2017-07-19 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: Bjorn, Nat, Dave, Joseph, Ralph, 
   * Guest: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Added Berlin Group. 

Implementer's draft voting for the Part 2 is going on (Nat)
================================================================
* PLEASE VOTE! The vote closes on July 24. 
* Most of the editorial changes are in. Couple of them, such as the support of RS256 in case of using HSM where HSM does not support ES256, PS256 is postponed to the next revision as it was a bit of work to come up with the note that does not raise criticism from cryptographers. Pull requests are welcome. Please see the tickets that are marked R3 - November 2017 for those. 

CIBA Profile (Dave) 
========================================================================
* Please put comments into the tickets. 

Issues
=========
* Looked at the issues list. All the new issues are related to CIBA Profile. 
* There are issues marked R3. They need to be dealt with. Pull Requests welcome. 

External Orgs
===============

UK Open Banking (Dave/Nat)
-----------------------------
* IPR contribution agreement received and posted to the site. 
* Need to ping Don for the "letter" to the OB trustee. 

Berlin Group (Dave)
---------------------------
* Talked with Torsten and hopeful to come up with a draft liaison letter next week. 

Events
==========

OAuth WS @ Zurich (July 13, 14)
---------------------------------
Very good discussions. Both Nat's paper and Torsten+John's paper is pertinent to the topic. 
* Nat's presentation: https://zisc.ethz.ch/wp-content/uploads/2017/02/sakimura_future-proofing-oauth.pptx
* Nat's paper: https://zisc.ethz.ch/wp-content/uploads/2017/02/sakimura_future-proofing-oauth.pdf
* Torsten's presentation: https://zisc.ethz.ch/wp-content/uploads/2017/02/lodderstedt_accesstoken.pdf

There are other interesting presentations as well. The entire agenda and files can be found at  https://zisc.ethz.ch/oauth-security-workshop-2017/. 

IETF99 OAuth WG (Nat)
-----------------------
* We had the first OAuth meeting. 
* Nat reported the status of OAuth JAR. It has now incorporated all the comments received and draft-14 will be pushed later today. 
* Torsten and John presented the pros and cons of various ways of constraining access token. The result of the discussion was that sender constrained token only did address the access token phishing properly. Others are not. At the same time, the deployment-ability of token binding is recognized as an issue. 
* Dave asked if it is too much of restriction for FAPI to only have Token binding for public clients. 
* Nat answered that it is not the client side problem. The client can include libraries, such as AppAuth and that will be fine. It is more of the server side issue. For example, if the server is behind the F5 and if F5 does not support token binding, then the server cannot support token binding. 

AOB
===========
* None. 

Next Call (Pacific)
-----------------------
* Please do refer to the group calendar for the time. 

The meeting was adjourned at 14:__ UTC.