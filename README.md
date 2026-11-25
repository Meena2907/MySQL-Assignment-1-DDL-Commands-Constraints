# MySQL-Assignment-1-DDL-Commands-Constraints


Create database Employee_db;
Use employee_db;

Create Table Departments(
Department_id Int,
Department_Name Varchar(100));


Create Table Location(
Location_id Int,
Location varchar(30));

Create Table Employees(
Employee_id Int,
Employee_name Varchar(50),
Gender enum('M','F'),
Age int,
hire_Date date,
designation varchar(100),
department_id int,
location_id int,
salary decimal(10,2));

Alter Table Employees
Add Column email varchar(50);
SELECT*FROM employees;

Alter Table Employees
Modify designation varchar(100);
DESC Employees;

Alter Table Employees
Rename Column hire_date to date_of_joining;
SELECT*FROM employees;
Rename Table Departments to Departments_info; 

Rename Table Location to Locations;

Truncate Table Employees;


Drop Table Employees;

Drop database employee_db;

Create DataBase Employee_db;
Use Employee_db;
Create Table Departments(
Department_id Int Primary Key,
Department_Name Varchar(100) Not null Unique);
DESC Departments;

Create Table Location(
Location_id Int PRIMARY KEY AUTO_INCREMENT,
Location varchar(30) Not null unique);
DESC Location;

Create Table Employees(
Employee_id Int Primary key,
Employee_name Varchar(50) Not Null,
Gender enum('M','F'),
Age int Check (age>=18),
hire_Date date default(Current_Date),
designation varchar(100),
department_id int,
location_id int,
salary decimal(10,2),
Foreign Key (Department_id) References Departments(Department_id),
Foreign Key (location_id) References Locations(location_id));
Desc Employees;
