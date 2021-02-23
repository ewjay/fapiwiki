============================================
FAPI WG Meeting Notes (2021-02-17) 
============================================
* Date & Time: 2020-02-17 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Dave, Joseph, Brian, Stuart, Dima, Don, Francis, Kosuke, Takahiko, Torsten Lukasz, Stenar Noem
* Regrets:
* Guest: 

Adoption of Agenda (Nat)
===========================
* Grant Management as the main item. 
* Pull Request 231. 

External Organizations (Nat)
================================
W3C Web Payment Interest Group (John)
--------------------------------------
Nat will connect with John. 

Australia (Dima/Stuart)
----------------------------------
Two suggested workshop. Data 61 to review it next Monday. 

Berlin Group (Francis)
---------------------------
Great workshop with Torsten and BG Advisory member on FAPI adoption. 
Emotional discussion on embedded mode. 

* this is our ticket on embedded: https://bitbucket.org/openid/fapi/issues/295/possible-support-for-embedded-sca-mode

We might have to provide them some alternative if we want to onboard the next gen group into FAPI and supply them with a good FAPI framework for redirect approach.


Ralph : There are better processes for embedded using hint processes, but it’s not a good idea.
Need to decide if we want to promote interoperability for something that’s inherently a bad idea and insecure or just not support it at all. If yes, then we might be able to codify some requirements and make it less bad.

Francis: It’s a question of science vs market. What market wants is not always scientifically clean, so we need to take their needs and prepare something that is scientifically acceptable.

Torsten: the discussion was dominated by people with specific view on topic, mainly provider of POS payment services, the way credit card payments work. They all work within trusted networks. PSD2 took the same approach to make TPPs part of the trusted network so they are allowed to handle credentials. Supporting unregulated clients may become more important. FAPI most likely will be positioned for truly open finance, whereas additional solutions are needed for more trusted and sophisticated parties with privileged/(heavily) regulated access, etc..

Francis: I’m against sharing passwords for TPPs, but would like to work on a ticket to the Open Banking association for sign payment requests where you sign a cryptogram and send over or one-time passwords. I would like to stop embedded mode where passwords are sent to TPPs.

Ralph: UK FCA is consulting on the action to compel every bank to make available their APIs that allow delegated third party access, i.e. kill passwords, 90 day reauthentication
The biggest barrier that was lobbied successfully by FData was that if you rely on something like TOPT, generated or pushed, customers won't use the services. The TPPs need access to the customers’ data in an unattended fashion without the customer’s necessary interruptions. They’re looking to remove the entire mechanism with justifications and support from FData and the wider TPP ecosystem. The consultation paper is highly recommended and contains compelling arguments, security concerns.

Ralph will send link to the consultation.

Chris: The argument is not about whether the customer is present or not, it’s about the TPP controlling the entire customer experience.

Ralph: If the intent is to allow the TPP to control absolutely everything, including aces to all those data, then it should be done the right way by exposing things via an interface that allows access safely.

Francis :  We need to have a common understanding on this topic. I will start the first post on the mailing list.

Discussion will continue on the ML.



Brazil (Chris/Ralph)
----------------------

The 830 banks have gone live.

Now moving into phase 2 with PKI and TLS requirements.

There’s some interesting proposals from the Brazilian Central Bank that I’m hoping to get permission to share with this WG.

There are still some fundamental issues.

* The Central Bank knows that the Banks and the ecosystem needs to create a model for the sharing and management of fine grained, fine grained grants. The are still in the introductory phase of recognizing that they need this.
* So, there is an opportunity, if we can get the next topic on the agenda quickly, to see if we can get the ecosystem to adopt Grant Management as the standard way to go forward.


Canada (Ralph)
------------------

UK (Chris/Ralph)
-----------------
* https://www.fca.org.uk/publication/consultation/cp21-3.pdf
* 90 days restriction removal. 
* Allow unattended access for OTP. 

* VRP consultation is finished. OBIE is publishing VRP standards at the end of March. 


Events (Nat)
======================

