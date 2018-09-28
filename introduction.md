#### Exercices

>1.What data types do each of these values represent?

```
    1. "A Clockwork Orange"
            A: string
    2. 42
            A: integer
    3. 09/02/1945
            A: date
    4. 98.7
            A: float
    5. $15.99
            A: float
```

>2.Explain when a database would be used. Explain when a text file would be used.

    A: a text file is more suitable when the data will only be downloaded but rarely updated, or when is smaller amounts of simple data. and is included in the application file system (for web aps as JSON )
    A database on the other hand a database is a much more complex system that manages large amounts of data and has built in specialized structures to quickly read and manipulate data

>3.Describe one difference between SQL and other programming languages.

    A: SQL is declarative this means you describe the goal or result you want to achieve and the program figures the best way to do it; other languages are imperative procedural or object oriented, etc, in this languages you tell the program step by step how to achieve the result.

>4.In your own words, explain how the pieces of a database system fit together at a high level.

    A: i am not sure exactly where this question is going to so this is my answer.
    There is the data that is stored in persistent storage, HDD, SDD is the most common, although there is cloud storage ( at the end of the day even the cloud has to store what they store in differnt physical spaces so...),this are usually in servers although can be as small as a laptop. anyways then there is the Database management system that manages the access to and modification of the data this systems simple or complex and are managed through an interface that can be GUI or in the command line. although many databases do not have this server-side but trough clients.

>5.Explain the meaning of table, row, column, and value.

    A: The data is organzed in tables, the columns define what the data represents, each cell contains a value what is a little piece of data which meaning is indicated by the column name. and each row contains all the information of each column for a specific item in the database.

>6.List three data types that can be used in a table.

    A: strings, floats, integers.

>7.Given this payments table, provide an English description of the following queries and include their results:

     SELECT date, amount
     FROM payments;
```
        A: The date and ammounts of all payments.
---


| date                     | amount    |
| ------------------------ | --------- |
| 2016-05-01T00:00:00.000Z | 1500.0000 |
| 2016-05-10T00:00:00.000Z | 37.0000   |
| 2016-05-15T00:00:00.000Z | 124.9300  |
| 2016-05-23T00:00:00.000Z | 54.7200   |

---
```
     SELECT amount
     FROM payments
     WHERE amount > 500;

        A: All the payments where the amount is less than 500.

     SELECT *
     FROM payments
     WHERE payee = 'Mega Foods';

        A: All the columns from the payments table where the payee is Mega Foods.
```

>8.Given this users table, write SQL queries using the following criteria and include the output:


The email and sign-up date for the user named DeAndre Data.

```
SELECT email, signup
FROM users
Where name = 'DeAndre Data';
```

The user ID for the user with email 'aleesia.algorithm@uw.edu'.

```
SELECT userid
FROM users
WHERE email = 'aleesia.algorithm@uw.edu';
```

All the columns for the user ID equal to 4.

```
SELECT *
FROM users
WHERE userid = 4;
```