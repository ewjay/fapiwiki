============================================
FAPI WG Informal Meeting Notes (2016-08-09)
============================================
Date & Time: 2016-08-09 23:00 UTC (16:00 PDT) - 00:10 UTC

Location: GoToMeeting 

Attendees: 

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

    Discuss whether we should be a member or request a liaison relationship. 

ISO TC68
----------------

ISO TC68 will have a meeting this November. We probably should send a liaison request. 

    To Mandate Nat to develop a liaison request. 



New & Open Issues
======================
In the call, participants discussed the following issues 
listed in the [issue tracker](https://bitbucket.org/openid/fapi/issues)

* issue #2: Accounts: Total Pages and Page does not make sense
* issue #4: Remove MessageFormat and references to it
* issue #7: Add "Open Data" data set
* issue #8: Should hard coded paths be avoided
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
As far as the terminology is concerned, it was prevalent among the callers 
that OAuth term should be used instead of creating something else. 

Some of the issue was related to the ambiguity etc. of 
the DDA spec that we are basing on. These (#17, #20, #22) was 
assigned to Anoop. 

AOB
========
* Next Call: Wed Aug 17, 2pm UTC (7am PDT, 11pm JST)

 


