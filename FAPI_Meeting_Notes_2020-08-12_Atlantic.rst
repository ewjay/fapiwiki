============================================
FAPI WG Meeting Notes (2020-08-12) 
============================================
Date & Time: 2020-08-12 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: 
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* 

Events 
======================

External Organizations
========================
W3C
-------
There are two workstreams that are potentially relevant to FAPI. 
One is Web Payment. 
The other is WebID CG. WebID is trying to sort the problem that a browser cannot reliably distinguish legitimate authentication federation and web tracking. It is related to ITP. 

Privacy Path @ IETF that uses JWT seems to be relevant here as well. 

OBIE (Chris)
----------------
1. rest of CMA9 still working towards certifications

2. Significant potential breaking issue reuse of PSD2 eIDAS certs in the UK if a no-deal Brexit after 1 Jan - see https://eba.europa.eu/eba-calls-financial-institutions-finalise-preparations-end-transitional-arrangements-between-eu-and

Particularly this phrase: Furthermore, account information service providers (AISPs) and payment initiation service providers (PISPs) registered/authorised in the UK will no longer be entitled to access customers' payment accounts held at the EU payment service providers and their PSD2 eIDAS certificates under Article 34 of the Commission Delegated Regulation (EU) 2018/389 will be revoked.

If taken at face value, and if all QTSPs revoke all UK firms' PSD2 eIDAS certs, and if FCA retains the current requirement for these PSD2 eIDAS certs in the UK, then...

PRs for 1.0 (Dave)
====================

Please give feedback to all the standing PRs. 

PR 182
---------
* https://bitbucket.org/openid/fapi/pull-requests/182

It is using the real domains as examples are straight out of the conformance test. It should be replaced with example.com etc. 

PR 161
----------
* https://bitbucket.org/openid/fapi/pull-requests/161

Changing a should to shall, requiring metadata to be obtained through OIDD. 

Note: a few banks currently fails this requirement. 

PR 181
----------
* https://bitbucket.org/openid/fapi/pull-requests/181

PR 186
----------
* https://bitbucket.org/openid/fapi/pull-requests/186

Nat proposed a text. Ralph is writing a friendly amendment to it. 
Once it is ready, it should be merged in. 

AOB
==========================
n/a

The meeting was adjourned at 14:59 UTC.