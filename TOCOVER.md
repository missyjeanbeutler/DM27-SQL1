# Topics to Cover

This is a list of topics that will be covered in today's lecture.

## What is a relational database? 

## Schemas 
- Like a blueprint. How you structure your database, not the actual data

CREATE TABLE [table name] (
   [column name] [data type] [constraints - optional]
);

CREATE TABLE products (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  price FLOAT
);

## Datatypes
- Numeric Types
  - FLOAT - 15 numbers after decimal point
  - INTEGER - rounds numbers
  - DECIMAL - good for precise numbers
- Character Types
  - TEXT - character length is unlimited
  - VARCHAR(n) - character length is limited
  - 'I''m super cool.' - two single quotes for a quote in string

## SQL statement 
- Also known as query
- Ends with the semi-colon

## SELECTS
- SELECT
  - SELECT * FROM [table name]
  - Can select multiple columns separated by commas
  - SELECT DISTINCT [column name] FROM [table name]
    - removes duplicates
- Conditionals
  - WHERE
    - SINGLE QUOTES ONLY
    - Comparison Operators and Logical operators
      - (>, >=, =, != or <> etc..)
      - AND (both true), OR (either or true) (Logical operators)
      - LIKE - will match pieces of a string, case insenstive - % (shows where in the string to match it)
      - IS NULL, IS NOT NULL (cannot do = null or != null)
      - BETWEEN, NOT BETWEEN shortcut for two logical operators
        - ex: WHERE number BETWEEN 900 AND 12000
      - NOT IN(), IN() - shortcut for a bunch of or statements, list stuff with commas
- ORDER BY [table name]
  - default is ascending order but better to write it out
  - DESC or ASC after the column name
- LIMIT [number]
- Functions
  - sum([column name]), min([column name]), max([column name]), avg([column name]) count(*) (aggregate functions)
  - as for aliases 
  - count ignores nulls (so use * if you want total entries, column name won't get total if there are nulls) - the rest do not ignore nulls

## Adding, Updating, Removing Rows in a Table
- INSERT INTO [table name] 
  ([column name], [...column name])
  VALUES 
  ([value], [...value])
- UPDATE [table name]
  SET [column name] = [value]
  WHERE [condition]
  - DO NOT FORGET YOUR WHERE CLAUSE
- DELETE FROM [table name]
  WHERE [condition]
  - DO NOT FORGET YOUR WHERE CLAUSE