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

# Creating the Data Table

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

The table is shown with "_describe coffee_table_" and there are no entries within the table yet:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/d09c1b49-d65a-44c1-8244-82145531f8c3)

After putting entries, the table should look like this:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/e63fe8a0-316f-4c18-9fe2-8ad052de1647)

Now the rows will be inserted following the format of the columns made:
- ID
- Name
- Region
- Roast

Example from Network Chuck's video:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/76d966af-48de-4ec0-9120-fd2b02073c31)

On my machine, the command "_insert into coffee_table values (1, "default route", "ethiopia", "light");_" is used to create a row with entries aligning with the columns made earlier:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/5eca556e-08d0-41e7-a351-5b99f9be22f4)

The entry is verified with the command "_select * from coffee_table;_":

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/68f9a709-39c1-4402-b8d9-ce712315836d)

The rest of the rows are created with similar commands shown earlier:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/49cd9e41-296d-42a3-9389-c95db5cf5b7b)

After completing the entries, the table now is now complete:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/0d266e26-c182-417b-948a-828da75b1478)

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/42099bcb-b585-4f37-ab48-f7b7c7f44e8c)

<br/> 


# SQL Queries Usage

The command "_select name from coffee_table;_" will return only the name column from the coffee table. (The nc_coffee database is currently selected.)

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/d46a0ba3-f963-4847-b60b-87013b4bb095)

<br/> 

# Creating a 2nd Data Table

The next data table will have the following format:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/dc0ee6bd-8047-472f-a203-d62c9887bba3)

The command "_create table avengers_" makes a new data table named avengers:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/5f2c6cbb-778b-4f01-8d15-b533a5d0dd55)

Next, columns are made:
- id,   integer
- first_name,   variable character string (255 characters)
- last_name,   variable character string (255 characters)
- origin,   variable character string (255 characters)
- age,   variable character string (255 characters)
- alias,   variable character string (255 characters)

  ![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/f78b9747-cea0-4e56-8508-e437d590aab6)

  The avengers table can now be seen in the nc_coffee database:

  ![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/f3b8a6b7-5316-47d8-8b72-4707f625540b)

Next the rest of the rows are created to align with the columns made:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/f88b8fd7-3dab-42e2-8f94-8c7ee2ceccc1)

After the entries, the table is now complete:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/14c8ca0d-b472-4c67-a199-bb37620a2b6a)

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/ed268c30-b61e-4265-887d-c92137c18447)

<br/> 

# SQL Queries Usage 2

This SQL query is for only wanting to see avengers from earth.

Select all columns from the table avengers, only want to see where the column origins = earth

"_select * from avengers where origin = "earth";_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/a084fe96-0acc-4d86-900e-9ac4db2c90e0)

This SQL query is for only showing all avengers from earth OR asgard.

"_select * from avengers where origin = "earth" or origin = "asgard"_;

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/22bc366e-e19a-45da-8296-446bdb92361b)

This SQL query is for only showing all avengers under 30 years old.

"_select alias from avengers where age < 30;_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/09565502-411c-4407-8bfb-b3933d7f2fa7)

This SQL query is for only showing the alias of avengers that do not originate from earth.

"_select alias from avengers where not origin = "earth";_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/27d89bbb-441b-4183-8ded-083f95bde50d)

This next SQL command removes Jeff from the avengers data table.

Here is Jeff who does not belong in the data table:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/d2af1a14-013a-4335-a672-8a8ddfbef508)

"_delete from avengers where first_name = "jeff";_" removes Jeff from the avengers table shown below:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/05373c9a-1d45-4bd3-9971-547451e4faa2)

This next SQL command will update Groot's last name to nothing since Groot has no last name.

"_update avengers set last_name = NULL where first_name = "groot";_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/a51fc822-bf33-4db7-9b48-aa609e5537d3)

This next SQL command updates the avengers table to add a beard column and if each avenger has a beard or not.

We want to alter the table avengers, and add a column named beard with boolean logic datatype of true or false. (0 or 1.)

"_alter table avengers add beard boolean;_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/fc83e3d1-07cc-401f-a2a1-1079816e37a9)

The avengers table after adding the beard column:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/2484761b-a66c-4f31-880e-5234ed3fb3d5)

This next SQL command updates Thor for the beard column to true.

"_update avengers set beard = True where first_name = "thor";_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/51982e5d-f461-4d20-8530-75886e9b1262)

This next SQL command updates Groot for the beard column to false.

"_update avengers set beard = False where first_name = "groot";_"

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/57d75555-489c-4b71-b66b-ad058cc0bcb0)

Here is the rest of the table updated with the beard column:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/3de1ffa0-a75f-4c16-b65d-34ec5eda43f9)

Resources:

Network Chuck's Youtube Video:
["you need to learn SQL RIGHT NOW!! (SQL Tutorial for Beginners)"](https://www.youtube.com/watch?v=xiUTqnI6xk8)



