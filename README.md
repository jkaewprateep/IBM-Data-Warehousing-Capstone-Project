# IBM-Data-Warehousing-Capstone-Project
IBM-Data Warehousing Capstone Project

<p align="center" width="100%">
    <img width="47%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/IBM%20Data%20WareHouse%20Instructors.png">
    <img width="20%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/kid_db01.png">
    <img width="20%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/kid_db02.png"> </br>
    <b> Pictures from the Internet </b> </br>
</p>

[IBM Data Warehouse Engineer Professional Certificate]( https://coursera.org/share/7b3eda47284a270158c979c19e543320 ) </br>
[Meta Database Engineer Professional Certificate]( https://coursera.org/share/0b7133ceaec8027d53af1c74b7d8e47d ) </br>
[Hacker Rank SQL (Advance)]( https://www.hackerrank.com/certificates/f225fa371510 ) </br>

### Sample ETL Shell Script - MySQL ###
🧸💬 There are multiple applications and event activation functions that can perform pre-build script and online statements into sequence and update commands for automation process where task scheduling, automation process management system, and IBM Apache Spark ( Airflow ) are allowed to create event update, communication messages, logging and monitoring platforms, report and evaluation for performance and detail information for investigation and development. They are known by many customers and working platforms - as microservices but do not miss understanding batch and an automation process is not micro-services but they can perform tasks with application workflow to complete solutions as planned with successful results that are micro-services. Micro-services include database services, and database integration and database report services because they can fulfill the solution requirements. </br>

🦁💬 Not only databases, statistics, reports and dataset return applications but web applications, communication applications, security and controls, and applications can work as micro-services since they perform tasks in their predictable manners and provide good results for the solution, trackable and evaluation create a good performance. </br>

🐑💬 ➰ Our applications are considered micro-services and communication endpoints can be created at both client and server, working seamlessly with data trackings and message guarantee services with high-standard communications and IT project implementation. There are some monitoring, communication fields data values transfer, import-export, realtime, and schedule data services where we can track new and updated data and communication in realtime with events sent to the communication hub for action response and guarantee database records management and backup management plan. </br>

🦁💬 In database services and communication services they are message tracking and guarantee message communication but do not restart the server during the process, I understand file-based management as a Microsoft directory and recordings system but the design of database architecture reliability database needs to full 100% online application had self-recovery features. </br>

```
#!/bin/sh

# This startup script does the following
# Creates a database sales
# Uses the sales database
# Creates a table sales_data with fields rowid,productid,customerid,price,quantity and timestamp.

# 🧸💬 Create database with column fields definition and default value.
mysql --host=mysql --port=3306 --user=root --password=<Replace with your mysqlserver password> -e "create database sales;
use sales;drop table if exists sales_data;create table sales_data(rowid int DEFAULT NULL,product_id int DEFAULT NULL,
customer_id int DEFAULT NULL,price decimal(10,0) DEFAULT NULL,
quantity int DEFAULT NULL,timestamp timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP);"

# Loading data from sales_olddata.csv into sales_data table.This csv consists of data with old timestamp.
# 🧸💬 Loading data from CSV format into target database
mysql --host=mysql --port=3306 --user=root --password=<Replace with your mysqlserver password> --local-infile=1
    -e "use sales;load data local infile '/home/project/sales_olddata.csv' into table sales_data fields
    terminated BY ','lines terminated BY '\n';"

# Loading data from sales_newdata.csv into sales_data table.This csv consists of data updated with the current timestamp.
# 🧸💬 Loading data from CSV format into target database
mysql --host=mysql --port=3306 --user=root --password=<Replace with your mysqlserver password> --local-infile=1
    -e "use sales;load data local infile '/home/project/sales_newdata.csv' into table sales_data fields
    terminated BY ',' lines terminated BY '\n'(rowid,product_id,customer_id,price, quantity);"
```

### Sample ETL Shell Script - Postgre ####
```
#!/bin/sh

# 🧸💬 Login Postgre database with command template.
psql --username=postgres --host=localhost -c "create database sales_new;"

# 🧸💬 Login Postgre database with command template.
psql --username=postgres --host=localhost --dbname=sales_new -c "CREATE TABLE sales_data(rowid int,product_id int,
    customer_id int,price decimal,quantity int,timestamp timestamp,dateid SERIAL PRIMARY KEY);

# 🧸💬 Create table command template.
create table DimDate(dateid int,day varchar(20),month varchar(30),year varchar(5));

# 🧸💬 Create table command template.
create table FactSales(rowid int,product_id int,customer_id int,price decimal,total_price decimal);"
```

### Automation process with Shell Script and Python ###

<p align="center" width="100%">
    <img width="47%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/extract_load_data.png">
    <img width="20%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/2648452-takeshigouda.jpg"> </br>
    <b> Pictures from the Internet </b> </br>    
</p>

### SQL Statement - aggregate tails data ###

<p align="center" width="100%">
    <img width="47%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/cube.png">
    <img width="26.5%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/006862000_1475647022-kotaku.png"> </br>
    <b> Pictures from the Internet </b> </br>    
</p>

### SQL Statement - grouping set ###

<p align="center" width="100%">
    <img width="47%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/groupingsets.png">
    <img width="26.5%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/kana.png"> </br>
    <b> Pictures from the Internet </b> </br>    
</p>
