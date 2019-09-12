Amelia Jay and Annie Flora

**Problem #1**

**Ch. 1 #13:**
*Give examples of systems in which it may make sense to use traditional file processing instead of a database approach.*

> Sometimes DBMS involves unnecessary costs that you wouldn't get with traditional file processing due to the high initial investment in hardware, software, training, security, control etc. If you are working with simple and well-defined database applications that aren't going to change *at all*, it is probably better to use a traditional file processing approach. It is also better to go with the traditional approach if you have any stringent, real-time requirements for application programs that may not be met because of DBMS overhead. Sometimes, DBMS won't fit if you have embedded systems with limited storage capacity, so it is better to use traditional file processing. Another really important use case for traditional file processing is where you have sensitive data that you don't want to give multiple user access to. 

______________

**Problem #2**

**Ch. 1 #14:**

*a. If the name of the 'CS' [Computer Science] Department changes to 'CSSE' [Computer Science and Software Engineering] Department and the correspondingg prefix for the course number also changes, identify the columns in the database that would need to be updated.*

> The `Major` column in the `STUDENT` table, the `Course_number` column in the `COURSE`, `SECTION`, and `PREREQUISITE` tables, the `Department` column in the `COURSE` table, and the `Prerequisite_number` column in the `PREREQUISITE` table.

*b. Can you restructure the columns in the COURSE, SECTION, and PREREQUISITE tables so that only one column will need to be updated?*




