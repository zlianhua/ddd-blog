---
layout: post
title: "Embracing Evolution: TM Forum's Information Framework at the Forefront"
date: 2024-03-01
author: Levon Zhang
sitemap: true
---

In the telecommunications industry, rapid technological advancements and customer demands shape the market. The TM Forum's Information Framework, formerly known as SID (Shared Information/Data model), has evolved into an essential toolkit for Communications Service Providers (CSPs). This framework aims to navigate the complexities of information architecture with agility, interoperability, and efficiency.

## The Essence of the Information Framework

The Information Framework provides an extensive information/data reference model complemented by a common vocabulary crucial for the implementation of business processes within the telecommunications sector. This strategic framework is designed to be independent of any platform, language, or protocol, offering CSPs the tools to identify key business entities. It lays the groundwork for a unified data model, dictionary, and the subsequent development of functions, applications, components, and APIs.

## Structured Approach through Domains and Business Entities

At the core of the Information Framework is its structured approach, organizing business entities into domains to reduce duplication and overlap. These domains include:

- Market & Sales
- Customer
- Product
- Service
- Resource
- Business Partner
- Enterprise
- Common

Each fosters a high level of cohesion within its sphere. This methodical categorization aligns with the Business Process Framework (eTOM) and the Functional Framework, bridging the "How" of eTOM with the "What" of the Information Framework.

![TMF Domain]({{ "/assets/image/TMFDomain.png" | relative_url }})

###	Market/Sales Domain

The Market & Sales Domain represents roles, information and activities pertaining to marketing and sales strategy, capability delivery, lifecycle management and support of parties (e.g., individuals / organizations ) that move through sales lifecycle stages (e.g., contact / lead / prospect) as they learn about, inquire, choose, negotiate, order and are supported for goods and services (i.e., products) that are offered by an enterprise. On the Sales side, this includes sales contacts / leads / prospects through to the sales force and sales statistics. Market includes market strategy and plans, market segments, competitors and their products, through to campaign formulation and reporting.

###	Product Domain

The Product domain represents roles, information and activities carried out by parties (e.g., individuals / organizations) playing roles that are involved in the strategic planning, definition, development and operational aspects of Products that are offered to customers by an enterprise. Activities include management of Product: strategies, capabilities, lifecycles, offerings, instances, performance, contract operations, usage statistics and support of goods and services (products) that are offered to customers by an enterprise.

###	Customer Domain

The Customer domain represents roles, information and activities carried out by parties (e.g., individuals / organizations) playing roles that are involved in the management of and all types of contact with customers as they acquire, use, pay for and are supported for goods and services (i.e., products) that they obtain from an enterprise. Activities include: Strategy to Readiness (e.g., customer strategies, capabilities, customer lifecycle management) and Operations (e.g., customer relationship management , data, privacy, interactions, communications, orders, accounts, balances, service level agreements (SLAs), training, problems, cases, invoices, payments, disputes, collections, loyalty, performance, usage statistics, analytics and support).

###	Service Domain

The Service domain represents roles, information and activities carried out by parties (e.g., individuals / organizations) playing  roles that are involved in the strategic planning, definition, development, and operational aspects of Services that are used to realize Product offerings to the market. Activities include management of: strategies, capabilities, lifecycles, catalogs, inventories, installations, activations, problems, performance, guiding, mediation, usage statistics and support of customer-facing services that are offered to customers and resource-facing services that are presented to resources by an enterprise..

###	Resource Domain

The Resource domain represents roles, information and activities carried out by parties (e.g., individuals / organizations) playing roles that are involved in the strategic planning, definition, development and operational aspects of Resources (e.g., functions, applications, computing, networking and storage) that represent the infrastructure of an enterprise that are used to realize Services. Activities include management of strategies, capabilities, lifecycles, catalogs, inventories, topologies, installations, activations, alarms, problems, performance, mediation, usage statistics and support of Resources that are managed by an enterprise.

###	Business Partner Domain

The Business Partner domain represents roles, information and activities carried out by parties (e.g., individuals / organizations) playing roles that are involved in the strategic planning, definition, development, operational aspects and all types of contact with Business Partners (e.g., Suppliers, Partners, etc.) with which an enterprise collaborates in order to operate their business. Activities include management of Business Partner: strategies, capabilities, value propositions, relationships, profiles, data, privacy, security, interactions, communications, tenders, agreements, orders, requisitions, supplies, accounts, balances, inventories, reconciliations, service level agreements (SLAs), training, problems, cases, invoices, payments, revenues, disputes, collections, loyalty, performance, usage statistics, analytics and support of Business Partners as they supply, acquire, use, support, purchase, pay for and are supported for goods and services (products) that they provide and / or obtain from an enterprise.

###	Enterprise Domain

