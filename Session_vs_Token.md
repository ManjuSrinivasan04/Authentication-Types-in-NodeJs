Session vs Token Based Authentication

# Session Based Authentication
     * In the session based authentication, the server will create a session for the user after the user logs in.
     * The session id is then stored on a cookie on the user’s browser. 
     * While the user stays logged in, the cookie would be sent along with every subsequent request. 
     * The server can then compare the session id stored on the cookie against the session information stored in the memory to verify user’s identity and sends response with the corresponding state!
     
<img src = "https://miro.medium.com/max/875/1*Hg1gUTXN5E3Nrku0jWCRow.png">

# Token Based Authentication

    * In the token based application, the server creates JWT with a secret and sends the JWT to the client. 
    * The client stores the JWT (usually in local storage) and includes JWT in the header with every request. 
    * The server would then validate the JWT with every request from the client and sends response.
    * The biggest difference here is that the user’s state is not stored on the server, as the state is stored inside the token on the client side instead.

<img src = "https://miro.medium.com/max/875/1*PDry-Wb8JRquwnikIbJOJQ.png">


# Scalability
    
    * Session based authentication:
       
      -> Because the sessions are stored in the server’s memory, scaling becomes an issue when there is a huge number of users using the system at once.
    
    * Token based authentication: 
        
        -> There is no issue with scaling because token is stored on the client side.

# Multiple Device
    
    * Session based authentication: 
      
      -> Cookies normally work on a single domain or subdomains and they are normally disabled by browser if they work cross-domain (3rd party cookies). 
      -> It poses issues when APIs are served from a different domain to mobile and web devices.
   
    * Token based authentication: 
    
      -> There is no issue with cookies as the JWT is included in the request header.
       