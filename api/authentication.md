# Authentication

The api is a REST based API that uses a Bearer token Authorization.

Each API endpoint for Users and Approvals requires an Authorization header containing the Bearer access token. Calls to endpoints without a valid token will result in a 401 Unauthorized http status code.

An access token is obtained by calling the /api/authentication/GetToken using the ClientId and ClientSecret for a registered account.

This access token is a JWT token with an expiry date. It is recommended that your implementation gets a new access token before the expiry otherwise calls to the API will result in a 401 Unauthorized https code.

Once the access token is obtained this is used for all subsequent calls to the other available API endpoints.

