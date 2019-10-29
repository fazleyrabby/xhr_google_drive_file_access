
SOURCE : https://stackoverflow.com/questions/32076503/using-postman-to-access-oauth-2-0-google-apis

Postman will query Google API impersonating a Web Application
Generate an OAuth 2.0 token:

Ensure that the Google APIs are enabled
Create an OAuth 2.0 client ID

Go to Google Console -> API -> OAuth consent screen
Add getpostman.com to the Authorized domains. Click Save.
Go to Google Console -> API -> Credentials
Click 'Create credentials' -> OAuth client ID -> Web application
Name: 'getpostman'
Authorized redirect URIs: https://www.getpostman.com/oauth2/callback
Copy the generated Client ID and Client secret fields for later use
In Postman select Authorization tab and select "OAuth 2.0" type. Click 'Get New Access Token'

Fill the GET NEW ACCESS TOKEN form as following

Token Name: 'Google OAuth getpostman'
Grant Type: 'Authorization Code'
Callback URL: https://www.getpostman.com/oauth2/callback
Auth URL: https://accounts.google.com/o/oauth2/auth
Access Token URL: https://accounts.google.com/o/oauth2/token
Client ID: Client ID generated in the step 2 (e.g., '123456789012-abracadabra1234546789blablabla12.apps.googleusercontent.com')
Client Secret: Client secret generated in the step 2 (e.g., 'ABRACADABRAus1ZMGHvq9R-L')
Scope: see the Google docs for the required OAuth scope (e.g., https://www.googleapis.com/auth/cloud-platform)
State: Empty
Client Authentication: "Send as Basic Auth header"
Click 'Request Token' and 'Use Token'
Set the method, parameters, and body of your request according to the Google docs
