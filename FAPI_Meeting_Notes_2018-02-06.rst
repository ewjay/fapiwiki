============================================
FAPI WG Meeting Notes (2018-02-06)
============================================
Date & Time: 2018-02-06 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:07 UTC. 

Roll Call
===========
* Attending: Nat, Tom, Joseph, Bjorn
   * Guest: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Pull request, Q 6 A added
* FS-ISAC dropped. 

External Organizations
=============================

Open Banking (Joseph)
-------------------------
* Open Banking WS (Jan 29) was held. 
* A lot of discussion about what is allowed under RTS. 
* UK FCA interpretation is that HTTP redirect is allowed under certain circumstances. 
* It probably depends on the jurisdiction what is allowed and not allowed. 

OpenAPI (Nat)
-----------------
* Nat has a homework to put OpenAPI people and Open Banking people in touch. 

Implementer's Draft (Edmund)
==================================
Waiting for the pull requests from Dave and Joseph. 

Two pull requests were discussed. 

* https://bitbucket.org/openid/fapi/pull-requests/45/bring-access-token-requirements-inline/diff
* https://bitbucket.org/openid/fapi/pull-requests/46/state-fixes/diff

For the pull request 45, it was pointed out that guessability does not easily translate into the length of the token. A lengthy discussion followed. A new text is going to be proposed. 

For the pull request 46, Nat pointed out some editorial issue like the need of s_hash to be back-quoted etc. 


Renumbering the parts
========================
Nat is aware of the part number duplication in the current repo state. It will be fixed. 

Events
==============
OAuth Security WS (Nat)
---------------------------
* March 14-16

IETF 101 London (Nat)
-------------------------
* March 18 - 23

Open Banking (Nat/Don)
----------------------
* March 21

AOB
===========
Base64url question
-------------------------
Joseph asked for the reference of Base64url encoding specification. There was a question raised if it should be padded. Nat answered it will never be padded and that was the intention at the IETF. Nat will find the reference and send it to the list.  

Next Call (Atlantic)
-----------------------
The next call is scheduled to be in the Atlantic time zone. 

* The meeting was adjourned at 23:58 UTC.