# Normalization Form
Normalization rules are divided into 4 forms.

- First Normal Form

- Second Normal Form

- Third Normal form

-BCNF

First Norma Form:

AS per the first Normal Form, not two rows of data must contain repeating data i.e whenever we search for a particular result the multiple columns cannot be used to fetch the same row.

Each table should be organized into rows, each row should have a primary key that distinguishes it as unique.

For example consider a table not in first Normal Form.

| Name    |Age       |Subject
| ------- |-------   |-------
| Alice   |15        |Maths,Physics
| Charles |16        |Biology
 |Eva     |17        |Maths

Student table in 1NF will be:

| Name    |Age       |Subject
| ------- |-------   |-------
| Alice   |15        |Maths
| Alice   |15        |Physics
| Charles |16        |Biology
|Eva     |17        |Maths

Using the first Normal form, data redundancy increases, as there will be many columns with the same data in multiple rows but each row as a whole will be unique.

Second Normal Form:

As per Second Normal Form there must not be any partial dependency of any column on primary key, each column in the table that is not part of the primary key must depend upon the entire concatenated key for its existence.

   - Meet all the requirements of the first Normal form.

   - Remove subjects of any data that apply to multiple rows of a table and place them in separate tables.

   - Create relationships between these new tables and their predecessors through the use of foreign keys.

For example

New student table following 2NF will be:

| Name    |Age
| ------- |-----  
| Alice   |15       
| Charles |16       
|Eva      |17   

In the student table the candidate key will be student column, because all the other column i.e Age is dependent on it.

| Name     |Subject
| -------  |-------
| Alice    |Maths
| Alice    |Physics
| Charles  |Biology
|Eva       |Maths

In the student table the candidate key will be {student,subject} column. Now, both the above table qualifies for second Normal form and will never suffer update anomalies.

Third Normal Form:
 
  - A relation is in the third normal form (3NF) if it is in the second normal form and contains no transitive dependencies.

  -Consider relation R containing attributes A,B, and C. R(A,B,C)

  - if A -> B and B -> C then A -> C

  - Transitive Dependency: Three attributes with the above dependencies. 

  For example:

Student details table

ID| Name     |Subject|DOB|Address|Mobile No.|city
--| -------  |-------|---|------|----------|----

New student Detail table:

ID| Name     |Subject
--|----------|--------

Address table

ID|Address|DOB|Mobile No.|city
--|-------|---|----------|-----

The advantage of removing transitive dependency is,

    - Amount of data duplication is reduced.

    - Data integrity is achieved.

Boyce and Codd Normal Form (BCNF)

This is a higher version of third normal form. This form deals with certain type of anamoly that is not handled by 3NF. A 3NF table which does not have multiple overlapping candidate keys is said to be in BCNF. For a table to be in BCNF, following conditions must be satisfied:

 •	R must be in 3rd Normal Form
 
 •	and, for each functional dependency ( X -> Y ), X should be a super Key.


