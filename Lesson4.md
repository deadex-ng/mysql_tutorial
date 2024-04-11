# Working with multiple tables
Our example so far involves only one table `patients`. A practical database contains many related tables.

- Patients
    - [ ] patient_id
    - [ ] first_name
    - [ ] last_name
    - [ ] dob
    - [ ] village

We are introducing two more tables, `programs` and `patient_enrollement` table.

- programs
    - [ ] program_id
    - [ ] program_name

Programs table
| program_id            | program                   | 
| ----------------------| --------------------------| 
| 1                     |  hypertension             |
| 2                     |  diabetes                 | 
| 3                     |  sickle cell              | 
| 4                     |  chronic kidney failure   | 


</br>
</br>
patient_enrollemnt table

A patient can be enrolled in one or multiple programs.
Let's say a patient with patient_id `1` visits the hospital on 1 January 2024. We find that the patient has hypertension and we enroll that patient
in the hypertension program. On 1 February 2024, the same patient visits the hospital, and medical tests show that the patient has sickle cell, we enroll that patient in the sickle cell program.


| enrollemnt_id         | patient_id | program_id   | enrollment_date |
| ----------------------| ---------- | ------------ |-----------------|
| 1                     |  1         | 1            | 2024-01-01      | 
| 2                     |  1         | 3            | 2024-02-01      |
| 3                     |  2         | 2            | 2024-01-17      |
| 3                     |  3         | 4            | 2024-03-20      |


