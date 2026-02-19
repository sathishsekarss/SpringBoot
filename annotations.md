## Table of contents
1. [Repository vs Service vs Controller](#Repository-vs-Service-vs-Controller)
2. [@suppressWarnings annotation](#suppressWarnings-annotation)
3. [@Data annotation](#Data-annotation)


## Repository vs Service vs Controller
In Spring Framework, @Repository, @Service, and @Controller are three important annotations that serve different purposes in the application architecture.
1. @Repository: This annotation is used to indicate that a class is a repository, which is responsible for data access and persistence. It typically interacts with the database and performs CRUD (Create, Read, Update, Delete) operations. The @Repository annotation also provides exception translation, converting database exceptions into Spring's DataAccessException hierarchy.
2. @Service: This annotation is used to indicate that a class is a service, which
contains business logic and acts as an intermediary between the controller and the repository. It is responsible for processing data, applying business rules, and coordinating interactions between different components of the application.
3. @Controller: This annotation is used to indicate that a class is a controller, which handles incoming HTTP requests and returns responses to the client. It is responsible for mapping URLs to specific methods, processing user input, and returning views or data as responses.
In summary, @Repository is for data access, @Service is for business logic, and @Controller is for handling HTTP requests and responses in a Spring application.

## @suppressWarnings annotation
The @SuppressWarnings annotation in Java is used to suppress compiler warnings for a specific piece of code. It can be applied to classes, methods, fields, or local variables. The annotation takes a string argument that specifies the type of warning to suppress. Common warning types include "unchecked", "deprecation", and "rawtypes". By using @SuppressWarnings, developers can prevent the compiler from generating warnings for code that they are aware of and have intentionally chosen to ignore. However, it is important to use this annotation judiciously, as it can hide potential issues in the code if used excessively or without proper justification.

## @Data annotation
The @Data annotation is a convenient shortcut provided by the Lombok library in Java. It is used to automatically generate boilerplate code for classes, such as getters, setters, toString(), equals(), and hashCode() methods. When you annotate a class with @Data, Lombok will generate these methods at compile time, reducing the amount of code you need to write and improving readability. This annotation is particularly useful for data transfer objects (DTOs) or any class that primarily holds data without complex behavior. By using @Data, developers can focus on the core logic of their application while letting Lombok handle the repetitive code generation.