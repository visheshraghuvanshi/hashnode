---
title: "Cloud Computing - 2"
seoTitle: "Cloud Computing Unit - 2 | RGPV | 8th Semester"
seoDescription: "Utility Computing, Elastic Computing, Ajax: asynchronous ‘rich’ interfaces, Mashups: User interface, Services Virtualization Technology ...................."
datePublished: Wed May 22 2024 01:32:28 GMT+0000 (Coordinated Universal Time)
cuid: clwh5fyow000908kx8jig7gqm
slug: cloud-computing-2
tags: ajax, 2articles1week, utility-computing, elastic-computin, mashups, services-virtualization-technology, pitfalls-of-virtualization, multitenant-software

---

## Utility Computing

#### Definition and Concept

Utility computing is a service provisioning model in which computing resources such as storage, compute power, applications, and infrastructure are offered on a pay-per-use basis. This model is analogous to traditional utilities like electricity, water, and gas, where users pay only for what they consume.

#### Historical Context

* **Early Vision**: The concept dates back to the 1960s, with American scientist John McCarthy suggesting in 1961 that computing could someday be organized as a public utility​​.
    
* **Mainframe Era**: The initial steps towards utility computing were seen in the mainframe era when IBM and other providers offered computing power to organizations like banks and government agencies​​.
    
* **Grid Computing**: In the 1990s, grid computing brought the concept to a new level by providing a distributed computing infrastructure accessible on demand, which helped in the realization of utility computing​​.
    

#### Technological Evolution

* **Internet and Web Technologies**: The widespread diffusion of the Internet and web technologies played a crucial role in realizing utility computing on a global scale. They provided the necessary infrastructure for services to be accessed and paid for on a per-use basis​​.
    
* **E-commerce and Online Services**: The growth of e-commerce in the late 1990s increased public willingness to buy online services, including computing resources. This period saw the development of infrastructures for online payment, which further supported the utility computing model​​.
    
* **Service-Oriented Architectures (SOA)**: The development of SOAs facilitated the composition of applications as a mesh of services provided by different entities, further advancing the utility computing model​​.
    

#### Cloud Computing Integration

* **Utility Computing and Cloud Computing**: Cloud computing has been recognized as a realization of the utility computing vision. It allows users to rent infrastructure, runtime environments, and services on a pay-per-use basis. This model provides flexibility, scalability, and cost-efficiency for both businesses and individual users​​.
    
* **Dynamic Provisioning**: A core feature of cloud computing that supports utility computing is dynamic provisioning, where resources are made available as needed, allowing for efficient use of IT resources​​.
    

#### Key Benefits

* **Cost Efficiency**: Users pay only for the computing resources they use, which reduces the need for significant upfront investments in IT infrastructure​​.
    
* **Scalability**: Utility computing models, especially those implemented through cloud computing, offer the ability to scale resources up or down based on demand​​.
    
* **Accessibility**: Services can be accessed from anywhere in the world, providing flexibility and convenience to users​.
    

## Elastic Computing

#### Overview

Elastic computing, often referred to as elasticity in cloud computing, is the ability to dynamically allocate and deallocate computing resources based on demand. This characteristic allows organizations to scale their IT resources efficiently, ensuring optimal performance while minimizing costs.

#### Key Concepts

1. **Self-Service Provisioning**
    
    * **Definition**: Allows users to provision and manage resources independently through a web interface without needing to go through IT departments.
        
    * **Benefits**: Reduces delays in resource allocation, accelerates development and testing processes, and enhances user autonomy.
        
    * **Example**: A developer can quickly spin up a new server for testing a new application feature without waiting for IT approval​​.
        
2. **Elasticity**
    
    * **Definition**: The ability of cloud resources to automatically scale up (expand) or scale down (shrink) based on current demands.
        
    * **Implementation**: Resources such as storage, processing power, and memory can be dynamically adjusted. For instance, a cloud application that stores customer pictures can automatically increase storage space as more pictures are uploaded​​.
        
