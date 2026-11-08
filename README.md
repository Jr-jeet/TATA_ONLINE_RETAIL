# TATA_ONLINE_RETAIL

# SQL QUREY FOR ANLYSIS
# FOR DATA UPLOAD
SET GLOBAL LOCAL_INFILE=ON ;
LOAD DATA LOCAL INFILE 'C:\KAGGLE(DATSET)\Spotfy\TATA_01.csv 'INTO TABLE online_retail
FIELDS TERMINATED BY ',' 
ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 LINES ;


SHOW GLOBAL VARIABLES like 'LOCAL_INFILE' ;

SET GLOBAL LOCAL_INFILE=1;
create database tata;
USE tata ;
CREATE TABLE ONLINE_RETAIL (
Description01 varchar(255),
Quantity int,
Unit_Price decimal(10,2),
Customer_ID int,
Country varchar(100),
Invoice_No varchar(30),
Stock_Code varchar(30),
Revenue Decimal(12.2),
date DATE,
time TIME

);
SET GLOBAL LOCAL_INFILE=ON ;

USE tata;
LOAD DATA LOCAL INFILE 'C:/KAGGLE(DATSET)/Spotfy/TATA_01.csv'
INTO TABLE online_retail
FIELDS TERMINATED BY ',' 
ENCLOSED BY '"'
LINES TERMINATED BY '\r\n'
IGNORE 1 LINES
(Description01, Quantity, Unit_Price, Customer_ID, Country, Invoice_No, Stock_Code, Revenue, date, time);


SELECT * FROM online_retail ;

SELECT COUNT(Description01) FROM online_retail ;
