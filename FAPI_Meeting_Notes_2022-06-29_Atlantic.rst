============================================
FAPI WG Meeting Notes (2022-06-29) 
============================================
* Date & Time: 2022-06-29T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-04-13_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Nat)
======================
* Attending: 
* * Dexter Awoyemi
* * Jacob Ideskog
* * Ralph Bragg
* * Michael Palage
* * Rifaat Shekh-Yusef (Okta)
* * Brian Campbell (Ping Identity)
* * Joseph Heenan (OIDF/Authlete)
* * Kosuke Koiwai
* * George Fletcher (Capital One)
* * Gail Hodges
* * Nat Sakimura
* * Daniel Fett (Yes.Com)
* * Elizabeth Garber
* * Lukasz Jaromin (Cloudentity)
* * Takahiko Kawasaki
* Regrets: Dave Tonge
* Guest: 

Adoption of Agenda (Nat)
================================
Adopted as is

Events & Liaisons (Joseph on behalf of Mike L.)
====================================================
Brazil
-----------------
preparing for OPIN (open insurance) certifications in August. And then open banking recertifications September through December that will also require DCR certs.

SAMA
--------------
positive meeting in Denver with SAMA representative confirming that 3rd party certification model works best for them. SAMA has requested formal communication/validation from WG regarding best practices for adopting FAPI 1 that will allow SAMA to most efficiently and effectively transition to FAPI 2 once it becomes a final spec.

Nigeria
-----------------
recent meeting highlighted central bank's guidance on open banking was more focused on policy and process than technology so there's more work to do there. We'll reconvene at the end of July to get an update from Open Banking Nigeria.

PRs (Nat)
=================
PR #342 – No Authorization Response encryption is required
------------------------------------------------------------------
Although it was acknowledged that "no confidential ... wording" had a push back as it is not correct, 
now the same words are in this PR (Security consideration). It should be revisited. 

PR #344 – Rename update action to merge
-------------------------------------------
Fixing #436. 
Lukasz expressed that he likes it and approved it during the call. 


Issues (Nat)
=====================
#436: Change grant_management_action "update" to "add" or "append"
------------------------------------------------------------------------------------
Reopened as the PR 344 is still not merged. 
To be resolved after the merge. 

#496: clock sync and FAPI2 baseline
--------------------------------------
Last week, we agreed that HTTP date header would work, but we still need a text. 

#505: Create security and privacy consideration for FAPI 2.0 Security Profile
-----------------------------------------------------------------------------------
The section is empty and needed to be filled before going to the next implementer's draft. 
Any contributions are welcome and please write them to this ticket. 

#506: Explicit security target
--------------------------------------
The attacker model states common requirements for all the FAPI 2.0 specs 
but each document lacks its specific ones. 

#507: FAPI2S 4.5 Differences to FAPI 1.0
---------------------------------------------
Some of the text is misplaced, missing, and inaccurate. 
They need to be fixed. 

#478: FAPI2 Baseline + jarm & iss draft
---------------------------------------------
It was reopened 5 days ago by Dave. Check with Dave to see why. 


AOB (Nat)
=================
* Gail reported that contact between U of NSW and U Stuttgart is being completed for the security analysis. 
* Joseph is planning to make some recommendations to the Executive Committee next Thursday on the relying party developer support. Essentially trying to encourage open source libraries across a variety of different languages, the ones that we identified in the ticket last year. He had a reasonable amount of interest in that proposal from various different parties. Multiple different parties helping to fund, will probably work out to about six to $7000 per code base, 50K to 60K in total cost, various parties offsetting the cost.

The call adjourned at 15:03 UTC