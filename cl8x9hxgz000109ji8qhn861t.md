# Hive Introduction

# Why Hive?

In Big Data ecosystem we have 3 main components,

1. Distributed File System - Storage Layer
2. Map Reduce - Processing Engine
3. YARN - Resource Manager

Before Hive we(Data folks) used Java as a scripting tool to interact with these components. But many of us not comfortable at that time, then the Facebook created a framework called Hive to interact with Big data ecosystem.

Hive is altered version of SQL and Hive is a processing engine, it will work on top of Map reduce(Not a replacement of Map Reduce).

**Note:** Hive is not a Database

A typical Hive process.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1665071935429/9ytKwWHTm.png align="left")

## Hive Architecture

Lets take a look at Hive architecture,

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1665072160533/Rdu9ihV1e.png align="left")

### JDBC
  Will see very well detail about JDBC in future, for now just understand JDBC is connection medium of Hive.

### Clients
- **CLI** -> It is a command line interface for hive, just to interact with Hive from command line. **Example:** Beeline
- **Thrift** -> It can be used in scripting to allocate a particular session. **Example:** Pyspark scripts
- **Web Interface** -> It used for some analytics purposes. **Example:** Hue

### Driver
Driver is a main component of Hive and 
- It will accepts incoming request, 
- Acts like a controller for HQL statements, 
- Creates a session for queries, 
- Maintain life cycle of query, 
- Maintain meta data for execution, 
- Collect the results from map reduce and display the results.

#### SQL Process
- SQL syntax and symmetric check will be happening, 
- Execution plan will be created
- Optimization will come into picture

#### Parsing and compilation part
- Syntax and Symmetric check
- Execution plan
- Steps to get the output
- Raise compile time errors

#### Optimizer
- Compare execution plans
- Calculate the cost
- Execution plan of DAG's
- Try to place or combine transformation together

#### Executors
execute the optimized dag with help of Map reduce and send the results to HDFS.

#### Meta data
Here we have all the required meta for Hive tables. We are not storing the data here and just we are doing meta definition and the actual data stored on HDFS. 

**Derby DB**

Hive will be using **Derby** DB for their meta data as default. 
We can't create multiple connection at a time with Derby(Concurrent not possible).
So we need external DB for Hive meta for production.

**Advantages of MySQL and PostgreSQL for Hive:**
- Meta Data Back up
- Concurrent connection
- We can be use this for some another analysis and automation


 


