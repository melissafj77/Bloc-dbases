### Exercises

Use the commands above to complete the following tasks, and submit the SQL statements. Real-world examples must be distinct from those used in the text.



>1.List the commands for adding, updating, and deleting data.
```
A:
   - Adding:  INSERT INTO, ALTER TABLE.

   - Deleting: DELETE, ALTER TABLE.

   - Updating: UPDATE, ALTER TABLE.
``` 

>2.Explain the structure for each type of command.
```
A:
   - INSERT INTO: fills up the values in the table; it requires the table name and  thecolumns  to be filled in the table must be defined. Next, you specify values for each row that needs to be inserted,  spearated by commas in the same order as the appear in the table. can insert one or more rows.
      
      INSERT INTO tableName (column1, column2, ...)

      VALUESlabor day 2018
      (column 1, column2, ...)
      (column 1, column 2, ...);

   - DELET FROM: Removes data. is irreversible, in order to delet a whole row it requres simply the name of the table and to specify one or more values to idetinfy the row we are looking to delet, is better to specify multiple values  with AND


        DELETE FROM tableName

        Where column=value AND column=value;
   
   
   - UPDATE: Changes a specific value or values in the table to dofferent value or values, it needs the table name, the new value to be set and a way to identify which of the rows will be altered, It tales multiple set clises both in set and where.

      UPDATE tableName
      SET <valueName=newValue>
      WHERE <identifies the row/s to be altered>;
```

>3.What are some of the data types that can be used in tables? Give a real-world example of each type.
```
A: numbers:
integers for the number of people in  class, floats  and doubles for money and other decimal numbers, 
Text like char for single letters like grades for a  class, text or strings, descriptions etc 
date & time, for intervals time lapsed, timestamps.
```
>4.Decide how to create a new table to hold a list of people invited to a wedding dinner. The table needs to have first and last names, whether they sent in their RSVP, the number of guests they are bringing, and the number of meals (1 for adults and 1/2 for children).

>Which data type would you use to store each of the following pieces of information?
  - First and last name.
```
  A: text
```
  - Whether they sent in their RSVP.
```  
  A: boolean
```
  - Number of guests.
``` 
 A: numeric, integer
```
 - Number of meals.
```
 A: numeric, integer.
```
 - Write a command that creates the table to track the wedding dinner.
```
 A:CREATE TABLE weddingDinner (
   firstName text,
   lastName text,
   RSVP boolean,
   guestNumber integer,
   mealNumber integer,
 );
```
-  Write a command that adds a column to track whether the guest sent a thank you card.
```   
 A: ALTER TABLE weddingDinner
    ADD COLUMN thankYouCard boolean;
```   
- You have decided to move the data about the meals to another table, so write a command to remove the column storing the number meals from the wedding table.
```
A:  ALTER TABLE weddingDInner
    DROP COLUMN mealNumber;
```
- The guests will need a place to sit at the reception, so write a command that adds a column for table number.
```
A:  ALTER TABLE weddingDinner
    ADD COLUM tableNumber intgeger;
```
- The wedding is over and we do not need to keep this information, so write a command that deletes the table numbers from the database.
```
A: DROP TABLE weddingDinner;
```

>5.Write a command to create a new table to hold the books in a library with the columns ISBN, title, author, genre, publishing date, number of copies, and available copies.
```
A:  CREATE TABLE booksList(ISBN-10 varchar (10),
  ISBN-13 varchar(13),
  title text,
  author text,
  genre text,
  pubDate date(),
  copies integer,
  availableCopies integer);
```
- Find three books and add their information to the table.
```
A:  INSERT INTO bookList (title, author, genre, pubDate, copies, availableCopies)
    VALUES
    ('9780395489314', '978-0395489314' 'The Fellowship of the ring', 'J.R.R. Tolken', 'Fantasy', 8, 2);
    ('9780395489338', '978-0395489338','The Two Towers', 'J.R.R. Tolken', 'Fantasy' 8, 5);
    ('9780395489307', '978-0395489307','The Return of The King', 'J.R.R. Tolken', 'Fantasy' 'Fantasy'9, 4);
```
- Someone has just checked out one of the books. Change the number of available copies to 1 fewer.
```
A:  UPDATE bookList
    SET availableCopies = 1
    Where title = 'The Fellowship Of The Ring' AND author = "J.R.R Tolken';
```
- Now one of the books has been added to the banned books list. Remove it from the table.
```
A:  DELETE FROM bookList
    WHERE title = 'The Return of The King';
```
>6.Write a command to make a new table to hold spacecrafts. Information should include id, name, year launched, country of origin, a brief description of the mission, orbiting body, if it is currently operating, and its approximate miles from Earth. In addition to the table creation, provide commands that perform the following operations:
```
A:  CREATE TABLE spaceCrafts(
    id varchar(8),
    name tinytext,
    yearLaunched year(),
    countryOrigin tinytext,
    description text,
    orbitingAt text),
    operating  boolean,
    distance varchar(50));
```
- Add three non-Earth-orbiting satellites to the table.
```
A:INSERT INTO spaceCrafts(id, name, yearLaunches, countryOrigin, description, orbitingAt, operating, distance)
VALUES
(124-324, 'Unimatrix1', 2016, 'France', 'This is the first expedition to the unimatrix section', 'moon' true, 238900 ),
(124-432, 'Spooky', 2015, 'Germany' 'orbiting around the asterod belts' 'asteroid belt' true, 434533240 ),
(324-123, 'heat wave' 2018, 'USA', 'the fist mission to venus', 'venus', false, 2332432454324);
```
- Remove one of the satellites from the table since it has just crashed into the planet.
```
A: DELETE FROM spaceCrafts
    WHERE id=324-123;
```
- Edit another satellite because it is no longer operating and change the value to reflect that.
```
A:  UPDATE spaceCrafts
    SET operating = false
    WHERE id=124-432;
```
>7.Write a command to create a new table to hold the emails in your inbox. This table should include an id, the subject line, the sender, any additional recipients, the body of the email, the timestamp, whether or not you have read the email, and the id of the email chain it's in. Also provide commands that perform the following operations:
```
A:  CREATE TABLE inbox(
  id integer,
  header tinytext,
  sender tinytext,
  otherCC text,
  bodt text,
  when timestamp(),
  read boolean,
  chainId integer);
```

   - Add three new emails to the inbox.
```
   A:INSERT INTO inbox(
  id, header, sender, otherCC, body, when, read, chainId)
  VALUES
  (3456, "East african lottery", "counsil of lotterys", " you didnt even play and you win because nobody wonand we selected you so now send us your bank account information and taxes we will deposit your 10000000trillion dollars", now(), yes, 1),
  (3457, "Dad's birthday", "mom", "call your father is his birthday", now(), yes, 1),
  (3455 "Cat pics", "car society" "donate money to cat charities and get free cat pics in your inbox daily", now(), no, 2);
```
   - You deleted one of the emails, so write a command to remove the row from the inbox table.
```
   A: DELETE FROM inbox
      where id= 3455;
```
   - You started reading an email but just heard a crash in another room. Mark the email as unread before investigating the crash, so you can come back and read it later.
```
   A: UPDATE inbox
    SET read = false
    WHERE id=3457;
```