# 📊 Ubuntu-MySQL-Database-Creation-Basic 📊

This showcases a basic MySQL installation and usage demonstration on Ubuntu Desktop, following [a guided video](https://www.youtube.com/watch?v=xiUTqnI6xk8) from Network Chuck's youtube. 

# Installation 

On Ubuntu, the command "_sudo apt update_" is used to update repositories:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/e2e90e43-b63b-4950-b25c-cd35b533ad9f)


Next "_sudo apt install mysql-server -y_" is used to install MySQL server:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/35c754a4-4958-4147-adc7-d405066cd609)

Then "_sudo systemctl status mysql_" is used to verify that the MySQL service is running:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/ae81fd8e-3f9b-46a3-8e78-d403aebbb69c)

<br/> 

# Creating the Database 

With MySQL running, we access the application with simply "_mysql_" since no password has been set yet:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/51efbafd-679e-4de7-abc9-bd3f1e3810f1)

Note that we are accessing MySQL locally where the service is actually installed. Accessing MySQL remotely will require different syntax to login from another machine. 

"_mysql - h hostname -u username -p_"

Using the command "_show databases;_" with the mysql> prompt, we show that our database is brand new and has no custom entries yet:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/fca5daf8-6d35-4ce6-a2cb-ee7e8196d8c7)

Next a database is created with the command "_create database nc_coffee;_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/56441df3-bfc1-41e1-b0a6-880b1691bbb3)

The nc_cffee database is now shown when the command "_show databases;_" is used again:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/c6db417a-007d-4139-9dc3-dc7e79d96b98)

The nc_coffee database is selected for modification with the command "_use nc_coffee;_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/13111e45-f7ca-4bef-8e63-1e9726d3d0fd)

Even though the database was created and selected, there are no data tables created yet. Shown with "_show tables;_":

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/848fa051-cc00-4fe1-895f-06f6c89a878a)

<br/> 

# Creating the Data Tables

From here a data table will be created in the following format from Network Chuck's video:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/93d032a9-2642-409d-afb4-97b598129bf2)

The command "create table coffee_table" creates a table within the nc_coffee database:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/9440b6fd-3b32-4bfe-9923-92efc315e648)

From here, columns will be added to the table, along with the data types for each column.

The Columns defined will be:
- ID,  datatype integer
- Name, datatype variable character string (255 characters max)
- Region, datatype variable character string (255 characters max)
- Roast, datatype variable character string (255 characters max)

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/a6b3f9f1-0f8f-4933-8b9a-830c62906754)

Running the "_show tables;_" command we can see that the coffee_table is present within the nc_coffee database:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/4471c84e-26c5-4aac-9d6a-c7d24a3870fa)

