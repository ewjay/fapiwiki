============================================
FAPI WG Meeting Notes (2017-12-06)
============================================
Date & Time: 2017-12-06 17:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 17:__ UTC. 

Roll Call
===========
* Attending: 
   * Guest: 
* Regrets: Anoop, Tony

Adoption of the Agenda (Nat)
==================================

Open Banking IE Topics (Ralph)
================================

Decision 088: authorizing multiple intent-ids at once
--------------------------------------------------------
* https://openbanking.atlassian.net/wiki/spaces/WOR/pages/28934198/088

Decision 089: Pertial acceptance of intents 
---------------------------------------------------
* https://openbanking.atlassian.net/wiki/spaces/WOR/pages/28934198/089

In addition to the decision 088 on authorizing multiple intent-ids at once, there's also two other related decisions on the expected behaviour during authorization:


Decision 090: how tokens issued from the authorization grant are managed
-------------------------------------------------------------------------------
* https://openbanking.atlassian.net/wiki/spaces/WOR/pages/28934212/090

CIBA FAPI profile (Dave)
=========================
* Device re-association attack for account takeover examined. 
* MNO will know if the phone is changed. 
* Authenticaiton and federation should be distinct. 
* Perhaps can leverage EAP. 

* User questioning API allows questions to be a part of the authentication flow. 
   * UQ does not provide access token. 
   * Do you approve this payment? 

* Joint call is going to be convened by Bjorn on the topic of CIBA and UQ. 

Next version of Part 1 & 2 (Nat)
===================================
* Nat and Edmund is preparing the next version. 
* Forward text perhaps should be modified. 


External Organizations
=============================
TC 68 and Fintech Call (Dave)
---------------------------------
* Dave joined the Fintech SG call. The chair mentioned about FAPI so it was good. 
* We need to find out if we need additional Class D liaison to join the group. 
* Nat thinks Class A liaison is adequate but will check with Jannet @ X9. 

FS-ISAC Response (Anoop)
---------------------------
* Document link has been shared to the meeting participant to start commenting. 
* Any WG member is welcome to join in the effort. Please contact Nat to get an access. 

OpenBank Project (Nat)
--------------------------
* Nat had a skype call with Simon Redfern, CEO of TESOBE who hosts OpenBank project. 
* OpenBank project currently uses OAuth 1.0 and Nat explained the advantage of FAPI. 
* He also explained the state of the work at FAPI WG. 
* Simon will consult with his engineering team to see if they should join FAPI WG. 

European Commission (Bjorn/Dave)
-----------------------------------
European Commission (EC) has published its final “supplementing Directive 2015/2366 of the European Parliament and of the Council with regard to regulatory technical standards for strong customer authentication and common and secure open standards of communication”

* http://ec.europa.eu/finance/docs/level-2-measures/psd2-rts-2017-7782_en.pdf

The official announcement can be found in the `EC press release <http://europa.eu/rapid/press-release_IP-17-4928_en.htm>`_ along with a `Fact Sheet <http://europa.eu/rapid/press-release_MEMO-17-4961_en.htm?locale=en>`_.

Some of the new articles are pretty horrific from a security point of view:


    Account servicing payment service providers that have put in place a dedicated interface shall ensure that this interface does not create obstacles to the provision of payment initiation and account information services. Such obstacles, may include, among others, preventing the use by payment service providers referred to in Article 30(1) of the credentials issued by account servicing payment service providers to their customers, imposing redirection to the account servicing payment service provider's authentication or other functions, requiring additional authorisations and registrations in addition to those provided for in Articles 11, 14 and 15 of Directive 2015/2366, or requiring additional checks of the consent given by payment service users to providers of payment initiation and account information services.

It seems to mean:

* Banks have to allow customers to use the same credentials when accessing their online banking interface, and when using a third party provider (TPP)
* Banks cannot force the TPP to redirect customers to the bank for auth
* Banks cannot force TPPs to register with any directory/registry - this seems to make it hard for a bank to require a TPP to create an OAuth client

Tom pointed out that banks are unlikely to accept that liability. 


Open Banking (Ralph)
--------------------------
* Multi Consent etc. are coming up as new requirements. 
* Tom pointed out that User Questioning API may work here. 


AOB
===========
* Dynamic Client Registration - Is Pam back? Nat will check. 

Next Call (Atlantic)
-----------------------
The next call is scheduled to be in the Atlantic time zone. 

* The meeting was adjourned at 23:59 UTC.