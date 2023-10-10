---
title: "Software Architecture - 3"
seoTitle: "An Introduction to Software Architecture Descriptions and ADLs"
seoDescription: "Learn how to document software architectures using Architecture Description Languages. Practical examples and easy explanations..."
datePublished: Mon Oct 09 2023 14:04:47 GMT+0000 (Coordinated Universal Time)
cuid: clniysx7n000009laapey6p6e
slug: software-architecture-3
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1696860022218/2b6dcb3e-008e-490c-8f66-c4aa8572225e.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1696860121980/aa2d07ad-94ca-4009-bbc2-ec2ec4f007c1.png
tags: framework, software-architecture, 2articles1week, architectural-style, adl

---

# **Software Architecture Description Languages (ADLs)**

ADLs are formal languages used to represent the architecture of a software system. They allow architects to specify a system’s structural and behavioural properties.

For example, in Rapide ADL, the architecture of an ATM system can be specified as:

```c
  system ATM {
     component CardReader;  
     component CashDispenser;
     ...
  }
```

## **Benefits of ADLs:**

### **Basis for communication**

ADLs provide a standardized way to describe a system's architecture, allowing architects and developers to communicate and understand the design.

### **Blueprint for design and development**

ADLs serve as a blueprint that guides the design and implementation of a system. The architectural constraints specified in an ADL must be enforced during development.

### **Reusable across projects**

The notations and abstractions defined in an ADL can be reused across multiple projects within an organization.

## **Examples of ADLs:**

### **Rapide:**

Focuses on the dynamic aspects of architecture. Allows specification of architectural styles and configurations.

### **UniCon:**

Supports architectural styles like pipes and filters, blackboard and layered systems. Focuses on reusability.

### **ArTek:**

Supports object-oriented architectural styles. Focuses on modifiability and scalability.

### **Wright:**

Supports formal analysis of architectures. Allows specification of architectural styles using formal grammar.

### **Meta-H:**

Supports hierarchical architectures. Allows encapsulation of subsystems and information hiding.

## **Key Features of ADLs:**

* Support for architectural styles
    
* Modularity and hierarchy
    
* Component-based modeling
    
* Constraint specification
    
* Analysis techniques
    
* Code generation
    

# **Frameworks**

## **Struts**

Struts is a popular MVC framework for developing Java web applications. It follows the MVC architecture.

### **Advantages:**

* **Encourages good design practices**
    
    Struts enforces the separation of business logic, data and presentation which leads to a well-designed application.
    
* **Simple and easy to learn**
    
    Struts have a simple architecture and configuration. It is easy for new Java developers to pick up.
    
* **Integrated with J2EE**
    
    Struts integrate well with other J2EE technologies like JDBC, JSP, Servlets, etc.
    

### **Architecture:**

* View: JSP pages
    
* Controller: Action servlets
    
* Model: JavaBeans, DAOs
    
* Configuration: struts-config.xml
    

struts-config.xml

```xml
  <struts-config>
    <form-beans>
      <form-bean name="loginForm" ...></form-bean>
    </form-beans>  
    <action-mappings>
      <action ...>  
        <forward ...>
      </action>
    </action-mappings>
  </struts-config>
```

Action class:

```java
  public class LoginAction extends Action {
    public ActionForward execute(...) {
      if(loginSuccess()) {
        return mapping.findForward("success");
       }
       return mapping.findForward("fail");     
    }
  }
```

JSP:

```javascript
  <html:form action="/login">
    <html:text property="userName"/>
    <html:password property="password"/>
    <html:submit/>  
  </html:form>
```

## **Hibernate**

Hibernate is an object-relational mapping framework for the Java programming language. It provides a framework for mapping an object-oriented domain model to a relational database.

### **Architecture:**

* Java application code - The domain model and business logic
    
* Hibernate framework - Provides ORM functionality
    
* Java APIs - Uses JDBC, JTA and JNDI APIs to interact with the database
    
* Database - Stores data in tables
    

### **Features:**

* **Persistence of Java objects**
    
    Hibernate can persist Java objects in a relational database and retrieve them.
    
* **Object-relational impedance mismatch**
    
    Hibernate provides an object-oriented view of the database that hides the relational schema details.
    
* **Query languages**
    
    Hibernate supports both object-oriented and SQL-based query languages.
    

```javascript
  Session session = factory.openSession();

  User user = new User("John", "password");  

  session.beginTransaction();  
  session.save(user);  
  session.getTransaction().commit();

  session.close();
```

Stores the User object in the database. You can retrieve it using:

```javascript
  session.get(User.class, 1);
```

# **JavaScript Technologies**

## **Node.js**

Node.js is a JavaScript runtime environment that allows you to run JavaScript on the server side.

### **Uses:**

* Building scalable network applications and real-time servers
    
* Creating APIs and backend services
    

### **Features:**

* **Fast and scalable**
    
    Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient.
    
* **Asynchronous and event-driven**
    
    Node.js handles each request in a non-blocking manner and relies on events to trigger functions.
    
