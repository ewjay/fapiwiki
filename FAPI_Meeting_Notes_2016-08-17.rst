============================================
FAPI WG Meeting Notes (2016-08-17)
============================================
Date & Time: 2016-08-17 14:00 UTC (07:00 PDT, 16:00 Denmark, 23:00 JST) 

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum::
   :suffix: .


.. contents:: Agenda

Roll Call
=============
Nat Sakimura, Sascha Preibisch, Paul Grassi, Henrik Biering, Nov Matake, John Bradley. 
Regrets from Anoop and Edmund. 

Adoption of the Agenda
=========================
* adopted. 

Result of Document Restructuring -- Editor's Draft 00
===========================================================
Nat explained about the restructuring of the Working Draft clause by clause. 
Current state can be seen at: https://bitbucket.org/openid/fapi/wiki/Editors-Draft-00

Note that the section structures are according to the ISO Directive Part 2. 

    ASK: Please start reviewing the document and file bugs/proposals in the issue tracker. 

Sascha asked about the security of public client. 
Nat pointed out that it is covered in the requirements in 5.2.2. 

John pointed out that BCP NAPPS does not cover device attestation. 

Action:: 

    Add line about device attestation to 5.2.2.


External Org Relationships
=============================

UK Groups 
------------------------------------
Dave reported via email [1] that we may want to establish 
liaison relationship with the implementation entity [2]. 

    The participants agreed that we should do both, following Dave's advise. 

Action::

    * Nat to consult with Dave and follow up with both group

[1] <http://lists.openid.net/pipermail/openid-specs-fapi/2016-August/000036.html>

[2] Implementation Entity: <http://www.paymentsuk.org.uk/policy/payments-CMA-remedy-phase1/temporary>

TC68
-----
Nat reported the result of the meeting with Bank of Japan, which is the secretariat of the 
TC68 JP NB. TC68 is currently going under the reorganization. 
The proposal is to close SC4 and SC7 and create two new SCs "Reference Data SC" 
and "Information Exchange SC". Current SC2 "Security" will remain. 

As such, FAPI works will span multiple SCs and thus the liaison should be set up 
at the TC level, i.e., Category A Liaison. 

We were advised that the current secretary of TC is Ms. Janet Busch and format and FAPI WG should 
get in touch with her on this matter. 

    Participants agreed to proceed. 

Action::

    * Paul to provide the introduction to Janet. 
    * Nat to follow it up from there. 

[3] ISO/TC 68 Financial Services <http://www.iso.org/iso/iso_technical_committee?commid=49650>

X9
------------
Paul Grassi talked about a possible liaison with X9 [4] 

[4] X9 Financial Industry Standards <http://x9.org/>. 

X.9 AB23, CNP fraud. WG just started. 
Conversations turned towards security best practices. 
Deliverable is TR for best practice. 

    More detailed text will be provided by Paul on this issue. 

Significant interest from the WG in learning more about our work is there that they are going to talk 
about it next Tuesday again. We probably should set up a liaison relationship with them as well. 

John pointed out that they may be interested in Modrna work, Back channel authentication request, as well. 
This is essentially transaction authorization. 

Paul told that X.9 AB23 is looking at Fido about it as well. 
John pointed out that Modrna work is not only for phones but server to server as well, 
which is the difference to Fido. 

Paul also explained the problem of current online credit cared transactions that 
users a required to provide only the credit card number and CVV digits etc, 
which is not really an authentication. They are interested in finding solution 
for this problem. 

John pointed out that there is 3D secure for it, which has not been adopted widely due to usability issue and resultant customer drop outs. Nat pointed out that it probably is not a technical issue but the execution as Paypal, Amazon pay, etc. are similar to 3D secure, but they are successful. 

    Participants agreed that we should proactively send liaison request to X.9

Action::

    * Paul will make introduction to Janet. 
    * Nat to follow up from there. 

Danish Bank
------------
Henrik is still waiting the response from Danish Bank, who is a member of OBDG. 

Henrik then described the p2p, p2b payments in Denmark. 

Currently banks use Mastercard, Visa etc. for the purpose of p2p and p2b payment and is costing them a lot. 
Due to the financial authority's regulation, the amount possible to send are limited. 
Use of National eID will raise the limit. 

Danish banks wants to address these issues and for it, they need to find common API for direct payment. 
e.g., Mobile Pay that everybody would be able to, and that meets the PSD2 requirements. 

Action::

    Henrik will send some English documentations around it. 

Other action items
--------------------

    * Nat to draft liaison requests
    * Anoop to follow up with Intuit UK Team (Next week) 


New & Open Issues
======================

Nat went over recently updated issues. Specifically, #13, #23, #17, #20, #22, #16. 

#13: TLS 1.0 should be banned
    Participants agreed that at the minimum, TLS 1.2 should be required. 

#23: How do I find AccountID to use in transfer?
    Resolved by the Anoop's reply. 

#17: Incomplete sentence "In line with FFIEC (Federal Financial Institutions Examination Council) guidance on Authentication to mitigate security risks."
    Resolved by the ANoop's reply. 

#20: Meaning of the Surrogate Identifier Clause not clear
    Needs further discussion. Will be treated next week. 

#22: Undefined OAuth response parameter "user_id" appears in the text
     Needs further discussion. 

Action:: 

     All members were asked to review these issues. 

Error report coding (Sascha)
----------------------------------
Unfortunately, Sascha had to drop off just before getting to this topic, 
so we will cover it in the next call or the one after, and on the list. 


AOB
========

Next Call
----------
* 2016-08-23 23:00 UTC (16:00 PDT, 01:00+1d Denmark, 08:00+1d JST) 

Meeting was adjourned at 2016-08-17 15:00 UTC
