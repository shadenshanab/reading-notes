# class 06

## Dependency Injection

----------------

### Dependency injection is a technique in software engineering in which one object (or static method) supplies the dependencies of another object. A dependency is a reusable object (a service)

### When class A makes use of some functionality from class B, it is said that class A is dependent on class B.

### In Java, before we can use methods from other classes, we must first create the class's object (i.e. class A needs to create an instance of class B).

### Delegating the task of creating the object to someone else and using the dependency directly is referred to as dependency injection.

### Dependency injection is classified into three types:-

1. constructor injection: dependencies are supplied via a class constructor.
2. setter injection: the client exposes a setter method through which the injector injects the dependency.
3. interface injection: the dependency includes an injector method that injects the dependency into any client that is passed to it. Clients must implement an interface that exposes a dependency-accepting setter method.

### DI Advantages:-

1. Aids in unit testing.
2. Boiler plate code is reduced because the injector component handles dependency initialization.
3. It is now easier to extend the application.
Allows for loose coupling, which is essential in application programming.

### Disadvantages of DI:-

1. It is difficult to learn and, if used excessively, can lead to management issues and other problems.
2. A large number of compile-time errors are propagated to run-time.
3. Reflection or dynamic programming is used to implement dependency injection frameworks. This can make it difficult to use IDE automation features like "find references," "show call hierarchy," and safe refactoring.

----------------

## Risk Analysis

----------------

### Risk is defined as the likelihood of any unwanted incident occurring. Risk analysis in software testing is the process of identifying and prioritizing risks in applications or software that you have created. The process of assigning the level of risk is then completed. The risks are classified, and the risk's impact is calculated as a result.

### Using risk analysis at the start of a project in any software highlights potential problem areas. Knowing about the risk areas assists developers and managers in mitigating the risks. When developing a test plan, the risks associated with testing the product, as well as the possibility of damage to your software, must be considered, as well as solutions.

### What exactly are these indicators of risk magnitude? So, here's an explanation.

- High: indicates that the risk's impact would be extremely severe and intolerable. The company may suffer a loss.

- Medium: it is tolerable but not desirable. The company may suffer financially, but the risk is small.

- Low: it is tolerable. There is little to no external risk or financial loss.

### Business Risks: The most common risk associated with our topic is this one. It is the risk posed by your company or your customer, not by your project.

### Testing Risks: You should be very familiar with the platform you are working on, as well as the software testing tools that are being used.

### Premature Release Risk: Analyzing the risk associated with releasing unsatisfactory or untested software necessitates a fair amount of knowledge.

### Software Risks: You should be aware of the risks involved in the software development process.

### Risk Evaluation: These are the most important steps in the risk analysis process. This step is said to be far too complicated and should be approached with extreme caution. Following risk identification, risk assessment must be dealt with programmatically.

----------------

## Design Patterns.

----------------

### A design pattern is nothing more than a description or template for solving a problem! that can be used in a variety of situations As a result, each design pattern provides a solution to commonly encountered software design problems. Patterns are formalized best practices that a Software Developer can use when designing an application to solve common problems.

### Design patterns in the object-oriented programming paradigm are generally aimed at solving problems of object generation and communication rather than the larger scale problems of overall software architecture. Patterns implying object-orientation or, more broadly, mutable state are not as applicable in functional programming languages.

### There are architectural patterns that are larger in scope than design patterns, usually describing an overall pattern followed by an entire system.

### There is 3 major types of design patterns:

1. Creational Patterns:

### Creational patterns enable the instantiation of single or groups of objects. Making it easier to create objects that are situationally appropriate.

- Factory Method. The factory pattern is used to replace class constructors, abstracting the process of object generation so that the type of the object instantiated can be determined at run-time.

- Singleton. The singleton pattern ensures that only one object of a particular class is ever created. All further references to objects of the singleton class refer to the same underlying instance.

- Abstract Factory. The abstract factory pattern is used to provide a client with a set of related or dependent objects. The “family” of objects created by the factory are determined at run-time.

2. Structural Patterns:

### Structural patterns provide a manner to define relationships between classes or objects. Making it easier for these entities to work together.

- Facade. The facade pattern is used to define a simplified interface to a more complex subsystem.

- Adapter. The adapter pattern is used to provide a link between two otherwise incompatible types by wrapping the “adaptee” with a class that supports the interface required by the client.

- Decorator. The decorator pattern is used to extend or alter the functionality of objects at run-time by wrapping them in an object of a decorator class. This provides a flexible alternative to using inheritance to modify behavior.

3. Behavioral Patterns:

### Behavioral patterns define manners of communication between classes and objects. Making it easier and more flexible for these entities to communicate.

- Observer. The observer pattern is used to allow an object to publish changes to its state. Other objects subscribe to be immediately notified of any changes.

- Mediator. The mediator pattern is used to reduce coupling between classes that communicate with each other. Instead of classes communicating directly, and thus requiring knowledge of their implementation, the classes send messages via a mediator object.

- Chain of Responsibility. The chain of responsibility pattern is used to process varied requests, each of which may be dealt with by a different handler.
