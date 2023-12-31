============================================
FAPI WG Meeting Notes (2017-10-03)
============================================
Date & Time: 2017-10-03 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:05 UTC. 

Roll Call
===========
* Attending: Bjorn, John, Nat, Edmund, Sascha, Tom, Pam, Carla
   * Guest: 

* Regrets: Anoop

Adoption of the Agenda (Nat)
==================================
* Added: CA report, FIDO report, 

External Orgs
================
Berling Group Consultation (Nat)
----------------------------------
Berlin group consultation is out. There are some concerning wrting around OAuth and we may want to respond as OIDF-FAPI WG. The conslutations are found at the following links. 

1. https://www.berlin-group.org/market-consultations
2. https://docs.wixstatic.com/ugd/c2914b_6a15d20b155a4d62922c67fe5a6e3dd5.pdf?index=true

Pam showed the section 4.3 and explained that while it does have code grant, it is markedly silent on the specifics. It also allows 'user password grant', which is concerning. Some comments were made that perhaps the existing APIs actually embed username and password in the request as some of the legacy APIs do. (Note: All the German banks have been mandated to have APIs for a long time.) 

FIDO (John)
--------------
Plenary in Sydney
CTAP going under legal review for publication so that W3C can see CTAP. 
Expected to become public next month. 

Making good progress on the W3C. 

Google is pushing for U2F to thwart session hijacking. 

Some confusion on PSD2 requirements re: PIN sleeve. 

Open Banking (Dave, Pam)
-------------------------
* request from OB to have more examples. 


Draft status and plans 
===========================

Streamlining the OBUK Implementer's Draft (Pam)
----------------------------------------------------

Verification: non-compliant JWT audience (Pam)
------------------------------------------------
The callers agreed to that taking `aud` out of the software statement is the best strategy. 

Tom also asked how we differentiate a software statement from another type of JWT. 
While it is sent to the specific endpoint in transit, it may be stored in the database and gets mixed up at a later stage so it is always good to have explicit typing. Callers agreed that explicit typing is a way to go. 

Pam is going to create an issue on the OB side. 


Pending pull requests (Edmund)
---------------------------------
All the pending pull requests have been accepted and merged. 

Events
================
Open Banking F2F (Nat)
--------------------------
* Nat relayed the info from the last week's Atlantic call that one is planned on Oct. 17 in London. 

FAPI/Modrna joint F2F
-----------------------
* Date fixed on Nov. 7. Given Berling Group and API Days, Do we want it to be in Berlin instead? 
* That seems to be certainly possible but if it is going to be joint WG with Modrna, some logistical shuffling may be needed. 
* Carla will find out about the Microsoft event that is happening before the Berling group meeting. 

AOB
===========

Next Call (Atlantic)
-----------------------
* The meeting was adjourned at 23:52 UTC.