3. **Financial Impact**: Consumers pay only for what they use, which can significantly reduce costs by avoiding over-provisioning​​.
    
4. **Dynamic Scaling**
    
    * **Automatic Scaling**: Cloud platforms can automatically allocate more resources when demand spikes and release them when demand decreases.
        
    * **On-Demand Scaling**: Users can manually adjust resource levels based on anticipated needs.
        
    * **Example**: An e-commerce website can handle increased traffic during a sale event by automatically adding more servers to manage the load and reducing them afterward​​.
        
5. **Elasticity in Infrastructure as a Service (IaaS)**
    
    * **Virtual Machines (VMs)**: Cloud VMs offer elasticity by allowing users to select different sizes (micro, small, large) and change them as needed based on the workload requirements.
        
    * **Serverless Computing**: Code is executed in stateless containers that scale resources dynamically, charging only for what is used. This is particularly beneficial for applications with variable workloads​​.
        
6. **Multicloud Strategy**
    
    * **Definition**: Utilizing multiple cloud service providers to optimize performance, cost, and reliability.
        
    * **Benefits**: Increases redundancy, allows for workload distribution across different geographical regions, and provides flexibility in selecting the best services from various providers​​.
        

#### Advantages of Elastic Computing

* **Cost Efficiency**: Reduces the need to invest in excess capacity that may only be used sporadically.
    
* **Scalability**: Supports business growth by easily accommodating increased demands.
    
* **Flexibility**: Provides the ability to quickly respond to changes in workload and resource requirements.
    
* **Resource Optimization**: Ensures that resources are used efficiently, reducing waste and improving performance.
    

#### Practical Applications

* **Web Applications**: Scale up during peak usage times and scale down during off-peak times.
    
* **Big Data Processing**: Allocate massive resources for data processing tasks and deallocate them after completion.
    
* **DevOps**: Provision and decommission environments for development, testing, and production as needed.
    

## Ajax: asynchronous ‘rich’ interfaces

**Definition and Overview:** AJAX (Asynchronous JavaScript and XML) is a conceptual framework that leverages JavaScript and XML to enable asynchronous behavior in web applications. This approach allows for the dynamic update of web content without reloading the entire web page, leading to richer, more interactive user experiences. AJAX operates by making asynchronous requests to the server, exchanging data, and updating parts of a webpage based on server responses.

**Core Components:**

1. **JavaScript:** The scripting language used to handle events, manipulate the Document Object Model (DOM), and make asynchronous calls to the server.
    
2. **XML (or JSON):** The data format used for exchanging information between the client and server. JSON (JavaScript Object Notation) is often preferred over XML due to its lighter syntax, which reduces the amount of data transferred.
    
3. **XMLHttpRequest Object:** The object used in JavaScript to send and receive data asynchronously to and from the server.
    

**Functionality:**

* **Asynchronous Communication:** AJAX allows web applications to send and retrieve data from a server asynchronously in the background without interfering with the display and behavior of the existing page.
    
* **Partial Page Updates:** Only parts of the web page that need to change are updated, rather than reloading the entire page, resulting in a smoother and faster user experience.
    
* **Improved User Interaction:** AJAX facilitates more responsive and dynamic web interfaces by allowing users to interact with a web page without waiting for the entire page to reload.
    

**Advantages:**

* **Reduced Server Load:** Since only necessary data is sent and received, AJAX can reduce the amount of data transmitted between the client and server, leading to reduced server load and bandwidth usage.
    
* **Enhanced User Experience:** The ability to update parts of a web page without a full reload leads to a more seamless and faster user experience.
    
* **Real-Time Data Display:** AJAX enables real-time updates of web content, which is particularly useful for applications that require up-to-the-minute information, such as news feeds, live scores, and chat applications.
    

**Example Use Cases:**

