# Updating and Deleting Data

## Updating selected rows
```sql
UPDATE patients SET village = 'Nkulumadzi' WHERE patient_id = 3 and first_name = 'Janet' ;
```

## You can modify more than one values
```sql
UPDATE patients SET dob = '2019-10-20', village = 'Matope' WHERE patient_id = 4;
```

## Deleting 
Delete all rows from the table. Use with extreme care! Records are NOT recoverable!!!

```sql
DELETE FROM tableName;
```

Delete only row(s) that meets the criteria
```sql
DELETE FROM patients WHERE patient_id = 5;
```

## Deleting database
```sql
DROP DATABASE databaseName;
```
