============================================
FAPI WG Meeting Notes (2020-12-02) 
============================================
* Date & Time: 2020-12-02 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-12-02_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Nat, Dave, Don, Takahiko, Kosuke, Crhis, Francis, Joseph, Dima, Brian, Lukaz, Don, Joseph, Ralph, Sascha, Torsten
* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
Adopted as is .


Events
===========

* OBIE is doing a consultation on Variable Recurring Payments.
* Please consult OpenBanking website.
* The deadline for feedback is 12/4/2020.


External Organizations
=================

Australia
-----------
Don is arranging a meeting with someone at ACCC.


Berlin Group (Francis)
----------------------------
* Renaming to Open Finance Framework is done.
* Now moving to renaming the Advisory group and advisory boards to Finance Advisory group.
* There is an action plan for 20-21 published with intent to get it broader.
* It’s very payment oriented focuses on payment accounts.
* Francis working to get FAPI adopted.

Switzerland (Francis)
----------------------------
Currently, there are 2 standards
* Open Banking CH  - openbanking.ch

  * Adopted Berlin group and has sandbox up and running

* SFTI (Swiss Fintech Innovation)

  * Francis is working to get them to adopt FAPI  They would like to know the following

    * Timeline of FAPI 1.0 and 2.0
    * Scope and validity
    * Stability of drafts
    * Implementations

  * They’re also talking to the Swiss Finance Authority to create a common certification body to help with centralizing the accreditation of third party providers.
  * There was an action item for FAPI WG to create an FAQ to answer some of these questions and provide some statistics.
  * Francis asked whether it would be better to get a SFTI member to join OIDF or an OIDF member to join SFTI

    * Joining OIDF is the better preferred option but OIDF can appoint a liason who is willing
    * Francis can facilitate introductions but can’t volunteer himself because he’s already a member of SFTI and is a conflict of interest

      * Informational links

        * https://common-api.ch/index.php/en/
        * https://swissfintechinnovations.ch/projects/common-api/
        * https://c-a-p-s.atlassian.net/wiki/spaces/PUB/overview
        * https://github.com/swissfintechinnovations/common-API

      * WG members interested in becoming liaison can volunteer


UK (Chris)
-----
* There are activity around Brexit and alternative certificates.
* There are guidance on explaining how different banks’ approaches to migration.
* FAPI Conformance certification is ongoing.
* Chris suggested having a session on FAPI 2.0 to increase visibility.


FDX
------
* Dima and Torsten will talk with FDX regarding grant management after one of their general meetings.
* 1st meeting of FDX taskforce looking at FAPI alignment will meet next Wednesday


Brazil
--------
* Brazil is regulation driver but standards are market led.
* The central bank and the security WG will ask a representative to come and join this working group.
* The central body gets submissions which are submitted to the central bank who will review and certify them.
* An implementation/standards body is being formed with WGs:

  * security
  * authorization
  * consent
  * functional APIs


Issues
======

FAPI 1.0 Issues
--------------------

#334 - Question regarding metadata

* Requests explanation for  the part “shall only distribute discovery metadata”
* Change to “Shall not use other means to distribute metadata”

#333 - Broken link to ISO Directive 2

* PR from Dima merged.

#332 - Hyperlinks not working in published versions

* Assigned to Edmund

#330 - potentailly misleading language WRT JWT ATs

* Suggested “access tokens should be opaque to clients which can be unstructured or structured”
* Dim to create PR

#331 - Editorial: Part2 - Section 7 missing

* Resolved

#90 - Create a sensible privacy consideration section

* Will use text from Part 2.
* Assigned to Dave.

#319 - (ed) awkward/incorrect language around request_uri

* Use PR # 222 from Brian

# 317 - Part 1 'require the redirect_uri parameter' could have a better wording

* Assigned to Dave

#232 - Part 1: Complete the privacy consideration section

* Duplicate of #90


Drafts
===================
Did not get to drafts.



HTTP Signing
------------------

* Dave and Brian looking at what to do for non-repudiation for generic API endpoints;
* Method will be based on DPOP



The meeting was adjourned at 15:00 UTC.