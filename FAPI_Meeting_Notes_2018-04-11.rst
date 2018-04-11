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
* Attending: Nat, Brian, Dave, Joseph, Justin, Ralph, Bjorn
   * Guest: 
* Regrets:  

Adoption of the Agenda (Nat)
==================================
* Adopted as presented. 

External Organizations
=========================

ISO/TC68/SC9 (Dave)
--------------------
Part 1 and 2 has been submitted. 
Dave is going to be in Zurich next week. 
He will also push for the remote participation. 

ISO/TC68/FinTech Tag (Nat)
------------------------------
Benoit, standards within DG Connect gave a brief overview of the FinTech task force's action plan from 7 March. 
DG Connect is Directory General of Communication in EU, including Blockchain and FinTech. 
Digital Single Market. 
DG FISMA (Stability for financial market). 
The report is online now.  

http://eur-lex.europa.eu/resource.html?uri=cellar:6793c578-22e6-11e8-ac73-01aa75ed71a1.0001.02/DOC_1&format=PDF

Nat suggested to look at Box 2 in P.8 that states: 

EC encourage and will support joint efforts by market players to develop, by mid-2019, standardized API 
that are compliant with the PSD and GDPR as a basis for a European open banking eco-system covering payment and other accounts. 

and pointed out that communicating with them through TC 68 might be an important strategy for us. 




Open Banking (Dave)
-------------------------
* https://openbanking.atlassian.net/wiki/spaces/DZ/pages/126321042/Open+Banking+Security+Profile+Conformance
* 15 TPPs approved. 30 to 40 in the pipeline. https://www.openbanking.org.uk/regulated-providers/

Events
==========
IIW (John)
--------------
* John presented FAPI in the pre-IIW OpenID Workshop. 
* Not much discussion about open banking in IIW. A lot of discussion was about DID and blockchain. 
* This time around, IIW was more focused on the education side and not too new thing came up. 
* Kazue's session on ZKP was very useful to understand the math around it. (Justin)
* It was a revelation for Justin that Git actually is a Hash graph and blockchain! 

Pull Requests
================
* https://bitbucket.org/openid/fapi/pull-requests/

Pull request #53
----------------------
Nat briefly explained that it is about the AS to show who is the client and what is being asked, just like in the case of the Open Banking. 

John pointed out that it is not only about that but also having the client to use EV certs so that company name etc. will be shown on the PSU's browser address bar. 

People are encouraged to review the draft and vote. 

Issues
===========
* https://bitbucket.org/openid/fapi/issues?status=new&status=open

#138
------------------------
The callers discussed #138. 
John argued that requiring 'openid' scope even in Part 1 will simplify the lives of many people. 
(It is required in Part 2 where ID Token is needed.) 
As we run out of the time, Nat put the topic on the table till next week. 

AOB
===========
* Name change proposed at the last board meeting. Members are reminded of their task of coming up with a name. 
  Nat suggested a retrofit acronym: Full Assurance Protection Interoperable 


Next Call
-----------------------
The next call is scheduled to be in the Pacific time zone. 

* The meeting was adjourned at 15:01 UTC.