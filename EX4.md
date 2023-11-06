# Ex. No: 4 Creating Procedures using PL/SQL
## DATE:
### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
CREATE TABLE employee(empid NUMBER,
empname VARCHAR(10),
 dept VARCHAR(10),
salary NUMBER);

CREATE OR REPLACE PROCEDURE insert_employee AS
BEGIN
INSERT INTO employee(empid, empname, dept, salary)
VALUES (1,'John','HR',50000);
INSERT INTO employee(empid, empname, dept, salary)
VALUES (2,'rose','IT',60000);
INSERT INTO employee(empid, empname, dept, salary)
VALUES (3,'Jack','Finance',55000);
COMMIT;
FOR emp_rec IN (SELECT * FROM employee) LOOP
DBMS_OUTPUT.PUT_LINE('Employee ID: ' || emp_rec.empid || 'Name' || emp_rec.empname
|| 'Department' || emp_rec.dept || 'Salary' || emp_rec.salary);
END LOOP;
END;
/
```

### Output:
![Screenshot 2023-10-02 143049](https://github.com/swetha1510/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/120623583/f34f69e3-8011-4896-8b00-d1f6bb230147)

### Result:
Thus a procedure has been successfully created and executed.
