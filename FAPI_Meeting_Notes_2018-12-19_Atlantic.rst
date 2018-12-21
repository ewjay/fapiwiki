============================================
FAPI WG Meeting Notes (2018-12-19) 
============================================
Date & Time: 2018-12-19 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call
===========
* Attending:　
    * Dave, Brian, Daniel Fett, Luke Popplewell, Nat, Torsten, Ralph, Freddi, Chris Wood

* Guests: 
* Regrets: 

Adoption of the Agenda (Dave)
==================================
* Agenda was posted in the chat and agreed

CIBA Progress Report (Brian/Dave)
============================================
* Implementers draft review period has started for the OpenID CIBA Core profile
* Work on the FAPI profile has started 
* OB Reference banks will implement CIBA core

External Organizations
==========================

EBA API WG (Dave)
-------------------
* We agreed on the call to nominate Ralph to represent FAPI at the new EBA WG
* Dave to email the list to give anyone else a chance to volunteer
* Ralph to draft application letter


STET, Berlin Group & Session Fixation in Payment Flows (Torsten)
-----------------------------------------------------------------
* Torsten and Daniel have a document explaining an attack on some PSD2 API specs where payment occurs as part of the auth flow
* Looking for a name for this, currently called: “Session Fixation in Payments Flows”
* Ralph brought up the functional issue, that a payment may be executed and the merchant may not know about it if there is some communication problem on the redirect back
* Nat talked about public / private disclosure of the vulnerability
* Nat proposes that the doc is sent to EBA, Commission, FISMA
* Freddie proposes a generic question to the EBA Q&A - i.e. what should API security benefits 
* We agreed that the document be made a FAPI WG doc, Nat to work with Torsten and the OpenID liaison committee
* Discussion over the crossover / differences between the OAuth Security BCP and FAPI, discussion to continue on the issue tracker.
* Once doc is ready, Nat, Dave, Ralph, Freddie and Torsten to distribute through a variety of private channels


Australia (Luke)
-----------------------------
* They are working on a security profile for Consumer Data Standards
* Based on FAPI RW and CIBA
* Very tight deadlines
* Luke with share the github repo

Next Call
-----------------------

* The next pacific call is cancelled. The next atlantic call will go ahead on 02-Jan-2019.