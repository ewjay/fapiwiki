============================================
FAPI WG Meeting Notes (2022-01-05) 
============================================
* Date & Time: 2022-01-05 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2021-12-15_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 
* Regrets:
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* 

Events (Dave/Nat)
======================
CFP for Identiverse (Nat)
--------------------------------
* Deadline: January 7. 
* Joseph is going to be proposing one on certification. 
* Link: https://identiverse.secure-platform.com/a

EuroDig 
----------------
Just had an initial call for a proposal that closed on Dec 31. Eurodig will be overlapping with Identiverse in June

* Call for proposals: https://www.eurodig.org/get-involved/
* List of proposals: https://www.eurodig.org/get-involved/planning-process/list-of-proposals-for-eurodig-2022/

Michael Palage's proposal: Digital Identity. Despite the critical role that digital identity plays, it is a widely misunderstood concept. We propose to take a holistic approach toward the topic through the single unifying lens of the Universal Declaration of Human Rights: a) Definition. An alphabet soup of terms used in digital identity in different technical standards/protocols and governance frameworks. Based on the current best thinking there is a need to agree on a working definition of digital identity. b) Technical Implementation. We need to look number of specific digital identity technical implementations and the strengths and weaknesses of each, and on how closely it aligned to the relevant articles in the UDHR and the OHCHR. c) Emerging Trust Frameworks. We need to look at some of the emerging trust frameworks that have been proposed to implement digital identity and identify points of convergence and divergence. d) Business Models. We need look at the various business models for digital identity solutions (private/public/hybrid), and how cultural considerations may have acted as a barrier to implementation in some countries. As the EU moves forward with proposed revisions to eIDAS regulations, it is importance for both the public and private sector to have an open dialog about digital identity. If the EU is successful, the revised eIDAS regulations can become the gold stands in digital identity.

External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------
N/A

Brazil (Mike L.)
---------------------------
* N/A
* Continue to receive RP certifications (Currently 19 organisations certified.) 

Berlin Group (Dave)
--------------------------------
* Dave to follow up. 

FDX (Gail)
------------------
Blog post on FAPI 1 v.s. 2. was published. 
Gail followed up with Don C. 

The Middle East and North Africa (Ali)
---------------------------------------
* Received the draft MOU today.

Mexico (Gail)
------------------
n/a

NIST (Gail)
--------------
NIST IR 8389 is now available for comments. 
See http://lists.openid.net/pipermail/openid-specs-fapi/2022-January/002514.html for more details. 

Russia (Dima/Mike)
--------------------
* BOR is looking at the security profile right now. 

UK (Chris)
--------------------
* No news yet. 

GAIN (Mike)
---------------
Participation agreement
~~~~~~~~~~~~~~~~~~~~~~~
It is under review. 

G5
~~~
Consensus on MOU among the five. 
Now socializing with their boards. 

Roadmap (Don)
~~~~~~~~~~~~~~~~
Identifying participants. 35 participants. 


FAPI DCR/M (Dynamic client registration and Management) (Joseph)
====================================================================
* Joseph will try to make it ready for the next week. 

Grant Management (Dima)
=============================
* Trying to close off as many issues. 


PRs (Dave/Nat)
=================
#269 - Compilable http signing, a lot of rejigging to get references right
-----------------------------------------------------------------------------
Joseph mentioned the glitch that may happen for the pipeline. 

#270 - Compilable deployment advice updates (Stuart)
-----------------------------------------------------

Issues (Dave/Nat)
=====================
#464 - Review casing of keywords (Travis)
---------------------------------------------
It will be reviewed. Assigned to Dima. 

#461 - FAPI2-Baseline - has the time come to recommend/require TLS 1.3? (Joseph)
---------------------------------------------------------------------------------
The working group agreed to recommend to contain TLS 1.2 just like in FAPI 1.0. 

#460 - FAPI2-Baseline TLS restrictions are written as prose
----------------------------------------------------------------------
Editorial one suggesting the text to be converted to a bullet list so that they can be enumerated. 

To be addressed with #461. 

There is an argument that if we allow rotation of refresh tokens it should happen relatively regularly so it doesn't become a surprise to the clients down the road.

AOB (Nat)
=================




The call adjourned at 15:02 UTC

Chat Log
-----------
Me to Everyone
1. Roll Call (Dave/Nat) 
2. Adoption of Agenda (Dave/Nat) 
3. Events (Dave/Nat) 
3.1. CFP for Identiverse 
4. External Organizations (Dave/Nat) 
4.1. Australia (Gail/Dima/Joseph) 
4.2. Brazil (Mike L.) 
4.3. Berlin Group (n/a) 
4.4. FDX (Gail) 
4.5. The Middle East and North Africa (Ali) 
4.6. Mexico (Gail) 
4.7. NIST (Gail) 
4.8. Russia (Dima/Mike) 
4.9. UK (Chris) 
4.10. GAIN (Gail) 
4.10.1. Participation agreement 
4.10.2. G5 
4.10.3. Roadmap (Don) 
5. FAPI DCR/M (Dynamic client registration and Management) (Joseph) 
6. Grant Management (Dima) 
7. PRs (Nat) 
8. Issues (Dave/Nat) 
9. AOB (Nat) 
9.1. Next Meeting (Dave/Nat) 
9.2. Chat Log

