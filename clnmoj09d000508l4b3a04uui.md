---
title: "Big Data - 4"
seoTitle: "Introduction to NoSQL and MongoDB | A Comparison with SQL"
seoDescription: "Get an overview of NoSQL databases, including what they are, differences from SQL databases, data models, use cases and examples like MongoDB and more"
datePublished: Thu Oct 12 2023 04:28:13 GMT+0000 (Coordinated Universal Time)
cuid: clnmoj09d000508l4b3a04uui
slug: big-data-4
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697084762034/4d5ab1f2-acff-4a2d-8148-734421d9335a.png
tags: nosql, mongodb, data-modeling, 2articles1week

---

## Introduction to NoSQL

## **What is NoSQL**

NoSQL stands for "Not only SQL" or "Non-relational".

* NoSQL databases provide an alternative to traditional relational databases.
    
* They are designed to overcome some limitations of relational databases:
    
    * Scaling
        
    * Agility
        
    * Performance
        
    * Flexibility
        
* Examples:
    
    * Key-Value stores: Redis, Voldemort
        
    * Document stores: MongoDB
        
    * Column stores: Cassandra, HBase
        
    * Graph databases: Neo4j, Titan
        

### **Differences from SQL databases**

* Schema
    
    * NoSQL databases have dynamic schemas
        
    * SQL databases have rigid schemas
        
* Scaling
    
    * NoSQL scales horizontally
        
    * SQL scales vertically
        
* Distribution
    
    * NoSQL is designed to be distributed
        
    * SQL is designed for single-server
        
* Query language
    
    * NoSQL uses limited query languages
        
    * SQL uses powerful SQL
        
* ACID compliance
    
    * NoSQL sacrifices ACID for performance
        
    * SQL provides ACID transactions
        
* Data model
    
    * NoSQL uses non-relational models
        
    * SQL uses a relational model
        
* Joins
    
    * NoSQL does not support joins like SQL
        

### **NoSQL data models**

![Types of NoSQL Databases - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20220405112418/NoSQLDatabases.jpg align="center")

* Key-value store
    
    * Data stored as keys associated with values
        
* Document store
    
    * Data stored as documents (JSON/BSON) with dynamic schema
        
* Column store
    
    * Data stored in columns rather than rows
        
* Graph database
    
    * Data stored as nodes and edges
        
* Wide column store
    
    * A variant of column store with column families
        
* The choice of data model depends on requirements.
    
* Each model has pros and cons in performance, scalability, flexibility, etc.
    

## Business Drivers for NoSQL

### **Scalability**

* NoSQL databases are designed to scale horizontally by adding more servers.
    
* They can scale to massive amounts of data and handle high volumes of read/write operations.
    
* This makes them suitable for applications with very large and fast-growing datasets.
    

### **Flexible schema**

* NoSQL databases have dynamic or flexible schemas as opposed to the rigid schemas of SQL databases.
    
* Schema changes do not require downtime and can be done on the fly.
    
* This agility makes NoSQL databases suitable for rapidly evolving datasets and models.
    

### **High availability**

* Most NoSQL databases are designed with high availability and fault tolerance in mind.
    
* They employ replication and data distribution techniques to ensure data is always accessible.
    
* This makes them suitable for applications that require constant uptime and access to data.
    

### **Low latency**

* Since NoSQL databases do not require complex joins and transactions, they can provide lower latency.
    
* This is especially true for read operations that can be served from memory.
    
* Low and predictable latency makes NoSQL suitable for real-time applications that have strict response time requirements.
    

## NoSQL Data Architectural Patterns

### **Key-value store**

