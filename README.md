# sql-practice-3-upasana
CREATE DATABASE UPPSMAM
USE UPPS MAM

CREATE TABLE UPPS(Emp_ID INT PRIMARY KEY IDENTITY not null, Emp_NAME VARCHAR(20) ,
Emp_SALARY MONEY ,Emp_DEPT VARCHAR(20),Emp_GENDER VARCHAR(20) )



INSERT INTO employee VALUES
('OPPS',25000,'IT','Female'),
('Mohini',30000,'HR','Male'),
('Jyoti',35000,'IT','Female'),
('sita',20000,'IT','Female'),
('Jacky',45000,'HR','Male')

CREATE TABLE Department (DEPT_ID int  identity not null,DEPT_Name varchar(20),DEPT_No int )

insert into  Department  values
('IT',2),
('HR',1),
('CS',4),
('IT',3),
('HR',6),
('IT',5)

SELECT * INTO Department FROM employee


select E_Name ,E_salary from EMP_DETAIL group  by E_NAME ,E_SALARY order by E_salary desc

select * into employee from Department WHERE 1=0

select * from employee where Emp_SALARY between 35000 and 45000

select * from employee
union 
select * from Department 

select * from employee
INTERSECT
select * from Department

SELECT*FROM Department WHERE Emp_NAME NOT IN (SELECT Emp_NAME FROM employee)

 
select Emp_NAME, sum(Emp_SALARY) as totalsal from employee group by Emp_NAME having sum(E_ID)>=2

select count(Emp_salary) totalemp from employee

select min(Emp_SALARY) totalsal from employee

select max(Emp_SALARY) totalsal from employee

select sum(Emp_SALARY) totalsal from employee

select avg(Emp_SALARY) totalsal from employee
