============================================
FAPI WG Meeting Notes (2018-04-25)
============================================
Date & Time: 2018-04-25 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call
===========
* Attending: Nat, Dave, Tom, Justin, Brian, Bjorn, Henrik
   * Guest: 
* Regrets:  

Adoption of the Agenda (Nat)
==================================
* Adopted as is.  

External Organizations
=========================

ISO/TC68/SC9 (Dave)
--------------------
Dave gave an overview of the ISO/TC68/SC9 first face to face. 
They are creating a TS for now. 
OIDF contributions are well received. 

In EU, there are some worries around redirection flow. 

The approach is very high level and not directly implementable. 

Different use cases are addressed and different trust models, which is outside of the FAPI, will be in the draft. 
The snippet that can be shared will be shared with FAPI WG. 

Berlin Group
~~~~~~~~~~~~~~

Swiss group
~~~~~~~~~~~~
Not subject to PSD2. However, they do have the initiative to bring something like Open Banking to the market. 
They are starting with SME and corporate market. 
They worry about the Phishing vectors so they are implementing a directly of all the trusted third parties and start the journey from the bank. They are collecting consent at the bank to start with, then put the fact into the cookie. Then, the user-agent is redirected to the TPP, where TPP will bounce the user back to the Bank with something like prompt=none and follows the usual OAuth authorization code flow. 

1. Editor's note: How does the bank know what to authorize to start with? 

Barclays UK is also doing current flow for the worry of the Phishing vector so it may be a common worry among the financial sectors. Dave is trying to get a spec for it so that FAPI WG can have a look at. 

Nat and Justin pointed out that OIDC had a discussion around OP initiated flow that calls an endpoint at the client the just redirects the user-agent to the authorization endpoint. The security property actually is not that different from the usual flow. More to be followed up. 

STET
~~~~~~~
A French group. They are currently vanilla OAuth 2.0 but they have a change request to Editors to support FAPI. 

There is an increasing pressure to support 3 flows: 

1. Redirect
1. Decoupled
1. Embedded. 

Their Decoupled flow is to utilize Device flow. Dave is trying to get hold of their draft to compare with the CIBA flow. 

They are also supporting Embedded but disallowing using static-password. They require a dynamic credential that is created by Bank's device, e.g., Chip-and-pin card. 

Open Banking (Dave)
-------------------------

Next Steps for the Drafts (Nat/Dave)
---------------------------------------

Events
==========
EIW (Nat)
--------------


Pull Requests
================
* https://bitbucket.org/openid/fapi/pull-requests/



Issues
===========
* https://bitbucket.org/openid/fapi/issues?status=new&status=open

AOB
===========
* Name change proposed at the last board meeting. Members are reminded of their task of coming up with a name. 
  Nat suggested a retrofit acronym: Full Assurance Protection Interoperable 


Next Call
-----------------------
The next call is scheduled to be in the Pacific time zone. 

* The meeting was adjourned at 15:01 UTC.