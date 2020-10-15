<img src = "https://cdn.auth0.com/blog/cookies-vs-tokens/cookie-token-auth.png">

# Cookie-Based Authentication
     
     * Cookie-based authentication has been the default, tried-and-true method for handling user authentication for a long time.
     * Cookie-based authentication is stateful.
     * This means that an authentication record or session must be kept both server and client-side. 
     * The server needs to keep track of active sessions in a database, while on the front-end a cookie is created that holds a session identifier, thus the name cookie based authentication. 
     
# The flow of traditional cookie-based authentication:
   
    * User enters their login credentials.
    * Server verifies the credentials are correct and creates a session which is then stored in a database.
    * A cookie with the session ID is placed in the users browser.
    * On subsequent requests, the session ID is verified against the database and if valid the request processed.
    * Once a user logs out of the app, the session is destroyed both client-side and server-side.

# Token-based authentication

    * Token-based authentication is stateless. 
    * The server does not keep a record of which users are logged in or which JWTs have been issued. 
    * Instead, every request to the server is accompanied by a token which the server uses to verify the authenticity of the request.
    *  The token is generally sent as an addition Authorization header in the form of Bearer {JWT}, but can additionally be sent in the body of a POST request or even as a query parameter. 

# The flow of token-based authentication: 


    * User enters their login credentials.
    * Server verifies the credentials are correct and returns a signed token.
    * This token is stored client-side, most commonly in local storage - but can be stored in session storage or a cookie as well.
    * Subsequent requests to server include this token as additional Authorization header or through one of the other methods mentioned above.
    * The server decodes the JWT and if the token is valid processes the request.
    * Once a user logs out, the token is destroyed client-side, no interaction with the server is necessary.



<img src = "https://miro.medium.com/max/1250/0*q4BbSrVFfpbiJPDQ.png">