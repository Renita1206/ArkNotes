# Database Management

A database is an organized, consistent and logical collection of data that can easily be accessed, updated and managed.
A tuple or a row represents a single entry in a table. An attribute or a column represents the basic units of data storage, which contain information about a particular aspect of the table. DBMS extracts data from a database in the form of queries given by the user.

DBMS stands for Database Management System, is a set of applications or programs that enable users to create and maintain a database. DBMS provides a tool or an interface for performing various operations such as inserting, deleting, updating, etc. into a database. It is software that enables the storage of data more compactly and securely as compared to a file-based system. A DBMS system helps a user to overcome problems like data inconsistency, data redundancy, etc. in a database and makes it more convenient and organized to use it.

RDBMS stands for Relational Database Management System and was introduced in the 1970s to access and store data more efficiently than DBMS. RDBMS stores data in the form of tables as compared to DBMS which stores data as files. Storing data as rows and columns makes it easier to locate specific values in the database and makes it more efficient as compared to DBMS.

The absence of indexing in a traditional file-based system leaves us with the only option of scanning the full page and hence making the access of content tedious and super slow. The other issue is redundancy and inconsistency as files have many duplicate and redundant data and changing one of them makes all of them inconsistent. Accessing data is harder in traditional file-based systems because data is unorganized in them.

Another issue is the lack of concurrency control, which leads to one operation locking the entire page, as compared to DBMS where multiple operations can work on a single file simultaneously.

Integrity check, data isolation, atomicity, security, etc. are some other issues with traditional file-based systems for which DBMSs have provided some good solutions.

### Advantages of DBMS
- Data Sharing: Data from a single database can be simultaneously shared by multiple users. Such sharing also enables end-users to react to changes quickly in the database environment.
- Integrity constraints: The existence of such constraints allows storing of data in an organized and refined manner.
- Controlling redundancy in a database: Eliminates redundancy in a database by providing a mechanism that integrates all the data in a single database.
- Data Independence: This allows changing the data structure without altering the composition of any of the executing application programs.
- Provides backup and recovery facility: It can be configured to automatically create the backup of the data and restore the data in the database whenever required.
- Data Security: DBMS provides the necessary tools to make the storage and transfer of data more reliable and secure. Authentication (the process of giving restricted access to a user) and encryption (encrypting sensitive data such as OTP, credit card information, etc.) are some popular tools used to secure data in a DBMS.


## ACID Properties
- A - Atomicity
    - An atomic action is an action that cannot be completed partiallly, the transaction is either executed completely or not at all
    - Implies that if an update occurs in a database then that update should either be reflected in the whole database or should not be reflected at all.
- C - Consistency
    - The database is consistent before and after the transaction
- I - Isolation
    - Only one process can change data during a transaction at once ie, multiple processes cannot be changing the same data at once
    - State of an ongoing transaction doesn’t affect the state of another ongoing transaction.
- D - Durable
    - The changes persist
    - Data is not lost in cases of a system failure or restart and is present in the same state as it was before the system failure or restart 

## CAP Theorem
The CAP theorem states that distributed databases can have at most two of the three properties: consistency, availability, and partition tolerance. As a result, database systems prioritize only two properties at a time.
- C - Consistency
    - The data is consistent between duplicates
    - A guarantee that every node in a distributed cluster returns the same, most recent and a successful write. Consistency refers to every client having the same view of the data.
- A - Availability
    - The data can be accessed at any time
    - Availability means that each read or write request for a data item will either be processed successfully or will receive a message that the operation cannot be completed.
- P - Partition Tolerance
    - Ability of system to run if one or more nodes go down or network fails
    - The system can be distributed across multiple nodes and is designed to operate reliably even in the face of network partitions.
![CAP theorem](image.png)
  
- CA -> RDBMS, PostgreSQL
- CP -> MongoDB, Redis
- AP -> Cassandra, CouchDB

## SQL vs NoSQL
| SQL | NoSQL |
|------------------|------------------|
| Fixed Predefined Schema | Dynamic Schema |
| Supports Complex Queries | Does not support complex queries |
| Vertically Scalable | Horizontally Scalable |
| Follows ACID properties | Does not follow ACID properties |
| Does not allow for hierarchical data | Supports data hierarchy |
| MySQL, Oracle | MongoDB, Neo4j, Cassandra |

## Levels of Abstraction
There are three levels of abstraction
- View or external - The level that describes only part of the database and hides the details of the table schema and its physical storage from the users. The result of a query is an example of View level data abstraction.  A view is a virtual table created by selecting fields from one or more tables present in the database.
- Logical or Conceptual - it is the level on which developers and system admins work and it determines what data is stored in the database and what is the relationship between the data points.
- Physical - This level consists of data storage descriptions and the details of this level are typically hidden from system admins, developers, and users.

## DBMS Languages
- DDL - Data Definition Language
    - to define the database
    - create, alter, rename, drop
- DML - Data Manipulation Language
    - to manipulate data
    - read, update, delete, insert
- DCL - Data Control Language
    - to define who gets access to what ie. permissions
    - grant, revoke
- TCL - Transaction Control Language
    - commit, savepoint, rollback


## Types of Relation
- One to one
- One to many
- Many to many
- Self Referential

## Some Important Commands
- CREATE - create a table or db
- SELECT - read
- INSERT - to insert rows
- ALTER - to change relation schema (add a column, rename col, change col datatype)
- DELETE - delete specific rows based on a condition
- TRUNCATE - delete all rows
- DROP - delete table or db

