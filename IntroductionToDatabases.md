# Introduction to Databases
## Database
Database:  is a collection of related data and data is a collection of facts and figures that can be processed to produce information.

Some attributes used for Databases in C#:
1. The DataType attribute is used to specify a data type that's more specific than the database intrinsic type.
2. The StringLength attribute sets the maximum length in the database and provides client side and server side validation for ASP.NET Core MVC.
3. The Required attribute makes the name properties required fields,
Types that can't be null are automatically treated as required fields.
4. The Display attribute specifies what the caption for the text boxes should be.

A database management system (DBMS) stores data in such a way that it becomes easier to retrieve, manipulate, and produce information.

A modern DBMS has the following characteristics:
1. Real-world entity − A modern DBMS is more realistic and uses real-world entities to design its architecture.
2. Relation-based tables − DBMS allows entities and relations among them to form tables.
3. Less redundancy.
4. Consistency − Consistency is a state where every relation in a database remains consistent.
5. Query Language − DBMS is equipped with query language, which makes it more efficient to retrieve and manipulate data.
6. Security

## Database Schema
A database schema is an abstract design that represents the storage of your data in a database. It describes both the organization of data and the relationships between tables in a given database.

A database schema is a blueprint or architecture of how our data will look. It doesn’t hold data itself, but instead describes the shape of the data and how it might relate to other tables or models.

A database schema will include:

1. All important or relevant data
2. Consistent formatting for all data entries
3. Unique keys for all entries and database objects
4. Each column in a table has a name and data type

## Database Keys
A key in DBMS is an attribute or a set of attributes that help to uniquely identify a row in a relation (or table). Keys are also used to establish relationships between the different tables and columns of a relational database.

>There are several types of keys used in a database. The primary key is used to identify a specific row in a table. The unique key is used to ensure that there is only one entry in a specific table. A foreign key is used to link entries in one table to another. A composite key is a collection of several columns in a table that all together are used to identify a row. These keys help you to identify a particular column of a row of a table accurately and uniquely.

More details about each one:
1. Primary Key<br>
A primary key is a column of a table or a set of columns that helps to identify every record present in that table uniquely. There can be only one primary Key in a table. Also, the primary Key cannot have the same values repeating for any row. Every value of the primary key has to be different with no repetitions.

2. Foreign Key<br>
Foreign Key is used to establish relationships between two tables. A foreign key will require each value in a column or set of columns to match the Primary Key of the referential table. Foreign keys help to maintain data and referential integrity. 

3. Composite Key<br>
Composite Key is a set of two or more attributes that help identify each tuple in a table uniquely. The attributes in the set may not be unique when considered separately.

## Types of Database Relationships
### 1. One to One Relationship (1:1):<br>
It is used to create a relationship between two tables in which a single row of the first table can only be related to one and only one records of a second table. Similarly, the row of a second table can also be related to anyone row of the first table.

### 2. One to Many Relationship:<br>
It is used to create a relationship between two tables. Any single rows of the first table can be related to one or more rows of the second tables, but the rows of second tables can only relate to the only row in the first table. It is also known as a many to one relationship.

### 3. Many to Many Relationship:<br>
It is many to many relationships that create a relationship between two tables. Each record of the first table can relate to any records (or no records) in the second table. Similarly, each record of the second table can also relate to more than one record of the first table. It is also represented an N:N relationship.
For example, there are many people involved in each project, and every person can involve more than one project.

#### References: [Database](https://www.tutorialspoint.com/dbms/dbms_overview.htm), [Schema](https://www.educative.io/blog/what-are-database-schemas-examples), [Keys](https://www.upgrad.com/blog/types-of-keys-in-dbms/) and [Relationships](https://www.javatpoint.com/types-of-relationship-in-database-table).