===========================================
FAPI WG Agenda & Meeting Notes (2021-11-05) 
===========================================
Date & Time: 2020-11-05 01:00 UTC 17:00 PST (5pm)

Location: GoToMeeting https://global.gotomeeting.com/join/321819862


.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 01:00 UTC. 

Roll Call (Nat)
=====================

* Attending:   Nat Sakimura, Mark Verstage (DSB), Dima Postnikov, Edmund Jay, Ivan Hosgood (DSB)
* Regrets:  Anoop

FAPI 2.0 Discussions (Mark)
===========================
Topics that we talked about are: 

* The scope of "FAPI 2.0 Suite", e.g., FAPI 2.0 Profiles, Grant Management, PAR, RAR, CAEP, RISC, CIBA etc. 
* The scope of the Formal Analysis may need to be synchronized with that. This would give really give a compelling advantage of FAPI 2.0 Suite over FAPI 1.0 as the latter's formal analysis does not involve those extra bits. 
* We also need to start planning for the conformance test suite development. Need to involve Gail and the team. 

Refresh Token Rotation (Mark)
==============================
* Issue #456
* A lot of interoperability issues on Refresh Token Rotation found in Australia. Many banks rotate refresh tokens with the change of Access Token. 
* Nat pointed out that is not the intention of Refresh Token and FAPI 1.0 does not ask for the rotation. It is always assumed that the refresh token is not rotated so we could even issue interpretation notes on it. 
* Watching at the fact that Many Implementation follows refresh token rotation anti-pattern, it would be advisable for FAPI 2.0 specs to explicitly prohibit Refresh Token rotation. 
  
Next Call
-----------------------

* The meeting was adjourned at 01:54 UTC.