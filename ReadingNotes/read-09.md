# https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/

Database normalization is a process used to organize a database into tables and columns.

The table should be about a specific topic and only supporting topics included.
By limiting a table to one purpose you reduce the number of duplicate data contained within your database.

There are three main reasons to normalize a database.  The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries.

There is an update anomaly- sometimes as info changes, changes need to be made in many different places.  If all of those places aren't updated inconsitiencies appear.

Deletion anomaly- deleting can sometimes cause you to lose information about other things that you need.

There are three common forms of database normalization: 1st, 2nd, and 3rd normal form. They are also abbreviated as 1NF, 2NF, and 3NF respectively

1. First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
1. Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
1. Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key.

## https://www.codeproject.com/Articles/33052/Visual-Representation-of-SQL-Joins

 seven different ways you can return data from two relational tables:

1. INNER JOIN- This is the simplest, most understood Join and is the most common. This query will return all of the records in the left table (table A) that have a matching record in the right table (table B):

SELECT <select_list> 
FROM Table_A A
INNER JOIN Table_B B
ON A.Key = B.Key

1. LEFT JOIN- This query will return all of the records in the left table (table A) regardless if any of those records have a match in the right table (table B). It will also return any matching records from the right table. This Join is written as follows:

SELECT <select_list>
FROM Table_A A
LEFT JOIN Table_B B
ON A.Key = B.Key

1. RIGHT JOIN- This query will return all of the records in the right table (table B) regardless if any of those records have a match in the left table (table A). It will also return any matching records from the left table. This Join is written as follows:

SELECT <select_list>
FROM Table_A A
RIGHT JOIN Table_B B
ON A.Key = B.Key

1. OUTER JOIN- This Join can also be referred to as a FULL OUTER JOIN or a FULL JOIN. This query will return all of the records from both tables, joining records from the left table (table A) that match records from the right table (table B). This Join is written as follows:

SELECT <select_list>
FROM Table_A A
FULL OUTER JOIN Table_B B
ON A.Key = B.Key

1. LEFT JOIN EXCLUDING INNER JOIN- This query will return all of the records in the left table (table A) that do not match any records in the right table (table B). This Join is written as follows:

SELECT <select_list> 
FROM Table_A A
LEFT JOIN Table_B B
ON A.Key = B.Key
WHERE B.Key IS NULL

1. RIGHT JOIN EXCLUDING INNER JOIN- This query will return all of the records in the right table (table B) that do not match any records in the left table (table A). This Join is written as follows:

SELECT <select_list>
FROM Table_A A
RIGHT JOIN Table_B B
ON A.Key = B.Key
WHERE A.Key IS NULL

1. OUTER JOIN EXCLUDING INNER JOIN- This query will return all of the records in the left table (table A) and all of the records in the right table (table B) that do not match. I have yet to have a need for using this type of Join, but all of the others, I use quite frequently. This Join is written as follows:

SELECT <select_list>
FROM Table_A A
FULL OUTER JOIN Table_B B
ON A.Key = B.Key
WHERE A.Key IS NULL OR B.Key IS NULL

