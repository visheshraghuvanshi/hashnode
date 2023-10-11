---
title: "Big Data - 3"
seoTitle: "Introduction to Hive and Pig | Data analytics on Hadoop"
seoDescription: "Gain an overview of Hive and Pig, two popular frameworks for data warehousing and analytics on Hadoop."
datePublished: Wed Oct 11 2023 12:10:24 GMT+0000 (Coordinated Universal Time)
cuid: clnlplj9p000a09ju89jphzzj
slug: big-data-3
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1697026112054/fefbe4d8-910a-4d85-9dc8-057e299ba978.png
tags: hadoop, big-data, hive, 2articles1week, pig

---

## Introduction to Hive

Hive is a data warehouse infrastructure built on top of Hadoop. It provides:

* A data summarization, query and analysis language called HiveQL, based on SQL.
    
* Tools to enable data extraction, transformation and loading for Hadoop datasets.
    

### **What is Hive**

Hive provides:

* A mechanism to project structure onto the data and query the data using a SQL-like language.
    
* Schema on read: The schema is imposed on the data only during the time of querying.
    
* Schema evolution: The schema for a table can be changed easily without affecting existing data.
    
* Partitioning of tables for performance gains and management of large datasets.
    
* Built-in data summarization: Aggregate functions, joining, filtering data, etc.
    

Hive enables data summarization, queries and analysis of large datasets.

### **Hive Architecture**

