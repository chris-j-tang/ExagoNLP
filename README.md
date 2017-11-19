# ExagoNLP

## Table of Contents
* Proposal
* Goals/Deliverables
* Minimal Requirements
* Optional Requirements
* Installing ExagoNLP
* Using ExagoNLP

### Proposal
Exago Business Intelligence is a software application that allows users to easily create their own reports and visualizations, and do analysis on the data that is being accessed.  A natural extension to this is NLP, where a user can ‘ask’ a question in either typed or voice input, and get an answer back based on the data in either displayed or voice (or potentially others such as SMS, email, etc.) output. 

We as humans can understand what the person is requesting, but how can we write computer algorithms that can make these conclusions?  If the computer can't understand ore receives an ambiguous request, can we build an AI that asks the user for more specific information, then ‘learn’ from the response going forward?  How do we use the names of data objects (e.g. tables, views) and field names to help make educated conclusions about what the user is asking?
 
The purpose of this project is to interpret what the user is asking, form a query against the database, and return a result.  If there is uncertainty in the question, then ask a question back to the user and learn the answer going forward.  

We are currently planning on using the freely-available Northwind database for development purposes as per recommendation from our Exago contacts, as it is well structured and used commonly within their organization. Other databases may be used for testing; we’ll look to ensure that there are no references in the code to any specific database.

### Goals/Deliverables
* Accessing and understanding NLP technology (9/31)
* Form a cohesive understanding of linguistics (10/15)
* Get NLP results as usable data in the program (11/1)
* Process the NLP data to generate a SQL query on the database (12/15)

### Minimal Requirements
#### Apache OpenNLP
##### Ubuntu Linux
Download the source file from Apache OpenNLP's website. The one our team used was `apache-opennlp-1.8.2-src.zip`. After downloading and extracting the resulting source files into the target directory, `cd` into the subdirectory that you wish to use, and run `mvn install`.
##### Windows 10

<!-- #### NLPTK -->
### Optional Requirements
### Installing ExagoNLP
### Installing MySQL-Python Connector:
* Install python 3.4 from windows here: https://www.python.org/downloads/release/python-340/
* Must use install for "all users"
* Add the location of this application to your system's PATH
* Install MySQL driver from https://dev.mysql.com/downloads/connector/python/

### To generate a Northwind database in MySQL from script:
*Install the MySQL app (stick with default settings, and configure as a development machine):
https://dev.mysql.com/downloads/installer/

* Use this link to download the script to build a Northwind Database:
https://www.aspsnippets.com/Articles/Download-and-Install-Microsoft-Northwind-Sample-database-in-MySql.aspx
(select Northwind.MySQL5.sql)
* Open script in a text editor, copy the contents to the MySQL instance and execute
* *There's a small SQL syntax error on line 4601, the line GROUP BY City WITH ROLLUP;
to fix it just remove WITH ROLLUP and the script should execute fully

* To verify the database has been built properly, open a new tab for querying and run a small query (ex):
USE northwind;
SHOW tables;
SHOW columns FROM employees;

* (Should generate two tables as results, with all database tables
   listed in the first and each employee entry columns in the second)
### Using ExagoNLP
