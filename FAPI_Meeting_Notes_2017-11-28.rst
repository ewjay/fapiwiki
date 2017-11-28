============================================
FAPI WG Meeting Notes (2017-11-28)
============================================
Date & Time: 2017-11-28 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:__ UTC. 

Roll Call
===========
* Attending: 
   * Guest: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Added European Commission item
* Added Open Banking item

Next version of Part 1 & 2 (Nat)
===================================
* Nat and Edmund is preparing the next version. 
* Forward text perhaps should be modified. 

CIBA FAPI profile (Dave)
=========================


External Organizations
=============================
TC 68 and Fintech Call (Dave)
---------------------------------

FS-ISAC Response (Anoop)
---------------------------


OpenBank Project (Nat)
--------------------------

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

Open Banking (Ralph)
--------------------------
* Multi Consent etc. 


AOB
===========

Next Call (Atlantic)
-----------------------
The next call is scheduled to be in the Atlantic time zone. 

* The meeting was adjourned at 23:__ UTC.