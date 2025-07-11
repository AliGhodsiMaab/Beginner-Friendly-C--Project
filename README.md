
# Beginner-Friendly C# Project with Entity Framework Core

This is a **learning project** built with C# and **Entity Framework Core**. It is designed for beginners who want to get familiar with core database concepts, data models, and LINQ-based querying using .NET.

---

## Prerequisites

To run this project smoothly, make sure the following tools and components are installed on your system:

- [.NET SDK](https://dotnet.microsoft.com/download) (compatible with EF Core 9)
- [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
- [SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-ssms) (to inspect database changes)
- NuGet packages:
  - `Microsoft.EntityFrameworkCore`
  - `Microsoft.EntityFrameworkCore.SqlServer`
  - `Microsoft.EntityFrameworkCore.Tools`

> ⚠Setting up these tools may take some time, but it's a natural and essential part of learning the .NET ecosystem.

---

## IDE Recommendation

You can use any of the following IDEs:

- [JetBrains Rider](https://www.jetbrains.com/rider/)
- [Visual Studio](https://visualstudio.microsoft.com/)

---

## Models & DbContext

- All **entity classes** are placed in the `Models` folder.
- The `SchoolContext` class extends `DbContext` and contains `DbSet<T>` properties which represent database tables.
- In the `OnConfiguring` method, the connection string is set. You may need to update it depending on your **local SQL Server setup**.
- In `OnModelCreating`, the **relationships** between entities are defined (e.g., one-to-many, many-to-many).

---

## Program Flow (Main Logic in `Program.cs`)

### 1. **Database Initialization**

We create an instance of the `StartAndDeleteAndCreateDbContext` class to:

- Clean the database
- Seed sample data using our predefined model instances  
This ensures consistent test data on every run.

---

### 2. **Working with Students via Methods**

The `MethodsOfStudent` class contains custom methods for handling data through the DbContext.

---

### 3. **Demonstrating Different Querying Styles**

We use the `ModelsMethods` class to showcase different data querying techniques:

- **Eager Loading**
- **Explicit Loading**
- **Ordered Queries**
- **LIKE Filtering**
- **Paging Results**

These examples will help you understand how EF Core retrieves data in different scenarios.

---

### 4. **Entity States Overview**

Finally, we demonstrate how **Entity States** work in EF Core via the `EntityState` class.

> ℹWhile this concept may not be frequently used in everyday apps, understanding it helps you better grasp how EF tracks changes to your entities.

---

## Final Notes

This project is intended to give beginners practical experience with EF Core, data modeling, and LINQ operations. If you're new to the world of C# and databases, you're in the right place!

Good luck, and enjoy your coding journey! 

---
