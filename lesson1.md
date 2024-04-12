# Creating and Populating a Database

## Create a database

```sql 
CREATE DATABASE test;
```

## Using the created database;
```sql
USE test;
```
https://github.com/deadex-ng/mysql_tutorial/
## Creating a table
```sql
CREATE TABLE patients (
patient_id int NOT NULL AUTO_INCREMENT,
first_name VARCHAR(30),
last_name  VARCHAR(30),
dob DATE,
village VARCHAR(30),
PRIMARY KEY (patient_id)
);
```

## Show tables
```sql
SHOW tables;
```

## Show all fields in a table
```sql 
DESCRIBE test.patients;
```

## Insert a row in a table
```sql
INSERT INTO patients ( first_name, last_name, dob, village)
VALUES ( 'James', 'Kadango', '2020-01-15', 'Donda' );
```

## Insert multiple rows in a table
```sql
INSERT INTO patients ( first_name, last_name, dob, village)
VALUES ( 'John', 'Kavuma', '2021-05-20', 'Donda' ),
( 'Janet', 'Chibvunde', '2020-01-15', 'Chitawira' );
```

## Question?
How can we insert some values while skipping other columns?

## Key Take aways
- [x] USE keyword
- [x] primary key
- [x] data types
