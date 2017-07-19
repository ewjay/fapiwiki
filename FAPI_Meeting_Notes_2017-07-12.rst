============================================
FAPI WG F2F Meeting Notes (2017-07-12)
============================================
Date & Time: 2017-07-12 08:30 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:10 UTC. 
It became late due to a technical problem that Nat had.  

Selection of a note taker
===========================
Mike Jones. 

Roll Call
===========
* Attending: 
Nat Sakimura - OIDF Chairman - FAPI WG Co-Chair - NRI
Torsten Lodderstedt - Yes
Gavin Wong - Open Banking - Working on R/W specifications
Tony Nadalin - FAPI WG Co-Chair - Microsoft
Tatsudo Kudo - NRI SecureTechnologies
Roland Hedberg - Independent Consul
Mike Jones - OIDF Secretary - Microsoft
Mark Haine - Open Banking
Dave Tonge - Moneyhub Enterprise - Getting rid of screen scraping
Don Thibeau - OIDF Executive Director
Ralph Bragg - Open Banking
Joseph Heenan - Authlete
John Bradley - OIDF Treasurer - Yubico
Freddie Guyera - Open Banking
 
* On the phone:
Bjorn Hjelm - MODRNA Working Group Chair - Verizon
Brian Campbell - Ping Identity
 

* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Adopted as is. 

UK Open Banking Status
==========================
General Status Report (Ralph)
-------------------------------------
Cooperation Update
 
Ralph:   Open Banking is working on setting up test suites for the FAPI specifications
Tony:    Does this include any certification testing in this framework?
Ralph:   No.  We are working towards that in the future, including establishing appropriate contracts and IPR
Tony:    Will you be requiring OpenID Certification?
Ralph:   Unless the request object is supported, all tests will fail
Roland: Supporting the request object should be easy to do
Tony:    To get the FAPI certification, you'll have to first get OpenID Connect certification
Ralph:   There are three ASPs creating their own OPs
Mark:    Mid-August and Mid-October are the key dates in the Open Banking plan
Ralph:   Open Banking can't mandate certification, but the banks have asked for it
              Competition and Markets (CMA) can mandate conformance

Mode of joint working and IPR Contribution (Ralph)
-------------------------------------------------------
Ralph:   The IPR has gone through legal review
Dave:    There are data schema requirements across Europe for PSD2
Joseph: The OpenID Foundation is sorting out the OpenID IPR issues
Ralph:   The standards used by Open Banking were the result of contributions by many parties
              There was no IPR agreement for these contributions
              Ralph would like a letter from FAPI about the IPR issues
              Getting a non-assert from all the contributors may be problematic
Don:      The OIDF will draft a letter to the trustee and others regarding our vision of licensing and adoption
John:     The IPR situation may be practically more comfortable for implementers in Europe than in other places
 

Certification test (Don/Mike)
==============================
Don:      It is expected that the contract to develop certification tests will be direct with Hans Zandbelt and not with the OIDF
              The OpenID Connect test suite will be updated to be able to support use of the request object
Mike:    We have updated the code in ways to enable adding new certification profiles
Roland: It would be a check box at configuration time to support use of the request object
John:     There may be issues about where the request objects are hosted
Mike:    The test suite already supports configuration time settings, such as whether encryption is supported
Ralph:   We use request objects by value - not by reference
Mike:    Any OpenID Certifications or use of the OpenID Certified mark must be under the auspices of the OpenID Foundation
Dave:    Open Banking should be a profile of FAPI
Ralph:   There may be exceptions.  For instance, not all banks will support Hybrid from day one
              We may not be supporting public clients from day one
Nat:      FAPI redirect_uris must be per-RP
Ralph:   Open Banking is publishing information on registering clients
Dave:    Do we want to enable configuring the same certification suite for both FAPI and Open Banking?
Mark:    There will be an end-stage where we allow for Open Banking peculiarities
Mike:    The OIDF believes that there should be one certification test code base
              It's fine for there to be additional tests not used for certifications, including those sponsored by Open Banking
Ralph:   That's Open Banking's view too.  That's what's in the MOU.  We don't want to own or maintain the code long-term.
Ralph:   One of the challenges will be establishing that the tests do what they need to do - testing the tests
Mark:    The banks will want assurances that the test suite does what it needs to do before they pay
Tony:    The current MOU doesn't provide for continuation.  That needs to be provided for in advance.
Mark:    Kim at Open Banking wants the conformance test suite in October.
              It sounds like there needs to be internal conversations on goals that drive timing of deliverables

Draft status and the future work plan
===============================================
Part 2 (Nat)
-----------------
Nat:      We are nearing the end of the 45-day review period for FAPI Part 2
              We have received a number of editorial comments
              Nat plans to apply those before the formal voting opens on Monday
              Brian Campbell also requested possible normative changes related to s_hash
Ralph:   The IAM vendors are already implementing FAPI as it stands
John:     The client an already integrity protect the state
              If you're implementing state properly, there's no requirement for s_hash
