# Workshop_Golang_Fiber

## Introduction

Welcome to our Workshop, today we will see how to create a web application with a login/register feature and to-do-list using [Golang](https://go.dev/) with the framework [Fiber](https://go.dev/) and the database [MYSQL](https://www.mysql.com/fr/).\
We hope that you will enjoy and learn as much as you can during this workshop ! :)

---
## Prerequisites

### **What we need ?**
For this workshop you will need to have **Golang** installed on your computer. If it's not already done, you can find the installation [here](https://go.dev/doc/install).
We also need to install our mysql database, you can download it from the package manager of your machine.

### How to compile a golang project ?
First of all, you have to init your "module"
```bash
    $ go mod init "name-of-the-project"
```
you can now compile the project
```bash
    $ go run main.go
```

## **DOCUMENTATION /!\\**
- _You will find all the documentation you need by clicking [here](https://go.dev/). (fiber documentation)

---
---


## __STEP 0__ : **_Create a server_**
Initiate a server who listen on the port 8000.

---
## __STEP 1__ : **_Create a basic route_**
    Create a route ("/home") and print "hello world"
    You can use an application to test your api or you can go to "https://localhost:8000/home"

---
## __STEP 2__ : **_Connect your database_**
To connect your database to your server, we advice you to use [Gorm](https://gorm.io/)

    Connect your  database to your fiber server.
    You can use the file "mydb.sql" gived in the repository.
    After that, you can put your table to a variable

---
## __STEP 3__ : **_Register_**
    For the registration, you have to :
        - Get the data from the request's parameters (username and password)
        - Check if the username and the password are not already used
        - If not, put the user to the "Users" table
        - Redirect the user  to the login page

## __STEP 4__ : **_Login_**
    For the login, you have to :
        - Get the data from the request's parameters (username and password)
        - Check if the user is in the database
        - Print welcome "username"

---
## __STEP 5__ : **_Logout_**
    The logout is pretty simple, you just have to redirect the user to the home page.

---

## __STEP 6__ : **_Make a route to print todos__**
    make a route "/todos" who will return the table todos as JSON data.

## __STEP 7__ : **_Add a todo_**
    Create a new route ("/todo/create-todo") to create a todo. In this route, you have to add the todo in the database (table todos)

---

## __STEP 8__ : **_Change the status of a todo_**
    Create a new route("/todo/achieve/:id) to change the status of a todo.

---
## __STEP 9__ : **_Delete a todo_**
    Create a new route("/todo/delete/:id) to delete a todo