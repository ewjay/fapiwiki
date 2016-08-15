#Financial Services – Financial API

## Warning

This document is not an OIDF International Standard. It is distributed for review and comment. It is subject to change without notice and may not be referred to as an International Standard.

Recipients of this draft are invited to submit, with their comments, notification of any relevant patent rights of which they are aware and to provide supporting documentation.

## Copyright notice
The OpenID Foundation (OIDF) grants to any Contributor, developer, implementer, or other interested party a non-exclusive, royalty free, worldwide copyright license to reproduce, prepare derivative works from, distribute, perform and display, this Implementers Draft or Final Specification solely for the purposes of (i) developing specifications, and (ii) implementing Implementers Drafts and Final Specifications based on such documents, provided that attribution be made to the OIDF as the source of the material, but that such attribution does not indicate an endorsement by the OIDF.

The technology described in this specification was made available from contributions from various sources, including members of the OpenID Foundation and others. Although the OpenID Foundation has taken steps to help ensure that the technology is available for distribution, it takes no position regarding the validity or scope of any intellectual property or other rights that might be claimed to pertain to the implementation or use of the technology described in this specification or the extent to which any license under such rights might or might not be available; neither does it represent that it has made any independent effort to identify any such rights. The OpenID Foundation and the contributors to this specification make no (and hereby expressly disclaim any) warranties (express, implied, or otherwise), including implied warranties of merchantability, non-infringement, fitness for a particular purpose, or title, related to this specification, and the entire risk as to implementing this specification is assumed by the implementer. The OpenID Intellectual Property Rights policy requires contributors to offer a patent promise not to assert certain patent claims against other contributors and against implementers. The OpenID Foundation invites any interested party to bring to its attention any copyrights, patents, patent applications, or other proprietary rights that may cover technology that may be required to practice this specification.



##Foreword

OIDF (OpenID Foundation) is an international standardizing body comprised by over 160 participating entities (working group participants). The work of preparing international standards is carried out through OIDF working groups according to OpenID Process. Each participants interested in a subject for which a working group has been established has the right to be represented on that working group. International organizations, governmental and non-governmental, in liaison with OIDF, also take part in the work. OIDF collaborates closely with other standardizing bodies in the related fields.

International standards are drafted in accordance with the rules given in the OpenID Process.

The main task of working group is to prepare Implementers Draft and Final Draft. Final Draft adopted by the Working Group through consensus are circulated to the OIDF members for voting. Publication as an OIDF Standard requires approval by at least 50 % of the member bodies casting a vote.

Attention is drawn to the possibility that some of the elements of this document may be the subject of patent rights. OIDF shall not be held responsible for identifying any or all such patent rights.

 Financial API consists of the following parts, under the general title Financial Services — Financial API:


##Introduction

In many cases, Fintech services such as aggregation services uses screen scraping and stores user passwords. This model is both brittle and insecure. To cope with the brittleness, it should utilize an API model with structured data and to cope with insecurity, it should utilize a token model such as OAuth [RFC6749, RFC6750].

This working group aims to rectify the situation by developing a REST/JSON model protected by OAuth. Specifically, the FAPI WG aims to provide JSON data schemas, security and privacy recommendations and protocols to:

* enable applications to utilize the data stored in the financial account,
* enable applications to interact with the financial account, and
* enable users to control the security and privacy settings.

Both commercial and investment banking account as well as insurance, and credit card accounts are to be considered.



#**Financial Services – Financial API**

[TOC]

## 1. Scope
**// TODO**

The goal of FAPI is to provide JSON data schemas, security and privacy recommendations and protocols to:

* enable applications to utilize the data stored in the financial account,
* enable applications to interact with the financial account, and
* enable users to control the security and privacy settings.

Both commercial and investment banking account as well as insurance, and credit card accounts are to be considered.

The group will define

* security profiles for OpenID Connect and OAuth,
* JSON format to represent account related data, e.g., Account Representation, Transactions, Current Status,
* REST API for the accounts,Purchase history of commerce site, and Receipt Data

