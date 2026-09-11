FMS vs DBMS
Entity 
Entity Type
Attribute
- Single Attribute
- Composite Attribute

Cardinality 
Tuple/field - rows
Attribute - column
Record - rows of data
Keys:
- Primary key → uniquely identifies rows in a table.
- Composite key → a primary key made of multiple columns.
- Secondary key → used for indexing, not integrity.
- Foreign key → enforces referential integrity by maintaining valid references.

Entity Relationship 
- 1:1
- 1:M
- M:M

Normalization 
- 1NF- eliminate repeating groups
- 2NF-remove functional dependency
- 3NF-remove transitive dependency

Denormalization
SQL Statement Categories:
- DML (Data Manipulation Language) → Deals with manipulating data inside tables. Examples: SELECT, INSERT, UPDATE, DELETE.

- DDL (Data Definition Language) → Defines or alters the structure of database objects. Examples: CREATE, ALTER, DROP, TRUNCATE.

- DCL (Data Control Language) → Controls access/permissions. Examples: GRANT, REVOKE.

- TCL (Transaction Control Language) → Manages transactions. Examples: COMMIT, ROLLBACK.

==DDL:==
- CREATE
- ALTER
  - add- add a primary key or column (after for adding next to a specific column)
  - modify - change the datatype
  - drop - delete a column
- DROP - deletes both table structure & data
- TRUNCATE - deletes only table data
- RENAME - change the column name 

ALTER USAGE:
```sql
alter table student add primary key(st_id);
alter table student add DOB date after st_name;
alter table student drop st_addr;
alter table student modify st_name varchar(50);
alter table student change st_name student_name varchar(50);
rename table student to participant;
truncate table participant;
drop table participant;

```

==Datatypes:==
 - INT
 - VARCHAR
 - DECIMAL
 - DATE
 - TIMESTAMP
 - TEXT
 - BOOLEAN
 - BLOB
 - ENUM

Table Creation Datatypes:
```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    email VARCHAR(100),
    age INT,
    salary DECIMAL(8,2),
    joined_date DATE,
    is_active BOOLEAN,
    status ENUM('Active','Inactive'),
    bio TEXT,
    created_at TIMESTAMP
);
```

Best Practice:

| Purpose     | Best Type    |
| ----------- | ------------ |
| ID          | INT / BIGINT |
| Name        | VARCHAR      |
| Price       | DECIMAL      |
| Date        | DATE         |
| Logs        | TIMESTAMP    |
| Description | TEXT         |
| Status      | ENUM         |

==Constraints== - Rules enforced on data columns on the table
- Primary key - `constraint pk_student primary key(st_id));`
- Foreign key
- Unique
- Not null
- Check
- A table can have one primary key, but it can have 'N' number of foreign keys, unique, not null and check constraints.

Primary Key Usage:-
```sql
CREATE TABLE TABLE_NAME(
	COLUMN_NAME1 DATATYPE(DATASIZE) PRIMARY KEY,
	COLUMN_NAME2 DATATYPE(DATASIZE),
	..
)
```

Foreign Key Usage:
```sql
CREATE TABLE TABLE_NAME(
	COLUMN_NAME1 DATATYPE(DATASIZE) PRIMARY KEY,
	COLUMN_NAME2 DATATYPE(DATASIZE),
	...,
	FOREIGN KEY (COLUMN_NAME2) REFERENCES TABLE_NAME(COLUMN_NAME)
)
```

DML:

INSERT:

```sql
Syntax
INSERT INTO TableName [(column 1, column2 ... )] VALUES (value1, value2 ... );

Example
INSERT INTO Customer VALUES (1,'Tom',9876523190,'Tom@gmail.com','Mumbai');

Specific insertion
INSERT INTO Customer (Cld,Cname,phoneno,address) VALUES
(2,'Mini',9128374605,'Chennai');

For multiple Values
INSERT INTO Customer VALUES (),(),(),();
```

- Data for date, char and varchar types should be always enclosed within single quotes.
- 

==UPDATE-==
- UPDATE ROWS IN A TABLE
	`UPDATE TableName SET ColumnName = value [,`ColumnName` = value, ... ][WHERE condition];`

- Modify existing rows with the UPDATE statement.
	`UPDATE Customer SET emailid='Tiny15@gmail.com' WHERE cname='Tiny';`

- All rows in the table are modified if we omit the WHERE clause.
	`UPDATE Customer SET emailid='Tiny15@gmail.com';`


