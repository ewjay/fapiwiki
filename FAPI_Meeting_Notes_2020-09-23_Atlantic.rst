============================================
FAPI WG Meeting Notes (2020-09-23) 
============================================
Date & Time: 2020-09-23 14:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .
https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-23_Atlantic

.. contents:: Agenda

The meeting was called to order at 14:__ UTC. 

Roll Call 
===========
* Attending:
  
  * Dave Tonge
  * Dima Postnikov
  * Don Thibeau
  * Francis Pouatcha
  * Joseph Heenan
  * Mark Haine
  * Nat Sakimura
  * Ralph Bragg
  * Stuart Low
  * Takahiko Kawasaki
  * Andrew Latham
  * Brian Campbell
  * Kosuke Koiwai (KDDI)


* Regrets: 
* Guest: 

Adoption of Agenda (Nat)
===========================
* Events
* External Organizations
* OB Signature
* Pull requests
* Issues
* WG FAPI Last call

Events 
======================
FDX Dev-Con Global Summit (Don)
---------------------------------
* Don to follow up with practical path forward for both FDX and OIDF
* 2 other items to follow up

  1) FDX members webinar about global interoperability
  2) OIDF workshop 10/28/20 will have keybnote slot for panel discussion about FDX standards and FAPI WG
    * Panelists : Nat Sakimura, John Cardinal, Anoop 

There were a question about compliance verification versus reference implementation and using one to test the other.
Ideally should have more than one reference implementation and make them freely available instead of anointing one particular vendor's reference implementation.

Need multiple implementations to thrash out differences in interpretation of the specification.

FDX approach is more towards bilateral agreements between Fintech and holder TPP.
Trying to avoid central directory or endorsement of some sort of directory.

If FDX wants to make changes, should start with FAPI Baseline and then make suggestions to WG instead of creating a new spec and make it conform to FAPI.

Still early phase.

Will FDX adopt FAPI profiles?
Formal adoption of FAPI will be challenging. Leaning towards learning and leveraging.
They have different business model from an organizational POV in a different certification program.
Will certify for uses cases rather than deployments.
FDX has no regulatory driver only volunteer orgs.
Still need to get an compliant/conformant strategy, certification program together, use cases, etc...
FDX intends to use FAPI but how to use, certify, and build it into their stack is still unanswered.

Depends if they will be a standards body or an implementation entity.
If Implementation, will need support from the vendors to implement whatever standard is created.
If standards body, they don't want to publish a standard no one can implement.


Francis's presentation is available on the mailing list.



External Organizations
========================
Australia (Dima/Stuart)
------------------------
Ping's Australian sandboxes are now FAPI certified and listed on the certifications page.
There is a question regarding whether the certification page should show which profiles are being conformed to.
Please provide feedback to certification team.

Berlin Group (Francis)
------------------------
Contacted by Swiss market forehead and taking FAPI approach
Waiting for 2.0 version for next year.

European Commission (Mark/Torsten)
------------------------------------
Sent out comments to EC. 

ETSI (Ralph)
-------------
Contact Ralph for provide feedback to Sonic specification, .

Would like to know if there is still a problem with b64 critic flag and libraries that are honoring it. Would like ETSI to require it so libraries can be fixed.

UK (Dave)
---------------------
EBA recently told  all issuers of 2 TSP based tickets across Europe, they're going to ask them to strike off an issued certificates given to British TPPs .British TPP could lose the EIDas certificates on Jan 1. Legislation requires banks to accept other certificates that British TPPs may no longer be able to get.


PRs for 1.0 (Dave)
====================

pull request #193 - Update purpose of the profile in the introduction
   * no objections


Some spelling editorial changes

Some security considerations were added to Part 2, will copy to Part 1 when finalized.

Ralph wants some feedback regarding the text around consent authorization on what participants should do when and why. There has been pushback in Europe against banks displaying consent or authorization screens during redirects.
The authorization request is not considered to be legal consent.
If customer is not present and consent only exists with TPP, if bank is allowed to help secure the system and help customers understand what data they are releasing, are we undermining the security or authorization process?

Should be good practice for banks since they're not collecting information. Let's users be aware that their information is being requested.

Ralph wants new text in highlighting the role in improving privacy for the AS. Add text in the privacy considerations to point out good practices to display notices when data is shared by the AS.

This seems like double consent (consent at TPP and consent at Bank) but it's actually consent at TPP and authorization at Bank.

Current legislation requires Bank to authenticate only (no authorization step).

Dave will create a new issue for this.


issue #317 - interaction with PAR , need some text clarification



AOB
==========================


The meeting was adjourned at 15:03 UTC.