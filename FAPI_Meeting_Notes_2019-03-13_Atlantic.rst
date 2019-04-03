============================================
FAPI WG Meeting Notes (2019-03-13) 
============================================
Date & Time: 2019-03-13 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending:　
  * Bjorn, Nat, Brian, Dave, Joseph, Torsten, Freddie

* Guests: 
* Regrets:      

Adoption of the Agenda (Dave)
==================================
* Agenda was agreed

External Organizations
==========================

3.1. ECB (Chris/Ralph/Dave)
-----------------------------

First meeting has been held. Chris to send on details.

3.2. STET, Berlin Group & Session Fixation in Payment Flows (Torsten)
-------------------------------------------------------------------

Liaison letter
STET editor indicated that they will change their spec 
Dave to provide links to other specifications to Torsten (e.g. Polish & Czech)

Chairs to send to BG
Torsten to send to other docs

3.3. Australia (Ralph)
-----------------------------

Working on the legislative side of things.

3.4. UK OpenBanking (Joseph, Dave)
----------------------------------

3.1.1 released includes dynamic client registration.
4.0 close to being released
Migration to eidas. QWACs are being used for mutual TLS.
Custom JOSE header to specify the trust anchor
 
Freddie to send the extract on message signing to list

3.5. ISO/TC68 (Dave)
---------------------
Dave to have an update on the next call

3.6. IETF:OAuth JAR (John)
-----------------------------

John is working on it. 


Draft Status
==========================

TR Cross-Browser Payment Initiation Attack (Daniel/Torsten)
-----------------------------------------------------------------

Torsten is proposing to change the document to make it clearer that we recommend using OAuth to solve the problem as it solves many other problems. 

We agreed to change it round. 


TR Lodging Intent Pattern (Torsten)
--------------------------------------

Torsten explained that the document is more of a BCP than a standards track document. And it should be updated from time to time if there are changes. 

We talked about request object endpoint. 

We can expand the lodging intent document to have both 

OSW work on it.

Brian raised the issue that it is mixing concerns


Issues
==========================

6.1. #216: TLS_ECDHE_ECDSA cipher suites
6.2. #215: Financial_API_Lodging_Intent should be an informational document
6.3. #214: restricting 'aud' in request object to a single value (Joseph)

AOB
==========================
* OpenID Foundation - certification programme changes
* Certification for FAPI goes live in April 1st (OP first)


Next Call
==========================

* Pacific call next week. Atlantic call in 2 weeks time.