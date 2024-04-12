# Querying the database
We use the SELECT command

## List all the rows of ALL columns
```sql
SELECT * FROM test.patients;
```
## List all the rows of the specified columns
```sql
SELECT first_name, last_name, dob from patients;
```
## List rows that meet the specified criteria in WHERE clause
```sql
SELECT * from patients WHERE village = 'Donda';
```

## Pattern Matching
## 'abc%' matches strings beginning with 'abc'
```sql
SELECT * FROM patients WHERE first_name LIKE 'Ja%';
```
## '%xyz' matches strings ending with 'xyz'

## '%aaa%' matches strings containing 'aaa'

## Calculating Age
```sql
SELECT first_name, last_name, dob, TIMESTAMPDIFF(YEAR, dob, CURDATE()) AS age, village from patients
```
This method is faulty.


Let's add a new row and calculate the age again
```sql
INSERT INTO patients ( first_name, last_name, dob, village)
VALUES ( 'Timothy', 'Phazi', '2024-01-31', 'Michiru' );

## Using ORDER BY
Order the results by first_name
```sql
SELECT * FROM patients ORDER BY first_name;
```

What is a better way of calculating age?

## Key take aways
- [x] `*` is a wildcard character
- [x] `WHERE` adds a criteria
- [x] Order by orders the results 

