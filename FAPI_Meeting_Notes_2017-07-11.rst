============================================
FAPI WG Meeting Notes (2017-07-11)
============================================
Date & Time: 2017-07-11 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:10 UTC. 
It became late due to a technical problem that Nat had.  

Roll Call
===========
* Attending: Nat, John, Bjorn, Edmund, Sascha, Tom, Brian
   * Guest: 

* Regrets: Anoop, Brian

Adoption of the Agenda (Nat)
==================================
* Adopted as is. 

External Orgs
================

FS-ISAC (Anoop/Nat)
--------------------
* Nat presented FAPI to the FS-ISAC Aggregation group. 
* There were comments that we are not far off that we should try to come together. 
* Dave explained situation around PSD2 and it was very well received. 

Fintech Association Japan (Nat)
--------------------------------
* Nat got a call from Fintec Association Japan. They are interested in the state of Part 3 onwards, especially Part 5. Nat is going to meet them on August 27. 
* Nat also started discussing with them about a potential joint workshop in Oct - Dec time period, if somebody from Open Banking can also participate. 

ISO/TC68 (Nat)
--------------------
* Now we are established as Class A liaison to TC68. 
* Beside Nat, we could elect another liaison officer. Default one would be Paul Grassi, who is the liaison officer to 
  X9, but if he cannot attend the TC68 meetings (twice a year) personally, then we need to elect somebody else. 
  John said he might be able to fill the role in that case. 

Others
------------
* Berlin Group (Dave)
* UK Open Banking (Dave)
* EBA Regulatory Technical Standards (Dave)
* NETS.eu (Dave)
* Apigee 

Draft status and plans 
===========================
Issues
------------------
We have gone over the issues #108 - #113. They are mostly editorial / clarification of the intent including some obvious bug. These editorial issues can be closed by accepting Brian's PR. 

One of the biggest questions around were `s_hash` (cf #109). 
Brian pointed out that if we are using OpenID Connect's hybrid flow only, then mandating the linking of  `nonce` to the `state` value would achieve the same effect as having `s_hash`, providing appropriate checking is done on the client side. This can be entirely be done on the client side. While it is not difficult to implement `s_hash` on the server side, being only needed to touch the client code has some merit. 

Nat pointed out that while it is true, it goes against our philosophy of pushing as much complexity towards the server. Also, if we change this, it will likely to be a restart of the public review and this is not something we can decide on the call. 

The group agreed to discuss it in the list as well as with Open Banking group on July 12 F2F. 


CIBA/Decoupled profile (Dave)
-------------------------------
* The first draft is now published. WG comments sought. 

PSD2 Trust Framework (Tom)
------------------------------
* See [FAPI_Meeting_Notes_2017-06-27]
* Is there a trust framework document? Just X.509 or together with metadata document? 
    * Friendly name. 
    * Using dynamic client registration and sending software statement as in Modrna and federation. 
    * Everybody has to be a member - they have X.509 and software statement through the portal. 
* Tom will send the document with screen / UI that he has in mind with dynamic registration. 
* OpenID Discovery needs a friendly name for IdP. -- needs to be signed JWT though. 
    * Federation spec has it. 

Implementation Status
-------------------------------
* Ping 
* ForgeRock 
* CA -- two teams working on FAPI and PSD2. Only spoken a few weeks ago. 


Others
----------

Events
================
July 12 F2F @ London
-------------------------
* Time and Location now in the OIDF calendar. 
* Remote participants should use the same bridge as our usual bridge. 

AOB
===========

Next Call (Atlantic)
-----------------------
* See the group calendar. 

The meeting was adjourned at 24:04 UTC.