## SQL Constraints
- NOT NULL - Restricts NULL value from being inserted into a column.
- CHECK - Verifies that all values in a field satisfy a condition.
- DEFAULT - Automatically assigns a default value if no value has been specified for the field.
- UNIQUE - Ensures unique values to be inserted into the field.
- INDEX - Indexes a field providing faster retrieval of records.
- PRIMARY KEY - Uniquely identifies each record in a table.
- FOREIGN KEY - Ensures referential integrity for a record in another table.

## Types of Joins
- Inner or Natural join
- Left join
- Right join
- Full join
- Cartesian Product or Cross-join
- Self join 
    -  It is a case of regular join where a table is joined to itself based on some relation between its own column(s). Self-join uses the INNER JOIN or LEFT JOIN clause and a table alias is used to assign different names to the table within the query.

## Types of keys
- Candidate Key: The candidate key represents a set of properties that can uniquely identify a table. Each table may have multiple candidate keys. One key amongst all candidate keys can be chosen as a primary key. 
- Super Key: The super key defines a set of attributes that can uniquely identify a tuple. Candidate key and primary key are subsets of the super key, in other words, the super key is their superset.
- Primary Key: The primary key defines a set of attributes that are used to uniquely identify every tuple. 
- Unique Key: The unique key is very similar to the primary key except that primary keys don’t allow NULL values in the column but unique keys allow them. So essentially unique keys are primary keys with NULL values.
- Alternate Key: All the candidate keys which are not chosen as primary keys are considered as alternate Keys.
- Foreign Key:  The foreign key defines an attribute that can only take the values present in one table common to the attribute present in another table. 
- Composite Key:  A composite key refers to a combination of two or more columns that can uniquely identify each tuple in a table. s

## DB Anomalies
Database anomalies are the faults in the database caused due to poor management of storing everything in the flat database. It can be removed with the process of Normalization, which generally splits the database which results in reducing the anomalies in the database.
### Insertion anomaly
If a tuple is inserted in referencing relation and referencing attribute value is not present in referenced attribute, it will not allow insertion in referencing relation. These anomalies occur when it is not possible to insert data into a database because the required fields are missing or because the data is incomplete. For example, if a database requires that every record has a primary key, but no value is provided for a particular record, it cannot be inserted into the database.
### Deletion and Updation anomaly
If a tuple is deleted or updated from referenced relation and the referenced attribute value is used by referencing attribute in referencing relation, it will not allow deleting the tuple from referenced relation. Deletion anomalies occur when deleting a record from a database and can result in the unintentional loss of data. Updation anomalies occur when modifying data in a database and can result in inconsistencies or errors.
- on delete/update set null | cascade


## Normalization
Normalization reduces redundancy and insert/update/delete anomalies
- 1NF 
    - All attributes depend on the key
    - No composite attributes, multivalued attributes or nested relations
- 2NF 
    - All attributes depend on the whole key
    - Every non-prime attribute of the table should be fully functionally dependent on the primary key
- 3NF
    - All attributes depend on nothing but the key
    - There is no transitive functional dependency of one attribute on any attribute in the same table.
    - For every functional dependency of any attribute A on B (X->A)
        - X is superkey of R
        - A is a prime attribute
- BCNF - Boyce Codd Normal Form
    - For every functional dependency of any attribute A on B (A->B), A should be the super key of the table. It simply implies that A can’t be a non-prime attribute if B is a prime attribute.

- Denormalization is the reverse process of normalization as it combines the tables which have been normalized into a single table so that data retrieval becomes faster. JOIN operation allows us to create a denormalized form of the data by reversing the normalization.

## Some Important Terms
- SQL - Structured Query Language
- NULL -  NULL value is very different from that of zero and blank space as it represents a value that is assigned, unknown, unavailable, or not applicable as compared to blank space which represents a character and zero represents a number.
- ER Model - An entity-relationship model is a diagrammatic approach to a database design where real-world objects are represented as entities and relationships between them are mentioned.
- Entity - An entity is defined as a real-world object having attributes that represent characteristics of that particular object. For example, a student, an employee, or a teacher represents an entity.
- Query - A query is a request for data or information from a database table or combination of tables. A database query can be either a select query or an action query.
- Trigger - A trigger is a task that executes in response to some predefined database event, such as after a new row is added to a particular table. Specifically, this event involves inserting, modifying, or deleting table data, and the task can occur either prior to or immediately following any such event. 
- Procedure - A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again.


## Data Warehousing?
- The process of collecting, extracting, transforming, and loading data from multiple sources and storing them in one database is known as data warehousing. 
- A data warehouse can be considered as a central repository where data flows from transactional systems and other relational databases and is used for data analytics. 
- A data warehouse comprises a wide variety of an organization’s historical data that supports the decision-making process in an organization.

## Lock
A database lock is a mechanism to protect a shared piece of data from getting updated by two or more database users at the same time. When a single database user or session has acquired a lock then no other database user or session can modify that data until the lock is released.

Shared Lock: A shared lock is required for reading a data item and many transactions may hold a lock on the same data item in a shared lock. Multiple transactions are allowed to read the data items in a shared lock.
Exclusive lock: An exclusive lock is a lock on any transaction that is about to perform a write operation. This type of lock doesn’t allow more than one transaction and hence prevents any inconsistency in the database. 

