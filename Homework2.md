*Amelia Jay and Annie Flora*

**Assignment 2**

_____________

**Problem #1**  TO DO

**Ch 9, #3:** 
*Try to map the relational schema in Figure 6.14 [page 189] into an ER schema. This is part of a process known as reverse engineering, in which a conceptual schema is created for an existing implemented database. State any assumptions you make.*

_____________
**Problem #2**

**Ch 9, #7:** 
*Is it possible to successfully map a binary M:N relationship type without requiring a new relation? Why or why not?*

It is not possible to successfully map a binary M:N relationship without requiring a new relation. This is because of the M:N cardinality ratio. Creating the new relation with the primary keys of the relations that represent the participating entity types and including them as foreign keys, will create a primary key from their combination. 
_____________
**Problem #3**

**Ch 10, #3:**
*Why is it important to design the schemas and applications in parallel?*

It is important to design the schemas and applications in parallel because these two activities strongly influence eachother. For example, by analyzing database applications, we can identify data items that will be stored in the database. We also usually specify the design of database applications by referring to the database schema constructs. It ensures that the database will work well with the application. 
_____________
**Problem #4**

**Ch 10, #4:**
*Why is it important to use an implementation-independent data model during conceptual schema design? What models are used in current design tools? Wny?*

The goal of conceptual schema design is to have a complete understanding of the database structure, meaning, interrelationships, and constraints. We want to map out all of the possible schemas of the database. This is best achieved independently of a specific DBMS because each DBMS typically has idiosyncrasies and restrictions that should not be allowed to influence the conceptual schema design. Use of a high-level data model that is more expressive and general than the data models of individual DBMSs is important. We use ER and EER models. 
_____________
**Problem #5** TO DO 

**Ch 10, #6:** 
*Consider an actual application of a database system of interest. [NOTE: this means pick one you are familiar with to use for this exercise.] Define the requirements of the different levels of users in terms of data needed, types of queries, and transactions to be processed.*

_____________
**Problem #6**

**Ch 15, #5:**
*What is a functional dependency? What are the possible sources of the information that defines the functional dependencies that hold among the attributes of a relation schema?*

A functional dependency is a constraint between two sets of attributes from the database. It is a property of the semantics or meaning of the attributes. These dependencies are defined by the designer of the database. The values of the Y component of a tuple in r depend on, the values of the X component and alternatively, the values of the X component of a tuple uniquely determine the values of the Y component.

_____________
**Problem #7**

**Ch 15, #9:**
*What undesirable dependencies are avoided when a relation is in 2NF?*

Second normal form (2NF) is based on the concept of full functional dependency and avoids all partial dependencies. A relation schema R is in 2NF if every nonprime attribute A in R is fully functionally dependent on the primary key of R. For relations where primary key contains multiple attributes, no nonkey attribute should be functionally dependent on a part of the primary key.
_____________
**Problem #8**

**Ch 15, #10:** 
*What undesirable dependencies are avoided when a relation is in 3NF?*

Third normal form (3NF) is based on the concept of transitive dependency. A relation schema R is in 3NF if it satisfies 2NF and no nonprime attribute of R is transitively dependent on the primary key. The relation should not have a nonkey attribute functionally determined by another nonkey attribute (or by a set of nonkey attributes) and there should be no transitive dependency of a nonkey attribute on the primary key. 
_____________
**Problem #9**

**Ch 15, #13:**
*What is a multivalued dependencey? When does it arise?*

Multivalued dependencies are a consequence of first normal form which disallows an attribute in a tuple to have a set of values, and the accompanying process of converting an unnormalized relation into 1NF. It arises if we have two or more multivalued independent attributes in the same relation schema. This leads to a problem of having to repeat every value of one of the attributes with every value of the other attribute to keep the relation state consistent and to maintain the independence among the attributes involved.
_____________
**Problem #10**

**Ch 21, #1:**
*What is meant by the concurrent execution of database transactions in a multiuser system? Dicscuss why concurrency control is needed, and give informal examples.*

Concurrent execution of database transactions is when multiple transactions are being executed on a database at a current time. In
these systems, hundreds or thousands of users are typically operating on the database by submitting transactions concurrently to the system. Examples are databases for banks or supermarkets, airline reservation system, etc. We need concurrency control because of problems such as: the lost update problem, the temporary update problem, the incorrect summary problem, and the unrepeatable read problem. An informational example of the lost update problem would be buying tickets for a concert. If two transactions are submitted at the same time for the last 2 tickets, and both individuals would like to purchase all remaining tickets, the values of tickets left will be wrong because the second person making the transaction will be seeing the value in the database from before the first transaction was made. 
_____________
**Problem #11**

**Ch 21, #6:** 
*Discuss the atomicity, durability, isolation, and consistency preservations properties of a database transaction.*

Transactions should possess several properties, and they should be enforced by the concurrency control and recovery methods of the
DBMS: 
 - Atomicity =  A transaction is an atomic unit of processing; it should either be performed in its entirety or not performed at all.
 - Consistency preservation: A transaction should be consistency preserving. This means that if it is completely executed from beginning to end without interference from other transactions, it should take the database from one consistent state to another.
- Isolation: A transaction should appear as though it is being executed in isolation from other transactions. The execution of a transaction should not be interfered with by any other transactions executing concurrently.
- Durability: The changes applied to the database by a committed
transaction must persist in the database. These changes must not be
lost because of any failure.
_____________
**Problem #12**

**Ch 4, #1:**
*The four fundamental data constructs of Neo4j are [select one and describe each of the items in your selection]:
Table, record, field, and constraint
Node, relationship, property, and schema
Node, relationship, property, and label
Document, relationship, property, and collection*

The four fundamental data constructs of Neo4j are: Node, relationship, property, and label. 

Nodes: These are typically used to store entity information.
Relationships: These are used to connect nodes to one another explicitly and therefore provide a means of structuring your entities. They are the equivalent of an explicitly stored, and therefore pre-calculated, join-like operation in a relational database management system. Relationships always have a type, a start- and an end-node, and a direction. They can be self-referencing/looping and can never be dangling.
Properties: Both nodes and relationships are containers for properties, which are effectively name/value pairs.
Labels: Labels are a means to quickly and efficiently create subgraphs. 
_____________
**Problem #13**

**Ch 4, #3:** 
*If you have a few entities in your dataset that have lots of relationships to other entities, then you can't use a graph database because of the dense node problem.*

False – you can very effectively use a graph database, but you should take precautions, for example, applying a fan-out pattern to your data
