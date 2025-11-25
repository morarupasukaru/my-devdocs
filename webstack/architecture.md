# Architecture

* Overview of tasks and responsibilities for architects and tech leads
* Ability for recognizing critical requirements for architecture
* Toolbox for creating, monitoring, documenting and evaluating architectures

## Definitions

* Software Architecture :=  Sum of important decisions of a system 
* Many aspects in software architecture are trade-offs
* [TOGAF](https://en.wikipedia.org/wiki/The_Open_Group_Architecture_Framework) framework

## Non-functional requirements (NFR)

* [Software Quality Attributes in Software Engineering](https://www.softwaretestinghelp.com/what-are-the-quality-attributes/)
* Tradeoffs of Quality Attributes
  * Flexibility  (layering, separation) <-> performance
  * User convenience  <-> security (2FA)
  * Scalability (more distribution) <-> single instance performance. Sessions, Kibana, splunk
  * Simplicity of system <-> performance (tuning such as caching, …)
  * Modifiability <-> performance (runtime plugins)
  * Decoupling, Reuseability <-> maintainable (Micro services)
  * Configurability <–> testability
* identifying [architecturally significant requirements (ASRs)](https://en.wikipedia.org/wiki/Architecturally_significant_requirements)
* technical issues for risk monitoring
* [the key points of Working Effectively with Legacy Code](https://understandlegacycode.com/blog/key-points-of-working-effectively-with-legacy-code/)

## Principles

* Separation of Concerns
* Consistency/ conceptual integrity
  * One technology for one problem, for example logging, data access (e.g. REST or SOAP but not both)
* Information Hiding/ Encapsulation/ Abstraction
* Avoid redundancy/ Don’t repeat yourself (DRY)
* High Cohesion
* Low Coupling
  * [difference Between Cohesion and Coupling](https://stackoverflow.com/questions/3085285/difference-between-cohesion-and-coupling/3085419#3085419)
  * [Cohesion and Coupling: the difference](https://enterprisecraftsmanship.com/posts/cohesion-coupling-difference/)
* Related: [Modular Design](https://en.wikipedia.org/wiki/Modular_design)
* Related: Care about dependencies (with e.g. SONAR dependency structure matrix)


## Patterns

* Basic ones (selection):  
  * Gang of Four (GoF) (some are less useful with functional programming)
  * GRASP patterns, GoF patterns reduced to 9 core patterns (Book: applying UML and patterns)
* Pattern selection, on higher level
  * Pattern-Oriented Software Architecture Volume 1, more educational than GoF-book
  * Domain Driven Design (DDD): effective OO design for our typical systems
  * Patterns of Enterprise Application Architecture -book
  * Enterprise Integration Patterns
  * Modern patters for cloud, big data, microservices<img width="1923" height="758" alt="image" src="https://github.com/user-attachments/assets/ff4e0ce0-1ab8-4bd4-9bb5-6993ce4bb9c4" />
* [The Importance of Domain Driven Design](https://simpleprogrammer.com/importance-domain-driven-design/)
* [A Domain-driven Design Example](https://www.mirkosertic.de/blog/2013/04/domain-driven-design-example/)
* [Clean Domain-Driven Design in 10 minutes](https://hackernoon.com/clean-domain-driven-design-in-10-minutes-6037a59c8b7b)

## Architectural styles

* To reason about an architecture, it is often useful to know different architectural styles
  * Pipe- & Filter (batch)
  * Repository style
  * Hexagonal / onion architecture
    * https://blog.octo.com/hexagonal-architecture-three-principles-and-an-implementation-example
  * Event system
  * Event sourcing (event log)
  * Microservices
 * Architectural Styles by Starke --> take image of slide 122
* [Architecture Anti patterns](https://architecture-antipatterns.tech/)
  * Architecture by implication – Too late decisions, decisions are taken implicitly
  * Covering your assets - documenting alternatives without decision
  * Witches brew – group of architects resulting in mix of ideas, lacking focus or consistency
  * Gold plating -  work well past the point where the extra effort is worth the value  
  * Vendor king - architecture built fully around a vendor product (aka vendor trap)
  * Big bang architecture - designing the entire architecture at the beginning of the project when you know least about the system
  * Groundhog day - discussions repeated as justification not known
  * Stovepipe Architecture - isolated system with different technologies without reuse
  * Golden hammer - one technology for all
  * Cargo-culting
  * Domain allergy
  * Emotional attachment
  * Horizontalism
  * Infrastructure ignorance
  * Misapplied genericity
* Be careful with Hype Driven Development (HDD)

## Views

[Viewpoints](http://www.viewpoints-and-perspectives.info/home/viewpoints/)
* Context View (black box)
* Functional view
* Deployment view
* ...

## Notation: DSL
Domain Specific Language (DSLs): a language that is well suited to express a domain or a solution (=implementation) for a domain
[fluent style APIs](http://www.martinfowler.com/bliki/FluentInterface.html) (e.g. Spring Data)

## Impact of AI to software architecture
* Prompt for comparing technologies
* Analyzing existing code
* Code generation for PoCs or demos
* Generating diagrams from code
* Generating tests
* Learning a new programming language
* Analysing logs
* Generating helper tools


## Tools
* [draw.io](https://www.drawio.com/)
architecture kata
