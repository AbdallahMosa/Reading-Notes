# Design Patterns
  
  ## What's a design pattern?
 - Design patterns are typical solutions to commonly occurring problems in software design. They are like pre-made blueprints that you can customize to solve a recurring design problem in your code.

  ## 3 major types of design patterns:
   ### 1. Creational Patterns:
   - Creational patterns provide ways to instantiate single or groups of objects. Making it easier to create objects in a way that suits the situation.


   ### 2. Structural Patterns:
   - Structural patterns provide a manner to define relationships between classes or objects. Making it easier for these entities to work together.


   ### 3. Behavioral Patterns:
   -  Behavioral patterns define manners of communication between classes and objects. Making it easier and more flexible for these entities to communicate.
  
 
# Risk Analysis 

 ## What is Risk Analysis :
  - risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done
 
 ## risks that you could encounter :
 1. Use of new hardware
 2. Use of new technology
 3. Use of new automation tool
 4. The sequence of code
 5. Availability of test resources for the application
 
 ## certain risks that are unavoidable :
 1. The time that you allocated for testing
 2. A defect leakage due to the complexity or size of the application
 3. Urgency from the clients to deliver the project
 4. Incomplete requirements

## situation 
1. Conduct Risk Assessment review meeting
2. Use maximum resources to work on high-risk areas
3. Create a Risk Assessment database for future use
4. Identify and notice the risk magnitude indicators: high, medium, low.

## risk magnitude indicators
1. High: means the effect of the risk would be very high and non-tolerable. The company might face loss.
2. Medium: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.
3. Low: it is tolerable. There lies little or no external exposure or no financial loss.



# Dependency Injection
   ## What is  Dependency Injection :
   - dependency injection is a technique whereby one object (or static method) supplies the dependencies of another object. A dependency is an object that can be used (a service).

  ##  types of dependency injection:
  1. constructor injection: the dependencies are provided through a class constructor.
  2. setter injection: the client exposes a setter method that the injector uses to inject the dependency.
  3. interface injection: the dependency provides an injector method that will inject the dependency into any client passed to it. Clients must implement an interface that exposes a setter method that accepts the dependency.
  ## dependency injection’s responsibility to:
  1. Create the objects
  2. Know which classes require those objects
  3. And provide them all those objects
  ## Benefits of using DI 
  1. Helps in Unit testing.
  2. Boiler plate code is reduced, as initializing of dependencies is done by the injector component.
  3. Extending the application becomes easier.
  4. Helps to enable loose coupling, which is important in application programming.
  ## Disadvantages of DI
  1. It’s a bit complex to learn, and if overused can lead to management issues and other problem
  2. Many compile time errors are pushed to run-time.
  3. Dependency injection frameworks are implemented with reflection or dynamic programming. This can hinder use of IDE automation, such as “find references”, “show call hierarchy” and safe refactoring.

