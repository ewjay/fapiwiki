============================================
FAPI WG Informal Meeting Notes (2016-08-09)
============================================
Date & Time: 2016-08-09 23:00 UTC (16:00 PDT) - 23:59 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

Attendees: Nat, Anoop, (Abel Rojas as guest), Edmund, Henrik

.. sectnum::
   :suffix: .

.. contents:: Agenda


Document Restructuring
============================
Nat introduced the document restructuring proposal. 
Current draft jumps all around on different topics and is hard to read. 
Proposed new structure is as follows, which is available on the 
WG Wiki(https://bitbucket.org/openid/fapi/wiki/Editors-Draft-00)

Financial Services – Financial API::

    1. Scope
    2. Normative references
    3. Terms and definitions
    4. Symbols and Abbreviated terms
    5. Getting Tokens
    5.1. Introduction
    5.2. Read Only Access
    5.3. Write Access
    6. Using Tokens
    6.1 Introduction
    6.2 Read Only Access
    6.3 Write Access
    7. Resource APIs
    8. Security Considerations
    8.1 TLS Considerations
    9. Privacy Considerations
    10. Acknowledgement
    11. Bibliography
    Annex A Financial Data API Level 1 (Normative)

Note that the section structures are according to the ISO Directive Part 2. 

    Discuss whether the proposed structure is adequate, and give mandate 
    to editors to come up with a new WD. 

External Org Relationships
=============================

UK Open Banking Development Group
------------------------------------

As the follow up to UK Open Banking Worg Group (OBWG) at ODI, Open Banking Development Group (OBDG) has been announced. 
See ODI Announcement (http://theodi.org/news/announcing-the-open-banking-development-group?platform=hootsuite). 

Membership strucutre etc. are available at (https://docs.google.com/document/d/1fUx0Hbc3k2F_NF4mXD55r2E_TKVU5KY6gDM1RJ0J1ds/edit#heading=h.g10eedc4thyf). 

Fee Structure:: 

    Corporate: GBP 5,000
    SME: GBP 720

Should we seek to be a member (under SME) or try to establish a liaison? 

    ASK: Discuss whether we should be a member or request a liaison relationship. 

* Nat to draft liaison request
* Anoop to follow up with Intuit UK Team
* Henrik to follow up with Danish Bank, who is a member of OBDG

ISO TC68
----------------

ISO TC68 will have a meeting this November. We probably should send a liaison request. 

    ASK: To Mandate Nat to develop a liaison request. 

Action::

    Nat to draft liaison request

New & Open Issues
======================
In the call, participants discussed the following issues 
listed in the [issue tracker](https://bitbucket.org/openid/fapi/issues)

Since we were short of time, we have gone through only the following issues: 

* issue #2: Accounts: Total Pages and Page does not make sense

    It is not meant to be physical page but "memory page". Some companies have hundreds of accounts 
    and need "pagination". 
    Assigned to Anoop. Anoop is going to send the example so that we can make a better "description" 

* issue #7: Add "Open Data" data set

    There is no such thing in DDA. We need to create our own. 
    David Tonge's group in UK is creating this. We need to get more info on it. 
    At the same time, we should gather more data on each countries so that we can come up with a sensible one. 
    Assigned to Anoop. 

* issue #8: Should hard coded paths be avoided

    It is desirable not to constrain the path. DDA's path is just an example and implementations are free to 
    create their own path as long as they adhere to the functional requirements. 
    We will write in the main text that the paths in Annex A are only examples. 
    Assigned to Nat. 

Working Group members are asked to go through the rest of issues and put comments in the tracker / discuss on the email list. 

* issue #4: Remove MessageFormat and references to it
* issue #10: Internationalization of strings
* issue #11: OAuth Profile should mandate RFC7636 (PKCE) for code flow
* issue #12: OAuth Profile should mandate per AS redirect URI for Clients with session comparison
* issue #13: TLS 1.0 should be banned
* issue #14: Allowed Redirection Client URI is not a defined term
* issue #15: Client Authentication, not Client Authorization
* issue #16: Client Authentication -- Do we need TLS mutual authentication?
* issue #17: Incomplete sentence "In line with FFIEC (Federal Financial Institutions Examination Council) guidance on Authentication to mitigate security risks."
* issue #18: "Authorization token" is not a defined term in RFC6749
* issue #19: Remove or Improve OAuth Interactions Diagram
* issue #20: Meaning of the Surrogate Identifier Clause not clear
* issue #21: Residual Data clause should be generalized and moved to privacy considerations
* issue #22: Undefined OAuth response parameter `user_id` appears in the text
* issue #23: How do I find AccountID to use in transfer?

The previous discussion results are recorded in each issue tickets. 

Some of the issue was related to the ambiguity etc. of 
the DDA spec that we are basing on. These (#17, #20, #22) was 
assigned to Anoop, and Anoop will follow up. 

Action: 
    WG members to follow up with the issues. Anoop to send notes especially on (#17, #20, #22). 

AOB
========

Next Call
----------
* Wed Aug 17, 2pm UTC (4pm Denmark, 7am PDT, 11pm JST)

    Anoop will not be able to join this call, but he will send notes before it so that the group can discuss it. 

Meeting was adjourned at 23:59 UTC. 
