===========================================
FAPI WG Agenda & Meeting Notes (2023-04-06) 
===========================================
Date & Time: 2023-04-07 00:00 UTC
Location: https://zoom.us/j/97456084642?pwd=bTRFVzk4ZmlRK1M3bEprRlN5c3JFZz09 


.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 00:00 UTC. 

Roll Call (Anoop)
=====================
* Attendees:   
* Regrets:    

Agenda

Events Update:
* Workshop at Microsoft – Monday, April 17, 2023
    https://openid.net/2023/03/17/registration-workshop-at-microsoft/ 

* Liaison

* * NIST 
* * * Mark is leading the discussion. Several meetings.
* * * Deadlines were postponed to April 14.

Link to the comment sheet that OIDF is compiling:
        https://docs.google.com/spreadsheets/d/1JHDypzbKg8x2AMfC_z4pzDBk4waVJBp2/edit#gid=571622526

* Government-issued Digital Credentials and the Privacy Landscape” whitepaper
* *  It is now open for comment: https://openid.net/2023/04/05/open-for-comment-privacy-landscape-whitepaper
* * Please review and comment.

* * OECD

* * * Online public consultation on the draft OECD Recommendation on the Governance of Digital Identity
            https://www.oecd.org/fr/gouvernance/gouvernement-numerique/online-public-consultation-draft-oecd-recommendation-on-the-governance-of-digital-identity.htm

* * * Gail created a draft letter:
            https://docs.google.com/document/d/1Vu-5Pt6K-4nPccNZ_0eC4RLavifUZntnGgBLKBEYsv0/edit




* Certifications
* * Continue to get new request for certification from Brazil (OpenFinance) & Saudi Arabia (Open Insurance)
* *  FAPI2 Conformance test is now available (Mike) 

    https://openid.net/2023/03/21/fapi-2-conformance-tests-available/

* A standards comparison table is being compiled. Volunteers to review / add content are sought.

Currently, it includes:

    Bahrain Open Banking Framework - Bahrain OBF
    Bank Interfaces for Standardized Payments - BISTRA
    Consumer Data Standards - CDR
    Czech Standard for Open Banking - COBS
    Financial Data Exchange API - FDX
    Open API Framework for Hong Kong
    India Stack
    Japan Open Banking Framework
    NextGenPSD2
    Open Banking In Nigeria (draft)
    API Centre standards
    Open Banking Brasil
    PolishAPI
    STET PSD2 API
    Singapore Financial Data Exchange - SGFinDex
    Slovak Banking API Standard
    SNAP
    KSA Open Banking Standard
    Open Banking Platform
    Swiss NextGen API
    UK Open Banking Standard

Also, we need to find out what is the best way of crediting individuals and the foundation of the work. Chris will ping Gail and Nat on this.

* Draft Updates
* * Dave has sent the fixed Implementer's draft documents to Mike J [related to message signing]
* * Dave is creating a submission package now. [ Grants Management ]

* PR Updates
* * Apart from one PR that we are parking until HTTP signature is settled, there is no standing PR.
* * Request/Response binding fix is waiting for IETF result next week.

* Issue Updates
* * CIBA
* * *  https://bitbucket.org/openid/fapi/issues/580/fapi-ciba
* * *  Discussed the changes it needs for supporting FAPI2.
* * *  Whether signing is required or not should be based on whether the base profile requires signing (e.g., FAPI2 Message Signing + CIBA should require it, while FAPI2 Security Profile + CIBA should not.)
* * *  5.2.2.6
* * *  Assigned to Filip.
* * Network Layer Protections restrict use of more recent TLS 1.2 ciphers
* * * Moving to TLS 1.3 removes the restrictions on the ciphers.
* * * However, the certification suite does not support TLS 1.3.
* * * Nat to create an issue on the tracker regarding this.




================================

 
Next Call
==============================
Next call will be an Pacific Call. 
Next Pacific call will be in two weeks (03-23-2023 @ 5pm PST) UTC - 03-24-2023 1:00 AM.