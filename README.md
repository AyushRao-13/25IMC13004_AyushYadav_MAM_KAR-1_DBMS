#25IMC13004

#TABLE CREATION AND DATA INSERTION
CREATE TABLE Employees (
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(50),
    manager_id INT,
    department VARCHAR(50),
    salary INT
);

INSERT INTO Employees VALUES
(1, 'Amit', NULL, 'Management', 120000),
(2, 'Ravi', 1, 'Engineering', 80000),
(3, 'Neha', 1, 'Engineering', 82000),
(4, 'Karan', 2, 'Engineering', 60000),
(5, 'Simran', 2, 'Engineering', 62000),
(6, 'Pooja', 3, 'Engineering', 61000),
(7, 'Rahul', 3, 'Engineering', 64000),
(8, 'Arjun', 1, 'HR', 70000);

<img width="1093" height="251" alt="image" src="https://github.com/user-attachments/assets/323ebb5a-661c-4f97-9611-4eb15f79410c" />



#Ques-1
SELECT 
    e1.manager_id,
    e1.emp_name AS employee_1,
    e2.emp_name AS employee_2
FROM Employees e1
JOIN Employees e2
    ON e1.manager_id = e2.manager_id
   AND e1.emp_id < e2.emp_id

<img width="578" height="193" alt="image" src="https://github.com/user-attachments/assets/3bd4cafa-6d3d-4452-9c58-9f42f08199e8" />



#Ques-2
SELECT MAX(Salary) AS SecondHighestSalary
FROM Employees
WHERE Salary < (SELECT MAX(Salary) FROM Employees);

<img width="297" height="73" alt="image" src="https://github.com/user-attachments/assets/ea8777c1-a473-4ee6-b680-9c6e4dda6c93" />


