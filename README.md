# library-management-system using python and mysql
# steps to run the project
- download python and mysql on your system
- set the user and root password for mysql
- now open the mysql command line client and enter the the root password
- then we run ```show databases;``` to show the existing databases
- We add our data based which we will call `db` code for it : ```create database db;```
- Then we run : ```create table books(bid varchar(20) primary key, title varchar(30), author varchar(30), status varchar(30));```
-  then : ```create table books_issued(bid varchar(20) primary key, issuedto varchar(30));```
-  *So basically we created 2 tables inside a database named db with multiple access elements*
-   Now to enter into the database you have created use teh code: ```use db;```
-   Now to ckeck the tables you have created you can say ener : ``` show tablesl;```
-   To see the elements inside the tables (for example books) code: ```select * from books;```
-   Similarly to use the elements insie the table ```books_issued``` run the code: ``` select * from books_issued;``
-   if you want to run the code you will need to run : main.py
-   as soon as you run ```main.py``` the UI will popup then as as soon as you add a book by filling the information(case sensitive), you can now get to the CLI of MYSql and run: ``` select * from books;``` and this will display if you have added any book into the database.
# desugn choices made
- The system follows a modular design to improve maintainability and scalability. 
- The project uses Object-Oriented Programming (OOP) principles to model real-world entities like books, users, and transactions.
- A relational database is chosen for its ability to handle relationships between books, users, and transactions efficiently.
- A Command-Line Interface (CLI) has been chosen to interact with the user. While more modern systems may use graphical interfaces, a CLI is lightweight and easy to implement, and it’s ideal for smaller systems or initial prototypes.
  # assumptions/limitations
  - This system assumes that the Library Management System will be used by a single user at a time.
  - The project assumes a relatively simple database structure where the books and users are stored with basic information such as book title, author, and availability status
  - books are manually registered in the system by an admin or librarian before they can be borrowed.
