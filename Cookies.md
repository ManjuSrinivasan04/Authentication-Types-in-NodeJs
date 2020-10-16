# Cookies
  
  * Cookies are simple, small files/data that are sent to client with a server request and stored on the client side. 
  * Every time the user loads the website back, this cookie is sent with the request. 
  * This helps us keep track of the user’s actions.

# The following are the numerous uses of the HTTP Cookies −

    * Session management
    * Personalization(Recommendation systems)
    * User tracking

   => To use cookies with Express, we need the cookie-parser middleware. To install it, use the following code −

               ## npm install --save cookie-parser

# With the help of cookies –

    * It is easy for websites to remember the user’s information
    * It is easy to capture the user’s browsing history
    * It is also useful in storing the user’s sessions
    * The session makes requests to all the servers using a secret Id. 
    * The information is stored on the server that is linked to this secret ID.

 <img src = "https://cms-assets.tutsplus.com/uploads/users/487/posts/22543/image/traditional-authentication-system-png.png">


 # Local Storage

    * LocalStorage is a way to store data on the client’s computer. 
    * It allows the saving of key/value pairs in a web browser and it stores data with no expiration date. 
    * LocalStorage can only be accessed via JavaScript, and HTML5. 
    * However, the user has the ability to clear the browser data/cache to erase all localStorage data.

    *  Web storage can be viewed simplistically as an improvement on cookies, providing much greater storage capacity The available size is 5MB, which is more space to work with than a typical 4KB cookie.

    * In addition with localStorage, the data is not sent back to the server for every HTTP request (HTML, images, JavaScript, CSS, etc.), which thus reduces the amount of traffic between client and server. Lastly, it works on same-origin policy, so the data stored will only be available on the same origin.