![Hive Architecture - Detailed Explanation - InterviewBit](https://www.interviewbit.com/blog/wp-content/uploads/2022/06/Hive-Architecture-1024x955.png align="center")

**Hive Client:** The Hive client is the interface that users interact with to issue HiveQL queries. It can be a command line interface, GUI tool or API. The client sends the queries to the Hive server.

**Hive Server:** The Hive server receives queries from clients and executes them. It consists of the following components:

* Hive Metastore Service: Manages the metadata about tables, partitions, columns, etc. It is accessed by the Hive Compiler.
    
* Hive Compiler: Parses HiveQL queries and converts them into a DAG of MapReduce jobs.
    
* Execution Engine: Executes the MapReduce jobs by scheduling them on Hadoop.
    

**Resource Management:** Hive queries are executed by utilizing the resources of the Hadoop cluster. YARN is typically used for resource management and scheduling tasks.

**Distributed Storage:** HDFS provides the distributed storage layer where Hive tables and partitions are stored. The data is split into blocks and replicated for fault tolerance.

**Processing:** Hive queries are converted into a series of MapReduce jobs that are executed in parallel across the nodes of the Hadoop cluster. The results are aggregated to generate the final output.

**Services:** In addition to the main components, Hive also utilizes services like:

* Metastore Service: Stores table schemas and other metadata.
    
* Zookeeper: Used for coordination and synchronization between Hive processes.
    
* JDBC/ODBC: Allows Hive to be accessed as a database from BI tools.
    

## Hive Data Types

Hive supports both primitive and complex data types.

### **Primitive Data Types**

* INT: 32-bit integer
    
* TINYINT: 8-bit integer
    
* SMALLINT: 16-bit integer
    
* BIGINT: 64-bit integer
    
* FLOAT: Single precision float
    
* DOUBLE: Double precision float
    
* STRING: Sequence of characters
    
* BOOLEAN: true/false
    
* TIMESTAMP: Represents date and time
    

### **Complex Data Types**

* ARRAY: An ordered collection of elements of the same type.  
    Syntax: `ARRAY<type>`
    
* STRUCT: A collection of named fields with different types.  
    Syntax: `STRUCT<col1:type1, col2:type2,...>`
    
* MAP: An unordered collection of (key,value) pairs, where the keys are strings.  
    Syntax: `MAP<type1, type2>`
    
* UNION: Represents a union of multiple types. Only one type can be present at any time.  
    Syntax: `uniontype = type1 | type2 | type3`
    

For example:

```plaintext
  name STRING,
  age INT,
  subjects ARRAY<STRING>,
  address STRUCT<street:STRING, city:STRING, pin:INT>
  marks MAP<STRING,INT>
  details UNIONTYPE<STRING, INT, DOUBLE>
```

Here:

* name is a STRING
    
* age is an INT
    
* subjects is an ARRAY of STRINGS
    
* address is a STRUCT with 3 fields
    
* marks is a MAP with string keys and int values
    
* details is a UNION of string, int and double
    

## Hive Query Language

HiveQL is Hive's SQL dialect for querying data. It is very similar to SQL but with some differences.

### **HiveQL Syntax**

The basic syntax of HiveQL statements is:

```sql
  [CREATE/DROP/ALTER/TRUNCATE] *Statement*
  SELECT * FROM table1 [JOIN table2]
  WHERE condition 
  GROUP BY column 
  HAVING condition
  ORDER BY column;
```

Some examples of HiveQL statements:

* `CREATE TABLE`: Creates a Hive table
    
* `SELECT`: Retrieves data from one or more tables
    
* `FROM`: Specifies the tables to query from
    
* `WHERE`: Filters rows
    
* `GROUP BY`: Groups rows based on a column
    
* `HAVING`: Filters groups
    
* `ORDER BY`: Sorts the result set
    
* `JOIN`: Joins two tables
    
* `INSERT INTO`: Inserts rows into a table
    
* `DROP TABLE`: Drops a table
    
* `LIMIT`: Limits the number of rows returned
    

### **Differences from SQL**

* HiveQL does not support transactions.
    
* JOINs are limited - only support CARTESIAN, LEFT OUTER and RIGHT OUTER JOINs.
    
* No subqueries or CTEs.
    
* Data types differ from SQL.
    
* Partitioning and bucketing are additional features.
    
* Functions and operators differ slightly.
    

## Introduction to Pig

### **What is Pig?**

Pig is a high-level platform for analyzing large data sets that consists of a high-level language for expressing data analysis programs, coupled with infrastructure for evaluating these programs.

* Pig Latin is the language used in Pig to analyze data.
    
* It is a platform for creating MapReduce programs without writing MapReduce code.
    
* Pig programs are translated into sequences of MapReduce jobs and executed on Hadoop.
    

Pig is ideally suited for typical data analysis tasks like:

* Data warehousing
    
* Reporting
    
* Joining/merging data from disparate sources
    
* Transforming data from one format to another
    

### **Anatomy of a Pig program**

A basic Pig program has two main parts:

The data loading and transformation part in Pig Latin. This consists of:

1. `LOAD` - To load input data
    
2. `FOREACH` - To define transformations
    
3. `FILTER` - To filter data
    
4. `JOIN` - To join relations
    
5. `GROUP` - To group data
    
6. `ORDER` - To sort data
    
7. `DISTINCT` - To remove duplicates
    

The `STORE` command to save the output.

An example program:

```sql
  -- Load input data 
  A = LOAD 'input' AS (name, age);  

  -- Define transformations   
  B = FOREACH A GENERATE name, age * 2 AS double_age;

  -- Store output
  STORE B INTO 'output';
```

This loads input data, doubles the age column, and stores the output.

## Pig on Hadoop

### **Translation to MapReduce**

Pig programs are translated into a series of MapReduce jobs which are then executed on Hadoop.

* The Pig compiler translates Pig Latin scripts into a series of MapReduce programs.
    
* These MapReduce programs are then compiled and executed on Hadoop.
    
* Pig handles the complexity of generating and executing MapReduce jobs, freeing the user from having to write MapReduce code.
    

The process of translating Pig Latin scripts to MapReduce jobs happens in three main steps:

1. Parsing - The Pig Latin script is parsed into an abstract syntax tree.
    
2. Logical optimization - The abstract syntax tree is optimized to reduce the number of MapReduce jobs.
    
    This includes:
    
    * Filter pushdown - Pushing filters up to reduce the amount of data read.
        
    * Combine pushdown - Pushing GROUP BYs before JOINs.
        
    * Constant folding - Evaluating constant expressions.
        
3. Physical optimization and code generation - The optimized logical plan is translated into a physical plan consisting of MapReduce jobs.
    
    This includes:
    
    * Generating map and reduce functions from algebraic expressions.
        
    * Splitting large jobs into multiple MapReduce jobs.
        
    * Generating job configuration parameters.
        
    * Execution - The generated MapReduce jobs are executed on Hadoop.
        

![Apache Pig - Architecture](https://www.tutorialspoint.com/apache_pig/images/apache_pig_architecture.jpg align="center")

### **Advantages of Pig**

* Pig significantly simplifies writing MapReduce programs by using a high-level language.
    
* This makes data analysis faster and easier, especially for non-Java programmers.
    
* Pig programs are concise and abstract, focusing on the data flow and not the details of MapReduce.
    
* Pig handles optimization, parallelization and execution of the MapReduce jobs.
    
* Pig programs are more scalable since they can leverage Hadoop's distributed processing.
    

## Use Case for Pig

### **ETL Processes**

One of the main use cases for Pig is for Extract, Transform and Load (ETL) processes.

* Pig is well suited for extracting data from different sources, transforming the data, and loading it into data warehouses.
    
* The high-level Pig Latin language makes it easy to write data transformation scripts for ETL.
    
* Pig's ability to execute MapReduce jobs on Hadoop allows it to handle large volumes of data.
    

Common ETL tasks Pig is used for:

* Extracting data from databases, files, APIs, etc.
    
* Transforming data - filtering, joining, grouping, merging, sorting, etc.
    
* Loading transformed data into data warehouses like Hive, HBase or HDFS files.
    

### **Data Cleaning and Transformation**

Another common use case is for cleaning and transforming raw data.

* Pig can be used to standardize data from multiple sources into a unified format.
    
* It can identify and remove duplicate, invalid or incomplete records.
    
* Pig's rich set of data transformation functions make it easy to reshape, restructure and reorganize data.
    
* The distributed processing of Hadoop enables Pig to handle large volumes of data for cleaning and transformation.
    

## ETL Processing using Pig

![ETL & ELT - Data Engineering Essentials - Analytics Vidhya](https://editor.analyticsvidhya.com/uploads/47661ETL-Process-for-linkedin3-1024x535.jpg align="center")

ETL stands for Extract, Transform and Load. It is the process of cleansing and organizing data for reporting and analysis purposes. Pig is well suited for ETL workflows due to its high-level data flow-oriented language and ability to execute MapReduce jobs on Hadoop. Here are the steps involved in an ETL process using Pig:

### **Loading data**

The first step is to load the raw data into Pig. This is done using the LOAD command. For example, to load data from a CSV file:

`raw_data = LOAD 'input.csv' USING PigStorage(',') AS (name:chararray, age:int, salary:float);`

We can load data from different sources like:

* HDFS files (text, sequence, RCFile)
    
* HBase
    
* Hive
    
* JDBC - from databases
    
* Kafka
    

The loaded data is stored in a relation that can be used for further transformations.

### **Data transformation**

Once the data is loaded, we can apply transformations using Pig's functions and operators. Common tasks are:

* Filtering irrelevant or invalid records using FILTER.
    
* Removing duplicates using DISTINCT.
    
* Converting data types using TYPECAST.
    
* Grouping and aggregating data using GROUP, COGROUP and FOREACH ... GENERATE.
    
* Joining relations using JOIN.
    
* Sorting data using ORDER BY.
    
* Splitting data into partitions using SPLIT.
    

We can apply multiple transformations on the loaded data to clean, reshape and aggregate it as required.

### **Storing results**

Finally, the transformed data is stored in the required format using the STORE command. For example:

`STORE cleaned INTO 'output' USING PigStorage (',');`

This will store the data in a CSV file. We can also store data in:

* HDFS
    
* Hive
    
* HBase
    
* Kafka
    

## Data Types in Pig

Pig supports a variety of data types to handle different kinds of data. The main types are:

### **Primitive types**

* int: Stores integer values.
    
* long: Stores long integer values.
    
* float: Stores floating point values (decimal numbers).
    
* double: Stores double precision floating point values.
    
* chararray: Stores string values.
    
* bytearray: Stores binary data.
    

For example:

`a = 1; // int`  
`b = 100L; // long`  
`c = 3.14; //float`  
`d = 'Hello'; // chararray`

### **Complex types**

* tuple: Stores a collection of related data as a single object.
    

`e = (1, 'John', 30.5); // tuple with int, chararray and float`

* bag: Stores a collection of objects of the same type. It's an unordered collection.
    

`f = {(1,'a'), (2,'b'), (3,'c')}; // bag of tuples`

* map: Stores key-value pairs. It's an unordered collection.
    

`g = [1:'a', 2:'b', 3:'c']; // map with int keys and chararray values`

* stream: Represents a continuous flow of data.
    

Pig also supports `NULL` as a type to represent missing values.

Complex types allow us to represent nested and hierarchical data structures in Pig.

Some other types:

* UNIONTYPE - Represents data that can have different types.
    
* BIGINTEGER - Represents integers with arbitrary precision.
    
* BIGDECIMAL - Represents arbitrary-precision signed decimal numbers.
    

## Running Pig Programs

### **Grunt shell**

The Grunt shell is an interactive shell for executing Pig Latin statements. It comes bundled with Pig and provides the following features:

* Interprets and executes Pig Latin statements.
    
* Provides command history and tab completion.
    
* Allows defining aliases for long relation names.
    
* Shows intermediate results after each statement.
    

We can start the Grunt shell by running the `pig` command. Then we can type Pig Latin statements and press Enter to execute them.

For example:

`pig`

`Grunt>` `data = LOAD 'student.csv' USING PigStorage(',') AS (name:chararray, age:int, score:int);`

`Grunt>` `DUMP data;`

`Grunt>` `EXIT;`

The Grunt shell is useful for testing and debugging Pig programs. However, for production jobs, it's better to use batch execution.

### **Execution model**

Pig programs are executed in the following steps:

1. The Pig Latin script is parsed into a logical plan consisting of algebraic operators.
    
2. The logical plan is optimized to reduce the number of MapReduce jobs.
    
3. The optimized logical plan is converted into a physical plan consisting of MapReduce jobs.
    
4. The MapReduce jobs are executed on the Hadoop cluster.
    
5. The output is stored as specified.
    

This execution model involves several phases:

* PARSE - Converts Pig Latin statements into a logical plan.
    
* OPTIMIZE - Optimizes the logical plan to reduce MapReduce jobs.
    
* GENERATE - Converts the optimized logical plan into a physical plan of MapReduce jobs.
    
* EXECUTE - Runs the MapReduce jobs on Hadoop.
    

For batch execution, we run the Pig program using the `pig` command as:

`pig script.pig`

This compiles and runs the program in the specified script file.

## Operators and Functions in Pig

### **Data flow operators**

These operators control the flow of data through the Pig Latin program. The main ones are:

* LOAD - Loads data from an external source into a relation.
    
* STORE - Stores a relation into an external storage source.
    
* DUMP - Prints the contents of a relation to the console. Useful for debugging.
    
* FILTER - Filters rows from a relation based on a condition.
    
* FOREACH...GENERATE - Applies transformations to each row of a relation and generates a new relation.
    

For example:

`LOAD 'data.txt' AS (name, age);`

`STORE result INTO 'output';`

`DUMP result;`

`filtered = FILTER data BY age > 30;`

`result = FOREACH filtered GENERATE name, age * 2;`

### **Filter, join, and group operators**

These operators modify or combine relations:

* FILTER - Filters rows from a relation (mentioned above).
    
* JOIN - Joins two relations based on a join condition.
    
* COGROUP - Groups data from multiple relations by a key.
    
* DISTINCT - Removes duplicate rows from a relation.
    
* LIMIT - Limits the number of rows in a relation.
    

For example:

`joined = JOIN data1 BY key, data2 BY key;`

`grouped = COGROUP data1 BY key, data2 BY key;`

`distinctData = DISTINCT data;`

### **Built-in and UDF functions**

Pig Latin provides many built-in functions to manipulate data:

* Mathematical functions - ABS(), ROUND(), CEIL(), FLOOR(), etc.
    
* String functions - TRIM(), SUBSTRING(), REPLACE(), REGEX\_EXTRACT(), etc.
    
* Logical functions - NOT(), OR(), AND(), etc.
    
* Type conversion functions - TOINTEGER(), TOFLOAT(), etc.
    

For example:

`result = FOREACH data GENERATE ROUND(column1), ABS(column2);`

We can also define User Defined Functions (UDFs) in Java or Python to extend Pig's functionality.