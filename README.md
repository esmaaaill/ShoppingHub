# ShoppingHub

ShoppingHub is an e-commerce web application built as our **graduation project for Project 1 of the ITI .NET Development Track**.

The project applies a layered architecture using ASP.NET Core MVC and separates the application into Presentation, Business Logic, and Data Access layers.

## Project Overview

ShoppingHub provides the foundation of a complete online shopping platform with support for user accounts, products, categories, shopping carts, orders, ratings, and multilingual UI.

## Features

- User registration, login, authentication, and role management
- ASP.NET Core Identity integration
- Admin and user roles
- Product and category management
- Shopping cart functionality
- Order and order-item management
- Product ratings
- User profile support
- English and Arabic localization
- SQL Server database integration
- Entity Framework Core migrations
- Repository and service layers
- AutoMapper support
- Email functionality using MailKit

## Tech Stack

- **.NET 8**
- **ASP.NET Core MVC**
- **C#**
- **Entity Framework Core**
- **SQL Server**
- **ASP.NET Core Identity**
- **AutoMapper**
- **MailKit**
- **Razor Views**
- **HTML / CSS / JavaScript**

## Architecture

The solution follows a three-layer architecture:

```text
ShoppingHub
├── ShoppingHub.PL     # Presentation Layer
├── ShoppingHub.BLL    # Business Logic Layer
├── ShoppingHub.DAL    # Data Access Layer
└── ShoppingHub.sln
```

### ShoppingHub.PL

The Presentation Layer contains the MVC application, including:

- Controllers
- Razor Views
- View models
- Localization resources
- Static files
- Application configuration

### ShoppingHub.BLL

The Business Logic Layer contains:

- Services
- Service abstractions
- View models
- Mapping configuration
- Helper classes

### ShoppingHub.DAL

The Data Access Layer contains:

- Entity models
- Database context
- Repository abstractions and implementations
- Entity Framework Core migrations

## Main Domain Models

The project currently includes domain models for:

- User
- Product
- Category
- Cart Item
- Order
- Order Item
- Product Rating

## Getting Started

### Prerequisites

Make sure you have the following installed:

- .NET 8 SDK
- SQL Server
- Visual Studio 2022 or another .NET-compatible IDE
- Git

### 1. Clone the repository

```bash
git clone https://github.com/esmaaaill/ShoppingHub.git
cd ShoppingHub
```

### 2. Configure the database

The default connection string is located in:

```text
ShoppingHub.PL/appsettings.json
```

By default, the application uses a local SQL Server instance and the database name:

```text
ShoppingHubDb
```

Update the connection string if your SQL Server configuration is different.

### 3. Restore dependencies

```bash
dotnet restore
```

### 4. Apply database migrations

From the repository root, run:

```bash
dotnet ef database update --project ShoppingHub.DAL --startup-project ShoppingHub.PL
```

If the Entity Framework CLI tool is not installed:

```bash
dotnet tool install --global dotnet-ef
```

### 5. Run the application

```bash
dotnet run --project ShoppingHub.PL
```

Then open the local URL shown in the terminal.

## Localization

ShoppingHub supports:

- English (`en-US`)
- Arabic (`ar-EG`)

The application uses ASP.NET Core localization and can change culture through query-string or cookie-based culture providers.

## Authentication and Authorization

ShoppingHub uses ASP.NET Core Identity.

The application creates the following roles at startup when they do not already exist:

- Admin
- User

## Academic Context

This repository was developed as a **graduation project for Project 1 of the ITI .NET Development Track**.

The purpose of the project was to apply the concepts covered during the track in a practical e-commerce application, including:

- ASP.NET Core MVC
- Layered architecture
- Entity Framework Core
- SQL Server
- Identity and authorization
- Repository and service patterns
- Localization
- Database migrations

## Contributing

This repository was created as a collaborative graduation project.

For future changes:

1. Create a new branch.
2. Make and test your changes.
3. Commit using a clear commit message.
4. Open a pull request.
5. Review the changes before merging into `main`.

Example:

```bash
git checkout -b feature/your-feature
git add .
git commit -m "Add your feature"
git push origin feature/your-feature
```

## Repository

[ShoppingHub on GitHub](https://github.com/esmaaaill/ShoppingHub)