The Enterprise domain represents roles, information and activities that are required to run and support a business. These concepts focus on both the setting and achieving of strategic corporate goals and objectives, as well as providing those support services that are required throughout an Enterprise. These concepts are sometimes considered to be the corporate functions and/or processes (e.g., Financial Management, Human Resources Management processes, etc.). Since Enterprise Management is aimed at general support within the Enterprise, they may interface as needed with almost every other process in the Enterprise, be they operational, strategy, infrastructure or product processes.

###	Common Domain

The Common domain which is part of the Information Framework (SID) and the Functional Framework (the Common domain was part of the eTOM in versions 19.0 to 21.0, but it was removed from the eTOM in the latest release 21.5) represents business roles, information, functions and metrics, etc. that support several Core Frameworks’ domains and are not specific to (i.e., are generic) or “owned by” any particular domain or are referenced or utilized from two or more other domains.

## Unleashing the Power of Design Patterns

The Information Framework adopts sophisticated design patterns to ensure robust, scalable, and flexible implementations. Let's delve deeper into two critical patterns: the Specification and Composite patterns.

### Specification Pattern

The Specification pattern is used in the Information Framework when:
“There needs to be a description about an item or service, independent of the current existence of any examples of those items or services”.

The Specification Entity doesn’t represent a concept or thing, but information about a concept or thing. Specification Entities are found in business concepts such as catalogs, manufacturing specifications, recipes and other documentation that relates to types of things rather than individual instances.

This pattern is used in the Information Framework Product Addendum (Product & ProductSpecification Entities) and most other Information Framework addenda.

![Specification Pattern]({{ "/assets/image/Specification.png" | relative_url }})

### Composite Pattern

The Composite pattern is usually thought of as a design pattern.
“Assemble objects into tree structures. COMPOSITE simplifies clients by
letting them treat individual objects and assemblies of objects uniformly.”

In the Information Framework, we use the Composite pattern when there is a business concept where a single thing or a collection of those things can be used interchangeably. For example, in a warehouse the concept of a “stock item” may include parts, sub-assemblies and complete items.
This pattern is used extensively in the Information Framework (e.g., Party, Individual & Organization Entities).

![Composite Pattern]({{ "/assets/image/Composite.png" | relative_url }})

### Abstract Superclass Pattern

The Abstract Superclass pattern groups similar entities together under a generalized parent, allowing for a streamlined and organized model structure. This pattern is instrumental in reducing complexity by providing a shared base for entities with common attributes, yet allowing for the specialization needed to address specific use cases.

We use the Abstract Superclass pattern to add superclass Entities to allow us to group similar Entities together. We make the parent Entity abstract, to show that it will not occur in the real world but is a modeling construct.

The Abstract Superclass pattern helps make the Information Framework more general and easier to extend. This pattern helps us improve the modularity (coupling & cohesion) of the Information Framework model.

This pattern is used extensively in the Information Framework (e.g., the Party Entity is an Abstract Superclass of the Individual Entity and the Organization Entity).

![Superclass Pattern]({{ "/assets/image/Superclass.png" | relative_url }})

### Role Entity Pattern

Role entities are used to represent the different roles an entity might play in various contexts. This pattern is vital for scenarios where an entity's behavior changes based on its interaction or relationship with other entities, providing flexibility and clarity in modeling such dynamic relationships.

Use of roles is a fundamental pattern that helps us simplify a model, and make it more closely represent the real world.
Intrinsic attributes are those that a thing always has. Contextual attributes are those that relate to a thing in certain situations.

When modeling a thing, ask yourself if it has different behaviors in different circumstances i.e., how it is being used, not just what it is. If so, the role pattern may be useful.

Representing the concept and its roles using two Entities makes the Information Framework model more robust to change and reduces duplication.

![RoleEntity Pattern]({{ "/assets/image/RoleEntity.png" | relative_url }})

### Temporal State Pattern

The Temporal State pattern addresses the need to capture the state of an entity over time. This pattern is crucial for tracking the lifecycle of entities, such as the status of a service or product, from inception through to retirement, enabling historical analysis and future state planning.

We use this pattern when we wish to be able to show the states of an entity, the attributes for each state and the temporal or lifecycle aspects of an Entity. An Entity’s state will change over time, and we may wish to keep only the current state or a complete history, depending on the business requirements.

Separating the characteristics that we need to monitor over time into a separate entity allows us to show this more clearly than if it was shown as attributes in the entity.

Note that this pattern looks similar to the “Role Entity” pattern but represents a different concept.
The articles “Patterns for things that change with time” on Martin Fowler’s [1] web site give a good understanding of time related issues and are well worth reading.

![TemporalStateEntity Pattern]({{ "/assets/image/TemporalStateEntity.png" | relative_url }})

## The Road Ahead

As the telecommunications industry continues to evolve, the Information Framework's role in guiding CSPs through digital transformation remains critical. By embracing this framework, CSPs ensure compliance with industry standards and a foundation for future growth and innovation.

In conclusion, the TM Forum's Information Framework is more than a set of definitions and models; it's a blueprint for building agile, efficient, and scalable telecommunications services. 