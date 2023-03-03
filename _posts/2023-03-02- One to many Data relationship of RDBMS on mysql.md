---
Layout:
Title:	" One to many Data relationship of RDBMS on mysql"
Date:	2023-03-02
Categories:
---

# Introduction
This week have learned about Database relationship which means how the data in 
one table is related to the data in another table.
i was mainly focused on "one to many" relationship.
# body

In RDBMS (Relational Database Management System). The term “Relational” refers to the tables with Relations. Relationships between two tables are created using keys. A key in one table will normally relate to a key in another table. Two tables in a database may also be unrelated. There are mainly 3 types of database relationships:
1,One-to-one (1:1) Relationship
2,One-to-many (1:M) Relationship
3,Many-to-many (M:M) Relationship

Well i have been focusing on "one to many" relationship and implemented it as follows: 
In One-To-Many (1:M) Relationship one records in one table relate to multiple records in another table. 

I created the database Students_portal and within the Students_portal database i created two tables i.e. Students and subjects. Then I see the One-To-Many Relationships between Students and subjects table.

In the subjects table, one Student can post multiple subjects, therefore, the subjects table may contain more than one ‘Studentid’ value for the same Student. But the same Student cannot have multiple Students in the id column.This represents the One-To-Many Relationship between the two tables.


# conclusion

The One-To-Many (1:M) Relationships is the most commonly used relationship in relational database management systems.
