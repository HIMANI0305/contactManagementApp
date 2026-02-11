# contactManagementApp

A web application built with ASP.NET Core MVC for managing personal contacts. Users can register, log in, and perform CRUD operations on their contacts, including uploading profile and contact images.

## Features

- **User Authentication**: Register and login functionality with session management.
- **Contact Management**: Add, view, update, and delete contacts.
- **Image Uploads**: Upload profile pictures for users and contact images.
- **Responsive UI**: Built with Bootstrap for a clean, responsive interface.
- **Database Integration**: Uses PostgreSQL for data storage.
- **Repository Pattern**: Clean architecture with separate repositories for data access.

## Prerequisites

- .NET 8.0 SDK
- PostgreSQL 12 or later
- Visual Studio 2022 or Visual Studio Code

## Installation

1. Clone the repository:
   ```
   git clone <repository-url>
   cd Ketan_MVC
   ```

2. Restore NuGet packages:
   ```
   dotnet restore
   ```

## Database Setup

1. Create a PostgreSQL database named `Demo`.

2. Update the connection string in `MVC/appsettings.json`:
   ```json
   "ConnectionStrings": {
     "pgconn": "Host=localhost;Port=5432;Database=Demo;Username=your_username;Password=your_password"
   }
   ```

3. Run the database migrations or create the necessary tables. (Note: Migration scripts may need to be added based on your schema.)

## Running the Application

1. Navigate to the MVC project directory:
   ```
   cd MVC
   ```

2. Run the application:
   ```
   dotnet run
   ```

3. Open your browser and navigate to `https://localhost:5001` (or the port specified in launchSettings.json).

## Technologies Used

- **ASP.NET Core MVC**: Web framework
- **C#**: Programming language
- **PostgreSQL**: Database
- **Npgsql**: PostgreSQL provider for .NET
- **Bootstrap**: CSS framework
- **jQuery**: JavaScript library

## Project Structure

```
Ketan_MVC/
├── DemoMVC.sln
├── MVC/                          # Main web application
│   ├── Controllers/
│   │   ├── HomeController.cs     # Handles login/register
│   │   ├── ContactController.cs  # Handles contact CRUD
│   │   └── ContactSingleController.cs
│   ├── Views/
│   │   ├── Home/
│   │   ├── Contact/
│   │   └── Shared/
│   ├── wwwroot/                  # Static files (CSS, JS, images)
│   ├── appsettings.json
│   └── Program.cs
└── Repositories/                  # Data access layer
    ├── Interfaces/
    ├── Implementations/
    └── Models/
```

## Usage

1. Register a new user account.
2. Log in with your credentials.
3. Navigate to the Contact section to manage your contacts.
4. Add new contacts with optional images.
5. View, edit, or delete existing contacts.

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Submit a pull request.

## License

This project is for demonstration purposes.