```sql
UPDATE Customer_Master
SET Street = 'No.21,Abbey Road',
    City = 'Denver'
WHERE C_first_name = 'Emma';

```

```sql
UPDATE Venue_Master
SET Capacity = Capacity + (Capacity * 0.10)
WHERE Location = 'San Antonio';

```

In(set) → Match any of the list values
Like → Match a character pattern
Between…and → Range of values
Isnull → Checks whether a value is null or not

==DELETE:==

- `DELETE FROM _table_name_ WHERE _condition_;`

- Delete all records: `DELETE FROM _table_name_;`

- Deletion is not possible if the row to be deleted is referred in the child table

- Deletion of the parent record is made possible by using a foreign key reference option
- Reference option

	- Cascade : Deletes the row from the parent table, and automatically deletes the matching rows in the child table
	- Set null : Deletes the row from the parent table, and sets the foreign key column in the child table to NULL.
	- Restrict: Rejects the delete or update operation for the parent table

- Syntax

	- R`EFERENCES tbl_name (index_col_name, ... ) ON DELETE reference_option`
	
	- `reference_option: RESTRICT | CASCADE | SET NULL`

- ON DELETE CASCADE

	- When a record is removed from the customer table, should it also be removed from the related records in the enrollment table?
	
	- Use "on delete cascade" while creating the table

```sql
CREATE TABLE PolicyEnrollment(Enrollmentld int(5) primary key, Cid int(10), foreign key(cid) REFERENCES
customers(Cid )on delete cascade, Pid varchar(10), Duedate date, Paiddate date, penalty int(10));
```
- ON DELETE SET NULL
- If you want to set null values instead of removing the record from the transaction
- table, how do you do that?

- Use "on delete set null" while creating the table

```sql
CREATE TABLE PolicyEnrollment(Enrollmentld int(5) 
primary key, Cid int(10), foreign key(cid) 
REFERENCES customers(Cid ) 
on delete set null, Pid varchar(10), Duedate date, Paiddate date, penalty int(10));
```
- **DELETE** removes rows one by one (slow but flexible),  
- **TRUNCATE** removes all rows at once (fast but no control).
---
==DATABASE TRANSACTION:== (TCL)

1. A transaction is a logical unit of work
2. Transaction begins when DML statement is executed
3. MySql ensures data consistency based on transactions
4. Transaction should end with either Commit or Rollback
5. Transaction does consistent data change
6. DDL commands are by default auto commit

- COMMIT 
	- Ends the current transaction by making all pending data changes permanent 
- SAVEPOINT name 
	- Marks a save point within the current transaction  
- ROLLBACK TO SAVEPOINT name 
	- ROLLBACK TO SAVEPOINT rolls back the current transaction to the specified savepoint, thereby discarding any changes or savepoints created after the savepoint to which you are rolling back.
- ROLLBACK
	ROLLBACK ends the current transaction by discarding all pending data changes 

ACID PROPERTIES:

| Property    | Meaning                        |
| ----------- | ------------------------------ |
| Atomicity   | All or nothing                 |
| Consistency | Data remains valid             |
| Isolation   | Transactions don’t interfere   |
| Durability  | Data is permanent after commit |
MAIN TRANSACTION COMMANDS:

| Command                   | Purpose                   |
| ------------------------- | ------------------------- |
| BEGIN / START TRANSACTION | Starts a transaction      |
| COMMIT                    | Saves changes permanently |
| ROLLBACK                  | Cancels all changes       |
| SAVEPOINT                 | Creates a checkpoint      |
| ROLLBACK TO               | Goes back to a savepoint  |
Transaction States
A transaction passes through these stages:
1. Active → Running
2. Partially Committed → Almost done
3. Committed → Saved
4.  Failed → Error occurred
5. Aborted → Rolled back

To Disable Auto Commit:
	`SET autocommit = 0;`


Rollback:
	Data will not be saved
```sql
START TRANSACTION;
INSERT INTO students VALUES (1, 'Rahul');
ROLLBACK;
```

SAVEPOINT with ROLLBACK:
	Only Amit is Saved, Ravi is removed
```sql
START TRANSACTION;
INSERT INTO students VALUES (1, 'Amit');
SAVEPOINT s1;
INSERT INTO students VALUES (2, 'Ravi');
ROLLBACK TO s1;
COMMIT;

```

---

==SQL SELECT: for data retrieval (Data Query Language)==
- Where
- Order by - ascending or descending
- Distinct - eliminate duplicate rows
- Operators(arithmetic+comparison)
	`Select pid, minamount+(minamount*0.1) from policy;`
