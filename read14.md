#  DATABASE NORMALIZATION

![](https://res.cloudinary.com/practicaldev/image/fetch/s--xnJ9XB9B--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://cdn.filestackcontent.com/SGIy2EgRQN4f28VaUYBS)

Database normalization is a database schema design technique, by which an existing schema is modified to minimize redundancy and dependency of data.

Normalization split a large table into smaller tables and define relationships between them to increases the clarity in organizing data.

## Database Normalization Rules

* First Normal Form (1NF)

Each column is unique in 1NF.

![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/Normalisation_normalforms_1.png)

* Second Normal Form (2NF)

The entity should be considered already in 1NF, and all attributes within the entity should depend solely on the unique identifier of the entity.

![](https://www.w3schools.in/wp-content/uploads/2014/08/Second-Normal-Form-2NF.png)

* Third Normal Form (3NF)

The entity should be considered already in 2NF, and no column entry should be dependent on any other entry (value) other than the key for the table.

If such an entity exists, move it outside into a new table.

3NF is achieved, considered as the database is normalized.

![](https://i0.wp.com/teachallaboutit.school/wp-content/uploads/2019/12/3NF.png?resize=578%2C404&ssl=1)

* Boyce-Codd Normal Form (BCNF)

3NF and all tables in the database should be only one primary key.



![](https://www.studytonight.com/dbms/images/BCNF.png)

* Fourth Normal Form (4NF)

Tables cannot have multi-valued dependencies on a Primary Key.



![](https://slideplayer.com/slide/3817886/13/images/25/Fourth+Normal+Form+A+table+is+in+4NF+if.jpg)


* Fifth Normal Form (5NF)

A composite key shouldn't have any cyclic dependencies.

Well, this is a highly simplified explanation for Database Normalization. One can study this process extensively, though. After working with databases for some time, you'll automatically create Normalized databases, as it's logical and practical.