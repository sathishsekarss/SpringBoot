<a id="Top"></a>
## Table of contents
1. [Repository vs Service vs Controller](#Repository-vs-Service-vs-Controller)
2. [@suppressWarnings annotation](#suppressWarnings-annotation)
3. [@Data annotation](#Data-annotation)
4. [Lombok](#Lombok)
5. [@Autowired annotation](#Autowired-annotation)
6. [@Builder annotation](#builder-annotation)
7. [@MockMVC annotation](#MockMVC-annotation)
8. [@Mapping annotation](#Mapping-annotation)

## Repository vs Service vs Controller
In Spring Framework, @Repository, @Service, and @Controller are three important annotations that serve different purposes in the application architecture.
1. @Repository: This annotation is used to indicate that a class is a repository, which is responsible for data access and persistence. It typically interacts with the database and performs CRUD (Create, Read, Update, Delete) operations. The @Repository annotation also provides exception translation, converting database exceptions into Spring's DataAccessException hierarchy.
2. @Service: This annotation is used to indicate that a class is a service, which
contains business logic and acts as an intermediary between the controller and the repository. It is responsible for processing data, applying business rules, and coordinating interactions between different components of the application.
3. @Controller: This annotation is used to indicate that a class is a controller, which handles incoming HTTP requests and returns responses to the client. It is responsible for mapping URLs to specific methods, processing user input, and returning views or data as responses.
In summary, @Repository is for data access, @Service is for business logic, and @Controller is for handling HTTP requests and responses in a Spring application.
[Go to Top](#Top)

## @suppressWarnings annotation
The @SuppressWarnings annotation in Java is used to suppress compiler warnings for a specific piece of code. It can be applied to classes, methods, fields, or local variables. The annotation takes a string argument that specifies the type of warning to suppress. Common warning types include "unchecked", "deprecation", and "rawtypes". By using @SuppressWarnings, developers can prevent the compiler from generating warnings for code that they are aware of and have intentionally chosen to ignore. However, it is important to use this annotation judiciously, as it can hide potential issues in the code if used excessively or without proper justification.
[Go to Top](#Top)

## @Data annotation
The @Data annotation is a convenient shortcut provided by the Lombok library in Java. It is used to automatically generate boilerplate code for classes, such as getters, setters, toString(), equals(), and hashCode() methods. When you annotate a class with @Data, Lombok will generate these methods at compile time, reducing the amount of code you need to write and improving readability. This annotation is particularly useful for data transfer objects (DTOs) or any class that primarily holds data without complex behavior. By using @Data, developers can focus on the core logic of their application while letting Lombok handle the repetitive code generation.
[Go to Top](#Top)

## Lombok
Lombok is a Java library that helps reduce boilerplate code by providing annotations that automatically generate common methods and constructors. It is widely used in Java projects to improve code readability and maintainability. Some of the key features of Lombok include:
1. @Getter and @Setter: Automatically generate getter and setter methods for class fields.
2. @ToString: Generates a toString() method that includes all class fields.
3. @EqualsAndHashCode: Generates equals() and hashCode() methods based on class
fields. Etc.
[Go to Top](#Top)

## @Autowired annotation
The @Autowired annotation in Spring Framework is used for automatic dependency injection. It allows Spring to automatically resolve and inject the required dependencies into a class. When you annotate a field, constructor, or setter method with @Autowired, Spring will look for a matching bean in the application context and inject it into the annotated element. This helps to decouple the components of an application and promotes loose coupling. The @Autowired annotation can be used with various types of dependencies, such as services, repositories, and other beans defined in the Spring context. It simplifies the process of managing dependencies and promotes a more modular and maintainable codebase.
[Go to Top](#Top)

## @Builder annotation
The @Builder annotation is a feature provided by the Lombok library in Java. It is used to implement the Builder design pattern, which allows for more flexible and readable object creation. When you annotate a class with @Builder, Lombok generates a builder class that provides a fluent API for constructing instances of the annotated class. This means you can create objects in a more readable and maintainable way, especially when dealing with classes that have many fields or optional parameters. The builder pattern helps to avoid issues with constructors that have too many parameters and improves code clarity by allowing you to specify only the fields you want to set while creating an object. For example, instead of using a constructor with multiple parameters, you can use the builder to set only the desired fields in a more readable manner.
[Go to Top](#Top)

## @MockMVC annotation
The @MockMVC annotation is not a standard annotation in Java or Spring Framework. However, it is likely referring to the MockMvc class in Spring's testing framework. MockMvc is used for testing Spring MVC applications by simulating HTTP requests and responses without the need for a running server. It allows developers to test the behavior of controllers and their interactions with the service layer in a controlled environment. By using MockMvc, you can perform various HTTP operations (GET, POST, PUT, DELETE) and verify the expected outcomes, such as status codes, response content, and headers. This helps to ensure that your controllers are functioning correctly and that your application behaves as expected under different scenarios.
[Go to Top](#Top)

## @Mapping annotation
Mapping annotation to map data field from mapper class to the model class.  It is used to map the fields of one class to another class.  It is used in the service layer to map the data from the repository layer to the model class.  It is also used in the controller layer to map the data from the service layer to the model class.  It is used to map the data from the model class to the DTO (Data Transfer Object) class.  It is used to map the data from the DTO class to the model class.  It is used to map the data from the model class to the entity class.  It is used to map the data from the entity class to the model class.
[Go to Top](#Top)
