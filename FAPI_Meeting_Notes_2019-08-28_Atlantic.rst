============================================
FAPI WG Meeting Notes (2019-08-28) 
============================================
Date & Time: 2019-08-28 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
Attending:
--------------------
#. Dave, Nat, Brian, Dima, Don, Joseph, Stuart, Torsten, Kosuke, Bjorn

Regrets: 
---------------------    

Adoption of the Agenda (Dave)
==================================
* Pull request 137 (Torsten)
* Outreach (Don) 

Outreach Activities (Don)
===============================
Two white papers are being prepared
Dummies guide for FAPI and Self-certification. 
The draft should be ready in one or two weeks. 

Joint white-paper with Financial Data Exchange (FDX)
It will be discussed in FDX developer conference on Sept. 11 and 12. 
FDX has invited OIDF members to join FDX. 
Folks who want to join FDX should email Don. 

Micro site "all things fapi" has been created. 
Next week, OIDF EC will be reviewing it. 

FAPI will be the key topic for OpenID Foundation Workshop in Mountain View on  
Sept. 30. at Verizon HQ. New members like Akamai and Ebay will be attending it. 
Workshop agenda is available on Eventbrite. 

Pull request 137 (Torsten)
==============================
There were some discussion around whether alg=none should be used or separate parameter such as request_raw to send unsigned request. The reason for not using alg=none is to avoid propagating the public perception about the insecurity of JWT. 

Also, there was some discussion around whether it should be raw=form encoded or base64url encoded if a separate parameters were to be used. 

It seemed everybody was on the fence and as we could not reach a definitive conclusion on it, it was decided that just to accept the pull request as is and come back to the issue later with more implementation experiences. 


External Organizations
=======================

Australia (Dima/Stuart)
-------------------------
* Response letter was received on August 27 and forwarded to LC on Aug 28. 
* Some of their reading of security analysis seems to be misguided. 
* The letter also is almost exclusively talking about the security analysis and not about interoperability and the compatibility with existing infrastructure. 
* There was some concern expressed on the WTO Technical Barrier to Trade issues on creating and mandating a national standard that is incompatible with international standards. 
* Nat asked Don to involve certification team to do more in-depth analysis and drafting of the response. The certification team will have a call this Friday and Joseph will brief them of it. 
* The topic will be discussed again in the next Pacific call. 

Open Banking (Dave)
----------------------
* 6 month extension to enforcement of RTS granted in the UK
* It seems to be replicated all over the EU. 

AOB
==========================
* none

The meeting was adjourned at 15:04 UTC.