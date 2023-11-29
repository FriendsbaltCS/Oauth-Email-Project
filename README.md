# OAuth Email Project

In this project, you will use your knowledge of the OAuth protocol to obtain
an access token for a user account and use it to send an email.

## Creating an Application

Using the Google Cloud Console, make sure that you have an application created
with access to the GMail API and to which you can add the correct GMail scopes
(you'll need to do some research to figure out which these are). Within this
application, create a new set of credentials for a Web Application. Then, add
to the list of allowed redirects the URL `https://acs.quakerlabs.org/lessons/oauth/redirect/`.
Finally, download and save the client secrets json file.

## Obtaining an Access Token

The point of this project is to _use_ access tokens rather than obtaining them. Hence,
we will not be implementing a complete flow through the project's code. However, you
will still need to obtain an access token for _some_ user account. To do this, you
will need to construct and visit the correct authorization url. You can do this using
the tool on MyFriends. Make sure to use `https://acs.quakerlabs.org/lessons/oauth/redirect/`
as the redirect uri.

Once you log into your google account and approve the authorization request, you will
be redirected to the quakerlabs.org page displaying your authorization code. Use curl
to post this to the token endpoint to obtain your access token. You can also use the
tool on MyFriends to create your POST request.
