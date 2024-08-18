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
```
#!/bin/sh

# This startup script does the following
# Creates a database sales
# Uses the sales database
# Creates a table sales_data with fields rowid,productid,customerid,price,quantity and timestamp.

mysql --host=mysql --port=3306 --user=root --password=<Replace with your mysqlserver password> -e "create database sales;
use sales;drop table if exists sales_data;create table sales_data(rowid int DEFAULT NULL,product_id int DEFAULT NULL,
customer_id int DEFAULT NULL,price decimal(10,0) DEFAULT NULL,
quantity int DEFAULT NULL,timestamp timestamp NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP);"

# Loading data from sales_olddata.csv into sales_data table.This csv consists of data with old timestamp.

mysql --host=mysql --port=3306 --user=root --password=<Replace with your mysqlserver password> --local-infile=1
    -e "use sales;load data local infile '/home/project/sales_olddata.csv' into table sales_data fields
    terminated BY ','lines terminated BY '\n';"

# Loading data from sales_newdata.csv into sales_data table.This csv consists of data updated with the current timestamp.
mysql --host=mysql --port=3306 --user=root --password=<Replace with your mysqlserver password> --local-infile=1
    -e "use sales;load data local infile '/home/project/sales_newdata.csv' into table sales_data fields
    terminated BY ',' lines terminated BY '\n'(rowid,product_id,customer_id,price, quantity);"
```

### Sample ETL Shell Script - Postgre ####
```
#!/bin/sh

psql --username=postgres --host=localhost -c "create database sales_new;"

psql --username=postgres --host=localhost --dbname=sales_new -c "CREATE TABLE sales_data(rowid int,product_id int,
    customer_id int,price decimal,quantity int,timestamp timestamp,dateid SERIAL PRIMARY KEY);

create table DimDate(dateid int,day varchar(20),month varchar(30),year varchar(5));

create table FactSales(rowid int,product_id int,customer_id int,price decimal,total_price decimal);"
```

<p align="center" width="100%">
    <img width="47%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/extract_load_data.png">
    <img width="20%" src="https://github.com/jkaewprateep/IBM-Data-Warehousing-Capstone-Project/blob/main/2648452-takeshigouda.jpg"> </br>
    <b> Pictures from the Internet </b> </br>    
</p>


