# What is Monolithic Architecture?

       * A software system is called "monolithic" if it has a monolithic architecture, in which functionally distinguishable aspects (for example data input and output, data processing, error handling, and the user interface), are not architecturally separate components but are all interwoven.

# Monolithic Architecture
          
          * Monolith means composed all in one piece. 
          * The Monolithic application describes a single-tiered software application in which different components combined into a single program from a single platform.  Components can be:
             
             * Authorization — responsible for authorizing a user
             * Presentation — responsible for handling HTTP requests and responding with either HTML or JSON/XML (for web services APIs).
             * Business logic — the application’s business logic.
             * Database layer — data access objects responsible for accessing the database.
             * Application integration — integration with other services (e.g. via messaging or REST API). Or integration with any other Data sources.
             * Notification module — responsible for sending email notifications whenever needed.


# Example for Monolithic Approach
           
        => Consider an example of Ecommerce application, that authorizes customer, takes an order, check products inventory, authorize payment and ships ordered products. 
        => This application consists of several components including e-Store User interface for customers (Store web view) along with some backend services to check products inventory, authorize and charge payments and shipping orders.

<img src = "https://miro.medium.com/max/875/1*TRmj8lWyzCufEGjxCONAog.jpeg">