* **Live Search:** As a user types into a search box, AJAX can be used to fetch search suggestions from the server and display them in real-time.
    
* **Form Validation:** AJAX can be used to validate form input on the server side in real-time, providing immediate feedback to the user without requiring a page reload.
    
* **Dynamic Content Loading:** Content such as news articles, images, or comments can be loaded dynamically as the user scrolls, improving the browsing experience and reducing initial load times.
    

**AJAX and Web 2.0:** AJAX is a fundamental technology of Web 2.0, which emphasizes user-generated content, usability, and interoperability for end users. By allowing web applications to update asynchronously, AJAX contributes to creating more dynamic and interactive websites, enhancing the overall user experience and enabling the development of rich internet applications (RIAs).

**Service Orientation and Cloud Computing:** AJAX-based clients are an integral part of cloud computing services. They facilitate interaction with cloud-based applications, delivering services through web browsers and enabling a vision of "Everything as a Service" (XaaS)​.

## Mashups: User interface

Mashups in the context of user interfaces are web applications that integrate data, presentation, or functionality from multiple sources to create new, composite services. These mashups are essential for modern web development, enabling the creation of rich, interactive user experiences by leveraging existing web services and APIs. Here are the key points on user interface mashups:

#### Characteristics of Mashups

1. **Combination of Data and Services**: Mashups aggregate content and services from different sources, often through APIs, to present a unified interface. For example, combining maps from Google Maps with local business data.
    
2. **Virtualization and Aggregation**: They leverage virtualization to combine resources and present them seamlessly to the user.
    
3. **Cost-Effectiveness**: Mashups can significantly reduce the cost for startups and businesses by utilizing existing web services instead of building everything from scratch.
    

#### Example of Cloud Mashup: AWS and GAE

A practical example of a cloud mashup involves integrating Amazon Web Services (AWS) with Google App Engine (GAE) to combine their strengths:

* **Google App Engine (GAE)**: Primarily used for creating web interfaces and managing user interactions.
    
* **Amazon Web Services (AWS)**: Utilized for heavy computational tasks and storage through services like EC2 and S3.
    

This integration allows businesses to use GAE for frontend user interactions while leveraging AWS for backend processing, thereby enhancing scalability and agility.

#### Steps in Creating a Mashup

1. **Data Collection**: Retrieve data from multiple sources using APIs.
    
2. **Data Processing**: Process and possibly aggregate the data using cloud services.
    
3. **Presentation**: Present the combined data in a user-friendly interface.
    

#### Advantages of Mashups

* **Scalability**: Mashups can dynamically scale resources based on demand. For example, scaling MapReduce operations on AWS from a single node to multiple nodes to handle large datasets.
    
* **Agility**: Provides businesses with the flexibility to quickly adapt and integrate new services, enhancing their ability to compete in the market.
    
* **User Experience**: Enhances the user experience by providing a richer, more interactive interface that combines multiple services seamlessly.
    

### Practical Example

A mashup could involve a social networking portal that needs to manage large amounts of data and ensure high availability. By using AWS for storage and computation and GAE for managing user interfaces, the startup can keep operational costs low while ensuring scalability and performance.

## Services Virtualization Technology: Virtualization applications in enterprises

Virtualization technology plays a crucial role in modern enterprises by enabling efficient resource management, improving system flexibility, and reducing operational costs. Virtualization abstracts the underlying hardware, allowing multiple virtual machines (VMs) to run on a single physical server, each with its own operating system and applications.

**Key Applications in Enterprises:**

1. **Server Consolidation:**
    
    * **Purpose:** Reduces the number of physical servers by running multiple VMs on a single server.
        
    * **Benefits:** Enhances hardware utilization, reduces costs related to hardware, space, power, and cooling, and simplifies management.
        
    * **Example:** Data centers often have many underutilized servers. Virtualization consolidates these into fewer servers, leading to significant cost savings and improved resource usage​​.
        
