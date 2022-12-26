# React Review
## What is a Component?
- A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.
- A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.
- A software component can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only. That is, a software component can be deployed independently and is subject to composition by third parties.

## Views of a Component
  - Object-oriented view : A component is viewed as a set of one or more cooperating classes. Each problem domain class (analysis) and infrastructure class (design) are explained to identify all attributes and operations that apply to its implementation. It also involves defining the interfaces that enable classes to communicate and cooperate.
  - Conventional view :It is viewed as a functional element or a module of a program that integrates the processing logic, the internal data structures that are required to implement the processing logic and an interface that enables the component to be invoked and data to be passed to it.
  - Process-related view : In this view, instead of creating each component from scratch, the system is building from existing components maintained in a library.

## Characteristics of Components
  - Reusability − Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.
  - Replaceable − Components may be freely substituted with other similar components.
  - Not context specific − Components are designed to operate in different environments and contexts.
  - Extensible − A component can be extended from existing components to provide new behavior.
  - Encapsulated − A A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.
  - Independent − Components are designed to have minimal dependencies on other components.


## Advantages
  1. Ease of deployment − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.
  2. Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.
  3. Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.
  4. Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.
  5. Modification of technical complexity − A component modifies the complexity through the use of a component container and its services.
  6. Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.
  7. System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system.
  8. Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.
