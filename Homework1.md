Amelia Jay and Annie Flora

**Problem #1:**

**Ch. 1 #13:**
*Give examples of systems in which it may make sense to use traditional file processing instead of a database approach.*

Sometimes DBMS involves unnecessary costs that you wouldn't get with traditional file processing due to the high initial investment in hardware, software, training, security, control etc. If you are working with simple and well-defined database applications that aren't going to change *at all*, it is probably better to use a traditional file processing approach. It is also better to go with the traditional approach if you have any stringent, real-time requirements for application programs that may not be met because of DBMS overhead. Sometimes, DBMS won't fit if you have embedded systems with limited storage capacity, so it is better to use traditional file processing. Another really important use case for traditional file processing is where you have sensitive data that you don't want to give multiple user access to. 

**Problem #2:**

**Ch. 1 #14:**
*Consider figure 1.2 on pg 8 of the Elmasri book.*
*a) If the name of the 'CS' [Computer Science] Department changes to 'CSSE' [Computer Science and Software Engineering] Department and the correspondingg prefix for the course number also changes, identify the columns in the database that would need to be updated.* 

The columns Major, Course_number, Department, and Prerequisite_number would be updated. 

*b) Can you restructure the columns in the COURSE, SECTION, and PREREQUISITE tables so that only one column will need to be updated?*

**Problem #3:**

**Ch. 2 #3:**
*What is the difference between a database schema and a database state?*

The database schema is the description of the database. It is specified during database design and is not expected to change frequently. The data in the database at a particular time is called a database state. It is the set of instances in the database and unlike schema it may change quite frequently. Many database states can be constructed to correspond to a particular database schema. 

**Problem #4**

**Ch. 2 #7:** 
*Discuss the different types of user-friendly interfaces and the types of users who typically use each.*

__Menu-Based Interfaces for Web Clients or Browsing:__ These present the user with lists of options that lead the user through the formulation of a request. Users who would use this 


