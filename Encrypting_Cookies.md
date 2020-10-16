# Encrypting Cookies
     
     * Encrypting your Node. js application cookies is a way to prevent unauthorized access to confidential and personal information

# Session cookies encryption 
       
       * If the session cookie doesn't have the secure attribute enabled, it is not encrypted between the client and the server, and this means the cookie is exposed to Unsecured Session Cookie hacking and abuse.

     
      * Data sent over SSL (HTTPS) is fully encrypted, headers included (hence cookies), only the Host you are sending the request to is not encrypted. It also means that the GET request is encrypted (the rest of the URL).


# Set cookies :
   
    * Creating simple route to set a “test” cookie.

        const cookieConfig = {
             httpOnly: true, // to disable accessing cookie via client side js
             secure: true, // to force https (if you use it)
             maxAge: 1000000000, // ttl in ms (remove this option and cookie will die when browser is closed)
             signed: true // if you use the secret with cookieParser
            };

        // make /set route 
        app.get('/set', (req, res) => {
        // MAIN CODE HERE :
        res.cookie('test', 'some value', cookieConfig);
        res.send('set cookie');
       });
       


# Get cookies
   
    * Will access to our cookie by adding simple route to your app.js :


         app.get('/get', (req, res) => {
        // MAIN CODE HERE :
        const signedCookies = req.signedCookies; // get signed cookies
        console.log('signed-cookies:', signedCookies);  
        const cookies = req.cookies; // get not signed cookies
        console.log('not-signed-cookies:', cookies);
        // or access directly to one cookie by its name :
        const myTestCookie = req.signedCookies.test;
        console.log('our test signed cookie:', myTestCookie);
       res.send('get cookie');
       });

# cookie-encrypter

     * Transparently encrypt/decrypt your cookie using an express middleware to set after the cookie-parser. 
     * Support all type of cookie (including http-only and signed) with string content or JSON. 
     * Use aes256 as the default encryption algorithm (internally use the nodejs crypto module).

    ## Installation
      
      $ npm install cookie-encrypter

