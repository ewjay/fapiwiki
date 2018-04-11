============================================
FAPI WG Meeting Notes (2018-04-11)
============================================
Date & Time: 2018-04-11 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: 
   * Guest: 
* Regrets:  

Adoption of the Agenda (Nat)
==================================
* 

External Organizations
=========================

ISO/TC68/Sc9 (Dave)
--------------------

ISO/TC68/FinTech Tag (Nat)
------------------------------
Benoit, standards within DG Connect gave a brief overview of the FinTech task force's action plan from 7 March. 
DG Connect is Directory General of Communication in EU, including Blockchain and FinTech. 
Digital Single Market. 
DG FISMA (Stability for financial market). 
The report is online now.  

http://eur-lex.europa.eu/resource.html?uri=cellar:6793c578-22e6-11e8-ac73-01aa75ed71a1.0001.02/DOC_1&format=PDF


Box 1 - Startup funding
1. Crowdfunding platforms. 
2. Licensing models
3. Crypto Assets. ICO. Subject to fraud. 

Box 2

EC encourage and will support joint efforts by market players to develop, by mid-2019, standardised aPI 
that ar compliant wiht the PSD and GDPR as a basis for a Euroopean open banking eco-system covering payment and other accounts. 

1.3. Facilitating the emergence of innovative business models across the EU


Open Banking (Joseph)
-------------------------
* Yolt announcement: https://www.yolt.com/blog/2018-03-15/open-banking-update-weve-officially-connected-to-three-banks
* Conformance suite is now open source. 

OpenAPI (Nat)
----------------
* There was a call with the OpenAPI Foundation last Friday. It is heading in a good direction, e.g., supporting signed JWT response, etc. Nat will send a link to it in the mail list. If you are interested, please get involved. 

Events
==========
IIW (John)
--------------
* John is going to present FAPI in the pre-IIW OpenID Workshop. 
* Please send the presentation ideas to the list to help John. 

Pull Requests
================
* https://bitbucket.org/openid/fapi/pull-requests/


Issues
===========
* https://bitbucket.org/openid/fapi/issues?status=new&status=open
* Talked about #135 at some length. It looks like a core problem is how to express the needs for "meaningful consent" at the authorization server. Unlike in the regular OAuth's case, FAPI Part 2 allows the client to be authenticated via a digital signature, so the authorization server can actually show who is requesting what to the end user. However, the actual user interface for showing that information is out of scope for OpenID Connect Core. We might want to come up with a text that expresses the need for the "meaningful consent." 



AOB
===========
* There seem to be some demands for FAL3 authentication in the US now, as a part of Fedramp program. 
* EAP WG has a draft that deals with it and it may go to the implementer's draft vote in the near future. If you are interested, please join the WG and submit your comments. 


Next Call
-----------------------
The next call is scheduled to be in the Pacific time zone. 

* The meeting was adjourned at 15:01 UTC.