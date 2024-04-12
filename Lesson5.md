# Working with multiple tables(Continued ...)

## Create programs table
```sql
CREATE TABLE programs (
program_id int NOT NULL AUTO_INCREMENT,
program VARCHAR(30),
PRIMARY KEY (program_id)
);
```

## Insert programs data
```sql
INSERT INTO programs ( program)
VALUES ( 'hypertension'),
( 'diabetes'),
( 'sickle cell'),
( 'chronic kidney failure');
```

## Create patient_enrollemnt table
```sql
CREATE TABLE patient_enrollemnt
(
enrollment_id int PRIMARY KEY NOT NULL AUTO_INCREMENT,
patient_id INT NOT NULL, 
program_id INT NOT NULL,
enrollemnt_date DATE,
FOREIGN KEY (patient_id) REFERENCES patients(patient_id),
FOREIGN KEY (program_id) REFERENCES programs(program_id)
)
```

## Insert patient_enrollment data
```sql
INSERT INTO patient_enrollemnt (patient_id, program_id, enrollemnt_date)
VALUES (1,1,'2024-01-01'),
(1,3,'2024-02-01'),
(2,2,'2024-01-17'),
(3,4,'2024-03-20');

```
