============================================
FAPI WG Meeting Notes (2022-01-19) 
============================================
* Date & Time: 2022-01-12 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Self: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2022-01-19_Atlantic
.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:03 UTC. 

Roll Call (Dave/Nat)
======================
* Attending: 

  * Ali Adnan
  * Brian Campbell
  * Chris Michael
  * Daniel Fett
  * Dima
  * Dima Postnikov
  * Don Thibeau
  * Gail Hodges
  * George Fletcher
  * Jacob Ideskog
  * Joseph Heenan
  * Michael Palage
  * Mike Leszcz
  * Nat Sakimura
  * Ralph Bragg
  * Rifaat Shekh-Yusef
  * Srivathsan Morkonda
  * Stuart Low
  * Takahiko Kawasaki


* Regrets: 
* Guest: 

Adoption of Agenda (Dave/Nat)
================================
* 

Events (Dave/Nat)
======================

Identiverse
------------------------------------
June 21, 2022 

Denver, Colorado

Mike and Gail had call regarding OIDF submissions and will follow up with sponsorship of Identiverse.

EIC
------------------------------------
Deadline for submissions is Feb 28, 2022

Contact Gail if interested in submitting a presentation.

There will also be a OIDF Workshop at EIC on Monday May 9, 9:00 AM - 12:30PM local time.

On Wednesday and Thursday, there will be sessions for deep dives. 

Deep dive topic proposals are accepted.



External Organizations (Dave/Nat)
===================================
Australia (Gail/Dima/Joseph)
------------------------------------

Consumer Data Standards team is interested in supporting security analysis for several spec:

* FAPI 2.0 
* FAPI 2.0Advanced
* FAPI CIBA
* Grant Management (maybe)
* RAR 

Also got a quote from University of Stuttgart for part of the analysis.

Maybe possible to have different entities contributing to the required analysis.

Goal is to be finished by the first half of this year, but some specs are still not final.


Gail heard some potential additional requirements for other channels , e.g. extending FAPI to point of sales or another way.

Need to keep this in mind.


Nigeria (Gail)
------------------------------------

Nigeria is looking into Open Banking.

Started to compile legislation and API requirements.

One requirement is to be able to serve users that do not have smart phones and browsers.

They are using GDSS standard.

Asked how  would secure authentication and authorization such as FAPI work on USSD?

It’s a standard means of communication for mobile networks. Very low bandwidth mechanism used for micro-payments, commonly used in India.

Might be a better fit for CIBA.

Dave will create an issue for discussion.

Gail will invite them to join the WG.

This might address other places where feature phones are still in use.

Open Banking is not possible if a large portion of the population cannot be served.

If not possible, we might be able to offer some expertise and transparency.


Brazil (Mike L.)
---------------------------
Continue to receive RP certification requests.

Working with Squad sandbox to confirm CIBA requirements and timeframe for certifications.


Berlin Group (Dave)
--------------------------------
Will notify us the dates for new Workshops by the end of January.


FDX (Mike)
------------------


The Middle East and North Africa (Ali)
---------------------------------------
Had a meeting with DFC to discuss action items going forward post MOU signing.

Agreed to include terms to foster common interests and to mention broad terms of scope of collaboration, which will include 

* a regional chapter of OIDF at DFC.
* DFC will support OIDF with preferred access to spaces for technical training and events.
* Both parties to engage with the community from banks to enablers to educate and promote OpenID standards
* Collaborate on research and thought leadership

Ali will send a copy to Don and Gail for review.


Mexico (Gail)
------------------


NIST (Gail)
--------------
NIST IR 8389 is now available for comments.

See http://lists.openid.net/pipermail/openid-specs-fapi/2022-January/002514.html for more details.

NIST Page: https://csrc.nist.gov/publications/detail/nistir/8389/draft?utm_campaign=Daily%20News&utm_medium=email&_hsmi=199892597&_hsenc=p2ANqtz-8e00EUjDiF3cjokSiAHdV2blyRoL4PdEUljePvkXfNQO4YqwPt-MachArLcSSoeen1_Y8lc3UlnOD734uGAZX1BPYbUg&utm_content=199892597&utm_source=hs_email

Gail and Don will try to talk with article authors.

Anyone with contact with the authors or NIST can contact Gail.

Dim offered to draft the first response to the NIST paper. Gail and Don will review, followed by WG.  Tom will clarify legal, IPR matters.

Contributions are welcome. 

Nat created a Google doc for collaboration.

Will take comments from the document and turn them into a clear, written response with our key messages and points for consideration.

Also will coordinate responses with FIDO, Global Finance Center of Excellence, and FData.

Russia (Dima/Mike)
--------------------
Mike had contacted Nikita to schedule a call for follow up. Still awaiting response.


UK (Chris)
--------------------

GAIN (Mike)
---------------
Participation agreement
~~~~~~~~~~~~~~~~~~~~~~~

G5
~~~

Roadmap (Don)
~~~~~~~~~~~~~~~~




Grant Management (Dima)
----------------------------------------

PRs (Dave/Nat)
=================

* PR #305 - FAPI2 Baseline: Align the chapter etc. structure to FAPI 1

  * Joseph made some changes
  * Had problem with normative references at the end. Unable to move them to the front like ISO format.
  * Is the effort to make it ISO format worth it when most other specs are IETF style?
  * Needs further discussion

* PR #269 - Compilable http signing, a lot of rejigging to get references right

  * Merged

* PR #270 -  Compilable deployment advice updates

  * Merged

* PR #302 - Clarify token introspection responses

  * merged

* PR #303 - Authorization response clarification - clarifying that there is no change

  * Clarify that authorization response is not changed and grant ID should not be supplied
  * Need to be explicit if we’re expecting an error condition and might have interop issues if some implementation expect something and others don’t
  * Make it clear that it’s not an error and shouldn’t return grant_id
  * Merged


Issues (Dave/Nat)
=====================

* #456 - Proposal - should we remove support for refresh token rotation from FAPI 2.0 (one of the drafts)

Is there value in refresh token cycling with confidential clients?

One use case is for migrating between competitor’s identity server, but it is questionable whether it should be considered a factor for supporting refresh token rotation.

OP must not support refresh token rotation and RPs must support it.

What is the user expectation when the existing refresh token expires? If a confidential client’s secret is compromised, do all users must go through reauthentication? 

User’s will need to go through the whole flow again to get a new refresh token.

It might be OK if we’re banning refresh token recycling not because of a security issue but because of a user experience issue.

As a TPP, if a bank has a communication problem and throws away a client’s refresh tokens, TPP customer’s will lose access to the resources which may be critical. This will become a security issue.

Users will need to reauthenticate to get access, but as a TPP, the user’s might not be present at the time.

This creates risk but may not be a security problem.

The current mechanisms available to support refresh token recycling do not have necessary resilience to support it. 

Therefore, the protocol should prohibit it or add a security consideration to recommend against support due to resiliency risk.

We should recommend against support but not ban it.

Perhaps some wording to say must not rotate refresh tokens unless the implementation has some mechanism for the client to recover from failed refresh tokens easily.,

CDR has mechanism for issuing refresh token where old refresh tokens are valid until the new one has been used.

Will need more discussion.

AOB (Nat)
=================



The call adjourned at 15:00 UTC