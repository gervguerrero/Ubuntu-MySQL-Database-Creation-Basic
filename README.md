# 📊 Ubuntu-MySQL-Database-Creation-Basic 📊

This showcases a basic MySQL installation and usage demonstration on Ubuntu Desktop, following [a guided video](https://www.youtube.com/watch?v=xiUTqnI6xk8) from Network Chuck's youtube. 

# Installation 

On Ubuntu, the command "_sudo apt update_" is used to update repositories:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/e2e90e43-b63b-4950-b25c-cd35b533ad9f)


Next "_sudo apt install mysql-server -y_" is used to install MySQL server:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/35c754a4-4958-4147-adc7-d405066cd609)

Then "_sudo systemctl status mysql_" is used to verify that the MySQL service is running:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/ae81fd8e-3f9b-46a3-8e78-d403aebbb69c)

# Usage  

With MySQL running, we access the application with simply "_mysql_" since no password has been set yet:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/51efbafd-679e-4de7-abc9-bd3f1e3810f1)

Note that we are accessing MySQL locally where the service is actually installed. Accessing MySQL remotely will require different syntax to login from another machine. 

"_mysql - h hostname -u username -p_"

Using the command "_show databases;_" we show that our database is brand new and has no custom entries yet:

![image](https://github.com/gervguerrero/Ubuntu-MySQL-Database-Creation-Basic/assets/140366635/fca5daf8-6d35-4ce6-a2cb-ee7e8196d8c7)
