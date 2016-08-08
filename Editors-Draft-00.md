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

The Client 

* shall use the RFC7636 with S256 as the code challenge method;  
* shall use separate and distinct Redirect URI for each Authorization Server that it talks to; 
* shall store the Redirect URI value in the User-Agent session and compare it with the Redirect URI that the Authorization Response was received at, where, if the URIs do not match, the Client shall terminate the process with error; 
* shall adhere to the best practice stated by [BCP NAPPS](https://tools.ietf.org/html/draft-ietf-oauth-native-apps-03); and 
* shall implement an effective CSRF protection. 

The Authorization Server 

* shall support RFC7636 with S265 as the code challenge method; 
* shall require exact match to the Redirect URI; 
* shall implement user authentication at LoA 2 or more; 
* shall issue a client secret longer than xxxxxx bytes; and 
* ... 

    Editor's Note: Requiring similar mechanism to PKCE to the Refresh and Access Token a good idea? 

### 5.3 Write Access

    Editor's Note: We have choice of Token Binding or POP. 

## 6. Using Tokens

### 6.1 Introduction

### 6.2 Read Only Access

### 6.3 Write Access

## 7. Resource APIs

## 8. Security Considerations

### 8.1 TLS Considerations

## 9. Privacy Considerations

## 10. Acknowledgement

## 11. References

## Annex A Financial Data API Level 1 (Normative) 
