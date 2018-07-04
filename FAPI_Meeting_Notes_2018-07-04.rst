============================================
FAPI WG Meeting Notes (2018-07-04)
============================================
Date & Time: 2018-07-04 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: 
   * Nat Sakimura
   * Ralph Bragg
   * Joseph Heenan
   * Henrik Biering
   * Rob Otto
   * Guest: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* 

Recap of the F2F @ Boston (Nat) 
=========================================
(see notes from last week for the detail)

Short term work plan (Nat)
==============================
* We need to distribute the work to expedite the change to the CIBA core spec. 

Ralph suggested that OB need an updated document in 8 weeks time.

Several people who had offered assistance weren't able to join the call so no decision was made. Nat will create a ticket in the issue tracker to talk about dividing the work.

Ralph indicated OpenBanking can provide some assistance.


Liaison Reports (If any)
===========================

Ralph reported that the STET/Berlin will consider moving to an international standard with a proven implementation, but there's no timescale for a decision.

The Berlin group are focussed on functional changes to their APIs to align with the latest EBA guidance. The EBA guidance has more effect on the rest of the EU (where it provides guidance on the intent of the law) than it does on the UK (where only the letter of the law matters)..

Issues
============

#149: Make it clear that the entire flow is OIDC Hybrid Flow - no one objection, Nat will suggest text

#150: Mandate at_hash check in the ID Token from the token endpoint - no objection was raised to going ahead with mandating at_hash

There was a discussion about the wider security points like certificate pinning, DNSSEC, etc that would need to be in order to ensure that the mechanism for the client to obtain the server's signing keys is sufficiently secure. Nat suggested that a broader spec like https://tools.ietf.org/html/draft-ietf-oauth-security-topics may be a better place for widely applicable recommendations like that. Nat will suggest to Torsten that this is discussed at IETF Montreal.

AOB
===========
Next Call
-----------------------
Next week's call is Pacific Time Zone. 

* The meeting was adjourned at 14:45 UTC.