Out of scope:

* Web Payment (will refer the W3C Web Payment WG product if needed.)
* Write Scope

## 2. Normative references
The following referenced documents are indispensable for the application of this document. For dated references, only the edition cited applied. For undated references, the latest edition of the referenced document (including any amendments) applies.

RFC 6749 - The OAuth 2.0 Authorization Framework

RFC 7636 - Proof Key for Code Exchange by OAuth Public Clients

RFC 5246 - The Transport Layer Security (TLS) Protocol Version 1.2

RFC 7525 - Recommendations for Secure Use of Transport Layer Security (TLS) and Datagram Transport Layer Security (DTLS)

RFC 6125 - Representation and Verification of Domain-Based Application Service Identity within Internet Public Key Infrastructure Using X.509 (PKIX) Certificates in the Context of Transport Layer Security (TLS)

BCP NAPPS - [OAuth 2.0 for Native Apps](https://tools.ietf.org/html/draft-ietf-oauth-native-apps-03)

OpenID Connect Core 1.0 incorporating errata set 1

OpenID Connect Discovery 1.0 incorporating errata set 1

OAuth 2.0 Multiple Response Type Encoding Practices

Open Financial Exchange 2.2

“HTML 4.01 Specification,” World Wide Web Consortium Recommendation REC-html401-19991224, December 1999



## 3. Terms and definitions
For the purpose of this standard, the terms defined in RFC6749, RFC6750, RFC7636, OpenID Connect Core applies.


## 4. Symbols and Abbreviated terms

API – Application Programming Interface

CSRF - Cross Site Request Forgery

FAPI - Financial API

FI – Financial Institution

HTTP – Hyper Text Transfer Protocol

REST – Representational State Transfer

TLS – Transport Layer Security

## 5. Getting Tokens

### 5.1 Introduction

The OIDF Financial API (FAPI) is a REST API that provides JSON data representing accounts and transactions related data. These APIs are protected by the OAuth 2.0 Authorization Framework that consists of [RFC6749], [RFC6750], [RFC7636], ..., and other specifications.

These API accesses have several levels of risks associated to it. Read only access is generally speaking associated with lower financial risk than the write access. As such, the characteristics required to the tokens are also different.

In the following subclauses, the method to obtain tokens are explained separately.


### 5.2 Read Only Access

Read Only Access typically is the lower risk scenario compared to the Write access, so the protection level can also be lower. However, since the FAPI would provide potentially sensitive information, it requires more protection level than a basic [RFC6749] requires.

As a profile of The OAuth 2.0 Authorization Framework, this specification mandates the following to the Read Only API of the FAPI.

#### 5.2.1 Authorization Server 

The Authorization Server

* shall support both public and confidential clients; 
* shall provide client secret longer than 12 characters; 
* shall support RFC7636 with S265 as the code challenge method;
* shall require Redirect URIs to be pre-registered; 
* shall required `redirect_uri` parameter in the authorization request; 
* shall require the value of `redirect_uri` to exactly match one of the pre-registered Redirect URI;  
* shall require user authentication at LoA 2 as defined in [X.1254] or more; 
* shall require explicit consent by the user to authorized the requested scope if it has not been previously authorized; and 
* shall verify that the Authorization Code has not been previously used if possible.  

    NOTE: Section 4.1.3 of [RFC6749] does not say anything about the `code` reuse, but this document is putting limitation on it as per Section 3.1.3.2 of [OIDC]. 

    NOTE: If replay identification of the authorization code is not possible, it is desirable to make the validity period of the authorization code very short. 

Further, if it wishes to provide the authenticated user's identifier to the client in the token response, the authorization server 

* shall support the authentication request as in Section 3.1.2.1 of [OIDC]; 
* shall perform the authentication request verification as in Section 3.1.2.2 of [OIDC]; 
* shall authenticate the user as in Section 3.1.2.2 and 3.1.2.3 of [OIDC]; 
* shall provide the authentication response as in Section 3.1.2.4 and 3.1.2.5 of [OIDC] depending on the outcome of the authentication; 
* shall perform the token request verification as in Section 3.1.3.2 of [OIDC]; and 
* shall issue an ID Token in the token response when `openid` was included in the requested `scope` 
  as in Section 3.1.3.3 of [OIDC] with its `sub` value equal to the value of the `CustomerId` 
  of the `Cusotmer` object corresponding to the authenticated user 
  and optional `acr` value in ID Token. 

    NOTE: [DDA] returns a parameter called `user_id` in the token response. 
    The value of `user_id` is identical to the value of `CustomerId` member of the `Customer` object. 

    Editor's Note: Requiring similar mechanism to PKCE to the Refresh and Access Token a good idea?

    Editor's Note 2: If `user_id` is indeed required in the token response of DDA, then, we should require OIDC. 

#### 5.2.2 Public Client

A Public Client

* shall suport [RFC7636]; 
* shall use the [RFC7636] with S256 as the code challenge method;
* shall use separate and distinct Redirect URI for each Authorization Server that it talks to;
* shall store the Redirect URI value in the User-Agent session and compare it with the Redirect URI that the Authorization Response was received at, where, if the URIs do not match, the Client shall terminate the process with error;
* shall adhere to the best practice stated by [BCP NAPPS](https://tools.ietf.org/html/draft-ietf-oauth-native-apps-03); and 
* shall implement an effective CSRF protection. 

Further, if it wishes to obtain a persistent identifier of the authenticated user, it 

* shall include `openid` in the `scope` value; and 
* shall include `nonce` parameter defined in Section 3.1.2.1 of [OIDC] in the authentication request.  

    NOTE: Adherance to [RFC7636] means that the token request includes `code_verifier` parameter in the request. 


#### 5.2.3 Confidential Client

In addition to the provision to the Public Client, the Confidential Client 

* shall authentciate with client secret to access the Token Endpoint as in Section 4.1.3 of OAuth 2.0 [RFC6749]; 



#### 5.2.3 Authorization Endpoint
The Authorization Endpoint is used in the same manner defined in Section 3.1.2 of OpenID Connect 1.0, with the exception of the differences specified in this section.

#### 5.2.3.1 Authentication Request
Authentication Requests are made as defined in Section 3.1.2.1, except that these Authentication Request parameters are used as follows:

* *response_type* REQUIRED. The value shall be set to `code`(Code Flow) or `code id_token`(Hybrid Flow). It is RECOMMENDED to use the value `code id_token` (Hybrid Flow) as defined in [OAuth 2.0 Multiple Response Type Encoding Practices]. This ensures that the Authorization Code correlates to the end user and the current session at the Financial Institution's Authorization Server provided that ID Token validation and authorization code validation are performed as described in section 3.3.2.9 and 3.3.2.10 of OpenID Connect 1.0.
* *scope* REQUIRED. The value shall be contain the values `openid` and `offline_access`. This allows the client to obtain authorization for an access token that can be used while the user is offline.
* *redirect_uri* REQUIRED. The value shall be unique for each Authorization Server for public clients.
* *state* REQUIRED.
* *nonce* REQUIRED.
* *prompt* REQUIRED. The value shall contain `consent` to request that Authorization Server perform user authentication and obtain explicit authorization for the client to read financial data.
* *acr_values* REQUIRED. The value shall be set to values that indicate an authentication context of LOA 2 or higher.

Public clients shall use RFC7636 - Proof Key for Code Exchange by OAuth Public Clients to mitigate authorization code interception. As such, a public client shall follow the protocol as defined in RFC7636. The public client shall create a Code Verifier. A Code Challenge shall be created using *S256* as the method. The following paremeters are added to the authentication request:

* *code_challenge* REQUIRED. The code challenge.
* *code_challenge_method* REQUIRED. The value shall be `S256`.

#### 5.2.3.2 Authentication Request Validation
The Authentication Request is validated in the same manner as for the Authorization Code Flow, as defined in Section 3.1.2.2 of OpenID Connect 1.0.

If the Authentication Request contains a *code_challenge* value and the *code_challenge_method* parameter value is not set to *S256*, an error is returned as defined in 4.4.1 of RFC7636.

#### 5.2.3.2 Successful Authentication Response

Authentication Responses are made in the same manner as for the Code Flow, as defined in Section 3.1.2.5 or Hybrid Flow as defined in 3.3.2.5 of OpenID Connect 1.0.

If the Authentication Request contains a *code_challenge* value, the Authorization Server shall follow section 4.4 of RFC7636 for associating an Authorization Code with a Code Challenge value.

#### 5.2.3.3 Authentication Response Validation
Authentication Responses are validated in the same manner as for the Code Flow, as defined in Section 3.1.2.7 or Hybrid Flow as defined in 3.3.2.8 of OpenID Connect 1.0.

#### 5.2.3.4 Token Endpoint

The Token Endpoint is used in the same manner as for the Authorization Code Flow, as defined in Section 3.1.3 of OpenID Connect 1.0, with the exception of the differences specified in this section.

For public clients, the following parameters are added to the Token request:

* *code_verifier*. REQUiRED. The Code Verifier generated in the Authentication Request.


#### 5.2.3.5 Token Request Validation

Token Requests are validated in as defined in Section 3.1.3.2 of OpenID Connect 1.0 except for the differences specified in this section.

If the Authorization Code has a Code Challenge and Code Challenge Method associated with it, the Authorization Server validates the *code_verifier* value as according to 4.6 of RFC7636.


#### 5.2.3.6 Token Response

Token Responses are made in the same manner as for the Authorization Code Flow, as defined in Section 3.1.3.3. of OpenID Connect 1.0.

#### 5.2.3.7 Token Response Validation
When using the Hybrid Flow, Token Responses are validated in the same manner as for the Authorization Code Flow, as defined in Section 3.1.3.5 of OpenID Connect 1.0.


### 5.3 Write Access

    Editor's Note: We have choice of Token Binding or POP?

####　5.3.1 Public Client

In addition to the provisions stated in the Read Access case, the systems that implements FAPI shall satisfy the following provisions:

* Each message shall be source authenticated;
* Each message shall be tamper evident;
* Each message shall be transmitted through encrypted channel or shall be encrypted otherwise;
* Each message shall be replay detectable;
* The Client shall include the intended interaction endpoints identifiers in the request;
* The Server shall attest that the endpoints in the Client intension is legitimate and return errors otherwise;

#### 5.3.2 Confidential Client

## 6. Using Tokens

### 6.1 Introduction

The FAPI endpoints are OAuth 2.0 protected resource endpoints that return various financial information for the resource owner assoicated with the submitted Acccess Token.

Communication with the FAPI Endpoint MUST utilize TLS 1.2 or later.

The FAPI Endpoints MUST support the use of the HTTP GET and HTTP POST methods defined in RFC 2616 [RFC2616].

The FAPI Endpoints MUST accept Access Tokens as OAuth 2.0 Bearer Token Usage [RFC6750].

The FAPI Endpoint SHOULD support the use of Cross Origin Resource Sharing (CORS) [CORS] and or other methods as appropriate to enable Java Script Clients to access the endpoint.

### 6.2 Read Only Access

### 6.3 Write Access

## 7. Resource APIs

## 8. Data Model

## 8. Message Serializations

Messages are serialized using one of the methods as described in section 13 of OpenID Connect 1.0.

## 9. Security Considerations

### 9.1 TLS Considerations
Since confidential information is being exchanged, all interactions shall be encrypted with TLS/SSL (HTTPS) in accordance with the recommendations in RFC 7525. TLS version 1.2 or later shall be used for all communications.

## 10. Privacy Considerations

### 10.1 Residual Data
Residual data is data that is no longer being used, for example if an account has been closed. Clients should delete residual data from their systems within 180 days.


## 11. Acknowledgement

## 12. Bibliography

## Annex A Financial Data API Level 1 (Normative)


## Parking Lot

     Do we need these? Is it not just repeating what is in OAuth or OpenID Connect? 

## 5.2 Access Overview
Financial API uses the OpenID Connect 1.0 protocol for authentication and authorization.

The Financial API client needs the following information to successfully interact with a Financial API server:

1. OpenID Authorization Server
    1. Authorization endpoint, e.g. https://oauth.example.com/authorization
    2. Client identifier, e.g. intuit.com
    3. Requested scope ("accounts", "customer", "images", "transfer", "transactions")
    4. Client Redirection Endpoint, e.g. https://oauth.intuit.com/client
    5. Token Endpoint, e.g. https://oauth.example.com/token
    6. Client Authentication Method and Client credentials (JWT or shared secret)
    7. Optional client authentication certificate
    8. Authorization Server Certifying Authority public key chain
2. Financial API Service (OAuth resource server)
    1. Endpoint, e.g. https://data.example.com
    2. Client authorization (Bearer or MAC token)
    3. (Optional) Client authentication certificate. Use mutual authentication for access by the client agents in addition to the refresh or access token.
    4. Resource Server Certifying Authority public key chain. Client will need to make sure server SSL certificate CA is in their trust store.

The full details of how a Financial API client obtain an OAuth Access Token are covered in Section 3.1.2 of OpenID Connect Core 1.0. The following steps summarize the method on how to obtain an access token from a Financial Institution Authorization Server and its usage.

1. The end user starts a Client application on the web or on a device.
2. The client application authenticates the end user.
3. The client application prompts the end user for information regarding the Financial Institution.
4. The client application may optionally perform discovery via OpenID Connect Discovery 1.0 to otain the Financial Institution's authorization, token, and resource endpoints if they are unknown.
5. The client constructs an Authorization request to the Financial Institution's Authorization Endpoint.
6. The client redirects the end user to the Authorization Endpoint with the request parameters.
7. The Authorization Server authenticates the end user and obtains authorization from the end user for the client application.
8. The Authorization Server sends the authorization response back to the client's *redirect\_uri* endpoint.
9. The client validates the response.
10. The client extracts the authorization code.
11. The authorization code is submitted to Authorization Server's Token Endpoint to get an Access Token.
12. Use the Access Token to access protected Financial API endpoints.
13. Store the Refresh Token for fetching a new Access Token once the current Access Token expires.


### 5.2.1 Financial API Scopes
The Financial API allows access to the user's private financial information while the user is offline. To obtain consent and authorization for an access token and refresh token that can be used while the user is offline, the authorization request shall contain the `openid` and `offline_access` values in the `scope` parameter. A refresh token will be returned in the authorization response that can be exchanged for an access token as described in Section 12 of OpenID Connect Core 1.0.

The Financial API client application shall include a list of desired scopes when requesting an Access Token. The following scopes are defined for Financial API data service:

| Resource       | Allowed Actions                                              | Scope          |
|----------------|--------------------------------------------------------------|----------------------|
| Account        | Read only Access to summary account information              | FinancialInformation |
| Customer       | Read only Access to customer information, including PII      | FinancialInformation |
| Image          | Read only Access to transaction images (checks and receipts) | FinancialInformation |
| Statement      | Read only Access to statement image                          | FinancialInformation |
| Transaction    | Read only Access to transaction information                  | FinancialInformation |
| Transfer       | Transfer of money between accounts                           | Transfer             |

The Financial API server will return the list of allowed scopes with the issued Access Token in the authorization server.

The Financial API server may limit the scopes for the purpose of not implementing certain APIs.

The Financial API server may also present scopes in the access confirmation page after end-user login to have them determine each account(s) access for the requesting application.

