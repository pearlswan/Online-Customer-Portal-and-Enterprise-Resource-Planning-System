# Online-Customer-Portal-and-Enterprise-Resource-Planning-System

**This repo is a demo POC of the corresponding project.**

## Project Description: ##
The client is a manufacture of injectable pharmaceutical packaging and delivery systems.  It also provides analytical services for analyze performance of packaging/delivery systems. As the company expands its business globally, it needs to upgrade its existing web application into microservices.

This project built a customer portal that allows customers to place orders, submit requests for analytical services. The Enterprise Resource Planning System also allows the company to easily manage its orders, customers, logistics and warehouse. 


## Existing System: ##

The existing system is built in monolithic architecture, which is difficult to scale, and prone to single point failure.

## Software Selection: ##
*Backend:*

    Spring ecosystem: SpringBoot 2.1, SpringCloud 2.1
    Message System: RabbitMQ 3.7.14
    Single-Sign-On: Spring Security 5.1.5, JWT
    Database: MySQL 8.0.20 
    Others: JasperReports 6.10, Lombok 1.16

*Front-end:*

    Angular 8, Bootstrap4, Node.js 

*CICD:*

    Jenkins 2.235, Docker

*Test-driven-development:*

    JUnit 5, Mockito 3.3.0.

## Backend Microservice sub-modules: ##
**admin:** Provides RestAPIs for the admin to login, add, remove other authorized users, do relevant database CRUD operations on MySQL admin table.

**product management:** Provides RestAPIs for the company to to add, remove, get products, and do relevant database CRUD operations on MySQL product table.

**customer management:** Provides RestAPIs for the company to to add, remove, get customer, and do relevant database CRUD operations on MySQL customer table.

**order management:** Provides RestAPIs for the company to to view and manage orders, and do relevant database CRUD operations on MySQL order table. Implement a RabbitMQ consumer that accepts message from client service.

**warehouse and logistics management:** Provides RestAPIs for the company to to add, remove warehouse, view and manage stock in each warehouse, and do relevant database CRUD operations on MySQL tables.

**financial management:** Provides RestAPIs for the company to to view financial reports.

**client services:** Provides RestAPIs for customer to register, sign-in, place order on products, or analytical services, access past-order page. Implement a RabbitMQ publisher that sends message to order service.
