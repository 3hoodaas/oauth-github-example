# oauth-github-example
Assignment
OAuth with GitHub Implementation of OAuth 
in GitHub application.


Steps:

1- Create new application in GitHub.com.
2- Coding at Visual Studio Code, built by using HTML with CSS formatting and JavaScript.

How the code work?

1-User redirect to request their GitHub identity when click sign in button. 
GitHub application decide parameter for logging with specific account to be saved for user sign in to authorize your OAuth app.

Most important parameter 

Client_id —> user gain after register an OAuth app in GitHub.com.

redirect_uri —> optional. 
By default in GitHub it redirect users to the callback URL configured in the OAuth Application settings. 

login —> Give suggestions to the user to sign in with specific account to authorize the app.

scope —> a method to limit an application’s access to the user’s account.
The application may request one or more scopes, this information is then presented to user in the consent screen and the access token issued to the application will be limited to the scopes granted.
Example, if a user has already performed the web flow twice and has authorized one token with user scope and another token with repo scope, a third web flow that does not provide a scope will receive a token with user and repo scope.

state -> Give protection from cross site request forgery attacks.

allow-signup —> the unauthenticated user get an signup offer for GitHub during OAuth flow.




2-Users are redirected back to your site by GitHub


When user approve your request, GitHub redirects back to your site with a temporary code parameter as well as the state you provided in the previous step in a state parameter. 

Note: Temporary code expiring after 10 mins.

In condition that the states not match, So a third party created the request, and you should abort this process.


client_id —> ID received from GitHub for OAuth App.

client_secret —> ID received from GitHub for OAuth App.

code —> code received as a response to Step 1.


redirect_uri —>URL at my application where users are sent after authorization.


Response “Token” 
ex —>access_token=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&scope=&token_type=bearer



3. Use the access token to access the API

The access token allows you to make requests to the API on a behalf of a user.


