============================================
FAPI WG Meeting Notes (2019-01-30) 
============================================
Date & Time: 2019-02-13 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: Nat, Bjorn, Brian, Daniel, Joseph, Ralph
  * 
* Guests: 
* Regrets:      
  * Dave, Torsten, John. 

Adoption of the Agenda (Nat)
==================================
* Accepted as is. 

External Organizations
==========================

ECB (Chris/Ralph/Dave)
------------------------
* Apparently, only Chris got into the ECB steering group. 
* Since it was sponsored by EBA, the final composition was not that surprising. 
* Technical community is way under-represented. The tendency may be resulting in un-workable "laws". 
* e.g., PSD2 now requiring QSeals only for signatures but that requires a human being to click a button. This is totally unrealistic for API calls. 
* For this matter, technical community should produce a concerted effort to promote better ways. 
* Ralph is going to send some pointers to the relevant documents. 

STET, Berlin Group & Session Fixation in Payment Flows (Torsten)
-----------------------------------------------------------------
* No updates. 

Australia (Ralph)
-----------------------------
* No updates. It is getting a little slowed down due to local factors. 

UK OpenBanking (Joseph, Dave)
-----------------------------
* Switching to PSD2 mode towards Sandbox was today. 
* Production date is 13 March. 

ISO/TC68 (Dave)
-----------------------------
* SR on 19092:2008 biometric authentication going on. 

Draft Status (Nat/Dave)
===========================
CIBA FAPI Profile (Dave)
---------------------------
* Core profile passed implementer's draft vote. 

TR Cross-Browser Payment Initiation Attack (Daniel/Torsten)
-------------------------------------------------------------
* TR-Cross_browser_payment_initiation_attack.md
* No updates. 

TR Lodging Intent Pattern (Torsten)
-------------------------------------------
* Financial_API_Lodging_Intent.md

Issues
==========================

#216: TLS_ECDHE_ECDSA cipher suites
------------------------------------
* https://bitbucket.org/openid/fapi/issues/216/tls_ecdhe_ecdsa-cipher-suites

Need to dig in why BCP195 is recommending only these four cipher suites. 

#215: Financial_API_Lodging_Intent should be an informational document
---------------------------------------------------------------------------
* #215
* Torsten seems to be wanting it to be a standard. Since we are lacking both Torsten and Dave from this call, the discussion was postponed to the next call. 

#214: restricting 'aud' in request object to a single value (Joseph)
--------------------------------------------------------------------------
* #214
* This has come up when writing a test suit. 
* Although Joseph argues that there is no case where multiple `aud` is justifiably useful, there may actually be in the Open Banking so we need to at least check the current configuration and assess the impact of the change. 


AOB
==========================

Next Call
-------------------------
* Pacific call next week. Nat will not be able to join. 
* Atlantic call in 2 weeks time.

The meeting was adjourned at 14:45 UTC.