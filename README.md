# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.


## DML(Data Manipulation Language)
<div align="justify">
The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.
</div>

## List of DML commands: 
<div align="justify">
INSERT: It is used to insert data into a table.<br>
UPDATE: It is used to update existing data within a table.<br>
DELETE: It is used to delete records from a database table.<br>
</div>

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:

![image](https://github.com/Naveensrinivasan07/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119475891/69bb52fd-0664-4fdc-9440-82a4f8166b7d)







### OUTPUT:
![image](https://github.com/Naveensrinivasan07/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119475891/7dea8b82-a988-4a53-80bc-363ce9f07f23)

### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
![image](https://github.com/Naveensrinivasan07/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119475891/ea87d773-31fd-44f4-9337-00f182eb18c7)



### OUTPUT:
![image](https://github.com/Naveensrinivasan07/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119475891/151bbb01-98e6-4525-9d0c-5e2cedf3d795)


### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
![image](https://github.com/Naveensrinivasan07/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/119475891/79fb1ce4-0221-404a-9f99-081e0c5b9fbc)



### OUTPUT:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/8f5dcfe3-2030-4d1d-8001-e8023052e863)

### Q5)	List the names of Clerks from emp table.


### QUERY:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/d6d15944-a24a-4b37-9d3b-1bd3158d8f7d)


### OUTPUT:
![271175098-86f71191-94a7-45e6-b756-6020a06350b7](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/4671643a-a6cc-45be-893d-6cea604ff84c)


### Q6)	List the names of employee who are not Managers.


### QUERY:
![271175146-a65b548c-2cd5-45c9-b21b-89cbdb1114c4](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/d90b257e-3667-4cae-8b2d-faf2b0b3fc41)


### OUTPUT:
![271175187-02933c79-0073-4274-9b90-2bc9f4814d8b](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/45fe4493-250e-4420-ad5c-88c7888bb512)


### Q7)	List the names of employees not eligible for commission.


### QUERY:
![271175220-6d3c980b-752e-4df5-9648-2a4bcf6e1962](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/ecba9a1d-6f18-4cf0-aec8-e50965cba81b)


### OUTPUT:
![271175271-f4a825b1-ac41-4d65-9b0c-e59a55e4ca33](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/9bfb4e21-5291-4439-ae57-d76079a0b652)


### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
![271175311-aec361f2-371a-43c0-8be2-7fae5ecfa2e8](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/9b39eca8-7872-4e30-bbd8-afb641187c6c)


### OUTPUT:
![271175346-6c098d6f-d039-4325-9810-93275772b07f](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/2992f15f-6765-4f75-bf03-e5de627d9411)


### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/e345320e-4376-4dc8-ba50-e93921ee5167)


### OUTPUT:


### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/59299a36-e7fa-47ae-bb79-64c89d095e2a)


### OUTPUT:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/77d2d67b-f465-4037-8a4b-f17c93d8a194)


### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/bb196b0a-3e16-4c73-bfe1-698144370d32)


### OUTPUT:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/2304fbb7-0281-49b6-9a92-bbdd477a93af)


### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/ccc5ffa9-2e54-4679-9611-06c98472dbc9)


### OUTPUT:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/f8a8c9f6-7da9-4cf3-9681-21edacf8fc85)

### Q13) Find number of rows in the table EMP

### QUERY:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/0e5edc43-ea57-4053-a999-2e3df7739f3a)


### OUTPUT:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/66d08168-139c-4c7b-ac5c-1998c69defa0)


### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/372a5b2e-1120-4177-b6f0-3499c58c58cd)


### OUTPUT:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/31c9af89-140e-49f7-8186-dc3d9fc7aab1)


### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
![image](https://github.com/22009011/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/118343461/025457d2-485a-4255-855c-8c950f6e8248)

# Result:
To create a manager database and execute DML queries using SQL is executed successfully.
