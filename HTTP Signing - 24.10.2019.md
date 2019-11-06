This was an ad hoc meeting held on 24.10.2019

## Roll Call ##
Dave, Anders, Mike, Brian, Joseph, Justin, Manu, Mark, Ralph, Torsten, Annabelle

## FAPI & HTTP Signing ##

We discussed why the FAPI WG was interested in standards around HTTP Signing and the initial document that we have started:

https://bitbucket.org/openid/fapi/src/master/Financial_API_HTTP_Signing.md
 
## Short introductions to the various solutions: ##

### Annabelle (https://docs.aws.amazon.com/general/latest/gr/sigv4_signing.html) ###

AWS relies on HTTP request signing for caller authentication.
Current version is: https://docs.aws.amazon.com/general/latest/gr/sigv4_signing.html
Most people use AWS provided SDKs, but there is enough information to implement libraries.
Algorithm for serialising headers, method, request body
Slide deck from IETF 105
AWS has been doing this for a long time, even before TLS had wide adoption, even now is used without TLS in some scenarios.
Also needed integrity protection as couldn’t rely on TLS
Unlikely to be single end-to-end TLS connection, so needed it to be at application level

Q. How wide is library support beyond AWS SDKs. 
A. Amazon publishes SDKs for large number of languages, but not aware of third party libraries

Q. Does Amazon want to standardise?
A. There is some interest, especially for situations where systems aren’t just speaking to AWS

### Manu (https://tools.ietf.org/html/draft-cavage-http-signatures-12) ###

Many of AWS requirements are the same as those driving draft-cavage.

Started many years ago when Mark Cavage was at Amazon

Digital Bazaar were looking at it for the work at W3C.

Needed to support XML, JSON, and other formats - in a multi-hop environment, that didn’t use bearer tokens.

Supposed to be a simple base layer, that other specs can build from.
22 Implementations of the spec
https://github.com/w3c-dvcg/http-signatures/issues/1

Test suite available to check conformance
Currently working with implementers to improve conformance
Project has lots of activity and the spec has been improved over time based on feedback
Used by quite a few financial APIs.
Close to finalising the spec, but the spec is already very mature.

Q. Do you have an IETF WG willing to finish it
A. Discussions with HTTP WG. 

There was discussion about the difficulty of taking an already developed standard for "rubber stamping" by a standards group.

### Anders (https://cyberphone.github.io/doc/research/fapi-signed-https-2019-10-16.pdf) ###

Presentation at IETF104
Serialisable requests is a core feature
Individual submission to IETF

### Ralph - JWTs (including detached payload)

UK Banks wanted to use JWS due to widespread libraries
Same method been used by Australia
Open Banking has a full conformance suite.

ETSI will publish a “signatures for JSON” standard that will use JWS. 
Polish API will support both draft-cavage and JWS.

### Mike (https://tools.ietf.org/html/draft-fett-oauth-dpop and) ###

Two things happening under OAuth WG.
DPoP has come out of the OAuth security work groups. We needed a proof of possession method not tied to the transport layer. 
Usable from a JavaScript application.
It is an HTTP signing method, but it signs very little by default, but this can be extended by profiles.

Request to get it adopted by the OAuth WG.

### Justin (https://tools.ietf.org/html/draft-ietf-oauth-signed-http-request) ###
Microsoft is using this internally.
Draft currently expired, but there are few implementations.
Built for situations where you can’t guarantee that the HTTP request won’t be mangled. 
Allows you to selectively sign different parts of the HTTP request. Designed around presenting a bound OAuth access token.

Q. Does the spec require access tokens?
A. The use-case it was designed for was OAuth access tokens, but could work without.

Key feature is robustness when HTTP requests are "mangled"
  
## Discussion and next steps

There was discussion around the fact that “draft-cavage” uses the Authorization header makes it incompatible with OAuth 2.

The FAPI WG will continue to advance its document about HTTP Signing and hopes that discussion around the various standards can continue on the list and in subsequent calls.