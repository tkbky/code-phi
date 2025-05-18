**Domain-Driven Design (DDD)**

**What Domain-Driven Design Is**

**Domain-Driven Design (DDD)** is a major software design approach. Its primary focus is on **modelling software to match a domain** based on input from that domain's experts. DDD places the project's primary focus on the **core domain and the domain logic layer**. It is fundamentally about basing complex designs on a model of the domain and fostering creative collaboration between technical and domain experts to refine a conceptual model addressing particular domain problems.

A key idea in DDD is that the **structure and language of software code** (like class names, methods, variables) should **match the business domain**. For example, in a loan application system, you might have classes like "loan application" or "customers", and methods such as "accept offer" or "withdraw".

DDD is **against the idea of having a single unified model** for a large system. Instead, it divides a large system into **bounded contexts**, each with its own model.

The term "Domain-Driven Design" was coined by Eric Evans in his book of the same name, published in 2003.

**Core Concepts and Practices**

DDD articulates a number of high-level concepts and practices:

- **Domain:** The subject area to which the user applies a program.
- **Domain Model:** A system of abstractions that describes selected aspects of a domain and can be used to solve problems related to that domain.
- **Ubiquitous Language:** A common language shared by domain experts, users, and developers. This language is used in the domain model and for describing system requirements. Ubiquitous language is considered one of the pillars of DDD.
- **Bounded Contexts:** Specific areas within a larger system where a domain model is consistent and valid, ensuring clarity and separation of concerns. DDD divides large systems into bounded contexts, each with its own model.
- **Kinds of Models**:
  - **Entity:** An object defined by its identity, not its attributes. Examples include a uniquely numbered seat on a flight.
  - **Value Object:** An immutable object containing attributes but lacking a conceptual identity. A business card, where the information matters more than the unique card itself, is an example.
  - **Events:** Something that happened in the past.
  - **Domain Event:** An event within a specific business domain that domain experts care about. These are restricted to a bounded context, are vital for preserving business logic, and typically have lighter payloads.
  - **Integration Event:** Events used to communicate changes across different bounded contexts. They are crucial for data consistency across the system and tend to have more complex payloads.
  - **Aggregate:** A collection of objects bound together by a root entity. Objects outside the aggregate can reference the root, but not other internal objects. The aggregate root checks the consistency of changes within the aggregate. A car, an aggregate of engine, brakes, etc., is an example.
- **Working with Models**:
  - **Repository:** An object with methods for retrieving domain objects from a data store.
  - **Factory:** An object with methods for directly creating domain objects.
  - **Service:** Used when a part of a program's functionality doesn't conceptually belong to any specific object.

**Practical Application and Related Concepts**

Applying DDD involves intentional simplification and focus on the domain. The "Domain-based" property from the CUPID principles aligns well with DDD. This property suggests code should convey what it's doing in the **language of the problem domain** to minimise cognitive distance.

- **Domain-based language** involves using domain concepts for naming types and operations, not just computer science constructs. This helps make the solution space navigable in code and aids in catching bugs. The idea is that a casual observer shouldn't be able to tell if people are discussing the code or the domain.
- **Domain-based structure** means the layout of code (directories, file grouping, naming) should mirror the problem domain, rather than imposing a structure based on frameworks or technology. This makes it easier to understand the code's purpose and navigate it. Domain-based code boundaries can align with deployment boundaries for cohesive business components.

DDD is often associated with **Hexagonal Architecture** (Ports and Adapters). Hexagonal Architecture shares a philosophy with DDD on the importance of business logic and can be implemented in a DDD context to ensure business logic is isolated from technical details. It places the business domain at the centre, using ports and adapters for communication. Hexagonal Architecture actively promotes DDD.

DDD has influenced or is related to other software development ideas:

- **Object-Oriented Programming (OOP):** While not strictly tied to OOP, DDD exploits its advantages, such as using entities/aggregate roots and encapsulation. This often leads to associations with Plain Old Java Objects (POJOs) and Plain Old CLR Objects (POCOs), emphasizing domain objects defined purely by business behaviour.
- **Model-Driven Engineering (MDE) / Model-Driven Architecture (MDA):** DDD is compatible with MDE/MDA, and MDE techniques can facilitate DDD practice.
- **Command Query Responsibility Segregation (CQRS):** An architectural pattern that makes the distinction between commands (mutating state) and queries (reading state) explicit, often using the aggregate root concept from DDD.
- **Event Storming:** A collaborative technique that can be used as a precursor to DDD to identify and understand domain events, helping discover subdomains, bounded contexts, and aggregate boundaries.
- **Event Sourcing:** An architectural pattern where state is tracked by committing events to an event store. When combined with CQRS and DDD, aggregate roots validate commands and publish events.
- **Microservices:** Bounded contexts in DDD often map to microservices. A one-to-one relationship is often ideal, but other mappings (one-to-many, many-to-one) can occur based on project needs.
- **Context Mapping Patterns:** Eric Evans described patterns like Partnership, Shared Kernel, Customer/Supplier Development, Conformist, Anticorruption Layer, Open-host Service, Published Language, Separate Ways, and Big Ball of Mud to describe how different bounded contexts interact.

**Benefits and Criticisms**

**Benefits** of DDD mentioned include maintainability, improved collaboration between technical and domain experts, and aligning system design with business goals. Domain-based code, which aligns with DDD, minimises the cognitive distance from need to solution.

**Criticisms** of DDD suggest that developers typically need to implement significant isolation and encapsulation to keep the model a pure and helpful construct. Microsoft recommends DDD **only for complex domains** where the model provides clear benefits in formulating a common understanding.