23:07Brian Campbell (Ping Identity) to Everyone
https://identiverse.secure-platform.com/a

23:11Michael Palage to Everyone
And there is new variant IHU :-( the identified in France

23:13Michael Palage to Everyone
Hello Nat. Sorry that I could not get off of mute sooner. But another event worth monitoring is EuroDig which just had an initial call for proposal that closed on Dec 31. Eurodig will be overlapping with Identiverse in June

23:16Michael Palage to Everyone
Here is the link - https://www.eurodig.org/get-involved/

23:19Me to Everyone
http://lists.openid.net/pipermail/openid-specs-fapi/2022-January/002514.html

23:20Me to Everyone
https://csrc.nist.gov/publications/detail/nistir/8389/draft?utm_campaign=Daily%20News&utm_medium=email&_hsmi=199892597&_hsenc=p2ANqtz-8e00EUjDiF3cjokSiAHdV2blyRoL4PdEUljePvkXfNQO4YqwPt-MachArLcSSoeen1_Y8lc3UlnOD734uGAZX1BPYbUg&utm_content=199892597&utm_source=hs_email

23:21Michael Palage to Everyone
branding branding branding :-)

23:24Dima Postnikov to Everyone
2 paragraphs on API security and one of them on SAML… 🤔

23:26Michael Palage to Everyone
@Daniel - will Mark be able to update on this list during this Friday's POC call?

23:27Michael Palage to Everyone
Ok - THX

23:29Mike Leszcz to Everyone
I have to drop early today. Have a good day.

23:35Dave Tonge to Everyone
https://bitbucket.org/openid/fapi/issues/464/review-casing-of-keywords

23:36Dave Tonge to Everyone
https://bitbucket.org/openid/fapi/issues/461/fapi2-baseline-has-the-time-come-to

23:37Michael Palage to Everyone
Nat for your notes here is the link to EuroDig proposals, https://www.eurodig.org/get-involved/planning-process/list-of-proposals-for-eurodig-2022/

23:37Michael Palage to Everyone
Here is a summary of the proposal I was involved in submitting

23:37Michael Palage to Everyone
Digital Identity. Despite the critical role that digital identity plays, it is a widely misunderstood concept. We propose to take a holistic approach toward the topic through the single unifying lens of the Universal Declaration of Human Rights: a) Definition. An alphabet soup of terms used in digital identity in different technical standards/protocols and governance frameworks. Based on the current best thinking there is a need to agree on a working definition of digital identity. b) Technical Implementation. We need to look number of specific digital identity technical implementations and the strengths and weaknesses of each, and on how closely it aligned to the relevant articles in the UDHR and the OHCHR. c) Emerging Trust Frameworks. We need to look at some of the emerging trust frameworks that have been proposed to implement digital identity and identify points of convergence and divergence. d) Business Models. We need look at the various business models for digital identity solutions (private/public/hybrid), and how cultural considerations may have acted as a barrier to implementation in some countries. As the EU moves forward with proposed revisions to eIDAS regulations, it is importance for both the public and private sector to have an open dialog about digital identity. If the EU is successful, the revised eIDAS regulations can become the gold stands in digital identity.

23:51Dave Tonge to Everyone
https://bitbucket.org/openid/fapi/issues/460/fapi2-baseline-tls-restrictions-are

23:51Kosuke Koiwai to Everyone
My personal note regarding TLS1.3 discussion we had in Oct.30:

23:51Kosuke Koiwai to Everyone
216 - any chance to update BCP195? could be just 1 line doc saying use TLS1.3 
so if BCP195 won’t be updated how can we. Wait for TLS1.3 to widely available? 
already issue with UK OB. prefer adding those two but need expert advice. 
trying to email to relevant WG for input?

23:52Dave Tonge to Everyone
https://bitbucket.org/openid/fapi/issues/456/proposal-should-we-remove-support-for

0:01Joseph Heenan (Authlete / OpenID Foundation) to Everyone
There is an argument that if we allow rotation of refresh tokens it should happen relatively regularly so it doesn't become a surprise to the clients down the road.

0:02Brian Campbell (Ping Identity) to Everyone
that's a good point Joseph

0:03Brian Campbell (Ping Identity) to Everyone
also somewhat tangential :)

0:03Michael Palage to Everyone
White Board session - Yhea !!!