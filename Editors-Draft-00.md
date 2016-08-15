#Financial Services – Financial API - Part 1: Read Only APIs

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



#**Financial Services – Financial API - Part 1: Read Only APIs **

[TOC]

## 1. Scope

The goal of FAPI is to provide JSON data schemas, security and privacy recommendations and protocols to:

* enable applications to utilize the data stored in the financial account,
* enable applications to interact with the financial account, and
* enable users to control the security and privacy settings.

Both commercial and investment banking account as well as insurance, and credit card accounts are to be considered.

This document defines 

* security profiles for and OAuth and OpenID Connect; 
* JSON format to represent account related data, e.g., Account Representation, Transactions, Current Status; 
* REST API for the accounts, Purchase history of commerce site, and Receipt Data

for a read only access. 

## 2. Normative references
The following referenced documents are indispensable for the application of this document. For dated references, only the edition cited applied. For undated references, the latest edition of the referenced document (including any amendments) applies.

RFC 6749 - The OAuth 2.0 Authorization Framework

RFC 7636 - Proof Key for Code Exchange by OAuth Public Clients

RFC 5246 - The Transport Layer Security (TLS) Protocol Version 1.2

RFC 7525 - Recommendations for Secure Use of Transport Layer Security (TLS) and Datagram Transport Layer Security (DTLS)

RFC 6125 - Representation and Verification of Domain-Based Application Service Identity within Internet Public Key Infrastructure Using X.509 (PKIX) Certificates in the Context of Transport Layer Security (TLS)

BCP NAPPS - [OAuth 2.0 for Native Apps](https://tools.ietf.org/html/draft-ietf-oauth-native-apps-03)

OIDC OpenID Connect Core 1.0 incorporating errata set 1

OIDD OpenID Connect Discovery 1.0 incorporating errata set 1

OIDM OAuth 2.0 Multiple Response Type Encoding Practices

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


### 5.2 Read Only Access Provisions

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


## 6. Accessing Protected Resources (Using tokens)

### 6.1 Introduction

The FAPI endpoints are OAuth 2.0 protected resource endpoints that return various financial information for the resource owner assoicated with the submitted Acccess Token. 

### 6.2 Read only access provisions 

#### 6.2.1 Protected resources provisions

The protected resources supporting this document 

* shall mandate TLS 1.2 as defined in [RFC5246] or later with the usage following the best practice in [RFC7525]; 
* shall support the use of the HTTP GET and HTTP POST methods defined in RFC2616 [RFC2616]; 
* shall accept access tokens in the HTTP header as in Section 2.1 of OAuth 2.0 Bearer Token Usage [RFC6750];  
* shall verify that the access token is not expired nor revoked; 
* shall verify that the scope associated with the access token authorizes the reading of the resource it is representing; 
* shall identify the associated user to the access token;  
* shall only return the resource identified by the combination of the user implicit in the access and the granted scope and otherwise return errors as in section 3.1 of [RFC6750]; 
* shall encode the response in UTF-8; // DDA allows client to ask for charset but restricting may be better for interoperability
* shall send the `Content-type` HTTP header `Content-Type: application/json; charset=UTF-8`;  
* shall send the server date in HTTP date header as in section 14.18 of [RFC2616];  
* shall send the `DDA-InteractionId` with the value set to the one received from the client in the `DDA-InteractionId` request header or a unique value created by the server if there was no corresponding request header to track the interaction, e.g., `DDA-InteractionId: c770aef3-6784-41f7-8e0e-ff5f97bddb3a`; and 
* shall log the value of `DDA-InteractionId` in the log entry. 


    NOTE: While this document does not specify the exact method to find out the user associated with the 
    access token and the granted scope, the protected resource can use OAuth Token Introspection [RFC7662]. 

Further, it 
 
* should support the use of Cross Origin Resource Sharing (CORS) [CORS] and or other methods as appropriate to enable Java Script Clients to access the endpoint; 

### 6.2.2 Client provisions

The client supporting this document 

* shall use TLS 1.2 as defined in [RFC5246] or later with the usage following the best practice in [RFC7525]; 
* shall send access tokens in the HTTP header as in Section 2.1 of OAuth 2.0 Bearer Token Usage [RFC6750];   
* shall send `User-Agent` header that identifies the client, e.g., `User-Agent: Intuit/1.2.3 Mint/4.3.1`; and 
* shall send `DDA-FinancialId` whose value is the unique identifier of the desired financial institution to interact assigned by the service beureau where the API is provided by a service bureau which uses the same end point for multiple institutions. 

    **NOTE**: Conceptually, the value of the DDA-FinancialID corresponds to `iss` in the ID Token 
    but is not required to be an https URI. It often is the routing number of the FI. 

Further, the client 

* can optionally supply the `sub` value associated with the customer with the `DDA-CustomerId` request header, e.g., `DDA-CustomerId: a237cb74-61c9-4319-9fc5-ff5812778d6b`; 
* can optionally supply the last time the customer logged into the client in the `DDA-CustomerLastLoggedTime` header where the value is supllied as ** w3c date **, e.g., `DDA-CustomerLastLoggedTime: Tue, 11 Sep 2012 19:43:31 UTC`; and 
* can supply the customer’s IP address if this data is available or applicable in the `DDA-CustomerIPAdress` header, e.g., `DDA-CustomerIPAdress: 198.51.100.119`; and 
* may send the `DDA-InteractionId` request header to the server to help correlate log entries between client
and server, e.g., `DDA-InteractionId: c770aef3-6784-41f7-8e0e-ff5f97bddb3a`. 


### 6.2.3 Open access resource provisions



## 7. Resource APIs

### 7.1 Introduction

This document specifies resources in two categories: 

* open acess resources; 
* protected resources; 

Open access resources does not require authorization to read them out. 
This document defines the following open acess resources: 

* Branch location
* ATM location
* Offered products list
* Offered product

Protected resources require the access token as defined above to read them out. 
This document defines the following protected resources: 

* customer; 
* account; 
* transaction; 
* transfer; 
* statement; 
* capability; 

### 7.2 Branch location

### 7.3 ATM location

### 7.4 Offered products list

### 7.5 Offered product

### 7.6 Customer

### 7.7 Account
### 7.8 Transaction
### 7.9 Transfer
### 7.10 Statement
### 7.11 Capability





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

* Open Financial Exchange 2.2
* “HTML 4.01 Specification,” World Wide Web Consortium Recommendation REC-html401-19991224, December 1999
* [RFC7662] OAuth 2.0 Token Introspection



## Annex A Financial Data API Level 1 (Normative)



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

