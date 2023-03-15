============================================
FAPI WG Agenda & Meeting Notes (2023-03-15) 
============================================
* Date & Time: 2023-03-15T14:00Z
* Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2023-03-15_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:02 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: Nat, Gail, Joseph, Mike, Tim, Aaron, Brian, Daniel, Dave, Filip, Geroge, Justin, Marcus, Kosuke, Pedram, Kelley, Pieter, Dima
* Regrets: Chris
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* Adopted as presented as draft agenda. 

Mini-kick off of FAPI2 Workpackage 2 project (Gail/Marcus)
=============================================================
* Scope is FAPI CIBA, Dynamic Client Registration (including Australian variant) and FAPI 2.0 Message Signing (including JARM, JAR. jIR, HttpSiG)
* Meeting at 8 AM CET. 


Events (Mike L)
====================================================
* Workshop on 1 PM Apr. 17. Details to be published this week. 

Internal Liaisons
======================
n/a

External Orgs & Liaisons (Mike L.)
============================================
Brazil
----------
* No material updates. 
* Certification request continues to come in. 

Saudi
-----------
* KSA FAPI Profile Framework is not publicly available yet. Quality control is being performed. 
* Publishing FAPI-specific component at openid.net. It will be confirmed shortly. 


Draft Updates
====================

FAPI 2 Msg Signing (Dave)
----------------------------
* Package was sent to the foundation secretary. 
* Question was raised whether the title should have "Draft" or "Implementer's draft"

  * It should be "Draft" because it has not been voted on. 

All other drafts: Put "draft" in the title (Nat)
----------------------------------------------------
* Editors, please make sure that your draft has "draft" or "Implementers draft #" in the title. 
* Also, please make sure to put warning text. 

PRs (Dave)
===============
* Apart from one PR that we are parking until HTTP signature is settled, there is no standing PR. 


Issues (Dave)
==================
FAPI2SP: Note about client assertion audience looks misleading
------------------------------------------------------------------------------
* #579
* https://bitbucket.org/openid/fapi/issues/579/fapi2sp-note-about-client-assertion
* Normative sentences should not go into Note. 
* We wanted to leave options open for CIBA and Token Endpoint. 

FAPI2SP appears to permit response_types "id_token", "id_token token" and "none"
------------------------------------------------------------------------------
* #577
* https://bitbucket.org/openid/fapi/issues/577/fapi2sp-appears-to-permit-response_types
* Brian's wording was discussed. 
* It was pointed out that while it is rejecting the response types quoted, it does not others. 
* Adding parameters (esp. tokens) would create a new authentication protocol and nullify the security analysis. 
* In view of this, it was suggested to lock it down to response_type=code while making it conditional that future extensions, such as CIBA, can be made. (They need a fresh security analysis and we are doing that in FAPI2 Workpackate 2 sponsored by the AU government.) 
* Filip came up with wording that sounded reasonable. He will put it in this ticket. 

AOB (Nat)
=============
* none

The call adjourned at 14:59