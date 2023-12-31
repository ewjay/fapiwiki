============================================
FAPI WG Meeting Notes (2018-09-12) 
============================================
Date & Time: 2018-09-12 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call
===========
* Attending: Nat, Dave, Bjorn, Brian, Chris Wood, Glyn, Joseph, Torsten, Daniel Fett, Rob Otto, Barry O'Donohoe, 
* Guests: 
* Regrets: 

Adoption of the Agenda (Nat)
==================================
* Security Document Comparison (Dave) added. 

CIBA Progress Report (Brian/Dave)
=====================================
* Now weekly meeting. 
* Substantial consensus. 
* Pull requests. Pull, Ping, and Push modes. 
* It should be done by the end of October (Core) for implementer's draft. 
* Then FAPI profile, a simple one. (Only push). 
* No CME9 plan to implement it for March, 2019. 
* No specific time. 
* login hint token might be Open Banking specific as it is likely to be eco-system specific. 
* SEC Event Token may be related. Generic subject identifier there. 

Test Harness (Joseph)
======================
* Test harness is now complete with the automation so that it can be used for CICD.  
* Banks have to re-certify in the next two weeks, and re-certify every 6 months going on. 
* List of all the test are best pulled out from test logs. 

External Organizations
==========================

Open Banking UK (Ralph)
---------------------------
* Nothing significant. (Barry)
* Last week officially approved ver. 3 of Open Banking Spec., that removed OB specific changes. 

Security Profile Comparison (Dave)
-------------------------------------
After the meeting with STET and Berlin group, Dave decided to come up with the security comparison of each protocol so that we will be able to see what are the diffs and what needs to be done to align more closely. 
During the process, Dave found a substantial attack vector to Berlin group draft. 

The draft is still private but has progressed substantially so that it can be shared among people who are interested to review the document. To do so, please write to Dave. 

Dave is also trying to list what portion of the current conformance suite can be used by STET and Berlin Group. 

Torsten, who has already seen the draft, pointed out that we should have threat models explained in the document so that people will understand what needs to be looked at. 

The end state of the document is still open to discussion. Some suggestion made were to publish it as WG Technical Report or as a FAPI Wiki page. 

Issues (Nat)
=================
Part 2 Related Issues
----------------------------
* https://bitbucket.org/openid/fapi/issues?status=new&status=open&component=Part%202%3A%20RW%20Security

Issues #171, #172, #173 were dealt with. Please refer to the tickets for the details. 

We were not able to reach part 1 issues and CIBA related issues by the end of the call. 
These are going to be dealt with in the mailing list, etc. 

* Part 1 Related Issues:  https://bitbucket.org/openid/fapi/issues?status=new&status=open&component=Part%201%3A%20RO%20Security

* CIBA Related Issues : https://bitbucket.org/openid/fapi/issues?status=new&status=open&component=CIBA

AOB
===========


Next Call
-----------------------
Next Pacific call will go as scheduled. 

* The meeting was adjourned at 15:03 UTC.