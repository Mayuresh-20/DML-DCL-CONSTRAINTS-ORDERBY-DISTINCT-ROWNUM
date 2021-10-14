# DML-DCL-CONSTRAINTS-ORDERBY-DISTINCT-ROWNUM

DML, DCL,CONSTRAINTS,ORDERBY, DISTINCT,ROWNUM

► DML(Data Manipulation Language): 
The SQL commands that deals with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

List of DML commands: 

• INSERT : It is used to insert data into a table.

• UPDATE: It is used to update existing data within a table.

• DELETE : It is used to delete records from a database table.

• LOCK: Table control concurrency.

• CALL: Call a PL/SQL or JAVA subprogram.

EXPLAIN PLAN: It describes the access path to data.

► DCL (Data Control Language): 

DCL includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions, and other controls of the database system. 

List of  DCL commands: 

• GRANT: This command gives users access privileges to the database.

• REVOKE: This command withdraws the user’s access privileges given by using the GRANT command.

► What are Constraints?

• Constraints are the rules enforced on the data columns of a table. These are used to limit the type of data that can go into a table. This ensures the accuracy and reliability of the data in the database.

Constraints could be either on a column level or a table level. The column level constraints are applied only to one column, whereas the table level constraints are applied to the whole table.

Following are some of the most commonly used constraints available in SQL. 


• NOT NULL Constraint − Ensures that a column cannot have NULL value.

• DEFAULT Constraint − Provides a default value for a column when none is specified.

• UNIQUE Constraint − Ensures that all values in a column are different.

• PRIMARY Key − Uniquely identifies each row/record in a database table.

• FOREIGN Key − Uniquely identifies a row/record in any of the given database table.

• CHECK Constraint − The CHECK constraint ensures that all the values in a column satisfies certain conditions.

• INDEX − Used to create and retrieve data from the database very quickly.

For example, to drop the primary key constraint in the EMPLOYEES table, you can use the following command.

• ALTER TABLE EMPLOYEES DROP CONSTRAINT EMPLOYEES_PK;
Some implementations may provide shortcuts for dropping certain constraints. For example, to drop the primary key constraint for a table in Oracle, you can use the following command.

• ALTER TABLE EMPLOYEES DROP PRIMARY KEY;

► Integrity Constraints

Integrity constraints are used to ensure accuracy and consistency of the data in a relational database. Data integrity is handled in a relational database through the concept of referential integrity.

► The SQL ORDER BY clause is used to sort the data in ascending or descending order, based on one or more columns. Some databases sort the query results in an ascending order by default.

Syntax
The basic syntax of the ORDER BY clause is as follows −

• SELECT column-list 

FROM table_name 

[WHERE condition] 

[ORDER BY column1, column2, .. columnN] [ASC | DESC];

![image](https://user-images.githubusercontent.com/91977965/137265486-c0fdc4a7-ea60-4402-bf1c-9b197b5403f0.png)

The following code block has an example, which would sort the result in an ascending order by the NAME and the SALARY −

SQL> 
SELECT * FROM CUSTOMERS

   ORDER BY NAME, SALARY;
   
 ![image](https://user-images.githubusercontent.com/91977965/137267569-53805f83-f398-4dfb-8863-8a7863f1d34a.png)

   

► The SQL DISTINCT keyword is used in conjunction with the SELECT statement to eliminate all the duplicate records and fetching only unique records.

There may be a situation when you have multiple duplicate records in a table. While fetching such records, it makes more sense to fetch only those unique records instead of fetching duplicate records.

Syntax
The basic syntax of DISTINCT keyword to eliminate the duplicate records is as follows −

SELECT DISTINCT column1, column2,.....columnN 

FROM table_name

WHERE [condition]


the following SELECT query returns the duplicate salary records.

SQL> SELECT SALARY FROM CUSTOMERS

   ORDER BY SALARY;
   
This would produce the following result, where the salary (2000) is coming twice which is a duplicate record from the original table.

![image](https://user-images.githubusercontent.com/91977965/137267705-ecd2a159-794f-4294-9f49-d98b0d4061d4.png)





