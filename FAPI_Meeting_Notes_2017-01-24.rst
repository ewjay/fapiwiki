============================================
FAPI WG Meeting Notes (2017-01-24)
============================================
Date & Time: 2017-01-24 23:00 UTC 
    (15:00 PDT, 23:00 UK, 00:00 Denmark, 08:00+1 JST)

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 15:05 UTC. 

Roll Call
=============
* Present: Nat, Anoop, Edmund, Henrik
* Regrets: Tony, John, Sascha
* Guest: 

Adoption of the Agenda (Nat)
===============================
* Adopted ammended: 
    * Skipping Events as we are missing John. 
    * New use case discussion added. 

Implementer's draft Part 1 voting preparation (Nat)
====================================================
* Voting announcement has been made. 
* Details can be found at: http://openid.net/2017/01/20/notice-of-vote-for-implementers-draft-of-financial-api-part-1-read-only-api-security-profile/
* Please prepare for voting: 
    * check if you can login etc. 

Working Drafts
===================

    * Financial_API_WD_001.md Financial API - Part 1: Read Only API Security Profile
    * Financial_API_WD_002.md Financial API - Part 2: Read and Write API Security Profile
    * Financial_API_WD_003.md Financial API - Part 3: Open Data API
    * Financial_API_WD_004.md Financial API - Part 4: Protected Data API and Schema - Read only
    * Financial_API_WD_005.md Financial API - Part 5: Protected Data API and Schema - Read and Write

Part 1: Read Only API Security Profile (Nat & Edmund)
-------------------------------------------------------------
* Edmund applied all the editorial bug fixes collected during the review period. 
* Edmund is also working on the Pandoc HTML template and .docx template so that 
  it will look more like OIDF specs for HTML and ISO specs for .docx. 

Part 2: Read & Write API Security Profile (Nat & Edmund)
------------------------------------------------------------
* `Part 2: Read & Write API Security Profile <https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_001.md>`_
    * https://bitbucket.org/openid/fapi/src/master/Financial_API_WD_002.md 

* Nat and Edmund have been adding previously identified requirements onto the drafts. 
* For request objects, it is currently referring the section 6 of OIDC, but if OAuth JAR emerges as RFC, we should use it instead. Nat is currently working on SECDIR comments in IETF for OAuth JAR and will be discussed at IESG on Feb. 3. 

Issues (Nat)
=========================
* No new issues. 


External Orgs
==================

FS-ISAC DDA (Anoop)
--------------------
* For some time, banks were meeting within themselves to work out the charter, especially working out the IPR around data they are sharing. Now they are reconvening the working group and intuit is going to provide the status and advise on how to plug-in OpenID. 

    * Nat will follow up with Bob Blakley at Citi. 
         * Citi participant at DDA: Clint Stephan, Security Group. 
    * Tony will follow up with EMV. 

OFX (Anoop)
------------------
* As FS-ISAC started moving along, OFX should also be aligned with them. 

JP Banking Association (Nat)
-----------------------------
* Nat and JP Fintech Association visited the JP Banking Association. 
* JP Banking association is in the process of creation of their API recommendations. The secretariat believes that it should adopt a standard created by experts so adopting FAPI Part 1 and Part 2 seems to be the course. 
* For the data schema part, they were pessimistic about the possibility of them being able to come up with a single schema, let alone adopting DDA etc., but Fintech Association advised that they should at least try to. From the point of view of a Fintech company operating worldwide, each countries creating their own schema means they have to prepare for over 200 schemas and that is bad enough. If each country starts to have multiple schemas, that will multiply the "badness". 

Denmark Banking Association(s) (Henrik)
------------------------------------------
Denmark situations are changing rapidly. 
There were two competing banking associations but they got merged. A few days before the merger, 
the absorbed side published API but as they were absorbed, the API was withdrawn. 
Now banks are looking at the possibility of postponing the PSD2 implementation as much as possible. 

Henrik wanted to know if anyone in FAPI is talking with EBA. 
Nat pointed out that Dave was responding to the second consultation by EBA (not as FAPI WG liaison) and that we can put it on the agenda of the next week's teleconference. 


New Use Cases Discussion (Anoop) 
==========================================
* Some use-cases where OAuth has shortcomings were identified. 

#. OAuth Left-out session problems
#. Adding two accounts from the same bank to a Fintech software

Shared computer use case 1
---------------------------------
Environment
~~~~~~~~~~~~
A shared computer "PC" with two users, Alice and Ben. 
The computer has multiple local applications, AppA and AppB, that use a browser to get OAuth tokens from a Web service "W" using the web browser, "UA". 

Use case
~~~~~~~~~~
1. Alice goes to the PC and starts AppA and logs into it. 
2. AppA invokes UA to get OAuth tokens from W.  
3. Alice is presented with login dialogue at W. 
4. Alice provides her credentials to W for logging in. 
5. W shows the consent screen through UA. 
6. Alice agrees to it. 
7. AppA gets tokens. 
8. Alice leaves the computer by closing the AppA. 
9. Ben now comes to the computer. He starts AppB. 
10. AppB invokes UA to get OAuth tokens from W. 
11. As the UA still has the session created by Alice, Ben will not be presented with the login dialogue but will be presented the consent screen (as Alice.) 
12. Unkowingly, Bob consents (as Alice). 
13. Alice's account at W is now linked to Bob at AppB. 

Discussions
~~~~~~~~~~~~~
This problem does not happen with OpenID Connect as the AppA and AppB can provide the intended user with login hint and also mandate the re-prompt. 

This is a problem caused by OAuth to mock the identity federation protocol. Pure play OAuth cannot do it. To cope with it, the OAuth 2.0 needs to be extended, and it will end up pretty much the same with OpenID Connect. 

Shared computer use case 2
-----------------------------
Environment
~~~~~~~~~~~~~~
Two users: Hal (Husband) and Wendy (Wife)
A Computer: PC
Web Browser: UA
Personal finance application: App
Bank Website: B

Use case
~~~~~~~~~~
1. Hal starts App and starts adding his and Wendy's account to it. 
2. App starts UA and redirects to B. 
3. B shows the login screen through the UA. 
4. Hal logs in and gives consent. 
5. App gets the token and Hal's account is now added to the App. 
6. Hal now wants to add Wendy's Bank account to the App. 
7. App starts UA and goes to B, but since Hal is not logged out, he will not be shown the login screen and cannot add Wendy's account. 

Discussion
~~~~~~~~~~~~~
Again, this is not much of the issue for OpenID Connect as the App can send "prompt=select_account" or "prompt=login" to B, but OAuth cannot do it. So, the temporary solution that the App is using is to do the website logout. 

General Discussion
-----------------------
Nat pointed out that all these "problems" are caused by the fact that the sites are using OAuth for login purpose, which is wrong. Many developers complain that OpenID Connect is complex but if you want to do a sign-in, then you cannot do it with pure RFC6749+6750 and have to extend it, which pretty much end up with the same thing as OpenID Connect. 

Nat also pointed out that OpenID Connect WG is working on the logout specs and is probably good to consult with them. Logout is a very complex problem and needs a lot of thinking before actually doing it. In many cases, a single solution will not work and it would require combination of multiple specs. 




AOB
========

Next Call (Atlantic)
--------------------------
* 2017-01-31 15:00 UTC
    (07:00 PDT, 15:00 UK, 16:00 Denmark, 00:00+1 JST)

The meeting adjourned at 23:59 UTC.