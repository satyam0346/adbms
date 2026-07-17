CREATE TABLE Departments(
DepartmentID number,
DeptName varchar(20),
Budget number,
Location varchar(20),
ManagerID number
);


INSERT INTO Departments VALUES(10,'Engineering',500000, 'New York', 101);
INSERT INTO Departments VALUES(20,'Marketing',150000,'San Franciso',104);
INSERT INTO Departments VALUES(30,'Sales',200000,'Chicago',105);
INSERT INTO Departments VALUES(40,'HR',80000,'New York',103);
INSERT INTO Departments VALUES(50,'Finance',300000,'San Francisco',102);


CREATE TABLE Employees(
    EmployeeID number,
    FirstName varchar(20),
    LastName varchar(20),
    DepartmentID number,
    Salary number
);

INSERT INTO Employees VALUES(101, 'Alice', 'Smith', 10, 95000);
INSERT INTO Employees VALUES(102, 'Bob', 'Jones', 50, 105000);
INSERT INTO Employees VALUES(103, 'Charlie', 'Brown', 40, 60000);
INSERT INTO Employees VALUES(104, 'Diana', 'Prince', 20, 85000);
INSERT INTO Employees VALUES(105, 'Evan', 'Wright', 30, 75000);

CREATE TABLE Projects(
    ProjectID number,
    ProjectName varchar(20),
    DepartmentID number,
    Status varchar(20),
    Deadlines number
);

INSERT INTO Projects VALUES(201, 'Cloud Migration', 10, 'Active', 2026);
INSERT INTO Projects VALUES(202, 'Ad Campaign', 20, 'Active', 2026);
INSERT INTO Projects VALUES(203, 'SEO Overhaul', 20, 'Completed', 2025);
INSERT INTO Projects VALUES(204, 'CRM Upgrade', 30, 'Active', 2027);
INSERT INTO Projects VALUES(205, 'Audit 2026', 50, 'Active', 2026);

CREATE TABLE Assignments(
    AssignmentID number,
    EmployeeID number,
    ProjectID number,
    HoursWorked number,
    Role varchar(20)
);

INSERT INTO Assignments VALUES(301, 101, 201, 120, 'Lead Architect');
INSERT INTO Assignments VALUES(302, 104, 202, 80, 'Manager');
INSERT INTO Assignments VALUES(303, 104, 203, 45, 'Analyst');
INSERT INTO Assignments VALUES(304, 105, 204, 95, 'Consultant');
INSERT INTO Assignments VALUES(305, 102, 205, 60, 'Auditor');