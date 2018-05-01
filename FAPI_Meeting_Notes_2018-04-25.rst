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

Swiss group (Dave)
~~~~~~~~~~~~~~~~~~~~~~
Not subject to PSD2. However, they do have the initiative to bring something like Open Banking to the market. 
They are starting with SME and corporate market. 
They worry about the Phishing vectors so they are implementing a directly of all the trusted third parties and start the journey from the bank. They are collecting consent at the bank to start with, then put the fact into the cookie. Then, the user-agent is redirected to the TPP, where TPP will bounce the user back to the Bank with something like prompt=none and follows the usual OAuth authorization code flow. 

1. Editor's note: How does the bank know what to authorize to start with? 

Barclays UK is also doing current flow for the worry of the Phishing vector so it may be a common worry among the financial sectors. Dave is trying to get a spec for it so that FAPI WG can have a look at. 

Nat and Justin pointed out that OIDC had a discussion around OP initiated flow that calls an endpoint at the client the just redirects the user-agent to the authorization endpoint. The security property actually is not that different from the usual flow. More to be followed up. 

STET (Dave)
~~~~~~~~~~~~~~~
A French group. They are currently vanilla OAuth 2.0 but they have a change request to Editors to support FAPI. 

There is an increasing pressure to support 3 flows: 

1. Redirect
1. Decoupled
1. Embedded. 

Their Decoupled flow is to utilize Device flow. Dave is trying to get hold of their draft to compare with the CIBA flow. 

They are also supporting Embedded but disallowing using static-password. They require a dynamic credential that is created by Bank's device, e.g., Chip-and-pin card. Nat pointed out that access token is a client-specific password had he had an implementation of an IMAP server that supports this kind of credential so that the access token can be used as a password on a stock email client, e.g., Thunderbird. It may be worth documenting it. 

Berlin Group (Dave)
~~~~~~~~~~~~~~~~~~~~~~~~
Finally, they are changing camel case to proper OAuth + PKCE. 

They are using eIDAS certificates and have a need for signing the headers and payload. 

Both Berling group and STET are looking at draft-cavage for this reason. 
They think that it is a standard since it is on IETF web site and is sponsored by Oracle. 

Nat pointed out that while it is written by an Oracle person, Oracle has no intention to standardize it. 

Nat asked Justin to give his view on the HTTP Signing. 

HTTP Signing (Justin)
~~~~~~~~~~~~~~~~~~~~~~~~~~
The problem with the traditional approach such as OAuth 1.0a and draft-cavage is that it assumes the pristine HTTP headers, which is not true in the reality. Middlewares, proxies, etc. would mess around with the header, breaking the implementations. 

A more modern approach used by some of the HTTP2 folks are to utilize additive hash. It adds complexity but is safer. 

The advantage of JWS approach is that middlewares etc. can not mess with it so that it is robust, and the disadvantage of the JWS approach is that it cannot be messed around so that it is inflexible and does not follow the modern HATEOAS principle. 

The approach taken by Justin's draft is to take JWS as a crypto container but have hashes for selected headers. 

Nat pointed out that it probably makes sense to explore these approaches in this working group. 

Dave pointed out that draft-cavage are selecting headers to be signed. Justing stated that is a relatively recent addition. The HTTP folk's approach is concentrated on the response. Combining these may actually work. 

Brian pointed out that Justin's draft is more towards the proof of possession while what is needed from the Financial sector is the non-repudiation so while the mechanism may be similar, they are addressing quite different problems. 

Justin stated that audit-ability, such that there is some way to find out who was making the call 6 months from now somehow, is important also in the Healthcare space. Nat pointed out that Estonia police is actually using JWS to store the messages for this purpose. Brian pointed out that for something like this, history of keys needs to be stored as well, i.e., key distribution and trust mechanism are going to be different than what is discussed in OAuth WG. 

Open Banking (Dave)
-------------------------
They need decoupled mode. 
We need to look at either CIBA or Device flow to help them out. 


Next Steps for the Drafts (Nat/Dave)
===========================================
* Do we want to continue with CIBA or switch to STET approach? Or embeded iFrame approach that John brought up. 
* Do we want to document application specific password flow etc? 
* HTTP signatures? 
* Document on strong customer authentication, e.g., Web Authentication. 

Tom pointed out that we should not rely on phone numbers as it is hackable. 

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