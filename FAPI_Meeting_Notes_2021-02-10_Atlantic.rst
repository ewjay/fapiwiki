============================================
FAPI WG Meeting Notes (2021-02-10) 
============================================
* Date & Time: 2020-02-10 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: 
* Regrets:
* Guest: 

Adoption of Agenda (Nat)
===========================
* 

External Organizations (Nat)
================================
W3C Web Payment Interest Group (John)
--------------------------------------
* OIDF’s interest in becoming a member as part of WPSIG’s re-charter. OIDF board EC is asking FAPI WG if they are interested to participate in their meeting. 
* OIDF opportunity to co-sponsor: An opportunity to be a co-chair. 


Australia Data 61 (Dima/Stuart)
----------------------------------
* Still in the process of organization of agenda and timing for workshop. 
* THe workshop will be very open. 
* Suggestions to contents, guests, etc. welcome. Send it to director@OIDF.org
* It will be OIDF workshop in collaboration with other organizations. 

Canada (Ralph)
------------------

UK (Chris/Ralph)
-----------------
There are a number of TPPs lobbying CIBA to regulators to support e-commerce and POS. 


Brazil (Chris/Ralph)
----------------------
n/a

Berlin Group (Francis)
---------------------------
Lots of activities on new operations on extended services -- regulated directory to identify the participants. 

Japan (Nat)
--------------------
n/a

Events (Nat)
======================
OBIE Extended Customer Attributes Events
--------------------------------------------
Feb. 10 Morning. 
Mark and Torsten will be speaking. 

Berlin Group Workshop
----------------------------
* 
* 


1st call of GOFCoE WG
------------------------
* Gavin Littlejohn setting up a new WG. 
* Coordinate identity in UK
* Curate different standards globally. 

KuppingerCole Event on March 3
------------------------------------
* https://www.kuppingercole.com/events/identity-fabrics-future-proofing-iam
* March 3. 
* On FAPI 2.0 and FAPI 1.0 differences

Hypermedia login API (Travis)
================================
Travis spencer will be presenting Hypermedia login API. 

* http://lists.openid.net/pipermail/openid-specs-fapi/2021-February/002259.html
* https://developer.curity.io/docs/latest/developer-guide/haapi/example-username.html

Justin pointed out perils of UI hints but ... 

* https://datatracker.ietf.org/doc/agenda-interim-2021-gnap-02-gnap-01/

FAPI 1.0 Updates (Nat)
===================================
* 

FAQ and Roadmap Updates (Dave)
==================================
FAQ
-----
Current draft: https://docs.google.com/document/d/1Fo44L_wM4TIMxF3f1xowNWdlqEqZkZdjAyd1pAtab9U/edit

No updates for this week. 

FAPI 2.0 Release communication
------------------------------------
Short document that refers to FAQ
Don to draft first cut?
Feb 3. 

FAPI 2.0 Baseline
------------------------------------
* FAPI Baseline 2.0: Just pending the release communication. 
* the working group last call - 27th Jan to 3rd Feb
* first public draft for the vote - 17th February
* implementers draft approval - 3rd April (45 days after vote starts)

FAPI 2.0 Signing
------------------------------------
Call for adoption: TBC, Nat to consult with Dave

FAPI 2.0 Advanced
------------------------------------
first implementers draft: dependent on signing

Grant management
------------------------------------
* Call for adoption: mid-February
* A dedicated call for the presentation of grant management to WG: 17th February 14:00 GMT
* Working group last call: end July
* First public comments: Aug 1 - Sept 15


FAPI 2.0 Updates (Daniel)
===========================
* https://bitbucket.org/openid/fapi/issues?status=new&status=open&component=FAPI2%3A%20Baseline
* Almost ready. Pending the release communication completion. 
* Nat will as Don to take the lead in the release communication. 

Grant Management (Dima)
============================
Still going through the data model. 
It should be ready for the presentation to the working group in two to three weeks. 

E



PRs (Dave)
========================
No time. 

Issues
=====================
No time. 

AOB
==========================
n/a

The meeting was adjourned at 15:00 UTC.


Chat Log
============
Me to Everyone
https://bitbucket.org/openid/fapi/wiki/FAPI_Meeting_Notes_2021-02-10_Atlantic

23:17Don Thibeau to Everyone
please note some new items re Financial-Grade APIs at https://openid.net/

23:20Don Thibeau to Everyone
FYI Yesterday Janet Yellen Treasury Seciretary gave the keymote at the U.S. Financial Sector Innovation Policy Roundtable panelists stressed the importance of the adoption of the OpenID Foundation Financial-Grade APIs for international open banking, US health care and of course OpenID Connect was noted as a given.

23:21Ralph Bragg to Everyone
That's a big one

23:21Ralph Bragg to Everyone
Nice

23:21Chris Michael to Everyone
Apologies for being late

23:28Justin Richer to Everyone
Can someone post a link to this flow diagram, please?

23:32Justin Richer to Everyone
q+

23:32Justin Richer to Everyone
(do we not queue on chat?)

23:32Dave Tonge to Everyone
ok (you next :-))

23:33Justin Richer to Everyone
I genuinely don't know :)

23:33Dave Tonge to Everyone
https://developer.curity.io/docs/latest/developer-guide/haapi/example-username.html

23:40Justin Richer to Everyone
https://datatracker.ietf.org/doc/agenda-interim-2021-gnap-02-gnap-01/

23:43Michael Schwartz to Everyone
Also, Hypermedia API is compatible with OAuth, while GNAP does not see this as a necessity constraint?

23:43Justin Richer to Everyone
I disagree with that statement.

23:44Michael Schwartz to Everyone
It wasn't a statement, it was a question.

23:44Justin Richer to Everyone
OAuth is not constrained by "hypermedia API" concepts at all. GNAP is being built explicitly on HTTP and JSON to start, and so could be more aligned. Neither are driven by it though.

23:54Travis Spencer (Curity) to Everyone
I'll add a nicely formatted version of the diagram on my web site later today, Justin, but a badly formatted one is on the mailing list.

23:57Ralph Bragg to Everyone
just copy the language from the OBIE.

23:57Ralph Bragg to Everyone
It has all of that in the website. i.e this is self provided, self managed and don't take any responsibiliyr or are not promoting it.