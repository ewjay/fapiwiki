# Additional Code Challenge Methods

code_challenge_method = "PS256" / "ES256"

# PS256 method

## Parameters

code-verifier = BASE64URL-ENCODE(PS256(code))

code_challenge = BASE64URL-ENCODE(JWK)

## Verification

AS MUST calculate BASE64URL-ENCODE(PS256(code))
from the received code_challange and compare it with code-verifier. 
If it does not exactly match, it MUST return an error. 

# ES256 method

## Parameters

code-verifier = BASE64URL-ENCODE(ES256(code))

code_challenge = BASE64URL-ENCODE(JWK)

## Verification

AS MUST calculate BASE64URL-ENCODE(ES256(code))
from the received code_challange and compare it with code-verifier. 
If it does not exactly match, it MUST return an error.