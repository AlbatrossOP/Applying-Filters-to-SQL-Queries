<h1>Applying Filters to SQL Queries</h1>

<h2>Description</h2>
For this Lab, I investigated potential security issues, updated employee computers, and performed other security related tasks. User/information in screenshots is from simulated SQL enviornment. 


<h2>Languages and Utilities Used</h2>

- <b>SQL</b>
- <b>Linux</b>

<h2>Environments Used </h2>

- <b>Linux Command Line Interface </b>

<h2>Lab walk-through:</h2>

<p align="center">
Retrieving after hours failed login attempts: <br/>

There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated. The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours.

<img src="https://i.imgur.com/TkfY5rF.png" height="80%" width="80%" alt="Retrieving after hours failed login attempts"/>

The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the "log_in_attempts" table. Then, I used a "WHERE" clause with an AND operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. The first condition is "login_time > '18:00'", which filters for the login attempts that occurred after 18:00. The second condition is "success = FALSE", which filters for the failed login attempts. 
<br />
<br />
<p align="center">
Retrieving Login Attempts on Specific Dates:  <br/>
A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated. The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.

<img src="https://i.imgur.com/sGCbE8m.png" height="80%" width="80%" alt="Retrieving Login Attempts on Specific Dates"/>
<br />

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with an OR operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is login_date = '2022-05-09', which filters for logins on 2022-05-09. The second condition is login_date = '2022-05-08', which filters for logins on 2022-05-08.

<br />
<p align="center">
Retrieving Login Attempts Outside of Mexico: <br/>

After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated. The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico. 

<img src="https://i.imgur.com/NV6hUcy.png" height="80%" width="80%" alt="Retrieving Login Attempts Outside of Mexico"/>
<br />

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred in countries other than Mexico. First, I started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause with NOT to filter for countries other than Mexico. I used LIKE with MEX% as the pattern to match because the dataset represents Mexico as MEX and MEXICO. The percentage sign (%) represents any number of unspecified characters when used with LIKE. 

<br />
<p align="center">
Retrieving Employees in Marketing:  <br/>
My team wants to update the computers for certain employees in the Marketing department. To do this, I have to get information on which employee machines to update. The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building.

<img src="https://i.imgur.com/4IdUEQF.png" height="80%" width="80%" alt="Retrieving Employees in Marketing"/>
<br />

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Marketing department in the East building. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with AND to filter for employees who work in the Marketing department and in the East building. I used LIKE with East% as the pattern to match because the data in the office column represents the East building with the specific office number. The first condition is the department = 'Marketing' portion, which filters for employees in the Marketing department. The second condition is the office LIKE 'East%' portion, which filters for employees in the East building.

<br />
<p align="center">
Retrieving Employees in Finance or Sales:  <br/>
The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is needed, I have to get information on employees only from these two departments. The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Finance or Sales departments.

<img src="https://i.imgur.com/Ha8AVEs.png" height="80%" width="80%" alt="Retrieving Employees in Finance or Sales"/>
<br />

The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Finance and Sales departments. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with OR to filter for employees who are in the Finance and Sales departments. I used the OR operator instead of AND because I want all employees who are in either department. The first condition is department = 'Finance', which filters for employees from the Finance department. The second condition is department = 'Sales', which filters for employees from the Sales department.

<br />
<p align="center">
Retrieving All Employees Not in IT:  <br/>
My team needs to make one more security update on employees who are not in the Information Technology department. To make the update, I first have to get information on these employees. The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department.

<img src="https://i.imgur.com/K5ppZJO.png" height="80%" width="80%" alt="Retrieving All Employees Not in IT"/>
<br />
The first part of the screenshot is my query, and the second part is a portion of the output. The query returns all employees not in the Information Technology department. First, I started by selecting all data from the employees table. Then, I used a WHERE clause with NOT to filter for employees not in this department.

<br />
<br />
<p align="center">
<h2>Summary</h2>
I applied filters to SQL queries to get specific information on login attempts and employee machines. I used two different tables, log_in_attempts and employees. I used the AND, OR, and NOT operators to filter for the specific information needed for each task. I also used LIKE and the percentage sign (%) wildcard to filter for patterns.

