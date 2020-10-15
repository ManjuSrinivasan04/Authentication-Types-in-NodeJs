# Consider the following authentication Methods:

    # Session Based Authentication
    # Token Based Authentication
    # Passwordless Authentication
    # Roll your own authentication
    # Delegate to a third party service


# Our Server/Api:

    Requirements:
         -> NodeJS have to be installed. Visit NodeJS.org to install 
         -> Mongodb 
         -> Any command line environment (i.e Terminal, iTerm, cmd, powershell, git bash e.t.c)
         -> A text editor - Visual Studio code


# I. Session Based Authentication

    * In session based authentication, users credentials(username/email and password for example) are compared with what is stored in the database and if they match, a session is initialized for the user with the fetched id. 
    * These sessions are terminated on user logout and they are meant to expire after a configured time.
 
    <img src = "https://res.cloudinary.com/practicaldev/image/fetch/s--jzM6Wq6e--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://cdn-images-1.medium.com/max/800/0%2AP5OxJMihg0S0jyqk.png">


# II. Token-Based Authentication
     
    * Here comes token based authentication that means the server will response with a generated token on user login which will save in client instead of storing in the server to use for the further request.
    * On each client request the token need to pass with the header which will verify in the server to serve data. 
    * The thought is much simpler, once you logged in just request with a valid token to get data on each request. 
    * Token authentication requires users to obtain a computer-generated code (or token) before they’re granted network entry. 
    * Token authentication is typically used in conjunction with password authentication for an added layer of security. 
    * This is what we refer to as two-factor authentication (2FA). 
    * That means even if an attacker successfully implements a brute force attack to take out any password in place, they’ll have to also bypass the token authentication layer. 
    * Without access to the token, gaining access to the network becomes increasingly difficult. 
    * This additional layer discourages attackers and can save networks from potentially disastrous breaches.
 
             
            >> Different types of NodeJS token-based authentication:
                  
                -> Passport
                -> JSON Web Tokens (JWT)
                -> Bcrypt 


      ## Passport 
          
            => Passport is an authentication middleware for Node.js. 
            => Passport describes itself as being a simple, unobtrusive authentication solution for Node.js.
            => Passport is a small framework that implements many different “providers”. 
            => There are tons of open source providers you can use with Passport to help authenticate users in a variety of ways.
            => Passport.js exclusively handles user authentication, meaning that things like user authorization, password reset workflows, etc., all require custom development to function.

         <img src = "https://www.ctl.io/developers/assets/images/blog/auth%204.png">
     
     ## Json Web Token

           => JWT is a type of token-based authentication. 
           => For every single request from a client to the server, a token is passed for authentication.
           => It supports the stateless API calls.

           ==>> Working
                  
                  1> A client sends username/password combination to the server
                  2> The server validates the authentication
                  3> If authentication is successful, the server creates a JWT token else establishes an error response
                  4> On successful authentication, the client gets JWT token in the response body
                  5> Client stores that token in local storage or session storage.
                  6> From next time, the client for making any request supplies the JWT token in request headers like this. Authorization: Bearer <jwt_token>
                  7> Server upon receiving the JWT validates it and sends the successful response else error.

        <img src = "https://www.positronx.io/wp-content/uploads/2019/10/jwt-flow-6896-01.png">

      
     ## Bcrypt 
         
          => The bcrypt library on NPM makes it really easy to hash and compare passwords in Node. 

          <img src = "https://1.bp.blogspot.com/-0nvN58ARlyk/XstNG8plL0I/AAAAAAAAcHw/weyT50uR70wTV7i8jmllw6pzUA0g27XlQCK4BGAsYHg/w640-h390/ivb-bcrypt.png">


# III. Passwordless

    * Passwordless as a build in authentication method using the common authentication library Passport.
    * By plugging into Passport, Passwordless can be easily and unobtrusively integrated into any application or framework that supports Connect-style middleware, including Express.

           
           <img src = "https://www.marshall.edu/it/files/BulkSMS-infographic-04-v3.png">

# IV. Rolling your own authentication

    * Rolling your own authentication seems to be the most popular choice for Node.js developers today.
    * It’s also the most dangerous choice you have as a developer.
    * To successfully build user authentication into your application, you need to build your own user database, handle sessions, user permissions (authorization), sensitive credentials, and sensitive data storage.
  
     <img src = "https://bs-uploads.toptal.io/blackfish-uploads/blog/article/content/cover_image_file/cover_image/39387/0821-RoleBasedAuthFirebase-Luke_Newsletter-c28a3f61bde83190bc7e6971ed9c8055.png">

# V. Delegating user authentication

    * Unlike rolling your own authentication or using Passport.js, delegating user authentication to a third party service requires far less custom development and almost always reduces risk and complexity.
    * By outsourcing user authentication to a provider, you’re essentially shifting the risk of handling authentication yourself to a third party while gaining simplicity, robustness, and time savings. 
    * In exchange, however, you’ll typically incur some cost. Third party services can be very affordable but aren’t free.

     <img src = "https://loopback.io/images/9830523.png">