Mike:    It's fine to obtain Implementer's Draft status as specified and then make an update and produce another Implementer's Draft
John:     We should document what clients need to do to be secure nonetheless
Freddie: We have very little control over what clients are used
Mike:    We can use negative tests to verify that clients correctly implement security features
              Surely you must be able to place technical requirements on clients
Ralph:   Yes, PSD2 can motivate technical requirements
Freddie: Liability rests with the banks
John:     The advantage of s_hash is that you can construct a negative test for it
Brian:    My concern is that s_hash is not part of OpenID Connect and so will likely not exist in products
              We would likely add it at some point but maybe not on a timeline that meets the needs of our customers
Ralph:   We fully expect that there be elements of the FAPI specs that not all vendors will support on day one
              The compliance testing will help us flesh out what exceptions we may need to make in practice
Nat:      As working group chairman, I'll conclude from our discussions that we don't need to touch the current draft in this regard

CIBA (Dave)
--------------
Dave:    This came from the European movement towards APIs
              The work in MODRNA seems to support this interaction method
              FAPI could profile CIBA to bring it into line with the FAPI R/W spec
              Dave has created a FAPI profile of CIBA
              MODRNA supports polling and notification methods
              Dave focused on the notification method
              He is requesting feedback on the spec
              For instance, should a client be able to register for multiple methods?
John:     There are privacy implications of CIBA - how to create a pairwise identifier without a redirect_uri
              MODRNA is still dealing with this problem
              The GSMA isn't supporting polling for this reason
Torsten:Couldn't you solve this with a software statement?
John:     A federation operator might have to make statements on your behalf
John:     If we can solve the sector identifier problem, there isn't a reason for clients not to be able to use multiple methods
Dave:    The profile uses both FAPI Part 2 and CIBA
John:     Axel is still working on this
              Any client authentication method should be able to be used
John:     FAPI is using signed request objects
Dave:    Described the use of TLS mutual authentication
John:     Described the use of Proof-of-Possession request objects in the CIBA back channel
 
Ralph:   SCIM 2.0 is being used as the API to get information from the IdP
              We are using Software Statements
Tony:    Did you extend the SCIM schema?
Ralph:   We have created new fields and will register them in the IANA registry

Part 3, 4, 5 (Nat)
--------------------

PSD2 Trust Framework and friendly names (John/Ralph)
------------------------------------------------------
Ralph:   Trust Framework and Security Profile for Open Banking should be issued in the next few months

Large-Scale Federations
 
Mike:    Asked for Roland to comment on joint work that maybe should happen on federation aspects
Roland: There is a large-scale
Roland: There is a design meeting September 15th in Copenhagen
Roland: It makes extensive use of metadata statements
Ralph:   Has work been done with the UK Verify program?
              For instance, about claims used?
              We need to know the origin of the claims
Don:      GDS is a member of the FAPI working group
Nat:      Tom Jones is reading the OpenID Connect Federation specification

ISO/TC68 Submission (Nat)
----------------------------
Nat:      We have Class A liaison relationship with ISO TC 68
              This means that we could submit our work to ISO
              We haven't made any decisions about this yet
Mike:    This would be an OpenID Board decision as well as a working group decision
Nat:      We could obtain submitter status or the UK national body could submit if it's a UK standard
Mike:    Wouldn't we want there to be final OpenID specifications before submission to ISO?
Nat:      Yes
Nat:      The ISO process is a multi-year process
Dave:    ISO standards status will help with adoption, particularly in developing nations

External Orgs
================

FS-ISAC (Anoop/Nat)
--------------------
There was a FS-ISAC meeting yesterday. Nat and Dave joined the call. 
Nat explained the FAPI WG and Dave followed up with the European situation. 
It was very well received. They commented that there are not large difference between FAPI and DDA that they could probably adopt. 

Fintech Association Japan (Nat)
--------------------------------
Nat:      They are interested in the Open Banking work
              They are exploring the possibility of having a joint workshop in Japan
Freddie:It's a conversation we should have with Chris Maple
Don:      Kuppinger Cole wants to include FAPI content in their Singapore event in December

ISO/TC68 (Nat)
--------------------
Class A liaison established. 

Modrna
----------------------
* Tony:    How will FAPI and MODRNA integrate?
* John:     One possibility is the project by Orange, HSBC, and Barclays
              FAPI hasn't addressed what is necessary for banks to be relying parties
              That's something that FAPI should address in the future
              At the moment MODRNA only uses symmetric keys
              There are impedance mismatches
* Tony:    There's a mismatch that we need to address so we can enter the mobile banking space
* Don:      This is part of why we're doing pilots
* Dave:    GSMA is promoting this as a second factor
* Bjorn:    CIBA is based on banking use cases
              Talk with Nat about having more collaboration between FAPI and MODRNA

Others
------------
* Berlin Group (Dave)
* UK Open Banking (Dave)
* EBA Regulatory Technical Standards (Dave)
* NETS.eu (Dave)
* Apigee 


Events
================
OAuth WS on July 14, 15.

AOB
===========
Ralph:   EBA has taken a preliminary position against the use of screen scraping
Dave:    Screen scraping may be allowed as a fallback measure for a year

Next Call (Atlantic)
-----------------------
* See the group calendar. 

The meeting was adjourned at 24:04 UTC.