![What is a Key Value Store? Definition & FAQs | ScyllaDB](https://www.scylladb.com/wp-content/uploads/Key-Value-Store-diagram-1-e1644958335886.png align="center")

* Data is stored as a collection of key-value pairs.
    
* Simple and fast data model.
    
* Suitable for:
    
    * Caching data
        
    * Storing session data
        
    * Storing user profiles
        
* Example databases: Redis, Voldemort
    

### **Document store**

![Relational Databases vs. NoSQL Document Databases | Lenni's Technology Blog](https://lennilobel.files.wordpress.com/2015/07/i4.png align="center")

* Data is stored as documents (JSON/BSON) with dynamic schema.
    
* Documents have a nested structure.
    
* Suitable for:
    
    * Storing and querying semi-structured data
        
    * Storing log data
        
    * Storing product catalogs
        
* Example databases: MongoDB, Couchbase
    

### **Column store**

![What is a Columnar Database? Definition and Related FAQs | HEAVY.AI](https://assets-global.website-files.com/620d42e86cb8ec4d0839e59d/6230f60beb40de5402e42afd_61c9dc6201b6e4d8debe7976_Columnar-Database-Diagram.png align="center")

* Data is stored in columns rather than rows.
    
* Columns are grouped into column families.
    
* Suitable for:
    
    * Handling large datasets with sparse data
        
    * Analytical workloads with heavy read loads
        
* Example databases: Cassandra, HBase
    

### **Graph database**

![What is a NoSQL Graph Database? | Ontotext Fundamentals](https://www.ontotext.com/wp-content/uploads/2016/06/Rich-Data-Model.png align="center")

* Data is stored as nodes and edges (relationships).
    
* Suited for data with complex relationships.
    
* Suitable for:
    
    * Social networking queries
        
    * Recommendation engines
        
    * Knowledge graphs
        
* Example databases: Neo4j, Titan
    

The choice of data model depends on:

* The type of data and queries
    
* Performance requirements
    
* Scalability requirements
    
* Data relationships
    

# Using NoSQL to Manage Big Data

### **Horizontal scaling**

* NoSQL databases are designed to scale horizontally by adding more servers.
    
* As data and traffic grow, more servers can be added to the cluster.
    
* This allows NoSQL databases to easily scale to massive amounts of big data.
    

### **Schema-less design**

* Since NoSQL databases have dynamic schemas, they can accommodate rapidly growing and changing datasets.
    
* New attributes can be added to documents on the fly without affecting existing data.
    
* This makes NoSQL a good fit for big data projects with evolving data models.
    

### **Real-time access**

* Many NoSQL databases are optimized for low latency and high throughput.
    
* They can provide real-time access to big data by caching frequently accessed data in memory.
    
* This makes NoSQL suitable for applications requiring real-time insights from big data.
    

### **Flexible queries**

* While SQL queries are powerful, they become inefficient at the big data scale.
    
* NoSQL databases offer more flexible query mechanisms that can scale to massive data volumes.
    
* This includes map-reduce functions, secondary indexes, and filtering on specific attributes.
    

## Introduction to MongoDB

### **What is MongoDB?**

* MongoDB is a popular open-source document database (NoSQL database)
    
* It stores data in flexible, JSON-like documents.
    
* It is horizontally scalable and high-performance.
    
* MongoDB is written in C++.
    

### **Data model - documents, collections, schemas**

![The MongoDB Basics: Databases, Collections & Documents | Studio 3T](https://studio3t.com/wp-content/uploads/2022/04/hierachy.png align="center")

* Data is stored in documents rather than tables.
    
* A document is a JSON-like data structure that consists of field-value pairs.
    
* Documents have a dynamic schema - different documents in a collection do not have to have the same fields.
    
* Documents with similar characteristics are grouped into collections.
    
* Collections live within databases.
    
* MongoDB has a dynamic schema - you do not define the schema in advance, it is defined by the data itself.
    

### **CRUD operations in MongoDB**

* **Create:** Use the `insert()` or `insertOne()`/`insertMany()` methods to insert documents into collections.
    
* **Read:** The `find()` and `findOne()` methods are used to query documents. You can use queries, projections and sorting.
    
* **Update:** The `update()` and `updateOne()`/`updateMany()` methods are used to update existing documents.
    
* **Delete:** The `remove()` and `deleteOne()`/`deleteMany()` methods are used to delete documents from a collection.
    

## MongoDB Architecture

### **Sharding**

![MongoDB Sharding | MongoDB](https://webimages.mongodb.com/_com_assets/cms/kyc0jb18ofictfyzk-image3.png?auto=format%252Ccompress align="center")

* Sharding allows MongoDB to split data across multiple servers.
    
* In MongoDB, sharding is done on the \_id field by default.
    
* A shard key is used to determine how data is distributed across shards.
    
* MongoDB uses a routing algorithm to determine which shard a document belongs to based on its shard key value.
    
* Sharding allows MongoDB to scale horizontally almost linearly by adding more shards.
    

### **Replication**

![Replication — MongoDB Manual](https://www.mongodb.com/docs/manual/images/replica-set-read-preference-secondary.bakedsvg.svg align="center")

* Replication in MongoDB involves copying and mirroring data on multiple servers.
    
* It provides data redundancy and high availability.
    
* MongoDB uses a primary-secondary replication model.
    
* There is one primary node that handles writes and secondaries that handle reads.
    
* When the primary node fails, a secondary is automatically elected as the new primary.
    

### **Indexing**

* Like any database, indexing improves the performance of queries in MongoDB.
    
* MongoDB supports several index types:
    
    * Single field index
        
    * Compound index
        
    * Multikey index
        
    * Hashed index
        
    * Text index
        
    * Geospatial 2d and 2dsphere index
        
* Indexes are created on one or more fields in a collection.
    
* MongoDB automatically creates indexes on the \_id field and any indexed fields.
    

## Storing Data in MongoDB

### **Insert, update, and delete documents**

* Documents are inserted into collections using the `insertOne()` and `insertMany()` methods.
    
    ```sql
    db.collection.insertOne({ name: "John", age: 30 })
    db.collection.insertMany([{ name: "Mary", age: 25 }, { name: "Steve", age: 35 }])
    ```
    
* Documents can be updated using the `updateOne()` and `updateMany()` methods.
    
    ```sql
    db.collection.updateOne({ name: "John" }, { $set: { age: 31 } })
    ```
    
* Documents can be deleted using the `deleteOne()` and `deleteMany()` methods.
    
    ```sql
    db.collection.deleteOne({ name: "John" })  
    db.collection.deleteMany({ age: { $lt: 25 } })
    ```
    

### **Embedded documents**

* MongoDB supports embedding related data as sub-documents within a document.
    
* This is useful when the related data has a one-to-one or one-to-few relationship.
    
* For example, a blog post may have embedded comments:
    
    ```json
    {
      "_id": 1,
      "title": "My First Blog",
      "body": "Lorem ipsum...",
      "comments": [
        {
          "user": "john", 
          "message": "Great blog!" 
        },
        {
          "user": "jane",
          "message": "Nice write up!"  
        }  
      ]
    }
    ```
    

### **Referencing other documents**

* MongoDB also supports referencing related data by storing the ID of the related document.
    
* This is useful when the related data has a one-to-many relationship.
    
* For example, a user document may reference many post documents:
    
    ```json
    { "name": "John", "posts": [ObjectId("5b11ca86aefd4f0474fcc4bb"), ObjectId("5b11d1cdaefd4f0474fcc4bd")] }
    
    { "_id": ObjectId("5b11ca86aefd4f0474fcc4bb"), "title": "My First Blog" }
    { "_id": ObjectId("5b11d1cdaefd4f0474fcc4bd"), "title": "My Second Blog" }
    ```
    

## Querying MongoDB Data

### **find() and findOne()**

The `find()` method is used to query documents in a collection. It returns a cursor to the matched documents.

The `findOne()` method returns only one document and is useful when you want to retrieve a single document that matches the query criteria.

Basic queries in MongoDB use the same selectors as JSON:

* Equality: `{"name": "John"}`
    
* Comparison: `{"age": {$gt: 30}}`
    
* Logical: `{"$or": [{"age": 18}, {"age": 30}]}`
    
* Regular expression: `{"name": /^J/}`
    

For example:

```sql
  db.users.find({"age": {$gt: 30}})
  db.users.findOne({"name": "John"})
```

### **Projection**

Projection allows you to specify which fields to include or exclude in the result documents.

You can project fields using the `1` to include and `0` to exclude:

```sql
  db.users.find({}, {"name": 1, "age": 1, "_id": 0})
```

### **Sorting, limiting and skipping results**

You can sort the results of a query using the `sort()` method:

```sql
  db.users.find().sort({"age": 1})  // Sort by age in ascending order
```

You can limit the number of results using the `limit()` method:

```sql
  db.users.find().limit(5)  // Limit to 5 results
```

You can skip the first `n` results using the `skip()` method:

```sql
  db.users.find().skip(5)  // Skip first 5 results
```

### **Aggregation framework**

The aggregation framework allows you to perform aggregations like:

* `$group` to group by some criteria and apply aggregate functions
    
* `$match` to filter the data
    
* `$project` to transform the data
    
* `$sort` to sort the data
    
* And many more stages.
    

For example, to calculate the average age by gender:

```php
  db.users.aggregate([
    {
      $group: {
        _id: "$gender", 
        avgAge: { $avg: "$age" } 
      }
    }
  ])
```