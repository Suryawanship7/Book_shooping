# BookShoppingCartMvc  
A beginner-friendly e-commerce system built using .NET Core MVC, demonstrating a fully functional shopping cart with features like user authentication, order management, and an admin panel.

---

## Features

### User Features
- Browse and search for books by genre.
- Add books to the shopping cart.
- Place orders and track order status.
- View order history.

### Admin Features
- Manage books, genres, and stock directly from the admin panel.
- Update and track order statuses.
- View top-selling books based on a custom date range.

---

## Tech Stack  
- **Framework**: ASP.NET Core MVC (Upgraded to .NET 8.0)  
- **Database**: MS SQL Server  
- **Frontend**: Bootstrap 5  
- **ORM**: Entity Framework Core  
- **Authentication**: Identity Core  

---

## Getting Started

### Prerequisites
1. **Visual Studio 2022**  
   - Install the latest version from [Visual Studio Downloads](https://visualstudio.microsoft.com/).
2. **MS SQL Server**  
   - Install [SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms).

---

### Setup Instructions

1. **Clone the Repository**  
   Open a terminal and run:
   ```bash
   git clone https://github.com/your-username/BookShoppingCartMvc.git
   cd BookShoppingCartMvc
2. **Open the Project**  
   - Locate the `BookShoppingCartMvc.sln` file in the project directory and open it in Visual Studio.

3. **Update the Database Connection**  
   - Navigate to the `appsettings.json` file in the project. Update the `ConnectionStrings` section with your SQL Server details:
     ```json
     "ConnectionStrings": {
       "conn": "data source=your_server_name;initial catalog=BookShoppingCartMvc;integrated security=true;encrypt=false"
     }
     ```

4. **Initialize the Database**  
   - Open **Tools > NuGet Package Manager > Package Manager Console** in Visual Studio.
   - Execute the following commands to create and update the database schema:
     ```bash
     add-migration Initial
     update-database
     ```

5. **Run the Application**  
   - Start the application by pressing **F5** or clicking the **Run** button in Visual Studio.

---

### Admin Login Credentials  
To access the admin panel, use the following credentials:  
- **Username**: `admin@gmail.com`  
- **Password**: `Admin@123`  

**Note**:  
If these credentials are not already set up, uncomment the lines in `Program.cs` to seed default admin data. Run the application once, then comment the lines back:  
```csharp
//using(var scope = app.Services.CreateScope())
//{
//    await DbSeeder.SeedDefaultData(scope.ServiceProvider);
//}
