## Questions

#### 1.  Return ALL the data in the 'movies' table.
```
SELECT * FROM movies;
```
#### 2.  Return ONLY the name column from the 'people' table
```
SELECT name FROM people;
```
#### 3.  Oops! Someone at CodeClan spelled Rose's name wrong! Change it to reflect the proper spelling ('Rose' not 'Ros').
```
UPDATE people SET name = 'Rose Ulldemolins' WHERE name LIKE 'Ros%';
```
#### 4.  Return ONLY your name from the 'people' table.
```
SELECT name FROM people WHERE name = 'James Berry';
```
#### 5.  The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.
```
DELETE FROM movies WHERE title LIKE 'Batman%';
```
#### 6.  Create a new entry in the 'people' table with the name of one of the instructors.
```
INSERT INTO	people (name) VALUES ('Keith Douglas');
```
#### 7.  Donald Trump has decided to hijack our movie evening, Remove him from the table of people.
```
DELETE FROM people WHERE name = 'Donald Trump';
```
#### 8.  The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this.
```
INSERT INTO movies (title, year, show_time) VALUES ('Avengers: Infinity War', 2018, '00:00');
```
#### 9.  The cinema would also like to make the Guardians movies a back to back feature. Find out the show time of "Guardians of the Galaxy" and set the show time of "Guardians of the Galaxy 2" to start two hours later.
```
SELECT (title, show_time) FROM movies WHERE title LIKE 'Guardians of the Galaxy%';

UPDATE movies SET show_time = '16:25' WHERE title = 'Guardians of the Galaxy 2';

SELECT (title, show_time) FROM movies WHERE title LIKE 'Guardians of the Galaxy%';
```

## Extension

#### 1.  Research how to delete multiple entries from your table in a single command.

Can delete multiple specific entries by listing them eg. could delete all Thor movies:
```
DELETE FROM movies WHERE title IN ('Thor', 'Thor: The Dark World', 'Thor: Ragnarok');
```
Can also delete based on a range of values using BETWEEN. eg. could delete all movies from released between 2005 and 2013 with:
```
DELETE FROM movies WHERE year BETWEEN 2005 and 2013;
```
