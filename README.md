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
🦭💬 There are multiple data integration endpoints but important we are select data integration methods by criteria where they need time response, amount of the data, update of related key, communication key ( foreign key tables and CTI data ), and target integration system because sometimes we need priority data as in application data flow design and scalability of the method. There are several times found that the CTI method is fast and easy to manage with tools, pre-build script templates, design, and data integrity but with the amount of data and a number of system integrations batch processes and updates perform best for the solution and adaptive for the operational process. </br>

🐐💬 By design there are several types of system databases and data integrity because of flat IT infrastructure design for working maintenance and accessibility, all communication networks are managed and monitored the same as user accessibility because any time permission is granted allows users can perform their tasks anywhere inside of the authorized solution. The system design of both system admin management tasks development and system performance and security. Multiple systems with the same functions may have a small difference in syntax operation commands when users may need time or preparation. For example Oracle SQL statement and Microsoft SQL statement with colons and we enchanted command case sensitivity, specific schemas, multiple-way access data sources, and created views or custom schemas for operational tasks. New users from administrative will have a difficult time even using multiple-purpose software applications or creating new data adaptors. </br>

🦁💬 Schemas management and local administrative policy support by appliation since programming and logic are created with permissions authorization design, working with data migration but security for data backup and transformation. One problem is recording are managed by the application itself the integration can be performed from their client and server for report and evaluation, statistics monitoring, update surveys reports, evaluation reports, and supervisor actions. </br>

🐑💬 ➰ It is possible and does not need to perform database access or duplicate encryption algorithms we can generate hyperlink addresses and data integration API for query and request data records, update statistics, perform the action, and some path of the integration from the communiation hub. </br>

🐯💬 Localization and F-view support application we can perform data integration with feed of data requirements from API request with Culture-INFO. </br>

🍳💬 That is I-frames we can build with multiple integrated systems. </br>
🧸💬 That is the same thing and do not like the flying wing⁉️ </br>
🍳💬 That is because it works in the airline business too but people may have multiple recognition of the application names. </br>
🧸💬 F-wings F-wings⁉️ </br>

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
💃( 👩‍🏫 )💬 We are looking data engineer for Airflow that was about 10 years ago but with time the application Airflow has had a high impact in the market but is not popular in Thailand, today it is back in the IBM brand called Apache Spark. </br>
🦤💬 In the picture example is only task management where they had GUI, database management, notification and monitoring, message filters, and automation task builders. Working with automation tasks is a trend as finding a boot for a party once you find of matching you where it everywhere even in your neighbors, selecting the application process and maintaining the same once they are fit to match that is forever. </br>

<p align="center" width="100%">
    <img width="47%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/extract_load_data.png">
    <img width="20%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/2648452-takeshigouda.jpg"> </br>
    <b> Pictures from the Internet </b> </br>    
</p>

### SQL Statement - aggregate tails data ###
🦭💬 When group aggregate and concatenate command is not enough you may be familiar with pre-grouping and taking, you can perform grouping at the tail of the dataset return from a select statement by CUBE ROLLUP that saves time to build the request and response command without command concatenation or create a temporary table, material table or views. </br>
🦭💬  IT requirements negotiations temporary views and single object are not allowed in the system, ALL objects need schemas and concatenate selection required to have views and schemas their own. </br>

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
