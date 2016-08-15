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

