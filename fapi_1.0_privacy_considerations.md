# 9. Privacy considerations

## 9.1 General
Each implementation should consider performing a Privacy Impact Assessment and produce the PIA Report. 
ISO/IEC 29134 provides a valuable resource for conducting PIA and the production of the PIA Report. 
Readers are highly recommended to make use of it. 

In what follows, some information that can be utilized during PIA is listed. 
The list is limited to only those that are related to the protocol transactions and does not include 
other aspects of the processing. 

## 9.2 Consent and choice

When obtaining user consent, the system should adhere to the requirements set forth in ISO/IEC 29184. 

## 9.3 Purpose legitimacy and specification

Organizations shall specify the purpose of the processing of the personal data involved in the system.  

Organizations shall determine the legal basis of the processing of the personal data involved in the FAPI transactions. 

For the specification, refer to ISO/IEC 29184. 

## 9.4 Collection limitation

A client should minimize the claims that it requests in the authorization request for the stated purpose. 

## 9.5 Data minimization

A client should minimize the claims that it requests to the resource server to what is strictly necessary for the particular processing. Obtaining larger dataset and filtering at the client shall not be permitted. 

## 9.6 Use, retention and disclosure limitation

When claims related to the subject are returned in the ID Token in the front channel, implementations should consider encrypting the ID Token to lower the risk of personal information disclosure.

## 9.7 Accuracy and quality

## 9.8 Openness, transparency and notice

## 9.9 Individual participation and access

## 9.10 Accountability

## 9.11 Information security

## 9.12 Privacy compliance

Organizations shall identify the requirements set forth by relevant privacy regulations 
that are relevant to this system and check regularly that the system fulfils the requirements. 

Organizations shall test the conformance to the requirements that it has set 
as part of the privacy risk assessment process.