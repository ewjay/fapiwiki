===========================================
FAPI WG Agenda & Meeting Notes (2022-09-28) 
===========================================
* Date & Time: 2020-09-28T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-07-10_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Nat)
======================
* Attending: 

* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
It was proposed to have a brief updates on events and external organization 
then to deal with the issue arose from the formal security verification.  

Events (Mike L.)
====================================================
"A GUIDE TO SECURING CLOUD ACCESS WITH CAEP" webinar
----------------------------------------------------------
Wednesday, October 5th -- "A GUIDE TO SECURING CLOUD ACCESS WITH CAEP" webinar with the Identity Defined Security Alliance
o   Registration is required: https://twitter.com/openid/status/1569779874310545408

Authenticate
-----------------------
Tuesday, October 18th – Authenticate – Seattle
o   OIDF Strategy and FAPI Panel – 1:45-2:40pm PT – Gail Hodges & Anoop Saxena

FIDO Member Plenary
-----------------------
Wednesday, October 19th – OIDF Sessions at FIDO Member Plenary

* 9:00-9:10 -- Welcome & Opening Remarks
* Presenter: Gail Hodges - OpenID Foundation Executive Director
* 9:10-9:45 -- Shared Signals & Events: A Secure Webhooks Framework
* Presenter:  Atul Tulshibagwale - SGNL
* 9:45-10:20 -- OpenID for Verifiable Credentials (OpenID4VC): Addressing Self-Sovereign Identity, Decentralized Identity, or User-Centric Identity
* Presenter: Kristina Yasuda – Microsoft
* 10:20-10:55 -- "A Review of the Global Assured Identity Network (GAIN): One Year On"
* Presenter:  Elizabeth Garber - Co-Chair GAIN Proof of Concept
* 10:55-11:30 -- OIDF Government Whitepaper Listening Session: "Citizen-Centric Identity Systems"
* Presenter: Elizabeth Garber – Whitepaper Co-Author
* 11:30-12:05 -- OIDF Privacy Whitepaper Listening Session: “Help Design a Scalable Future for Personal Privacy”
* Presenter: Heather Flanagan - Principal at Spherical Cow Consulting
* 12:05-12:30 -- Closing Remarks, Open Q&A and Networking
* Presenter: Gail Hodges – OpenID Foundation Executive Director

FDX Global Summit Fall 2022
----------------------------------
October 18th – 19th – FDX Global Summit Fall 2022

Wes Dunnington & Joseph Heenan will be presenting “he journey from OAuth to FAPI: Why should I do this and what do I need to know?” (reference final agenda for date and time TBC)

OIDF Workshop prior to IIW Fall 2022
----------------------------------------
Monday, November 14th – OIDF Workshop prior to IIW Fall 2022

* Finalizing host location in the Mountain View area.
* Details including registration link will be published to the OIDF website.


External Orgs & Liaisons (Mike L./Chris)
============================================
Brazil 
-----------
Recertification stated. Chicago consultants to become a sustaining member of OIDF. 

Saudi
---------


Security Analysis (Daniel)
=============================
The WG discussed how the identified issue during the formal analysis could be addressed. 
It can be characterised as an attack tricking the honest user into following the link that causes authorization requests on behalf of the attacker. 

The issue came up only in the current analysis as the attacker is slightly stronger than what was presumed in the previous analysis. 

During the discussion, the following was mentioned as being useful

* Cross-Device Flows (Draft) - https://docs.google.com/document/d/1Cka4ZZvi4z-nf55UbW4nmtgzlfAZSLLR4CRkvv3xVKc/edit?pli=1#heading=h.ej62mrgnmec6
* Trust Tokens - https://developer.chrome.com/en/docs/privacy-sandbox/trust-tokens/

Daniel and Pedram will discuss the matter again tomorrow morning and report back to the WG. 

The call adjourned at 15:15