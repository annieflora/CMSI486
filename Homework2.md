*Amelia Jay and Annie Flora*

**Assignment 2**

_____________

**Problem #1**

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

It is important to design the schemas and applications in parallel because these two activities strongly influence eachother. For example, by analyzing database
applications, we can identify data items that will be stored in the database. We also usually specify the design of database applications by referring to the database schema constructs. 
_____________
**Problem #4**

**Ch 10, #4:**
*Why is it important to use an implementation-independent data model during conceptual schema design? What models are used in current design tools? Wny?*

**FINISH**

The goal of conceptual schema design is to have a complete understanding of the
database structure, meaning, interrelationships, and constraints. This is best achieved independently of a specific DBMS because each DBMS typically has idiosyncrasies and restrictions that should not be allowed to influence the conceptual schema design. The conceptual schema is invaluable as a stable description of the database
contents. The choice of DBMS and later design decisions may change without
changing the DBMS-independent conceptual schema. A good understanding of the conceptual schema is crucial for database users and application designers. Use of a high-level data model that is more expressive and general than the data models of individual DBMSs is therefore quite important. The diagrammatic description of the conceptual schema can serve as a vehicle of communication among database users, designers, and analysts. Because high-level data models usually rely on concepts that are easier to
understand than lower-level DBMS-specific data models, or syntactic definitions
of data, any communication concerning the schema design becomes
more exact and more straightforward.
_____________
**Problem #5**

**Ch 10, #6:** 
*Consider an actual application of a database system of interest. [NOTE: this means pick one you are familiar with to use for this exercise.] Define the requirements of the different levels of users in terms of data needed, types of queries, and transactions to be processed.*

_____________
**Problem #6**

**Ch 15, #5:**
*What is a functional dependency? What are the possible sources of the information that defines the functional dependencies that hold among the attributes of a relation schema?*

A functional dependency is a formal constraint among attributes that is the main tool for formally measuring the appropriateness of attribute groupings into relation schemas.  
_____________
**Problem #7**

**Ch 15, #9:**
*What undesirable dependencies are avoided when a relation is in 2NF?*

_____________
**Problem #8**

**Ch 15, #10:** 
*What undesirable dependencies are avoided when a relation is in 3NF?*

_____________
**Problem #9**

**Ch 15, #13:**
*What is a multivalued dependencey? When does it arise?*

_____________
**Problem #10**

**Ch 21, #1:**
*What is meant by the concurrent execution of database transactions in a multiuser system? Dicscuss why concurrency control is needed, and give informal examples.*

_____________
**Problem #11**

**Ch 21, #6:** 
*Discuss the atomicity, durability, isolation, and consistency preservations properties of a database transaction.*

_____________
**Problem #12**

**Ch 4, #1:**
*The four fundamental data constructs of Neo4j are [select one and describe each of the items in your selection]:
Table, record, field, and constraint
Node, relationship, property, and schema
Node, relationship, property, and label
Document, relationship, property, and collection*

_____________
**Problem #13**

**Ch 4, #3:** 
*If you have a few entities in your dataset that have lots of relationships to other entities, then you can't use a graph database because of the dense node problem.
True – you will have to use a relational system
True – but there is no alternative, so you will have to live with it
False – you can still use a graph database but it will be painfully slow for all queries
False – you can very effectively use a graph database, but you should take precautions, for example, applying a fan-out pattern to your data*
