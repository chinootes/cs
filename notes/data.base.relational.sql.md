---
id: rlkj1x8knu6tng03w7jfnkb
title: SQL
desc: ''
updated: 1715188512817
created: 1715182470853
---

SQL contains sub-languages within it for different purposes.

## Data Definition Language (DDL)

- `CREATE`: Creates a new table or database.
- `ALTER`: Modifies an existing table or database.
- `DROP`: Deletes an existing table or database.
- `TRUNCATE`: Removes all records from a table, including all spaces allocated for the records.

## Data Manipulation Language (DML)

- `INSERT`: Inserts new data into a database.
- `UPDATE`: Modifies existing data in a database.
- `DELETE`: Removes data from a database.

## Data Control Language (DCL)

- `GRANT`: Gives a privilege to user.
- `REVOKE`: Takes back privileges granted from user.

## Transaction Control Language (TCL)

- `COMMIT`: Saves all the transactions to the database.
- `ROLLBACK`: Restores the database to the last committed state.
- `SAVEPOINT`: Sets a savepoint within a transaction.
- `SET TRANSACTION`: Places a name on a transaction.

## Data Query Language (DQL)

### `SELECT`

- Retrieves data from a database.
- Root clause of DQL

#### Clauses

- `WHERE`: Filters results based on a condition.
- `GROUP BY`: Groups rows that have the same values in specified columns into summary rows.
- `HAVING`: Filters groups based on a condition.
- `ORDER BY`: Sorts the result set in ascending or descending order.

##### `LIMIT`

Restricts the number of rows returned. Often used in pagination.

```sql
SELECT * FROM table_name LIMIT number;
```

##### `OFFSET`

Skips the specified number of rows before starting to return rows from a query

```sql
SELECT * FROM table_name LIMIT number OFFSET start;
```

Usually used with `LIMIT`.

For example: Query to select 3rd largest salary. #interview-question
```sql
SELECT DISTINCT salary
FROM employees
ORDER BY salary DESC
LIMIT 1 OFFSET 2;
```

#### Aggregate Functions

- `COUNT`: Returns the number of rows.
- `SUM`: Returns the sum of a numeric column.
- `AVG`: Returns the average value of a numeric column.
- `MIN`: Returns the smallest value of the selected column.
- `MAX`: Returns the largest value of the selected column.
- 

#### Scalar Functions

- `UCASE()` (or `UPPER()`): Converts a field to uppercase.
- `LCASE()` (or `LOWER()`): Converts a field to lowercase.
- `MID()` (or `SUBSTRING()`): Extracts characters from a text field.
- `LEN()` (or `LENGTH()`): Returns the length of a text field.
- `ROUND()`: Rounds a numeric field to the number of decimals specified.
- `NOW()`: Returns the current system date and time.
- `FORMAT()`: Formats how a field is to be displayed.

#### Join Commands

- `INNER JOIN`: Returns records that have matching values in both tables.
- `LEFT JOIN` (or `LEFT OUTER JOIN`): Returns all records from the left table, and the matched records from the right table.
- `RIGHT JOIN` (or `RIGHT OUTER JOIN`): Returns all records from the right table, and the matched records from the left table.
- `FULL JOIN` (or `FULL OUTER JOIN`): Returns all records when there is a match in either left or right table.
- `CROSS JOIN`: Returns all records where each row from the first table is combined with each row from the second table.
SELF JOIN: A regular join, but the table is joined with itself.
