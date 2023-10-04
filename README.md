# Data Manipulation Language (DML) Commands and built in functions in SQL
# AIM:
To create a manager database and execute DML queries using SQL.

# DML(Data Manipulation Language)
The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.
List of DML commands:
INSERT: It is used to insert data into a table.
UPDATE: It is used to update existing data within a table.
DELETE: It is used to delete records from a database table.
Create the table as given below:
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
insert the following values into the table
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
Q1) Update all the records of manager table by increasing 10% of their salary as bonus.
# QUERY:
update manager set salary=salary+(salary*0.10);

# OUTPUT:
<br>
![271218363-1d66948b-7919-4849-81d5-c2a58efa216c](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/62b9c8e4-c0dc-434b-a6d6-04147d0175cf)




Q2) Delete the records from manager table where the salary less than 2750.
# QUERY:
delete from manager where salary<2750;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/c56aea16-9509-44e8-a5aa-f365c7ea3fc9)


Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)
# QUERY:
select ename as "Name",salary*12 as "Annual salary" from manager;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/22aeec09-8f23-4fad-98bd-5a5d392ec002)


Q4) List the names of Clerks from emp table.
# QUERY:
select ename from manager where designation='clerk';
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/d993d489-bde8-489b-acea-19f8c25a647c)


Q5) List the names of employee who are not Managers.
QUERY:
select ename from manager where designation <> 'manager';
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/9f423c7e-a4fe-4d9e-8d28-347975c49e9b)


Q6) List the names of employees not eligible for commission.
# QUERY:
select ename from manager where commission=0;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/6d6e91d6-2d44-41ec-98a0-c1bdee0b18ac)




Q7) List employees whose name either start or end with ‘s’.
# QUERY:
select ename from manager where ename like '%s' or ename like 's%';
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/ecb2120f-79ec-4239-9ae9-aee1a5414f1e)


Q8) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.
# QUERY:
select ename,designation as "job",deptno,hiredate from manager order by hiredate asc;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/eda32d9a-cb1d-404c-bd28-3e67f7092a56)


Q9) List the Details of Employees who have joined before 30 Sept 81.
# QUERY:
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/0d703273-b3eb-41ab-86e8-6ba8f902dc82)


Q10) List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.
# QUERY:
 select ename,deptno,salary from manager order by deptno asc,salary desc;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/10e4eb64-a233-4f7f-8e4a-1ebfb8fd74c9)


Q11) List the names of employees not belonging to dept no 30,40 & 10
# QUERY:
select ename from manager where deptno not in (30,40,10);
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/eefd70b2-5977-44a0-b84b-e3625cb73644)


Q12) Find number of rows in the table EMP
# QUERY:
 select count(*) from manager;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/8fa3d1b9-20d5-4595-b9df-578aef5ddda5)


Q13) Find maximum, minimum and average salary in EMP table.
# QUERY:
MAXIMUM:
select max(salary) from manager;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/f219f440-14a7-4af9-afd3-521d17755c8b)


# MINIMUM:
select min(salary) from manager;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/769fdd20-e0cb-48a4-8377-9e9dff895f7b)


AVERAGE:
select avg(salary) from manager;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/6dafe81b-ac42-40c1-b245-91382b0376eb)


Q14) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.
# QUERY:
SELECT designation AS job, COUNT(*) AS num_employees FROM manager GROUP BY designation ORDER BY num_employees DESC;
# OUTPUT:
<br>
![image](https://github.com/thrikesh/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119576222/d07fee37-55c2-49b3-9307-33d1d546b4c5)


# Result:
To create a manager database and execute DML queries using SQL is executed successfully.