* **Single-threaded**
    
    Node.js runs in a single thread, relying on the event loop to handle concurrency.
    

For More: [https://nodejs.org/en/docs/](https://nodejs.org/en/docs/guides)

## **Angular**

Angular is a JavaScript framework for building client-side web applications.

### **Advantages:**

* **Dependency injection**
    
    Angular automatically manages the dependencies between components.
    
* **Two-way data binding**
    
    Data flows both ways between components without manual updates.
    
* **Testability**
    
    Angular makes components highly testable through built-in support for unit testing.
    
* **Model-view-controller architecture**
    
    Angular follows an MVC architecture, separating business logic from UI.
    

For More: [https://angular.io/docs](https://angular.io/docs)/

# **J2EE Technologies**

### **JSP:**

* JavaServer Pages (JSP) are used to generate dynamic web pages.
    
* JSPs contain HTML markup, scripting elements and Java code.
    
* JSPs are compiled to Servlets and executed on the server.
    

index.jsp

```xml
  <form action="process.jsp">
   Name: <input type="text" name="name">
   <input type="submit"> 
  </form>
```

process.jsp

```javascript
  <% String name = request.getParameter("name");%>
  Hello <%= name %>!
```

### **Servlets:**

* Servlets are Java programs that run on the server.
    
* They extend the functionality of the web server by generating dynamic content.
    
* Servlets handle HTTP requests and responses.
    

[HelloServlet.java](http://HelloServlet.java)

```java
  public void doGet(HttpServletRequest request,  
                    HttpServletResponse response)    
            throws ServletException, IOException {

     response.setContentType("text/html");    
     PrintWriter out = response.getWriter();    
     String name = request.getParameter("name");
     out.println("Hello " + name + "!");
  }
```

### **EJBs:**

* Enterprise JavaBeans (EJB) are server-side components that contain business logic.
    
* EJBs are used to encapsulate reusable business rules and logic.
    
* EJBs are managed by the EJB container which provides services like security, transaction management and pooling.
    

```java
  @Stateless
  public class UserService {

    @PersistenceContext
    EntityManager em;

    public void registerUser(User user) {
      em.persist(user);
    }

    // Other business methods
  }
```

The EJB is then injected into a Servlet/JSP and used.

### **JDBC:**

Java Database Connectivity API is used to connect Java applications to databases. It provides a standard interface to execute SQL statements.

### **JNDI:**

Java Naming and Directory Interface is used to access various naming and directory services like LDAP and DNS. It provides a standard API to look up and manage named objects.

### **JMS:**

Java Message Service API is used for sending messages between J2EE applications. It supports both point-to-point and publish-subscribe messaging models.

### **RMI:**

Remote Method Invocation allows a Java object to invoke methods of another Java object that exists in a different JVM. It provides remote communication between Java programs.

### **CORBA:**

Common Object Request Broker Architecture is a standard that allows objects to communicate with one another regardless of their programming language or operating system.

# **The Role of UML in Software Architecture**

Unified Modeling Language (UML) is a standardized modelling language used to visualize the design of software systems. UML can be used to model a software architecture in the following ways:

### **Class Diagrams**

Class diagrams show the types of objects in the system and their relationships. They model the static view of an architecture by showing:

* Classes
    
* Attributes
    
* Operations
    
* Relationships between classes like association, generalization, dependency, etc.
    

Class diagrams help architects model the object-oriented design of the system.

![Class Diagram - StarUML documentation](https://2107204891-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-L9shwSMiocGHpSKcbss%2F-MICRkvtgCev38ZdEOzz%2F-MICXxhUZPR6Q1UWMdUN%2FClass%20Diagram!UML%20Property_6.png?alt=media&token=cc7829d2-8dac-45fa-a4c9-00745fd212f8 align="center")

### **Component Diagrams**

Component diagrams illustrate how software is organized into components and their dependencies. They show:

* System components
    
* Interfaces
    
* Dependencies between components
    

This helps architects model the high-level design of the system in terms of its major components and interfaces.

![What is Component Diagram?](https://cdn-images.visual-paradigm.com/guide/uml/what-is-component-diagram/02-component-diagram-overview.png align="center")

### **Deployment Diagrams**

Deployment diagrams depict how software components are deployed to physical nodes or devices. They show:

* Nodes representing hardware
    
* Artifacts representing deployable software
    
* Connections showing communication between nodes
    

This models the physical deployment architecture of the system.

![Deployment Diagram - StarUML documentation](https://2107204891-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-L9shwSMiocGHpSKcbss%2F-MICiA7nW7dUuY-RKDPz%2F-MICkWhlRoCujD6QGjK6%2FBook%20Club%20Web%20Application.png?alt=media&token=7866c4d7-5b89-47b1-b327-798e33551b41 align="center")

### **Sequence Diagrams**

Sequence diagrams illustrate how objects interact and messages are passed between them over time. They show:

* Objects
    
* Messages passed between objects
    
* Time sequence
    

A sequence diagram for an emotion-based music player:

![Unified Modeling Language (UML) | Sequence Diagrams - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/cdn-uploads/seq19.png align="center")