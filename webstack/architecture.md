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


TODO Slide 83
