# Book_shooping
BookShoppingCartMvc
A basic e-commerce system for beginners built using .NET Core MVC. This project demonstrates the functionality of a shopping cart and includes authentication, database integration, and admin features.

Tech Stack
Backend: .NET Core MVC (Upgraded to .NET 8.0)
Frontend: Bootstrap 5
Database: MS SQL Server
ORM: Entity Framework Core
Authentication: Identity Core
How to Run the Project
Follow these steps to set up and run the project locally:

Clone the repository:

bash
Copy code
git clone https://github.com/your-username/BookShoppingCartMvc.git
cd BookShoppingCartMvc
Open the solution file BookShoppingCartMvc.sln in Visual Studio.

Update the appsettings.json file with your database connection string:

json
Copy code
"ConnectionStrings": {
  "conn": "data source=your_server_name;initial catalog=BookShoppingCartMvc; integrated security=true;encrypt=false"
}
Delete the Migrations folder (if it exists).

Open Tools > Package Manager > Package Manager Console in Visual Studio and run:

bash
Copy code
add-migration init
update-database
Run the project in Visual Studio.

Admin Credentials
Use the following credentials to log in as an admin:

Username: admin@gmail.com
Password: Admin@123
Note: To register as admin, uncomment the DbSeeder.SeedDefaultData lines in Program.cs, run the project, then comment them again.

Database Setup
Add the following data to test the application:

Genres
Run these SQL scripts to populate the Genre table:

sql
Copy code
INSERT INTO [Genre] (Id, GenreName) VALUES 
(1, 'Romance'), (2, 'Action'), (3, 'Thriller'), (4, 'Crime'), 
(5, 'SelfHelp'), (6, 'Programming');
Books
Add sample books linked to genres:

sql
Copy code
INSERT INTO [Book] (BookName, AuthorName, Price, GenreId) VALUES
('Pride and Prejudice', 'Jane Austen', 12.99, 1),
('The Notebook', 'Nicholas Sparks', 11.99, 1);
Order Status
Populate the OrderStatus table:

sql
Copy code
INSERT INTO [OrderStatus] (Id, StatusId, StatusName) VALUES
(1, 1, 'Pending'), (2, 2, 'Shipped'), (3, 3, 'Delivered');
Stored Procedure
Create the stored procedure for fetching top-selling books:

sql
Copy code
CREATE PROCEDURE [dbo].[Usp_GetTopNSellingBooksByDate]
@startDate datetime, @endDate datetime
AS
BEGIN
    SET NOCOUNT ON;
    -- Your stored procedure logic
END
Features
User Registration and Login
Add to Cart and Checkout
Admin Panel: Manage Books, Genres, and Orders
Display Stock and Update Stock
View Top-Selling Books
Screenshots
(Include screenshots of your application here: Homepage, Login, Cart, Admin Dashboard, etc.)

License
This project is licensed under the MIT License.

BookShoppingCartMvc
A basic e-commerce system for beginners built using .NET Core MVC. This project demonstrates the functionality of a shopping cart and includes authentication, database integration, and admin features.

Tech Stack
Backend: .NET Core MVC (Upgraded to .NET 8.0)
Frontend: Bootstrap 5
Database: MS SQL Server
ORM: Entity Framework Core
Authentication: Identity Core
How to Run the Project
Follow these steps to set up and run the project locally:

Clone the repository:

bash
Copy code
git clone https://github.com/your-username/BookShoppingCartMvc.git
cd BookShoppingCartMvc
Open the solution file BookShoppingCartMvc.sln in Visual Studio.

Update the appsettings.json file with your database connection string:

json
Copy code
"ConnectionStrings": {
  "conn": "data source=your_server_name;initial catalog=BookShoppingCartMvc; integrated security=true;encrypt=false"
}
Delete the Migrations folder (if it exists).

Open Tools > Package Manager > Package Manager Console in Visual Studio and run:

bash
Copy code
add-migration init
update-database
Run the project in Visual Studio.

Admin Credentials
Use the following credentials to log in as an admin:

Username: admin@gmail.com
Password: Admin@123
Note: To register as admin, uncomment the DbSeeder.SeedDefaultData lines in Program.cs, run the project, then comment them again.

Database Setup
Add the following data to test the application:

Genres
Run these SQL scripts to populate the Genre table:

sql
Copy code
INSERT INTO [Genre] (Id, GenreName) VALUES 
(1, 'Romance'), (2, 'Action'), (3, 'Thriller'), (4, 'Crime'), 
(5, 'SelfHelp'), (6, 'Programming');
Books
Add sample books linked to genres:

sql
Copy code
INSERT INTO [Book] (BookName, AuthorName, Price, GenreId) VALUES
('Pride and Prejudice', 'Jane Austen', 12.99, 1),
('The Notebook', 'Nicholas Sparks', 11.99, 1);
Order Status
Populate the OrderStatus table:

sql
Copy code
INSERT INTO [OrderStatus] (Id, StatusId, StatusName) VALUES
(1, 1, 'Pending'), (2, 2, 'Shipped'), (3, 3, 'Delivered');
Stored Procedure
Create the stored procedure for fetching top-selling books:

sql
Copy code
CREATE PROCEDURE [dbo].[Usp_GetTopNSellingBooksByDate]
@startDate datetime, @endDate datetime
AS
BEGIN
    SET NOCOUNT ON;
    -- Your stored procedure logic
END
Features
User Registration and Login
Add to Cart and Checkout
Admin Panel: Manage Books, Genres, and Orders
Display Stock and Update Stock
View Top-Selling Books
Screenshots
(Include screenshots of your application here: Homepage, Login, Cart, Admin Dashboard, etc.)

License
This project is licensed under the MIT License.

