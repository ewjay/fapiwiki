===========================================

FAPI WG Meeting Notes (2018-10-16) 

===========================================

Date & Time: 2018-10-16 23:00 UTC

Location: GoToMeeting https://global.gotomeeting.com/join/321819862

.. sectnum:: 
   :suffix: .


.. contents:: Agenda

The meeting was called to order at 23:__ UTC. 

Roll Call
===========
* Attending:  Nat, Bjorn, Ed and Anoop
* Guests: 
* Regrets: 

Adoption of the Agenda (Anoop)
==================================
*  As is (no change)

Data Schema (Anoop)
======================
* Discuss the difference between data/schema DDA and Open Banking APIs
* Only deposit account type is supported. (no credit card, loan/LOC and investment).
* Both specs have list query as a first starting point.
* DDA

* * Details give all account details
* * Balances are current balance & available balances
* * Transactions as separate call includes pending
* * Pagination is supported
* * All accounts details and transaction.
* * PFM focus

* Open Banking
* * Separate calls to get balance and many balances available.
* * Other information Beneficiaries, direct debits, standing orders and product (Not in DDA)
* * Product calls gives detail about the type of account (DDA is included as part of detail call).
* * Transactions as a separate call. Also, support of multiple accounts belongs to one customer in one call. (may be ok if one account type it is challenging when it goes with different account type.
* * Standing order (pending transactions) is separate call but in DDA it is included as part of transactions call.
* * Pagination is supported
* * Transactional focus

* Investment schema 
* * NRI proposal needs to be reviewed and follow up discussion with NRI [ Anoop to review and compare NRI schema & DDA schema for investment. ]

External Organization
========================
* India (RBI - Reserve bank of India) directive 
* * https://www.rbi.org.in/Scripts/BS_ViewMasDirections.aspx?id=10598
* * swagger proposal:  http://swagger-ui.rebit.org.in/?url=https://api.rebit.org.in/assets/specifications/NBFC-AA-Service.yaml#/
===========

Next Call
-----------------------
Next call will be an Atlantic Call. 

* The meeting was adjourned at 23:__ UTC.