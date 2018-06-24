============================================
FAPI WG Meeting Notes (2018-06-20)
============================================
Date & Time: 2018-06-20 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call
===========
* Attending: Nat, Bjorn, Brian, Sarah, Dave, Ralph, JOseph, Rob Otto, John
   * Guest: 
* Regrets: 

Rob is new to this call and he made an introduction that he is representing Ping and is in charge of EMEA. 

Adoption of the Agenda (Nat)
==================================
* Adopted as is. 

CIBA Spec Discussion (Dave/Brian/Sarah)
=========================================
* CIBA Spec: http://openid.net/specs/openid-connect-modrna-client-initiated-backchannel-authentication-1_0.html
* FAPI CIBA Profile: https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_CIBA.md
* Brian's comment: http://lists.openid.net/pipermail/openid-specs-fapi/2018-June/000924.html
* Sarah's Proposal: #147 - Anonymous Point of Sale Backchannel Authentication
* #146 - Fraud Indicator Standards and Signed Communication Mechanism of them. (Ralph)
* #148: IANA Considerations : Disovery, Grant Types, dynamic reg (Ralph)

Most of the call was spent on this topic. 

After Dave has set the context around it by explaining the genesis of CIBA profile that FAPI WG has been working on and introduced the outcome of the Pacific call of the previous week where Sarah's proposal was taken up as a potential basis for a new work, Ralph was asked to provide the European context to it. 

Ralph explained that there is a requirement from PSD RTS that PSUs to surrender all their credentials to TPPs, based on the TPPs' use cases, despite the industry's effort to persuade that is a bad idea from the security point of view. Given the situation, we need to find a better way of doing it. If we do not come up with a way, OB has to define it by itself, but it is much more preferable to standardize it in a standardization body. 

Then Sara explained that the main objection to the current CIBA flow is the correlation and that's why she has proposed her flow. Ralph responded that CIBA can still be used without leaking the information. The steps are

1. The user creates the ephemeral identifier QR code on his banking app. 
2. POS scans the QR code and sends the intent. 
3. The bank sends the push notification to the user's app. Since the user is on the app, it is not a bad user experience. (What goes into the QR code should be standardized.) 

Sarah agreed that it solves the privacy problem. 

Then Dave, as a WG member, suggested that having one spec instead of staring the second will cause less confusion. 

THen Dave, as the co-chair, asked Brian whether there is a problem in going forward with the CIBA spec. 

Brian explained that basic concepts of CIBA spec are good. The problem is that from the implementer's point of view, there are major problems with consistency that it cannot be reliably implemented. Also, it was pointed out that some statements in the CIBA spec is very MNO specific. Bjorn explained that the Modrna WG was waiting for feedback/pull requests on these things so that it can be improved and generalized. John also pointed out that discovery on ephemeral identifier can also be added to CIBA. 

Callers agreed to go with modifying the CIBA spec and CIBA profile instead of creating another spec. 
Sarah expressed their desire to standardize the pairwise hint. 
John suggested defining the hint token in the CIBA spec. (Currently, it is in the Modrna discovery spec and people misses it.) 

Another issue is to whether to do the JWT in a JWT or string in a JWT. 

Working Mode
----------------
To expedite the process, we are going to keep the main CIBA spec in the Modrna and the FAPI profile in the FAPI WG. The people who has access to both group should cross post to both mailing list and issues should be filed against the respective repository. 

People are conrourage to join both group. 




AOB
===========
F2F at Identiverse
-----------------------
Nat Suggestedto have a F2F work at Identiverse to progress the work quickly. 
People agreed. The timing will be announced separately. 


Next Call
-----------------------
Next week's call is cancelled due to Identiverse. 

* The meeting was adjourned at 24:03 UTC.