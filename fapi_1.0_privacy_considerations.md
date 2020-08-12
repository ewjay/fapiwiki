# 9. Privacy considerations

## 9.1 General
Each implementation should consider performing a Privacy Impact Assessment and produce the PIA Report. 
ISO/IEC 29134 provides a valuable resource for conducting PIA and the production of the PIA Report. 
Readers are highly recommended to make use of it. 

In what follows, some information that can be utilized during PIA is listed. 
The list is limited to only those that are related to the protocol transactions and does not include 
other aspects of the processing. 

## 9.2 Client registration

In many cases, the organization operating the authorization server 
will be providing PII as parts of FAPi based transactions. 
In such cases, at the time of the client registration, the authorization server 
should obtain enough amount of client-related metadata to determine if the client is operated by a trustworthy party that adheres to the privacy notice and terms and conditions that 
the client presents to PII principals. The metadata shall also include enough metadata 
to present to the PII principal so that the PII principal can determine who is involved in the transaction.

The organization that operates the authorization server shall determine and document the legal basis for the transfer of PII to each registered client.   

## 9.3 Sending authorization requests

Authorization requests in many cases request some PII. 
In such cases, the client shall create a privacy notice following the guidance given in ISO/IEC 29184. 

NOTE: ISO/IEC 29184 requires the determination and documentation of the legal basis, purpose specification, etc. 

If the legal basis is consent, then it shall obtain the consent before making the authorization request. 
The organization providing the client should follow the guidance given in ISO/IEC 29184. 

The authorization request should request only the claims that are needed for the purpose of the processing of PII. 

## 9.4 Authorization server upon receiving the authorization request

If the legal basis for the transfer of PII at the authorization server was consent, the authorization server shall obtain the consent from the PII principal after having authenticated the PII principal. 
The organization should follow the guidance given in ISO/IEC 29184. 

If the legal basis for the transfer was not consent, the authorization server may skip the consent screen. However, it shall make sure that the privacy notice has been provided to the PII principal before proceeding with the transaction. The privacy notice should follow the guidance given in ISO/IEC 29184. 

## 9.5 Authrorization response

When claims related to the subject are returned in the ID Token in the front channel, implementations should consider encrypting the ID Token to lower the risk of personal information disclosure. This is needed to adhere to the disclosure limitation principle of ISO/IEC 29100. 

## 9.6 Resource request

When the client makes a resource request, the client should minimize the claims requested to adhere to the data minimization principle of ISO/IEC 29100. 

To adhere to the retention limitation principle and "accuracy and quality" principle of ISO/IEC 29100, the client should minimize the duration that it retains the PII and obtain potentially updated PII from the resource server whenever possible and appropriate. 

## 9.7 Resource response

When the resource server responds to the request, 

a) it shall ensure that the authorization has not been revoked; 
b) it shall not provide more claims than requested to adhere to the disclosure limitation principle of ISO/IEC 29100. 

## 9.8 Openness, transparency and notice

Organizations shall provide notices that adhere to ISO/IEC 29184 to the public so that 

a) the PII principal can always refer to it; 
b) other parties can always refer to it to check if it is legitimate; 

## 9.9 Individual participation and access

The client shall provide a way to access one's own PII stored in the client or by the organization that operates the client. It shall provide a way to correct or delete PII as needed by the PII principal. 

## 9.10 Accountability

Organizations shall collect and retain the log data so that 

a) organization can explain what has happened to the PII; and  
b) third-parties can verify the explanation given in a). 

## 9.11 Information security

Organizations should test their implementations against the conformance test suite that tests the conformance to this document. If a security non-conformance was detected, it shall rectify it as soon as possible. 

Organizations should implement an information security management system for their systems. 

## 9.12 Privacy compliance

Organizations shall identify the requirements set forth by relevant privacy regulations 
that are relevant to this system and check regularly that the system fulfils the requirements. 

Organizations shall test the conformance to the requirements that it has set 
as part of the privacy risk assessment process.