2. **Enhanced Resource Management:**
    
    * **Dynamic Allocation:** Resources like CPU, memory, and storage can be allocated dynamically based on demand, improving efficiency and ensuring high availability.
        
    * **Scheduling and Automation:** Advanced scheduling and automation techniques enable optimal resource allocation and management, ensuring quality of service (QoS) and efficient power management​​.
        
3. **Disaster Recovery and High Availability:**
    
    * **VM Migration:** VMs can be easily moved between physical servers without downtime, facilitating disaster recovery and ensuring business continuity.
        
    * **Backup Services:** Virtualization allows for efficient backup and restoration of entire VMs, improving data protection and recovery capabilities​​.
        
4. **Development and Testing:**
    
    * **Sandbox Environments:** VMs provide isolated environments for development and testing, allowing developers to experiment without affecting production systems.
        
    * **Rapid Provisioning:** New VMs can be quickly created and destroyed, enabling faster development cycles and more efficient testing processes​​.
        
5. **Security and Isolation:**
    
    * **Isolated Environments:** Each VM operates in isolation from others, enhancing security by preventing one compromised VM from affecting others.
        
    * **Multi-Tenancy:** Virtualization supports multi-tenancy, allowing different users or departments to share the same physical infrastructure securely​.
        
6. **Support for Legacy Applications:**
    
    * **Compatibility:** Virtualization enables older applications to run on modern hardware and operating systems by encapsulating them in VMs, extending their useful life.
        
    * **Cost Savings:** Avoids the need for costly application rewrites or hardware upgrades to maintain legacy systems​.
        

## Pitfalls of virtualization, Multitenant software

### Pitfalls of Virtualization

**1\. Performance Degradation**  
Virtualization can introduce significant performance issues due to the overhead required to maintain the virtual environment. Some specific causes of performance degradation include:

* Maintaining the status of virtual processors.
    
* Trapping and simulating privileged instructions.
    
* Supporting paging within the virtual machine (VM).
    
* Console functions. Performance can be particularly affected when the virtualization layer is managed by a program running atop the host OS, as the virtual machine manager (VMM) must compete with other applications for resources​​.
    

**2\. Inefficiency and Degraded User Experience**  
Inefficiencies arise because some features of the host system may not be fully exposed by the virtualization layer. This can lead to scenarios where:

* Device drivers are not fully supported by the virtual machine.
    
* Certain features of the underlying OS are inaccessible without specific libraries. These inefficiencies can limit the capabilities of the virtualized environment and degrade user experience​​.
    

**3\. Security Vulnerabilities**  
Virtualization introduces new security risks, such as the potential for malicious programs to emulate a host environment and extract sensitive information from the guest. This risk is heightened by the ability to preload malicious programs before the OS boots, acting as a thin virtual machine manager to intercept data​.

### Multitenant Software

**1\. Multi-entity Support**  
Multi-entity support in cloud data stores allows for the storage of multiple entities within a single database. Entities can be efficiently organized using `PartitionKey` and `RowKey`, which help speed up search performance and ensure each entity is uniquely identifiable. This flexible schema is designed to scale well with distributed computing environments​.

**2\. Multi-schema Approach**  
The multi-schema approach in a cloud environment supports the storage of diverse data structures within a single database. This flexibility allows for the storage of both structured and unstructured data, making it easier to manage different types of data under one schema. The approach ensures that as data grows, the system can scale accordingly without major restructuring​.

**3\. Multi-tenancy Using Cloud Data Stores**  
Multi-tenancy in cloud environments means that a single instance of the software serves multiple users. Each user's data is isolated and secured, ensuring no data leakage between tenants. The advantages of multi-tenancy include:

* Cost savings from shared resources.
    
* Simplified maintenance and updates.
    
* Configurability without altering the underlying codebase, which simplifies upgrades.
    
* Improved vendor commitment to uptime and performance, as service disruptions impact all tenants​.