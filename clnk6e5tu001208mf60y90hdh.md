---
title: "Software Architecture - 4"
seoTitle: "How to Document Software Architectures Effectively"
seoDescription: "Learn how to effectively document software architectures using architectural views, UML, architecture description languages and more."
datePublished: Tue Oct 10 2023 10:25:01 GMT+0000 (Coordinated Universal Time)
cuid: clnk6e5tu001208mf60y90hdh
slug: software-architecture-4
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696933374886/25aa4f43-aafd-40f2-97c9-470727c7f16b.png
tags: software-architecture, 2articles1week, architecture-design, architecture-documentation

---

# Requirements for Architecture

## **Architectural requirements**

### **Functional requirements**

Functional requirements define what the system should do or its functions and features. They include:

* System functions
    
* Business processes
    
* User tasks
    

Functional requirements shape the high-level design and modules of the system architecture.

### **Non-functional requirements**

Non-functional requirements define how well the system should perform or behave. They include:

* Performance (speed, scalability, throughput)
    
* Usability (interface design)
    
* Reliability
    
* Security
    
* Maintainability
    

Non-functional requirements constrain architectural decisions and choices.

## **Constraints and Assumptions**

These include:

* Technical constraints (hardware, software, platforms)
    
* Resource constraints (time, cost, people)
    
* Environmental constraints (operating conditions)
    

Assumptions about the system scope, users, and usage scenarios also influence the architecture.

# Architecture Life Cycle

## **Architecture Design in SDLC**

In the Software Development Life Cycle, architecture design typically happens in the following phases:

