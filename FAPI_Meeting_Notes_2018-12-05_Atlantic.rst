============================================
FAPI WG Meeting Notes (2018-12-05) 
============================================
Date & Time: 2018-12-05 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call
===========
* Attending:　
    * Nat, Bjorn, Brian, Chris WOod, Dave, Freddi Gyara, Joseph, Torsten

* Guests: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Added the discussion on two clients using a same key in AOB. 

CIBA Progress Report (Brian/Dave/Bjorn)
============================================
* No outstanding issues
* The split on-going. 
* Added privacy considerations for different types of identifiers which can be used in core spec, not just FAPI

External Organizations
==========================

Australia (Ralph)
-------------------

UK Open Banking (Ralph)
-----------------------------
* Published ver. 3.1 last week. 
* It was approved by steering group and available in OB's confluence site.
* Have authority from Steering group to start thinking about 4.0 API and what parts will be mandatory. In process of gathering info from Interop sources. 
* One key feedback from API Evaluation Group is what areas API should be covering and will be taken into consideration for next version.
* Security profile which adopts FAPI R/W profile have been adopted but dates for adoption by banks are not set.
* Should be next few weeks but nothing publicly stated.

Berling Group (Torsten)
----------------------------
* Meeting tomorrow and the day after. Torsten will be there. 
* For last 1.03 version, Torsten contributed some enhancements to OAuth section based on Dave's security analysis of OB and Berlin group's specs. Added text for security checks recommended for security BCP.
* Berlin group did not add contributions even though it has promised to do so and there have been no proposals for collaboration from Berlin.
* Torsten pointed out problems in SCA model of initiating payment within authorization process, but was ignored. 
* Vulnerable to session fixation attacks which was solved in Oauth 1.0a. Solution is to use Access token to trigger payment. 
* BG considers Using access token to initiate payment a premium service. 
* Not just OAuth flow impacted, but also proprietary redirect based flows and embedded mode.
* Torsten will ask when they will conduct security analysis.

* EBA published guidelines around  ASPSP will get exemption from stopping screen scrapping. 
* ASPSP can't  ask for consent /approval. Can only do authentication.
* Not allowed to replay the request for which account you're giving access to and this is the payment you're initiating. 
* Supposed to happen only at TPP side. Will send referenced section to mailing list. 
* Makes for easier session fixation attack.
* Financial industry regulating something is good. Puts legal entity under competent authority. 
* But not looking for technical solution but legal solution for problem of screen scraping. 
* Established regulative umbrella, but increases costs and processes for TPPS.
* UK may do OB mode and PSD2 mode. OB mode has easier onboarding to attract more Fintechs. 
* But will still need to be compliant to PSD2 and need to be SCA authorized in home state.
* Some countries are more strict in regulations so will face different burdens. Companies will go to countries with less strict regulations.


Issues
==================

* Following issues were discussed. For the details, see the tickets. 
* #193 : Part 2, Section 5.2.2.: remove response type "code id_token token". Spec doesn't allow "id_token token" so "code id_token token" should  also beremove.

* #190 : aud (& iss?) should be mandatory in requests objects
* iss  in this context is the client_id so will be redundant
* aud must be present
* aud being optional in OIDCC is a bug that should be raised to OIDCC, and the consensus was we should make it mandatory in FAPI.
* Consensus is that both should be mandatory
* Freddi to do consistency check with OB spec


Pull Requests
==================
* Merged the following pull request 
* pull request #82 (issue #191), 
* pull request #83 (issue #176), 
* pull request #81 (spelling for american english)
* pull request #78 (issue #195) 



AOB
======================
Discussion on two clients using a same key on MTLS(Joseph)
-----------------------------------------------------------

* Allowing same cert to be used, under reasonable conditions make sense
* Joseph described case where applications really should be treated as different, so shouldn't do it
* If cert of a private key from R/W app is exported to Read-only app, the library relies on R/W app
* If TPP host 2 applications,  1 widely used app and 1 naughty development app. If  someone manages to steal an access token from the popular properly secured cient, then he could use in naughty one.
 

Next Call
-----------------------

* The meeting was adjourned at 14:59 UTC.