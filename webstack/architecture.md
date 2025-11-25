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
  * Modern patters for cloud, big data, microservices
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

## ARC 42 template

* ADD - Documenting Architectures with [arc42](https://arc42.org/overview)
* A short alternative to the ADD or the ADP (see below) is the [Architecture Inception Canvas](https://canvas.arc42.org/architecture-inception-canvas)
* or the [Architecture Communication Canvas](https://canvas.arc42.org/architecture-communication-canvas).

## Interfaces

Interfaces are not only hard to do well, they are also expensive.

In fixed-price projects:
* Exclude external interfaces from the fixed scope
Aim for minimum-work/zero-external depencies (e.g. DB interface table)
Remember:
* Interfaces are contracts, not only technically, but also organizationally and operationally

Checklist for good-practise about interfaces
* Understand the business scope
* Sketch and redesign, make it simple
* Create and follow guidelines
* Respect the contract
* Communicate with the stakeholders
* Document the usage
* (Support batching)
* Follow common security guidelines
* Support monitoring
* Clear error handling
* Mocks and test cases

## Tools
* [draw.io](https://www.drawio.com/)
* [architecture kata](https://github.com/tedneward/ArchKatas)
  
[*Go to parent page*](../README.md)

*Page mainly written in november 2025*
