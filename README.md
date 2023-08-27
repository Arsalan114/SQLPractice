# SQLPractice
SQL Code Based on AlexTheAnalyst Tutorial

-- create database, table and insert values in table

DROP DATABASE IF exists SQLTutorial;
create database SQLTutorial;
Use SQLTutorial;

create table EmployeeDemographics (
EmployeeID int,
FirstName varchar(40),
LastName varchar(40),
Age int,
Gender varchar(40)
);

Create table EmployeeSalary (
EmployeeID int,
JobTitle varchar(40),
Salary int,
primary key (EmployeeID)
);

insert into EmployeeDemographics
values (1001, 'Jim', 'Hooper', 30,'Male'), (1002, 'Pam', 'Beasley', 30, 'Female'),
(1003, 'Dwight', 'Schrute', 29, 'Male'),
(1004, 'Angela', 'Martin', 31, 'Female'),
(1005, 'Toby', 'Flenderson', 32, 'Male'),
(1006, 'Michael', 'Scott', 35, 'Male'),
(1007, 'Meredith', 'Palmer', 32, 'Female'),
(1008, 'Stanley', 'Hudson', 38, 'Male'),
(1009, 'Kevin', 'Malone', 31, 'Male');

insert into EmployeeSalary
Values	(1001, 'Salesman', 45000),
(1002, 'Receptionist', 36000),
(1003, 'Salesman', 63000),
(1004, 'Accountant', 47000),
(1005, 'HR', 50000),
(1006, 'Regional Manager', 65000),
(1007, 'Supplier Relations', 41000),
(1008, 'Salesman', 48000),
(1009, 'Accountant', 42000)

-- Query table;

select	*
from EmployeeDemographics;

select Count(LastName) AS LastNameCount
from EmployeeDemographics;

Select Max(Salary) AS MaxSalary
From EmployeeSalary;

Select jobtitle, Salary
From EmployeeSalary
Order by Salary DESC;
