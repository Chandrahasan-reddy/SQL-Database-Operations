SQL Database Operations

Overview

This repository contains SQL scripts that demonstrate various database operations, including table creation, data insertion, updates, deletions, and system-defined functions. The scripts are designed for learning and practicing SQL commands with an emphasis on constraints, relationships, and built-in functions.# SQL-Database-Operations

Database Schema

COUNTRIES Table

Definition:
CREATE TABLE COUNTRIES
(
    CountryID    INT,
    CountryCode CHAR(2),
    CountryName VARCHAR(20)
);

Operations:

Insert country records, including handling NULL values.

Update country details.

Delete specific country records.

Truncate and drop the table.

Alter table to modify and add columns.

DEPT Table

Definition:
CREATE TABLE dept
(
    deptno INT PRIMARY KEY,
    deptName VARCHAR(20),
    loc VARCHAR(20)
);

Operations:

Insert department records.

Retrieve department details.

EMP Table

Definition:
CREATE TABLE emp
(
    empno INT PRIMARY KEY,
    empnmae VARCHAR(20),
    job VARCHAR(20),
    mgr INT,
    hiredate DATE,
    sal DECIMAL(9,2) CHECK (sal > 0),
    comm DECIMAL(7,2),
    deptno INT,
    CONSTRAINT FK_DEPTNO FOREIGN KEY (deptno) REFERENCES dept (deptno)
);


Operations:

Insert employee records.

Retrieve employee details.

System-Defined Functions Demonstrated

String Functions:

LOWER(), UPPER() – Convert text to lower and upper case.

LEFT(), RIGHT() – Extract substrings from left and right.

SUBSTRING() – Extract part of a string.

Mathematical Functions:

FLOOR(), CEILING() – Rounding operations.

ROUND() – Round a decimal value to a specified precision.

Date & Time Functions:

Retrieve the current year, month, and weekday.

Extract and format date parts using DATENAME().

SYSDATETIME(), CURRENT_TIMESTAMP – Get the current system timestamp.

CONVERT() – Convert datetime to different formats.

Usage Instructions

Execute the SQL scripts in a database management system that supports standard SQL.

Ensure referential integrity by creating the dept table before inserting emp records.

Modify queries as needed to adapt to different use cases.

