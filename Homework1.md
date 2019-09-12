Amelia Jay and Annie Flora

**Problem #1**

**Ch. 1 #13:**
*Give examples of systems in which it may make sense to use traditional file processing instead of a database approach.*

Sometimes DBMS involves unnecessary costs that you wouldn't get with traditional file processing due to the high initial investment in hardware, software, training, security, control etc. If you are working with simple and well-defined database applications that aren't going to change *at all*, it is probably better to use a traditional file processing approach. It is also better to go with the traditional approach if you have any stringent, real-time requirements for application programs that may not be met because of DBMS overhead. Sometimes, DBMS won't fit if you have embedded systems with limited storage capacity, so it is better to use traditional file processing. Another really important use case for traditional file processing is where you have sensitive data that you don't want to give multiple user access to. 

_____________

**Problem #2**

**Ch. 1 #14:**
*Consider figure 1.2 on pg 8 of the Elmasri book.*

*a) If the name of the 'CS' [Computer Science] Department changes to 'CSSE' [Computer Science and Software Engineering] Department and the correspondingg prefix for the course number also changes, identify the columns in the database that would need to be updated.* 

The columns `Major`, `Course_number`, `Department`, and `Prerequisite_number` would be updated. 

*b) Can you restructure the columns in the COURSE, SECTION, and PREREQUISITE tables so that only one column will need to be updated?*

_____________


**Problem #3**

**Ch. 2 #3:**
*What is the difference between a database schema and a database state?*

The database schema is the description of the database. It is specified during database design and is not expected to change frequently. The data in the database at a particular time is called a database state. It is the set of instances in the database and unlike schema it may change quite frequently. Many database states can be constructed to correspond to a particular database schema. 

_____________


**Problem #4**

**Ch. 2 #7:** 
*Discuss the different types of user-friendly interfaces and the types of users who typically use each.*

1. **Menu-Based Interfaces for Web Clients or Browsing:** These present the user with lists of options that lead the user through the formulation of a request. These are commonly used in Web-based and browsing interfaces because the users are able to look at the contents of the database in an unstructured manner; many of the users may not know the commands and syntax of a query language which is why they would prefer menus.

2. **Forms-based Interfaces:** These display a form to each user that the user can fill out to insert new data. Forms are usually designed for naive users as interfaces to canned transactions.

3. **Graphical User Interfaces:** These display a schema to the user in diagrammatic form where the user can specify a query by manipulating the diagram. GUIs utilize both menus and forms which can be used by naive users like the above mentioned interfaces.

4. **Natural Language Interfaces:** These accept requests written in English (or another language) and attempt to understand them. 


_____________


**Problem #5**

_____________


**Problem #6**

**Ch. 3 #2:** 
*Why are tuples in a relation not ordered?*

A relation is a set of tuples and elements of a set have no order among them. Therefore, tuples in a relation have no particular order.  A tuple is a set of attributes in a relation schema and the order of attributes and their values is not that important as long as the correspondence between attributes and values is maintained. Each tuple is a mapping and because of this, a tuple can be considered as a set of pairs, where each pair gives the value of the mapping from an attribute A to a value v from dom(A). The ordering of attributes is not important because the attribute name appears with its value. 

