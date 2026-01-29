This repository contains concepts about spring boot.

## Table of contents
1. [What is spring framework](#Spring-Framework)
2. [What is spring boot ?](#Spring-boot)
3. [What are the core features of Spring ?](#Core-features-of-Spring)
4. [Why spring ?](#why-Spring)
5. [What is inversion of control ?](#Inversion-Of-Control)
6. [What is Dependency Injection ?](#dependency-Injection)
7. [Types of dependency Injection?](#types-of-dependency-Injection)
8. [What is Auto wiring ?](#Auto-Wiring)
9. [What is Application context ?](#Application-context)
10. [What is @Repository annotation ?](#Repository-annotation)
11. [What is @Service annotation ?](#Service-annotation)
12. [What is Application properites ?](#Application-properties)
13. [What is JDBC Template ?](#JDBC-Template)
14. [Describe the flow of HTTPS requests through the Spring Boot application.](#flow-HTTP-Request)
15. [Types of configurations in Spring Boot ?](#Types-of-configurations-in-Spring-Boot)

## Spring Framework
Spring is a comprehensive Java framework for building robust, enterprise grade applications. Spring provides a complete solution for all application needs, including 
web, database, security, and transaction management.

## Spring boot 
Spring Boot is an extension of the Spring framework that simplifies the process of building Spring-based applications. It offers a set of conventions and defaults that help developers get started quickly without extensive configuration.

Note:  Initially with Spring framework, the problem was configuring spring to work.  It had lot of configurations file to even print a simple message.  So, the spring team addressed this issue and came up with spring boot concept.  From the name spring boot, boot implies that boot the spring framework application.  In simple words it gives a template to get started with Spring framework application by default.

## core features of Spring
	1. POJO - Plain old Java Objects
	2. Dependency Injection
	3. Aspect Oriented programming

## why spring
	1.  Lightweight and modular
	2.  Clean and maintainable code
	3.  Supports a wide range of technologies.

## Inversion of control
Inversion of Control (IoC) is a design principle where the control of object creation and management is transferred from the application code to a framework or container, allowing developers to focus on business logic rather than dependency management.

The org.springframework.beans and org.springframework.context packages are the basis for Spring Framework’s IoC container.

[Refer this link for detail overview on containers](https://docs.spring.io/spring-framework/reference/core/beans/basics.html)

## Dependency Injection
Dependency Injection (DI) is a specific implementation of IoC that provides an object's dependencies from an external source, rather than having the object create them internally. This promotes loose coupling, making code more modular, testable, and maintainable.

## types-of-Dependency-Injection
Types of Dependency Injection are:
1.  Constructor-based Dependency Injection
2.  Setter-based Dependency Injection

## Auto Wiring
Autowiring is a feature in the Spring Framework that allows the Spring container to automatically inject dependencies into a bean. It simplifies the process of wiring together beans by eliminating the need for explicit setter or constructor calls. When a bean requires a dependency, Spring resolves and injects it into the bean automatically.

**💡 Tips:**  Class path is src/main which holds the resource folder to store statics files and any other configuration files.

## Application context
ApplicationContext is an advanced IOC container in Spring. It builds on top of BeanFactory and provides additional features like:
	1. Handles events published by beans.
	2. Supports declarative AOP features.
	3. Allows support for internationalization and easy access to resource bundles.
	4. Automatic injection of dependencies based on bean types.
	5. Provides several specialized types of ApplicationContext implementations, such as:
	6. Loads context from an XML file located in the classpath.

## Repository-annotation

@Repository in Spring Boot

@Repository is a Spring stereotype annotation used on classes that handle data access (DAO layer).

It marks the class as a bean so Spring can detect it during component scanning.

It provides automatic exception translation: converts low-level persistence exceptions (like JDBC/Hibernate errors) into Spring’s DataAccessException.

Used typically with classes that interact with the database, such as JPA repositories, CRUD operations, or custom DAO implementations.

## Service-annotation

@Service is a Spring stereotype annotation used to mark a class as a service layer bean.
Spring automatically detects it during component scanning and registers it in the application context.

## Application-properties
Application properties in spring stores all the configuration related to the spring application.  Such as database connection string, static variables, location of files etc.

Application properties file can be in .yaml file, .properties file or even .xml file.

## JDBC-Template
JDBC Template is used to read write in Database.  We have to pass the query to the methods to create/modify the database.


## flow-HTTP-Request

First client makes an HTTP request ( GET, POST, PUT, DELETE ) to the browser.
After that the request will go to the controller, where all the requests will be mapped and handled.
After this in Service layer, all the business logic will be performed. It performs the business logic on the data that is mapped to JPA (Java Persistence API) using model classes.
In repository layer, all the CRUD operations are being done for the REST APIs .
A JSP page is returned to the end users if no errors are there.
If there is no error, the response is returned.

## Types-of-configurations-in-Spring-Boot
There are three types of configurations in Spring Boot:
1.  Annotation-based configuration
2.  XML-based configuration
3.  Java-based configuration