![Everything You Need to Know About SDLC - Bleuwire](https://bleuwire.com/wp-content/uploads/2020/02/software-development-life-cycle-sdlc.png align="center")

### Requirements Analysis:

* Functional and non-functional requirements are gathered from stakeholders.
    
* Initial high-level architectural decisions are made based on requirements.
    
* System scope, constraints and assumptions are documented.
    

### Design:

Detailed architectural design is done including:

* Module decomposition into subsystems and components
    
* Component allocation to tiers or layers
    
* Interface design between components
    
* Selection of architectural patterns and styles
    
* Low-level design of components is done.
    

### Implementation:

The architecture is implemented by:

* Developing individual components
    
* Integrating components through their interfaces
    
* Configuring and deploying infrastructure to support the architecture
    

### Testing:

* Unit testing of individual components
    
* Integration testing of groups of components
    
* System testing of the whole architecture:
    
* Functional testing
    
* Performance testing
    
* Stress testing
    
* Scalability testing
    

### Deployment:

* The system is deployed onto the target environment based on the defined architecture.
    
* Deployment details like server configurations, network settings, etc. are finalized.
    

### Maintenance:

The architecture evolves over time through:

* Adding new features
    
* Improving performance and scalability
    
* Changing technologies
    
* Replacing obsolete components
    
* Changes are made through iterative cycles of:
    
* Requirements analysis
    
* Design changes
    
* Implementation of changes
    
* Regression testing
    
* The architecture is continuously evaluated and improved.
    

## **Evolutionary prototyping model**

In this model, an initial architecture is designed and implemented. Then it evolves through iterations by:

* Developing prototypes
    
* Evaluating prototypes
    
* Making necessary changes to the architecture
    

This allows for continuous improvement of the architecture based on user feedback.

## **Analysis and Evaluation Methods**

The architecture is evaluated using methods like:

### **Inspections**

Experts inspect and evaluate the architecture design against requirements and quality attributes.

### **Walkthroughs**

The architecture design is presented and explained to stakeholders who provide feedback.

The architecture life cycle is iterative and evolutionary in nature. The initial architecture is designed based on requirements and then evolves through prototyping, evaluation and refinement. The architecture continues to change and improve as the system evolves over time.

# Economic Analysis Methods

## **Cost Benefit Analysis Method (CBAM)**

This method compares the costs and benefits of different architectural alternatives.

Steps in CBAM:

1. Identify architectural alternatives
    
2. Identify costs and benefits for each alternative
    
3. Quantify costs and benefits in monetary terms
    
4. Calculate the net present value (NPV) for each alternative
    
5. Select the alternative with the highest NPV
    

CBAM helps choose the alternative with the best return on investment.

Cost Benefit Analysis (CBA) evaluates alternatives based on their costs and benefits. CBA would identify things like:

* Development and implementation costs of different architectural options
    
* Expected income or productivity gains from each option
    
* Overall return on investment of each alternative
    

CBA helps choose the architectural option with the highest net present value.

## **Architecture Tradeoff Analysis Method (ATAM)**

ATAM evaluates architectural design based on:

* Quality attribute requirements
    
* Architectural approaches
    
* Trade-offs
    

The ATAM process:

1. Identify stakeholders and quality attributes
    
2. Present architectural approaches
    
3. Evaluate architectural approaches against quality attributes
    
4. Identify trade-offs
    
5. Prioritize trade-offs
    
6. Generate and evaluate risk items
    
7. Develop revised architecture based on findings
    

ATAM helps improve the architecture by identifying risks, trade-offs and mismatches with respect to quality attribute requirements.

Architecture Tradeoff Analysis Method (ATAM) evaluates architectures based on quality attributes and trade-offs. ATAM would identify things like:

* How well each architectural approach meets quality requirements like performance, security, modifiability, etc.
    
* Trade-offs between quality attributes, for example, improved security may reduce performance.
    
* Risks in the architecture that could impact quality attributes.
    

ATAM helps improve the architecture by finding ways to better meet quality requirements and manage trade-offs and risks.

# Active Reviews

Active reviews involve stakeholders actively participating in evaluating and improving the architecture.

## **Active Reviews for Intermediate Design (ARID)**

ARID is a method for reviewing architecture during the design phase. It involves:

1. Preparation  
    Identify reviewers, materials, goals and criteria
    
2. Overview  
    Present the architectural overview and design rationale
    
3. Walkthrough  
    Explain the details of the architecture and answer questions
    
4. Hypothetical Scenarios  
    Pose hypothetical scenarios to evaluate how well the architecture meets its goals
    

Example scenario: "What if there is a 10x increase in the number of users?"

1. Issues List Reviewers document issues, concerns, risks and suggestions
    
2. Negotiation  
    Discuss and negotiate resolutions for issues
    
3. Closure  
    Document action items and next steps
    
4. Follow Up  
    Implement changes and revisit unresolved issues
    

For example, during the hypothetical scenarios in an e-commerce site ARID, a scenario about a 10x increase in users uncovered that the architecture did not scale well. This led to identifying an issue around scalability and suggesting changes like using a distributed cache to improve it.

# Attribute Driven Design

Attribute Driven Design (ADD) is an architectural design process that focuses on quality attributes.

## **ADD process**

The steps in ADD are:

1. Attribute Identification Identify quality attributes that are important for the system.
    
2. Attribute Prioritization  
    Prioritize attributes based on stakeholder needs.
    
3. Architecture Synthesis Generate architectural candidates that satisfy the attributes.
    
4. Analysis and Evaluation  
    Analyze and evaluate candidates against attributes.
    
5. Decision Making  
    Select the final architecture based on analysis.
    

## **Attribute classification**

Attributes can be classified as:

* Functional: Reliability, performance, security
    
* Non-functional: Usability, maintainability, portability
    

## **Attribute-driven design decisions**

Design decisions are made to satisfy attributes, like:

* Data distribution to improve performance
    
* Caching to improve response time
    
* Module decomposition to improve maintainability
    
* Exception handling to improve reliability
    

## Example

Here are some examples of design decisions that target specific quality attributes in attribute-driven design:

Performance

* Caching frequently used data
    
* Partitioning data across multiple servers
    
* Using in-memory databases
    

Reliability

* Implementing retry mechanisms
    
* Adding redundancy through failover systems
    
* Handling exceptions gracefully
    

Maintainability

* Creating modular, loosely coupled components
    
* Abstracting low-level details into libraries and frameworks
    
* Implementing design patterns for code reuse
    

Security

* Performing input validation
    
* Encrypting sensitive data
    
* Using access control lists to restrict access
    

Usability

* Providing meaningful error messages
    
* Using familiar UI metaphors and navigation
    
* Supporting undo/redo actions
    

# Architecture Reuse

Reusing existing architectures can provide many benefits.

## **Benefits of architecture reuse**

* Faster development time
    
* Reduced development costs
    
* Increased reliability
    
* Proven designs
    

## **Methods of architecture reuse**

* Component reuse: Reusing existing architectural components to build a new system.
    
* Reference model reuse: Reusing an existing architectural model or framework as a template.
    

## **Challenges of architecture reuse**

* Matching requirements: Existing architectures may not match new requirements perfectly.
    
* Integration issues: Integrating reused components into a new system can be difficult.
    
* Incompatible styles: The style of the reused architecture may be different.
    
* Outdated technology: The reused architecture may use outdated technologies.
    

# Domain-Specific Architecture

Domain-specific architecture focuses on the architectural needs of a particular domain.

## **Concept**

A domain-specific architecture:

* Addresses the core abstractions and constraints of a domain
    
* Reuses architectural knowledge within that domain
    
* Is optimized for a specific type of system
    

Examples of domains:

* E-commerce
    
* Business information systems
    
* Real-time systems
    
* Mobile applications
    

## **Benefits and Challenges**

Benefits:

* Faster development time
    
* Architectures optimized for the domain
    

Challenges:

* Limited reusability outside the domain
    
* Requires domain knowledge
    

## **Design patterns for specific domains**

* User interface patterns for desktop, web and mobile applications
    
* Distribution patterns for real-time and embedded systems
    
* Integration patterns for enterprise information systems
    

## Example

Here are some examples of design patterns for domain-specific architectures:

Real-time systems:

* Polling - Constantly check for new data at fixed intervals
    
* Interrupt-driven - Use hardware interrupts to trigger event handlers
    
* Preemptive multitasking - Allow tasks to preempt each other to meet deadlines
    

Embedded systems:

* Event-driven - Trigger actions in response to external events
    
* Cooperative multitasking - Tasks voluntarily relinquish control
    
* Producer-consumer - For asynchronous data flow between components
    

Mobile applications:

* Model-view-controller - Separate data, UI and logic
    
* Fragment - Reusable UI components
    
* Service locator - Locate and share services across app components
    

E-commerce systems:

* Order processing - Handle order creation, validation and fulfillment
    
* Catalog management- Manage product listings and attributes
    
* Shopping cart - Maintain state of customer purchases
    

These patterns provide domain-specific solutions that address the needs of real-time systems, mobile apps, e-commerce systems and other domains. They reuse architectural knowledge within a particular domain.