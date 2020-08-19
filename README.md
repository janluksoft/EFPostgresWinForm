# Entity Framework with Postgres Server

The application demonstrates the use of Entity Framework to perform simple CRUD operations on a Postgres Server database using WinForm windows.

The structure of the table is defined by the POCO (CPerson) class. The class (PeopleDBContext) creates a context (dbPersons) that represents a table (Sprinters) in the form of an object. Operations on this object are automatically transferred to the table (Sprinters) in the database.

## Using the application

- Create a table (Sprinters) in pgAdmin4, in (Query Editor) via SQL command: pgAdmin4 will create the (Sprinters) table. (is described further). The (SaveChanges()) method in SQL Server creates the table itself when it is missing. In Postgres, it will not create a table in this way. Therefore, it should be done in pgAdmin4.

- On the (Login) tab, enter the login information from Postgres Server
- Check the connection with the button 2 (Check Connection)
- For valid data, a message will be shown: (Connection Good)

![](/Jpg/Entity-Framework_Postgres_Login-parameters.png)
![](/Jpg/Entity-Framework_Postgres_Login-params_pgAdmin.png)

- In the (Proposal) tab, you can press the button: the application should save 5 example rows to a table (Sprinters) and on the Postgres Server.

- In the (DataBase) tab you can: (5) read the table from the SQL server, (6) add rows, (7) delete rows. 

![](/Jpg/Entity-Framework_Postgres_Table_Sprinters.png)

## Create Table

   ```
CREATE TABLE public."Sprinters" 
("Id" serial NOT NULL PRIMARY KEY, 
"name" text, 
"surname" text, 
"age" real,
"city" text,
"height" real ); 
   ```

![](/Jpg/Create_Table_in_Postgres.png)


## Details

- Environment: VS2019
- Target Framework: .NET Framework 4.7.2
- Window: WinForm




