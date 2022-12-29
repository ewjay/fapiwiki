===========================================
FAPI WG Agenda & Meeting Notes (2022-11-16) 
===========================================
* Date & Time: 2020-11-16T14:00Z
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-11-16_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call (Nat)
======================
* Attending: 

  * Brian Campbell
  * Daniel Fett
  * Dave Tonge
  * Dima
  * Gal hodges
  * Joseph Heenan
  * Pieter Kasselman
  * Ramesh Narayanan
  * Ali Adnan
  * Craig Borysowich
  * Dima
  * Kosuke Koiwai
  * Lukasz Jaromin
  * Luyllie Freitas
  * Pieter Kasselman
  * Takahiko Kawasaki


* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================

* Events
* External Organizations
* PRs
* Issues


Events (Mike L.)
====================================================






External Orgs & Liaisons (Mike L./Chris)
============================================
Brazil 
-----------


Saudi/SAMA
---------
Received specs last week

Joseph discussed some issues which may result in a new revision of the spec

Spec looks similar to OB-UK

Examples show use of parameterized scope passing the intent ID



IETF
-----------
RAR and DPoP are in review

No breaking changes were made to DPoP 



Canada
-----------


New Zealand
-----------

FAPI Specs
========================

General
-----------

Joseph noted that files in the repo keeps being renamed at the last moment due to Mike Jones asking them to be renamed so that the Markdown files have the same names as the corresponding XML and HTML.

There are rules constraining the format of the final file names

We should rename all files so that they follow the rules or change the build pipeline to output the correct file names

FAPI 2 Security Profile ended up with the file name FAPI 2 Security which might be a result of the build tools

Links to the FAPI 2 Markdown are now broken

Should we rename files to follow rules? If yes, we still need to keep old file names with pointers to the new file location

Investigate why FAPI 2 Security Profile resulted in FAPI 2 Security 

 * Due to the ‘Seriesinfo’ name value
 * Dave will add “profile” back to the filename

Should links point to compile ones or the Markdown?

 * Put links to the compiled version in the Markdown


Security Profile
-----------
Started Review period

Attacker Model
-----------
Started Review period

Message Signing
-----------
Ready for last call

Dave will start process


Grant Management
-----------
Need to create PR for remaining issue before last call

Implementation Advice
-----------
Moved some issues to the advice document

Need people to help with drafting the document


JARM
-----------
Spec is final

CIBA
-----------
Need to align it with FAPI 2



PRs
========

* PR # 387 - Fix typo in DPoP Proof Replay Security Considerations

  * Fixes some typos
  * Will be merged

* PR #385 -  Remove Financial from CIBA in line with FAPI?

  * Removed “Financial-grade” wording from document
  * Joseph commented that an introductory sentence is also deleted.
  * Dima will double check for anything missing.
  * Will need to remove wording from the website and other areas.
  * Mini-site (https://fapi.openid.net) is very open banking focused and will be addressed with web redesign





Issues
========
* #553 - More details on obtaining tokens for existing grant use case

  * Asking for more clarification for actions required for refreshing tokens using same grant


* University of Stuttgart - add researchers to acknowledgements

  * Should also add link to security analysis but link is not yet available


* #549 - Network Layer Protections restrict use of more recent TLS 1.2 ciphers

  * Will leave for Final draft

* #551 -Extra security considerations for clients as a result of formal analysis

  * Will leave for Final draft

* #532 - Token chaining and ID Token / multiple bearer tokens

  * Will leave open for now
  * Not within OIDF scope
  * IETF seems to be taking up this issue

* #467 - Can FAPI specs support ecosystems where smart phones aren't common, e.g. by using USSD

  * USSD is becoming a less important criteria for Nigeria
  * Nigeria’s priority is shifting away from open banking at the moment

  * *“The Central Bank of Nigeria has stalled on open banking since they released the draft guidance last May. It may be that their priorities have shifted from Open Banking to fighting inflation, releasing new currency designs, and pushing the e-Naira CBDC.  However, industry engagements continue to happen around authentication and authorization. From what we are seeing, trying to lasso FAPI or oAuth2 over USSD may not be a priority for the banks and CBN almost immediately. The technical challenges to make this happen is significantly more than the positive impact it may have for the target cohort of users. On the other hand, the adoption of smartphones continues to rise as internet access becomes cheaper and smartphones become available at  affordable price points. Invariably, the need for auth over USSD may not be required.  Thanks for the updates as well and it’s heartwarming to see the progress that FAPI has made good progress in other jurisdictions.  “*



* Open Banking Cross Borders WhitePaper

  * New version available at 
  * https://docs.google.com/document/d/176au5lZcR0vHbQG43wE7pZr7PBgVd7O7AqAzb6rqDzU/edit#heading=h.13q9deqt8x4g

  * Updated chart of ecosystem analysis

  * WG call for feedback by 11/23
  * Aim to publish before the end of the year

  * Recommendations and Monday calls will disband due to achieving work goals, but work remains to be done.
  * Gail suggested an interim community group for discussions


* Identiverse

  * Call for presentations due by January
  * https://identiverse.com




The call adjourned at 15:15