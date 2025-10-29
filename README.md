This repository contains concepts about spring boot.

## Table of contents
1. [What is spring framework](#Spring-Framework)
2. [What is spring boot ?](#Spring-boot)
3. [What are the core features of Spring ?](#Core-features-of-Spring)
4. [Why spring ?](#why-Spring)
5. [What is inversion of control ?](#Inversion-Of-Control)
6. [What is Dependency Injection ?](#dependency-Injection)
7. [What is Auto wiring ?](#Auto-Wiring)
8. [What is Application context ?](#Application-context)

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

[Refer this link for detail overview on containers](https://docs.spring.io/spring-framework/reference/core/beans/basics.html#beans-factory-xml)

## Dependency Injection
Dependency Injection (DI) is a specific implementation of IoC that provides an object's dependencies from an external source, rather than having the object create them internally. This promotes loose coupling, making code more modular, testable, and maintainable.

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