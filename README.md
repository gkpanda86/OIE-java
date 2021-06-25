# OIE-java
The project connects to Okta usingthe SDK and exposes operations as REST service to be consumed by SPAs or mobile apps.
Most of the SDK interactions is in AuthServiceImpl.

To handle multi step authentication and registration process and still be able to perform using REST operations, 
the application stores the proceed context for the operations in session and returns the session id to client apps in response header X-Auth-Token.
The client have to send the session id back in request header to continue with the interaction.
