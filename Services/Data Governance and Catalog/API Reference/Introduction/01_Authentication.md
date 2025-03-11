# Authentication

Before you make REST API calls, you must authenticate yourself with JWT authentication. First, use the Login API with your organization user name and password to receive the session ID and org ID. Then, use the session ID and org ID to generate a JSON Web (JW) token. Subsequently, you use the session ID and JW token to secure your API calls without having to authenticate yourself for each call.

### Obtain the session ID

To get a session ID, use the Login API V1. The Login API is also available with SAML. For more information about logging in using SAML, see the REST API Reference in the Administrator help. Ensure that you have your Informatica Intelligent Cloud Services user name and password.

Send the POST request with the following URI, header, and request body:

| URI | <LoginURL>/identity-service/api/v1/Login |
|-----|------------------------------------------|
| | Note that <LoginURL> is the Informatica Intelligent Cloud Services login URL based on the region, such as https://dm-**us**.informaticacloud.com, https://dm-**em**.informaticacloud.com, https://dm-**ap**.informaticacloud.com, https://dm-**uk**.informaticacloud.com, and so on. |
| Header | Content-Type: application/json |
| Request Body | {<br>     "username": "<your_IICS_user>",<br>     "password": "<your_IICS_password>",<br>} |

The response generates the session ID and the org ID. Note the value of the sessionId field to include in the subsequent API call.

### Generate a JW Access Token

Use the value from the sessionId field that you obtained from the previous Login API response, and send the POST request with the following URL and headers to generate a JW access token:

| URI | <LoginURL>/identity-service/api/v1/jwt/Token?client_id=idmc_api&nonce=1234 |
|-----|-------------------------------------------------------------------|
| | Note that <LoginURL> is the Informatica Intelligent Cloud Services login URL based on the region, such as https://dm-**us**.informaticacloud.com, https://dm-**em**.informaticacloud.com, https://dm-**ap**.informaticacloud.com, https://dm-**uk**.informaticacloud.com, and so on. |
| Headers | - cookie: USER_SESSION=<sessionId value> <br>- IDS-SESSION-ID: <sessionId value> |

The response generates the JW access token that you include in the authorization header for all subsequent API calls. The access token expires after 30 minutes from the initial grant of the token. You must regenerate the access token after every 30 minutes to authenticate your API calls.
