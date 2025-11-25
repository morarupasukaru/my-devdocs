# Architecture

* Overview of tasks and responsibilities for architects and tech leads
* Ability for recognizing critical requirements for architecture
* Toolbox for creating, monitoring, documenting and evaluating architectures

---
* Definitions
* Non-functional requirements
* Building blocks & tools
---

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

TODO Slide 27
