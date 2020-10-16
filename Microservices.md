# What is Microservices Architecture?
           
    * In computing, microservices is a software architecture style in which complex applications are composed of small, independent processes communicating with each other using language-agnostic APIs.
    * These services are small, highly decoupled and focus on doing a small task, facilitating a modular approach to system-building.

# What are microservices?
   
    * Microservices - also known as the microservice architecture - is an architectural style that structures an application as a collection of services that are

       => Highly maintainable and testable
       => Loosely coupled
       => Independently deployable
       => Organized around business capabilities
       => Owned by a small team

    * The microservice architecture enables the rapid, frequent and reliable delivery of large, complex applications. 
    * It also enables an organization to evolve its technology stack.

# The main advantages of Microservices are:
        
        
    * The form and size will be maintained due to its structure, where components are dissected into smaller services.
    * Independence is the key here, continues deployment is easily possible, unlike monolithic architecture as each service can be deployed independently.
    * It follows the Single Responsibility Principle, where each service is responsible over a single part of the functionality.
    * Scaling components individually is possible here, as components are de-coupled to different services, so can be scaled horizontally and individually without impacting the overall system.
    * Light-weight Communication: Services communicate with each other using a lightweight communication, such as REST over HTTP.

<img src = "https://23o0161033pm1289qo1hzrwi-wpengine.netdna-ssl.com/wp-content/uploads/2019/04/Microservices-infographics-03-2.png">


# Microservice Architecture :

       * Each module supports a specific business goal and uses a simple, well-defined interface to communicate with other sets of services.
       * Instead of sharing a single database as in Monolithic application, each microservice has its own database.
       * Having a database per service is essential if you want to benefit from microservices, because it ensures loose coupling.
       * Each of the services has its own database. Moreover, a service can use a type of database that is best suited to its needs.

# Example :

       * Consider the same example of the e-commerce application, which consists of several components/modules. 
       * Define each component/module as a separate loosely coupled service depending on the requirement, which may collaborate with each other based on the scenario. We can have following services for a complete application:
            
            * Authorization Service — Responsible for authorizing customer.
            * Order Service — takes an order and process it.
            * Catalog Service — Manage products and check products inventory.
            * Cart Service — Manage user cart, this service can utilize Catalog service as a data source.
            * Payment Service — Manage and Authorize payments.
            * Shipping Service — Ships ordered products.

<img src = "https://miro.medium.com/max/875/1*3mY6LcrO3o0nkpAZkNjF0Q.jpeg">


# Node.js Is Good Choice For Microservices Because It Offers:
    * Superior performance.
    * Faster execution.
    * Cost-effective and scalable.
    * Easy to maintain and update.
    * Simplified, modular development.
    * API support.
    * Wider community support.
    * Easily available frameworks.
    * Easy learning curve.


<img src = "https://23o0161033pm1289qo1hzrwi-wpengine.netdna-ssl.com/wp-content/uploads/2016/02/Microservices-blog-infographics-02-1024x682.png">


# Building Microservices with Node.js

    * 1. Assess the Business Need
    * 2. Initialization
    * 3. Setting up the Server
    * 4. Specifying the Routes
    * 5. Building the Controller
    * 6. Establishing the External API Call
    * 7. Execution

<img src = "https://dzone.com/storage/temp/12480229-microservices-and-nodejs.jpg">