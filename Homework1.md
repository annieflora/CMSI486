*Amelia Jay and Annie Flora*

**Assignment 1**

_____________


**Problem #1**

**Ch. 1 #13:**
*Give examples of systems in which it may make sense to use traditional file processing instead of a database approach.*

Sometimes DBMS involves unnecessary costs that you wouldn't get with traditional file processing due to the high initial investment in hardware, software, training, security, control etc. If you are working with simple and well-defined database applications that aren't going to change *at all*, it is probably better to use a traditional file processing approach. It is also better to go with the traditional approach if you have any stringent, real-time requirements for application programs that may not be met because of DBMS overhead. Sometimes, DBMS won't fit if you have embedded systems with limited storage capacity, so it is better to use traditional file processing. Another really important use case for traditional file processing is where you have sensitive data that you don't want to give multiple user access to. 

_____________

**Problem #2**

**Ch. 1 #14:**
*Consider figure 1.2 on pg 8 of the Elmasri book.*

*a) If the name of the 'CS' [Computer Science] Department changes to 'CSSE' [Computer Science and Software Engineering] Department and the correspondingg prefix for the course number also changes, identify the columns in the database that would need to be updated.* 

The columns `Major`in STUDENT, `Course_number`in COURSE, `Course_number` in SECTION, `Department`in COURSE, and `Prerequisite_number` in PREREQUISITE would be updated. 

*b) Can you restructure the columns in the COURSE, SECTION, and PREREQUISITE tables so that only one column will need to be updated?*

You could change the naming format of courses to simply use numbers. This way, courses would be represented with a `Course_number` that does not include CS or CSSE and therefore would not need to be updated becasue each class would have its own unique number sequence. With this formatting structure, the only one column that would need to be updated would be the `Department` in COURSE. 

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

4. **Natural Language Interfaces:** These accept requests written in English (or another language) and attempt to understand them. Search engines, for example, take in a string of natural language words and match them to documents etc.

5. **Speech and Output:** There is limited use of speech as an input query or result of a query. Applications with limited vocabularies (like a telephone directory) can use this though.

6. **Interfaces for Parametric Users:** These allow people to use single function keys to invoke routine and repetitive actions. For example, bank tellers often use this type of interface because they have to perform repetitive functions like account deposits or withdrawals and balance inquiries.

7. **Interfaces for the DBA:** Most database systems have commands that can *only* be used by the DBA staff. These commands include functions to create accounts, set system parameters, grant account authorization, change a schema, and reorganize the storage structure of the database.

_____________


**Problem #5**

**Ch. 2 #14:**
*If you were designing a Web-based system to make airline reservations and sell airline tickets, which DBMS architecture would you choose from Section 2.5? Why? Why would the other architectures not be a good choice?*

The best DBMS architecture for this Web-based system would be the three-tier architecture for web applications. This is because in this architecture the client is actually a GUI that the user interacts with. The data about the airline reservations is held in a database that the web server that the GUI lives on interacts with. The web interface calls upon functions from the web server, but the application logic and the GUI do not have to live on the same machine. When both the logic and GUI have to live on the same machine, there is a heavy load put on the server which is why the basic client/server architecture and the two-tier client/server architecture aren't the best choices. The centralized DBMS architecture would not work at all because users would not be able to be on the same machine as the database at an industrial scale.

_____________


**Problem #6**

**Ch. 3 #2:** 
*Why are tuples in a relation not ordered?*

A relation is a set of tuples and elements of a set have no order among them. Therefore, tuples in a relation have no particular order.  A tuple is a set of attributes in a relation schema and the order of attributes and their values is not that important as long as the correspondence between attributes and values is maintained. Each tuple is a mapping and because of this, a tuple can be considered as a set of pairs, where each pair gives the value of the mapping from an attribute A to a value v from dom(A). The ordering of attributes is not important because the attribute name appears with its value. 

_____________


**Problem #7**

**Ch. 3 #5:**
*Why do we designate one of the candidate keys of a relation to be the primary key?*

We designate one of the candidate keys of a relation to be a primary key to make it easier to identify tuples in a relation. We choose a primary key with a single attribute or a smaller number of attributes. 

_____________


**Problem #8**

**Ch. 3 #9:**
*Define foreign key. What is this concept used for?*

A foreign key is a set of attributes in a relational schema that references the primary key of another relation. The foreign key and the primary key it references must have the same domain. This is used when cross referencing multiple relational schemas as well as joining data from multiple entities in order to manipulate it.

_____________


**Problem #9**

**Ch. 3 #13:**
*Consider the relation CLASS(Course#, Univ_Section#, Instructor_name, Semester, Building_code, Room#, Time_period, Weekdays, Credit_hours). This represents classes taught in a university, with unique Univ_section#s. Identify what you think should be various candidate keys, and write in your own words the conditions or assumptions under which each candidate key would be valid.*

`Course#` and `Univ_Section#` could be candidate keys for the relation CLASS. The `Course#` can be paired with `Univ_Section#` to create a unique value. Since each class will have a `Course#` which may not be unique to each class if there are multiple sections of all classes, but when paired with `Univ_Section#` then these can be unique and used as candidate keys. If the `Univ_Section#` is not unique to each semester, then the 2 paired with `Semester` can be candidate keys. You could also pair `Semester`, `Building_code`, `Room#`, `Time_period`, and `Weekdays`, assuming there is one class per room at a time, then you would also have a set of candidate keys. 

_____________


**Problem #10**

**Ch. 3 #20 [part c only]:**
*Recent changes in privacy laws have disallowed organizations from using Social Security numbers to identify individuals unless certain restrictions are satisfied. As a result, most U.S. universities cannot use SSNs as primary keys [except for financial data]. In practice, Student_id, a unique identifier assigned to every student, is likely to be used as the primary key rather than SSN since Student_id can be used throughout the system. What are the advantages and disadvantages of using generated [surrogate] keys?*

The advantages are that you ensure a unique identifier for each student. This will make sure there are no issues when referencing the data. The disadvantages are that they have to be generated and this takes time and space. If there are a large number of unique identifiers that need to be generated you could also run out of possible options if there is only a set amount of digits or letters that can be used. 

