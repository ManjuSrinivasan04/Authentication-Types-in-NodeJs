<img src = "https://miro.medium.com/max/4198/1*HC1PWdue5ZofBEwOMEsBBA.png">



# Cookies Vs Local Storage

   * Cookies are primarily for reading server-side
   * local storage can only be read by the client-side. 

   => So the question is, in your app, who needs this data — the client or the server?

        * If it's your client (your JavaScript), then by all means switch. You're wasting bandwidth by sending all the data in each HTTP header.

        * If it's your server, local storage isn't so useful because you'd have to forward the data along somehow (with Ajax or hidden form fields or something). This might be okay if the server only needs a small subset of the total data for each request.

        * Apart from being an old way of saving data, Cookies give you a limit of 4096 bytes (4095, actually) — it's per cookie. 
        * Local Storage is as big as 5MB per domain — SO Question also mentions it.
        * localStorage is an implementation of the Storage Interface. 
        * It stores data with no expiration date, and gets cleared only through JavaScript, or clearing the Browser Cache / Locally Stored Data — unlike cookie expiry.



<img  src = "https://ic.pics.livejournal.com/dotnetinter/32561056/128955/128955_original.png">






# Cookies Vs Session Storage

       * E-commerce and other Web applications often rely on cookies to identify users. 
       * A cookie is a small text file that a Web server stores on your computer.
       * Cookie files typically contain data about you, such as your user name or viewing preferences. 
       * While You can describe Session as a server-side storage of information that stores information of the user’s interaction with the website or web application. 
       * Unlike Cookies, Sessions stored on the server side.



<img src = "https://anydifferencebetween.com/wp-content/uploads/2016/09/Difference-Between-Cookies-and-Sessions.jpg">




# Cookies Vs Local Storage Vs Session Storage





<img src = "https://i.stack.imgur.com/cI5kT.jpg">


