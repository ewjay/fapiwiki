============================================
FAPI WG Meeting Notes (2020-11-25) 
============================================
* Date & Time: 2020-11-25 14:00 UTC
* Location: GoToMeeting https://global.gotomeeting.com/join/321819862
* Note URI: https://bitbucket.org/openid/fapi/wiki/edit/FAPI_Meeting_Notes_2020-09-30_Atlantic

.. sectnum:: 
   :suffix: .

.. contents:: Agenda

The meeting was called to order at 14:05 UTC. 

Roll Call 
===========
* Attending: Dave, Kosuke, Dexter, Brian, Ralph, Dima, Nat, Joseph, Daniel, 

* Regrets: 
* Guest: 

Adoption of Agenda
===========================

FAPI 2.0 Issues



FAPI 2.0 Issues
======================

# 343 - what is authenticity and integrity of the redirect URI?

* redirect_uri in PAR has priority since the request is signed
* no requirement for redirect_uri in authorization request, but if provided, but it’s safe to override pre-registered ones.
* if one one redict_uri is registered, then parameter is not required
Can have 3 options

  * Traditional behavior which doesn’t have same variability as PAR
  * Leave it open
  * Prescribe behavior if redirect_uri is provided

* The question is whether AS must support not pre-registered redirect_uris when using PAR.
* The consensus is to allow this behavior but not require it.
* Dexter stated that error messages are lacking, thus making client development difficult.
* Many banks have policies of not telling you what’s wrong beyond absolute minimum.
* FAPI 2.0 will go along with PAR error handling but the WG members are in favor of more error information. Brian and Joseph to take up the issue in PAR draft.
* Resolution: first part shall require the redirect_uri in the authorization request with note stating that with PAR redirect_uri in tha authorization request and the first authorization request might differ from registered redirect_uris with reference to PAR section.

# 346 - RAR requirement may be unnecessary?

* RAR might not be needed for simpler use cases and  AS can signal no support by not publishing metadata supporting RAR.
* Brian : Requiring RAR support might be too complex and overreaching.
* Mandate RAR if you need rich request and if you don’t need rich request, don’t mandate RAR.
* Banks doing complex consent using the existing model of lodge intent will be non-compliant.
* Change to “should use RAR if you need rich authorization request”

#345 - it's okay if a refresh token can be guessed?

* Brian proposed text with “sufficient entropy” but Daniel suggested to change to “128 bits of entropy” according to RFC6749

# 349 - authorization code replay

* Agreed to use text from FAPI 1.0

#282 - FAPI 2.0: x-fapi-* headers

* FAPI headers might be useful on requests to the resources where RS are doing transaction and data risk analysis by evaluating metadata to make security decisions.
* Still to be discussed.



The meeting was adjourned at 15:00 UTC.