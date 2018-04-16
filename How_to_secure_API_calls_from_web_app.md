# How to secure API calls from web app to the server
First step: Set up the API to require authentication. The client must first authenticate itself via the server (or some other security server) for example asking the human user to provide the correct password.

Before authentication the calls to the API are not accepted.

During authentication a "token" is returned.

After authentication only API calls with the authentication "token" will be accepted.