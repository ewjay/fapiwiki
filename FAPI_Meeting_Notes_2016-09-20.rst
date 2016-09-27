============================================
FAPI WG Meeting Notes (2016-09-20)
============================================
Date & Time: 2016-09-20 23:00 UTC
      (16:00 PDT, 00:00+1d UK, 01:00+1d Denmark, 08:00+1d JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: Nat, John, Dave, Edmund, Henrik, Anoop, Ryan
* Regrets: Sascha
* Guest: Eric Plaad. 

Adoption of the Agenda
=========================
* OIX added. 

External Org Relationships 
=============================

UK Implementation Entity (Dave)
-------------------------------
* Fdata <http://fdata.org.uk/>is the main voice of fintech community while IE is top 9 banks. 
* They are making subgroups on standard, data, infrastructure. 
* Dave was in their meeting yesterday and presented verbally in addition to the liaison letter 
  that FAPI WG is working internationally to create an international standard, and about its expertise. 
* Hopefully, IE can make the liaison relationship more official in their advisory board or/and different 
  working group. 
* Continue to update the group. 
* Split of the current draft into security and data scheme would be useful as different WGs will be 
  looking at separate aspects. 
* John was talking to the UK Cabinet office and eIDAS making aware of FAPI given their involvement in iGov. 
    * Given the acceptance of OpenID Connect in the commercial sector, they will shift to it from SAML 
      in the long run. 
    * They understand that IE liaising with us and try to get on the same page on OAuth and Connect 
      will be beneficial. 
    * Hopefully, this will influence IE as well. 

EBA Consultation (Dave)
----------------------------
* Dave has started the draft at https://docs.google.com/document/d/1V3q1avS1zO2n2YaB-Y2Z1Vf6j-DrE7OwiISRuRpvs24/edit
* From FAPI point of view, it would be wise to limit some of the answers and concentrate on the topics that we can add the most value. 
    * Q.7 and Q.8 Common and secure open standards communication
* Work in progress draft, will fresh out and send it out to the list. 
* We still have two to three weeks before we send it out. 
* NOTE: UK IE is set up as a response to  different legislation (CMA), but the view of the room is that 
  whatever the standard they create will be in-line with the guidance from EBA. 
* EBA consultation put some arbitrary limits such as they want "strong customer authentication once a month". 
    * From FAPI point of view, we probably do not want such an arbitrary limit on the refresh token. 
    * Note: mix up authentication and authorization quite a bit. 
* It is also related to eIDAS. 
* Collaborative editing welcome. 
* Once it is in a good shape, Dave will send it around for the final comments. 

Action:: 

    WG members are invited for collaborative editing. 
    Dave to send out the final draft to the WG for review when it is ready. 


Federal Reserve of Minnesota (John)
---------------------------------------
* No updates on Minnesota. 
* Neither John nor Paul has heard about it. 
* Will try to follow up after this week's conference is over. 
    
OFX (Anoop, Nat)
--------------------
* We had an enquiry about the membership (of WG or OIDF) from them to the chair's list and will have the first call in half an hour. 
    * Expect that it will be the introductions of each other. Real discussion probably will sart next week. 
* Intuit is participating in OFX as well. Intuit and Microsoft are some of the founding members. 
* OFX went quiet for sometime but re-invigorated lately. 
* About 6 to 8 months back, DDA OAuth based implementation came out. 
* Some of the banks felt that they already have big OFX infrastructure and replacing it new with REST based service is a big investment -> can we update the OFX specs to include a token based aggregation of data. 
    * First bank to pick it up was the Chase Bank (about 6 to 8 months ago). 
    * Implemented OAuth and OFX. 
* They defined spec in such a way that token can be any token (OpenID Connect, OAuth, JWT, etc.) 
* It is not REST based nor JSON based. It is SOAPy, that it has special header in XML. Does not comply with any REST based principles. 
* Specification can be downloaded from http://ofx.net/downloads.html
* Many of the banks that Anoop talked to except Chase Bank wanted to remove the complexity from the implementation of that kind of APIs and one of the reason for DDA got traction in FS-ISAC was the complexity of OFX. 
* Nat pointed out that in other industries, the XML/SOAP paradigm became so out of fashion that Nat and John had to start creating signature format standard for JSON from scratch instead of relying on XML DSig. 
* Anoop pointed out that more and broader participation would be good especially if they can contribute and adopt the standard. 
 

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Review Results (John)
--------------------------------
* The text in clause 6 is good but we should leave TLS option as well. 
* Problem is that there is no good reference document to point to. 
* John talked to Brian that perhaps he can start drafting an IETF document. 
   * It will be a small document. 
* Nat pointed out that IETF process will take a long time while we want to publish at least the security section of FAPI specs early as we have challenging timeline that we may want to include the text in the initial spec. Once IETF process is done, we can take the text out and reference it. 
* John pointed out that perhaps we can create a separate OpenID Connect Mutual TLS Authentication Method document so that from the FAPI point of view, it will just be the change of the reference. 
* Brian already has written it down so John needs to dig it up. It should be relatively quick. 
* Once we have the draft, we can insert it in the requirements. 
* It is related to #16. 
* John suggested that for client authentication, the option would be: 
    * Mutual TLS + JWT; or 
    * JWT + Token Binding
* Nat pointed out that it might be better to consider it in the Read-Write access timeline as we have less time pressure as Token Binding is still young. For read only access, it probably would suffice to do Mutual TLS+Basic or JWT client authn only. 


Issues 
=========================

#16 Client Authentication (John)
----------------------------------------
* issue #16
* Mutual Auth TLS profile not defined anywhere for token endpoint. We probably need to do ourselves. 
* Client auth JWT (secret, private key) can also be used, so it is either of them. 
   * Nat has suggested a text for this bit on #16. 
* We probably should not allow Basic auth only. 
* John volunteered to craft text. 

Action:: 

    John to come up with the additional text to be applied and do a pull request. 

#29 Draft Split (Nat)
--------------------
* issue #29
* Per the result of the Atlantic call last week, the split of the draft is suggested as recorded in #29. 
* The call participants agreed that 5 parts structure as below would be good. 
  * part 1: Read Only API Security
  * part 2: Open Data API
  * part 3: Protected Resource Data API
  * part 4: Read Write API Security
  * part 5: Read Write Data API
* Incorporate branch issue/26 into the current master branch, and then do the split. 
* During the time, we can continue reviewing the current WD esp. on the Read only security 
  so that we can go quickly to the implementer's draft vote on the part 1. 

#28 International names for retirement savings account names (Dave/Nat)
-----------------------------------------------------------------------------
* issue #28
* Dave pointed out that this is a tricky area where we have to cover vast array of products. 
   * e.g., while trying to come up with a strawman Dave started wondering whether it would make sense to have 
     interest in a single field as they now seem to depends on the account balance. 
* Nat pointed out that it is easier with the concrete account data as it can talk about the "currently applicable interest rate" but when it comes to "open data", it would be difficult. 
* NRI's team is also looking through the investment account data and they started feeling that some refactoring is needed. 
* Nat wanted to have a separate call for DDA-Customer-ID with Anoop. 

#30 Hanging Paragraph in 5.2 (Nat)
-----------------------------------
* issue #30 : Editorial
* disposition suggested in the ticket. 

#31 5.2 - te - More fine grained scope needed (Nat)
----------------------------------------------------
* issue #31 : technical
* Currently we have only one scope `FinancialInformation`. 
* Nat suggested that perhaps we need more fine grained ones? 
* Dave pointed out that he has use cases for just asking for account balance and separately the transactions details. They are two clear different scopes. 
* Nat pointed out that from the collection minimization point of view, it would also be good to have sub-scopes. 
* It is not suggesting to ditch the current scope, but is just suggesting that we need to have more granular ways to specify the access target. 

Events
=============
Pre-IIW (John)
----------------
* Location fixed (VM Ware). We will have time allocated. Likely to be 20 min. 
* Sascha is in the process of preparing a presentation. It should be ready for review next week. 
* John will see Don tomorrow to ask for the est. of time and agenda. 

Action::

    * Develop a presentation for the occasion (Lead by Sascha) in two weeks. 

Pre-IETF (Nat)
-----------------
* Not yet. 

Action::

    * Nat will get in touch with them and get back to the list. 


AOB
========

How to communicate back the partial errors to the client (Anoop) 
-------------------------------------------------------------------
While implementing DDA, Anoop et al. came across a new use case. 
Sometimes, when banks are returning data, some of the sub-system 
may not be available temporarily and results in partial results. 
For example, the Bank's credit card system may be on maintenance mode 
and the bank may not be able to return data on credit card 
while it can return everything else. It is just a temporary error. 
We have not defined anything on this. 
Bank needs to communicate it back to the client. e.g., 
yesterday I returned 5 accounts but today I am returning only 3. 
Hoever do note delete the 2 as it is only temporarily unavailable. 
When we come back, I might be able to return them. 

Anoop can come up with suggested text. 

Action:: 

    Nat to create a ticket and assign it to Anoop.  


Next Call
----------
* 2016-09-28 14:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 23:00 JST)

The meeting adjourned at 23:55 UTC.