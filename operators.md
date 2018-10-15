#### Exercices

1. Write out a generic SELECT statement.
```
A:  SELECT <column1, column2, ... *>
    FROM <table1, table2 ...>
    <optional: WHERE <condition>>
```

2. Create a fun way to remember the order of operations in a SELECT statement, such as a mnemonic.
```
A:SELECT FROM JOIN WHERE GROUP HAVING ORDER LIMIT
S-F-J-W-G-H-O-L
Surfers From Jakarta With Green Hair On Land
```

3. Given this dogs table, write queries to select the following pieces of data:Intake teams typically guess the breed of shelter dogs, so the breed column may have multiple words (for example, "Labrador Collie mix").

  Display the name, gender, and age of all dogs that are part Labrador.
```
A:SELECT name, gender, age
  FROM dogs
  WHERE breed LIKE '%labrador';
```
  Display the ids of all dogs that are under 1 year old.
```
A:SELECT id
  FROM dogs
  Where age < 1;
```
   Display the name and age of all dogs that are female and over 35lbs.
```
A:SELECT name, age
  FROM dogs,
  WHERE weight > 35 AND gender = 'F'
```
   - Display all of the information about all dogs that are not Shepherd mixes.
```
A:SELECT *
  FROM dogs
  WHERE breed NOT LIKE '%sheperd%';
```
   - Display the id, age, weight, and breed of all dogs that are either over 60lbs or Great Danes.
```
A:SELECT id, age, weigth, breed
  FROM dogs
  WHERE weight > 60 OR breed = 'great dane';
```

4.Given this cats table, what records are returned from these queries?

  - SELECT name, adoption_date FROM cats;
```
A:    name    | adoption_date
    ----------|--------------
    Mushi     |2016-03-22
    Seashell  |(null)
    Azul      |2016-04-17
    Victoire  |2016-09-01
    Nala      |(null)
```

  - SELECT name, age FROM cats;
```
A:  name      | age
    ----------|---------
    Mushi     |1
    Seashell  |7
    Azul      |3
    Victoire  |7
    Nala      |1

```

5.From the cats table, write queries to select the following pieces of data.
 - Display all the information about all of the available cats.
```
A:SELECT *
  FROM cats;
```
 - Display the name and sex of all cats who are 7 years old.
```
A:SELECT name, gender
  FROM cats
  WHERE age = 7
```
 - Find all of the names of the cats, so you don’t choose duplicate names for new cats.
```
A:SELECT DINSTINCT name
  FROM cats;
```
6.List each comparison operator and explain when you would use it. Include a real world example for each.
If you can’t list these from memory, do these flashcards until you can!
```
A: = equal:  when we need to match somthine exactly 1 is equal to 1 or 'car = car' 
  != not equal: when we need everything that is NOT the same. 1 is not equal to 2 or 'car' != 'Car'
  >= greater than or equal to : when you ant to get a range from  a number to all the ones bigger, the numbers from 100 to 138 are greater or equal to 100
  <= less than or equal to : reverse as the previous so get all the numbers that are less and up to  a number inclusive 0 to 100 are less or equal to 100.
  > greater than : who is bigger  4 is greater than 3
  < less than : who is smaller 2 is less than 3
  <> greater than or less than: euqivalent to not equal when we are looking for everything that is greater or smaller than a number, for example we want to know the name of anyone not 35 so greater or than or less than 35 is our criteria.
``` 
From the cats table, what data is returned from these queries?
  - SELECT name FROM cats WHERE gender = ‘F’;
```
  A:  name
    ------------
    Seashell
    Nala
```
  - SELECT name FROM cats WHERE age <> 3;
```
A:  name
-------------
  Mushi
  Seashell
  Victoire
  Nala
```
  - SELECT ID FROM cats WHERE name != ‘Mushi’ AND gender = ‘M’;
```
A:    id
    --------
    3
    4
```  
