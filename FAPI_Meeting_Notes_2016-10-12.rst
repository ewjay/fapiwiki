============================================
FAPI WG Meeting Notes (2016-10-12)
============================================
Date & Time: 2016-10-12 14:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 23:00 JST)
Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
=============
* Present: Dave, Nat, Sascha, Henrik, Anton, John
* Regrets: Anoop

Adoption of the Agenda (Nat)
===============================
* Pre-IIW switched from John to Sascha for IIW presentation review. 
* API Days added. 

Pacific Call Report (Nat)
===============================
* Nat briefly explained the outcome of the last week's Pacific call 
  which is recorded at [[FAPI_Meeting_Notes_2016-10-04]]

External Org Relationships 
=============================

EBA Consultation (Dave)
----------------------------
* Draft response at https://docs.google.com/document/d/1V3q1avS1zO2n2YaB-Y2Z1Vf6j-DrE7OwiISRuRpvs24/edit
* 

UK Implementation Entity (Dave)
-------------------------------
* They have appointed trustee but not yet announced. 

Others
----------------
* OFX: 
* FIGO: http://docs.figo.io/ (Anton) 
* Apigee: https://openbank.apigee.com/home


Action::

    * Anton to get in touch with FIGO. 
    * Dave will get in touch with Apigee, who is in the API Days conference today. 
    * Nat and John will try to get in touch with Apigee as well. 

Working Draft 01
===================

* `WD1 Financial Services – Financial API - Part 1: Read Only APIs <https://bitbucket.org/openid/fapi/src/ec8fde27efc98db7e9cd3e2a7c9d3afcd5aba01c/Financial_API_WD_001.md?at=master&fileviewer=file-view-default>`_   

Client Certs Authentication Draft (John)
--------------------------------------------
* issue #16: Client Authentication -- Do we need TLS mutual authentication?
* https://datatracker.ietf.org/doc/draft-campbell-oauth-tls-client-auth/
* Registering the discovery endpoint probably is a good reason for it to get it done. 
* Please comment. 

Action::

    * WG members please comment. 

2nd WD Roadmap (Nat)
------------------------------
* issue #29: Splitting WD1 further
* Nat explained that now we have all the changes needed for the 2nd WD, we are going to make one. 
  It should be ready in couple of weeks. 

Issues 
=========================

#33: John's Security Section Review Result (Nat)
------------------------------------------------------
* issue #33

#32: How to communicate back the partial errors to the client (Nat)
----------------------------------------------------------------------------
* issue #32
* Sascha explained his rationale for not returning errors but just explanation. 
* We need the lists of AccountStatus Codes. 

#31 5.2 - te - More fine grained scope needed (Nat)
----------------------------------------------------
* issue #31 
* Scopes to be moved to the API sections. 

#12: redirect URI for Clients with session comparison (Sascha)
-------------------------------------------------------------------------
* issue #12
* Closing the ticket. 

Events
=============
Pre-IIW (Sascha)
----------------
* Location fixed (VM Ware). We will have time allocated. Likely to be 20 min. 
* Sascha reviewed IIW presentation. It is the current slide deck + progress, e.g., outreach, and draft status.  
* Nat pointed out that it would be good idea to add a slide on the 2nd WD draft parts structure as well. 

Pre-IETF (Nat)
-----------------
* Looks like only John and Nat will be there so it will not be a WG meeting but just the introduction of the work to Korean audience. 
* John will ask for the room. 
* Good idea to run by Mike to ask to other WGs. Maybe FastFed wants to do the same. 

Action::

    * John: request a room. 
    * Nat: ask LC if they want to present if the room is granted. 

API Days (Dave)
-------------------
* API Days: Main one in Paris in December 13, 14: http://www.apidays.io/
* The organizer will be at IIW. 
* There currently is a FUD that "OAuth is no good for financial APIs", so 
  we need to find somebody to be there to present. 

Action::

    * Dave to make introduction to the organizer of API Days, who is going to be in IIW, with Sascha and John. 
    * Identify the presenter. 
    * Develop a presentation. 

AOB
========

Next Call
----------
* 2016-10-18 23:00 UTC
    (16:00 PDT, 00:00+1 UK, 01:00+1 Denmark, 08:00+1 JST)

* No call for the week of Oct. 24 as it collides with IIW and ISO. 

The meeting adjourned at 14:50 UTC.