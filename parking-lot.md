this is a parking lot for the text excluded from the editor's draft. 

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

