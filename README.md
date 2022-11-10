# NOSQL

**NoSQL** Database is a non-relational Data Management System that provides a mechanism for storage and retrieval of data, that does not require a fixed schema. It avoids joins and is easy to scale. The primary purpose of using a NoSQL database is for distributed data stores with humongous data storage needs. NoSQL is used for Big data and real-time web apps. 

RDBMS uses SQL syntax to store and retrieve data for further insights. Instead, a NoSQL database system encompasses a wide range of database technologies that can store structured, semi-structured, unstructured, and polymorphic data.

![image](https://user-images.githubusercontent.com/117327677/201009690-83c7633c-fb54-43ec-b9f9-9ca3b385c0f4.png)

Fig.1: Data models for NoSQL databases

## Characteristics of NoSQL Database:
### 1:Complex-free working
Unlike SQL databases, NoSQL databases are not complicated. They store data in an unstructured or semi-structured form that require no relational or tabular arrangement. Perhaps they are easier to use and can be accomplished by all.
### 2: Independent of Schema
Secondly, NoSQL databases are independent of schemas which implies that they can be run over without any predetermined schemas.
	That said, they are far more efficient to work with and perhaps this particular feature works well for young programmers and organizations handling large amounts of heterogeneous data that requires no schemas to structure it.

### 3: Better Scalability
One of the most prominent features of such a database is that it has high scalability which makes it suitable for large amounts of data.
	Needless to mention that contemporary data scientists often prefer to work with NoSQL databases due to this feature since it allows them to accommodate humongous data without rupturing its efficacy.
### 4: Flexible to accommodate
Since such databases can accommodate heterogeneous data that requires no structuring, they are claimed to be flexible in terms of their usage and reliability.
	For beginners intending to try their hands in the field, NoSQL databases are easy to handle yet very useful.
### 5: Durable
If durability is not one of its most striking features, then what is? NoSQL databases are highly durable as they can accommodate data ranging from heterogeneous to homogeneous.
	Not only can they accommodate structured data, but they can also incorporate unstructured data that requires no query language. Undoubtedly, these databases are durable and efficient.
## Types of NoSQL Databases:
NoSQL Databases are mainly categorized into four types: Key-value pair, Column-oriented, Graph-based and Document-oriented. Every category has its unique attributes and limitations. None of the above-specified databases is better to solve all the problems. Users should select the database based on their product needs.
   
### 1: Key-value Pair Based

Data is stored in key/value pairs. It is designed in such a way as to handle lots of data and heavy load. Key-value pair store data as a hash table where each key is unique, and the value can be a JSON, BLOB(Binary Large Objects), string, etc.
Key value stores help the developer to store schema-less data. Redis, Dynamo, and Riak are some NoSQL examples of key-value store DataBases. They are all based on Amazon’s Dynamo paper.
### 2: Column-oriented 
Column-oriented databases work on columns and are based on BigTable paper by Google. Every column is treated separately. Values of single-column databases are stored contiguously. They deliver high performance on aggregation queries like SUM, COUNT, AVG, MIN, etc. as the data is readily available in a column. Column-based NoSQL databases are widely used to manage data warehouses, CRM, Library card catalogs,
HBase, Cassandra, HBase, and Hypertable are NoSQL query examples of column-based databases.
### 3:Graph Graphs based 
A graph-type database stores entities as well the relations amongst those entities. The entity is stored as a node with the relationship as edges. An edge gives a relationship between nodes. Every node and edge has a unique identifier.
Compared to a relational database where tables are loosely connected, a Graph database is multi-relational. Traversing relationships as fast as they are already captured in the DB, and there is no need to calculate them.
Graph base database mostly used for social networks, logistics, and spatial data.
Neo4J, Infinite Graph, OrientDB, and FlockDB are some popular graph-based databases.
### 4:Document-oriented 
Document-Oriented NoSQL DB stores and retrieves data as a key value pair but the value part is stored as a document. The document is stored in JSON or XML formats. The value is understood by the DB and can be queried. Now for the relational database, you have to know what columns you have and so on. However, for a document database, you have data stored like a JSON object. You do not require to define which makes it flexible.
The document type is mostly used for CMS systems, blogging platforms, real-time analytics & e-commerce applications. It should not use for complex transactions which require multiple operations or queries against varying aggregate structures.
Amazon SimpleDB, CouchDB, and MongoDB, Riak, Lotus Notes, MongoDB, are popular Document originated DBMS systems.


## When should NoSQL be used:
1. When a huge amount of data needs to be stored and retrieved.
2. The relationship between the data you store is not that important.
3. The data changes over time and is not structured.
4. Support of Constraints and Joins is not required at the database level.
5. The data is growing continuously and you need to scale the database regularly to handle the data.

## Here are a couple of examples of some NoSQL databases:
## • MongoDB
The most popular NoSQL database, is an open-source document-oriented database. It means that MongoDB isn’t based on the table-like relational database structure but provides an altogether different mechanism for the storage and retrieval of data. This format of storage is called BSON ( similar to JSON format).  MongoDB is a NoSQL database that scales by adding more and more servers and increases productivity with its flexible document model.

### Where do we use MongoDB?

MongoDB is preferred over RDBMS in the following scenarios:

**Big Data:** If you have a huge amount of data to be stored in tables, think of MongoDB before RDBMS databases. MongoDB has a built-in solution for partitioning and sharding your database.

**Unstable Schema:** Adding a new column in RDBMS is hard whereas MongoDB is schema-less. Adding a new field does not affect old documents and will be very easy.

**Distributed data** Since multiple copies of data are stored across different servers, recovery of data is instant and safe even if there is a hardware failure.
    
## • Cassandra
Apache Cassandra is an open-source, distributed, and decentralized/distributed storage system (database), for managing very large amounts of structured data spread out across the world. It provides highly available service with no single point of failure.

### Listed below are some of the notable points of Apache Cassandra −

It is scalable, fault-tolerant, and consistent.

It is a column-oriented database.

Its distribution design is based on Amazon’s Dynamo and its data model on Google’s Bigtable.

Created at Facebook, it differs sharply from relational database management systems.

Cassandra implements a Dynamo-style replication model with no single point of failure but adds a more powerful “column family” data model.

Cassandra is being used by some of the biggest companies such as Facebook, Twitter, Cisco, Rackspace, eBay,, Twitter, Netflix, and more.
    
## • Redis
		
Redis is an open-source database that supports many different data structures such as strings, lists, hashes, sets, sorted sets, etc. It is written in ANSI C and it can be used with almost all programming languages and Linux and OS X operating systems. Redis works with an in-memory dataset to preserve its extremely fast performance and the implementation uses the fork system call to create a duplicate of the current process with the data so that the parent process can continue its operations with the existing clients and the child process can create a data copy on the disk.	
    
## • Apache CouchDB

Apache CouchDB is an open-source project and a single-node database that allows you to easily store your data and access it when you need it. Couch DB can also scale up for more demanding projects into a cluster of nodes with multiple servers. It supports the HTTP protocol along with the JSON data format and also integrates with HTTP proxy servers. Apache CouchDB is designed for reliability with a crash-resistant structure that supports “Offline First” applications and a system that saves data redundantly so that it is never lost and available in a state of emergency.
## • Apache HBase

Apache HBase is an open-source distributed Hadoop database that can be used to read and write big data. HBase has been constructed so that it can manage billions of rows and millions of columns using commodity hardware clusters. This database is based on the Big Table which was a distributed storage system created for structured data. Apache HBase has many different capabilities including scalability, automatic sharding of tables,  consistent reading and writing capabilities, support against failure for all the servers, etc.

## Reference:
* https://www.guru99.com/nosql-tutorial.html

* https://www.mongodb.com/nosql-explained

* https://www.youtube.com/watch?v=0buKQHokLK8

* https://www.geeksforgeeks.org