- Column Alias - `as`
- Concatenate Columns or Character Strings
	`Select Cname || "lives in" || Address as CustomerAddress from customer;`
 - Comparison Operators :
	 - =,>,<,>=,<=,!=,<> - `Select * from Policy where MinAmount<1500`
	 - Between ... and - Range of values
		 - `Select * from policy where MinAmount between 2500 and 5000;`
	 - in(Set) - Match any of the list of the values
		 - `Select cid, pid from policyenrollment where cid in (101,105);`
	 - Like - Match a character pattern
		 - `Select cid, cname, emailid from customer where emailid like '%yahoo%';`
	 - is null is a null value
		 - `Select * from policyenrollment where penalty is null;`
- Logical Operators:
	- And or Not
	- 'NOT' can be used with BETWEEN, IN, LIKE and IS NULL operators
	- `Select cid, cname from customer where cid=1 and address='chennai';`
 - SYNTAX:
	```sql
	SELECT [distinct] [column_name1,column_name2 ... ] | *
	FROM table_name [alias] [,table_name [alias] ..
	[WHERE conditions]
	[GROUP BY group [HAVING group_conditions]]
	[ORDER BY sort_columns[asc|desc]];
	```

- GROUPBY
```sql
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```
- HAVING -> To filter groups
- UNION
- INTERSECT
- MINUS
- EXCEPT

---
==FUNCTION:==

SCALAR FUNCTION -> 1 row
AGGREGATE FUNCTION -> Multi Row

1. Character Functions(String Functions)  
	Lower(column | exp)  Upper(column |exp)  Concat(col1|exp1,col2|exp2)  Substr(col| exp,m,n)  Length(col|exp)  Trim(col|exp)
2. Number Functions  
	Abs(col|exp)  Ceil(col|exp)  Floor(col|exp)  Mod(m,n)  Round(n,m)  Truncate(n,m)
3. Date Functions  
		ADDDATE(date, INTERVAL value unit)  Or  ADDDATE(date, days)  SUBDATE(date, INTERVAL value unit)  Or  SUBDATE(date, days)  DAYNAME(col|date)  MONTHNAME(col|date)
4. Conversion Functions  
		CAST|CONVERT to any datatype
5. Nesting Functions 
		`select cid,concat(upper(cname),' ',lower(address))as Details from customers`
6. General Functions  
		IFNULL(expr1,expr2)  NULLIF()  COALESCE()
7. Group Functions 
		AVG COUNT MAX MIN SUM,They ignore the nul values
8. Group by clause  
9. Having clause

CASE EXPRESSION:
```sql
Select column_name CASE [ expression ] WHEN condition_1 THEN result_1 WHEN condition_2 THEN result_2 ... WHEN condition_n THEN result_n ELSE result END as alias name from table_name;
```
---

==JOINS==
**JOIN** is used to combine rows from two or more tables based on a related column

Equi Join(Simple Or Inner Join)-> Equal Operator & on clause
Non-Equi Join
Self Join
Outer Join
- Left Outer Join
- Right Outer Join

| Join Type | Meaning             |
| --------- | ------------------- |
| INNER     | Matching rows only  |
| LEFT      | All left + matches  |
| RIGHT     | All right + matches |
| FULL      | All from both       |
| CROSS     | All combinations    |

JOIN Multiple Tables (Example):
	Customer → Enquiry → Booking
```sql
SELECT c.c_first_name, b.total_amount
FROM customer_master c
JOIN enquiry_master e ON c.cust_id = e.cust_id
JOIN booking_master b ON e.enquiry_id = b.enquiry_id;
```
- Always join using **primary key ↔ foreign key**.

Natural Join - inner Join or left outer join or right outer join
Cartesian Product-->Cross Join

---
SUBQUERY
A **subquery** is a query written **inside another query**.
It is used to get data that is needed by the main query.

TYPES:
Single
Multi 
Co related 

---
==DCL==
Used to create privileges to allow users to access and manipulate the database

GRANT 
REVOKE

Views ->Virtual table->Select Query
- Only display what is needed
- For Simplification & Security
- Doesn't store data, acts as a perspective of a table

SYNTAX:

```sql
CREATE OR REPLAVE VIEW VIEW_NAME AS  ( <Your SELECT Statement> )
```

```sql
CREATE VIEW view name AS select query [WITH CHECK OPTION [CONSTRAINT constraint]] [WITH READ ONLY [CONSTRAINT constraint]];
```

Deny DML operations

Simple View
Complex View

With Check option

Index 
Auto increment