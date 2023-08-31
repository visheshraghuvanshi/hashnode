---
title: "Software Architecture - 2"
datePublished: Fri Aug 25 2023 03:43:52 GMT+0000 (Coordinated Universal Time)
cuid: cllq1t3at000f0am40g2jc1nn
slug: software-architecture-2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1692976158043/ea9c6c7f-7feb-4b68-87b2-d259617e83aa.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1692976175140/045a1a51-1e7c-4b47-8bd4-cd1d2134d1b2.png

---

## **Software Architecture Models**

Software architecture models provide a structured approach to understanding, designing, and communicating the various aspects of a software system. These models help developers, designers, and stakeholders visualize different facets of the system, aiding in its successful design, implementation, and maintenance. Four key types of software architecture models are:

### **Structural Models:**

* Focus: Depict the static structure of the software system, including its components, relationships, and organization.
    
* Examples:
    
    * **Component Diagrams:** Illustrate high-level components and their interactions in the system.
        
    * **Class Diagrams:** Display classes, their attributes, methods, and associations, highlighting the system's object-oriented structure.
        
    * **Package Diagrams:** Group related classes into packages, showing dependencies between packages.
        

| Diagram | Description |
| --- | --- |
| **Class** | Represents the object orientation of a system. Shows how classes are statically related. |
| **Object** | Represents a set of objects and their relationships at runtime and also represents the static view of the system. |
| **Component** | Describes all the components, their interrelationship, interactions and interface of the system. |
| **Composite structure** | Describes the inner structure of the component including all classes, interfaces of the component, etc. |
| **Package** | Describes the package structure and organization. Covers classes in the package and packages within another package. |
| **Deployment** | Deployment diagrams are a set of nodes and their relationships. These nodes are physical entities where the components are deployed. |

* Purpose: Visualize the building blocks and their relationships, aiding in understanding the system's structure.
    

### **Framework Models:**

* Focus: Outline reusable architectural structures that serve as templates for designing software systems.
    
* Definition: Frameworks provide a predefined structure, conventions, and guidelines for creating applications.
    
* Purpose: Offer a blueprint to streamline system design, encourage best practices, and ensure consistency.
    
* Note: Frameworks can be technology-specific (e.g., Django for Python web applications) or domain-specific (e.g., Android framework for mobile app development).
    

### **Dynamic Models:**

* Focus: Capture the system's behaviour, interactions, and flow of activities over time.
    
* Examples:
    
    * **Sequence Diagrams:** Show the sequence of interactions among objects or components in a specific scenario.
        
    * **Activity Diagrams:** Illustrate the flow of activities, actions, and decisions in processes or workflows.
        
    * **State Diagrams:** Model the states that an object or system can transition through in response to events.
        
* Purpose: Clarify how components collaborate, data flows, and processes unfold within the system.
    

### **Process Models:**

* Focus: Describe the execution and management of processes within the software system.
    
* Examples:
    
    * **Flowcharts:** Use symbols to represent steps, decisions, and processes, showing the flow of control.
        
    * **BPMN (Business Process Model and Notation) Diagrams:** Represent business processes using standard symbols.
        
* Purpose: Offer a visual representation of how processes are carried out, aiding in understanding and improvement.
    
* Note: Process models are valuable for depicting both software-specific processes and broader business processes.
    

## **Architectural Styles**

Architectural styles define the fundamental structure and organization of a software system, shaping how its components interact, its behaviour, and its overall design. Here are some key architectural styles along with their characteristics:

### **Dataflow Architecture:**

* Emphasis: Focuses on the flow and transformation of data through processing components.
    
* Characteristics:
    
    * Components process data as it flows through the system.
        
    * Well-suited for data-intensive applications, such as data analysis or transformation systems.
        
    * Examples: ETL (Extract, Transform, Load) pipelines.
        

### **Pipes and Filters Architecture:**

* Concept: Involves a sequence of processing steps (filters) connected by data pipes.
    
* Characteristics:
    
    * Each filter performs a specific task independently.
        
    * Data flows through filters, undergoing transformation at each stage.
        
    * Suitable for scenarios where data processing can be modularized and pipelined.
        
    * Examples: Unix command line filters, audio and image processing pipelines.
        

### **Call-and-Return Architecture:**

* Concept: Modules or components call each other to accomplish tasks.
    
* Characteristics:
    
    * Collaboration through method or function calls.
        
    * Often used in procedural and object-oriented programming.
        
    * Well-organized for tasks with clear dependencies and sequential steps.
        

### **Data-Centered Architecture:**

* Focus: Centers on data storage and retrieval, often using databases.
    
* Characteristics:
    
    * Data storage is a central concern, and components interact with data repositories.
        
    * Common in database-driven applications, like content management systems or e-commerce platforms.
        

### **Layered Architecture:**

* Structure: Organizes components into distinct layers, with each layer providing specific functionality.
    
* Characteristics:
    
    * Each layer communicates only with adjacent layers.
        
    * Promotes separation of concerns and modularity.
        
    * Common in applications where clear separation between presentation, business logic, and data is crucial.
        

### **Agent-Based Architecture:**

* Focus: Revolves around autonomous agents that interact to accomplish tasks.
    
* Characteristics:
    
    * Agents are self-contained, autonomous entities capable of decision-making.
        
    * Suited for systems with distributed and complex interactions, like simulations or multi-agent systems.
        

### **Microservices Architecture:**

* Concept: Divides the system into small, independent services that communicate through APIs.
    
* Characteristics:
    
    * Each microservice focuses on a specific business capability.
        
    * Promotes scalability, ease of maintenance, and technology heterogeneity.
        
    * Well-aligned with agile development and continuous deployment practices.
        

### **Reactive Architecture:**

* Focus: Handles events and ensures responsiveness, scalability, and resilience.
    
* Characteristics:
    
    * The system reacts to events asynchronously, supporting high concurrency.
        
    * Resilience to failures and varying workloads is a key concern.
        
    * Suited for real-time systems, IoT applications, and systems with unpredictable demands.
        

### **Representational State Transfer (REST) Architecture:**

* Concept: Uses HTTP methods for communication in a stateless, client-server model.
    
* Characteristics:
    
    * Resources are identified by URLs and manipulated using standard HTTP methods.
        
    * A stateless nature simplifies scalability and caching.
        
    * Widely used for designing web APIs.