1st call of GOFCoE WG
------------------------
* The Global Open Finance Centre of Excellence’s aim is to create a forum where a group of standards bodies aligning standards and open finance.
* Will recommend that FAPI be one one of the first items to be taken up by the group.


KuppingerCole Event on March 3
------------------------------------
* https://www.kuppingercole.com/events/identity-fabrics-future-proofing-iam
* March 3. 
* On FAPI 2.0 and FAPI 1.0 differences by Daniel. Mainly on FAPI 2. 

Open Identity Summit 
-----------------------------
* https://oid2021.compute.dtu.dk/
* Submission deadline: March 1. 
* June. 

Grant Management SG report (Dima)
====================================
Dima presented the Grant Management Draft and asked for the adoption. 

https://bitbucket.org/openid/fapi/src/master/Financial_API_Grant_Management.md

* FAPI 1.0 doesn’t provide ability to manage consents and authorizations
* Every ecosystem that’s being created had to solve this problem in different ways
* Try to come up with an interoperable and secure protocol to convene authorization between the 

  * clients and authorization server, 
  * the TPP and the banks,
  * Data recipients and data holders

* Key modules

  * Ability to specify authorizations
  
    * authorization has to be jurisdiction specific

  * Management of consents
  * Client awareness for complex approval processes

* Try to use existing grant concept that every authorization service already supports and expose it via a standardized interface
* Key use cases

  * Establish concurrent grants
  * Update existing grants
  * Revoke grants

* Grant management

  * Support concurrent, independent grants
  * Support update of grants
  * Make grant (status) accessible and manageable by clients

* Grant Management spec sits between Client and AS

  * Authorization information needs to be transmitted between client and AS in order for consent to be established

* Changes

  * Modify existing authorization endpoint to support grant_id
  * Add 2 additional endpoints (revoke and query grants)

 
Francis: Also fits in well with Berline consent management. 

Nat: What are concurrent grants?

Dima: In Australia, we have regulatory requirements for users to have multiple active grants at the same time with the same TPP. Also for banks between data recipients and data holders.
It’s not a new behavior.

Francis: French authority requires concurrent grants, whereas German and most of Berlin group does not allow concurrent grants. Allowing concurrent grants in the spec will allow it to be adjusted for specific jurisdictions.

Torsten: We're trying to establish an interoperable way to control the behavior regarding grants from a client perspective. There are 2 types of implementations:
Always establish a new grant for a new authorization request
Merge base on user ID and client ID
We can support both. Clients can request a new grant or update an existing grant. Can also be specified in metadata.

Grants are independent of tokens. They can have a status.

Ralph via chat: I'd like to register support for this being formally adopted as a spec, to adopt, create extension, and the revocation delete, as the first draft, as modification may be quite a challenge to agree on implementation.

Brian: I disagreed with the comment that grant management doesn’t introduce any new functionality. There’s quite a bit of new functionality. Supporting both types of grants(new or update) results in forcing servers to be able to do both. I do not oppose it but it is a significant new introduction of functionality in this way.

Torsten: The point I’m trying to make is that the ability to support the different grants are there. We’re providing an interoperable interface for controlling the behavior. 
Support for updates can be published using metadata and will not be mandatory.
We would like to make adoption simpler and would like some feedback.

Takahiko: Are there any implementations of this draft?

Torsten: Not aware of any direct one-to-one implementations. CDR does something similar.

Stuart: CDR solution is essentially based on this draft.

Nat will send a call for adoption to the mailing list. The call attendees were generally in favor of adoption.


Pull Request 231 (Joseph)
==============================
Pull request #231 - From Edmund which updates introductory text which explains the two profiles. 

Has 2 comments from Torsten.

* Suggested replacing token binding with send constrained access tokens.
* Delete the sentence “The majority of uses cases identified that credit industries will require non-repudiation”

  * Assessment should be done by implementer

PR will be accepted after incorporating Torsten's comments.



The meeting was adjourned at 15:00 UTC.


Chat Log
============