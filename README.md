# SIMS - Secure Information Management System

ASP.NET Core MVC-based web application for managing investigative information with role-based access control.

## 📋 Project Overview

SIMS is a secure web application designed for managing investigative cases and reports with three distinct user roles:
- **Admin** - Complete system management and oversight
- **Investigator** - Case investigation and management
- **Reporter** - Report submission and tracking

## 🛠️ Technology Stack

- **Framework**: ASP.NET Core 10.0 (MVC)
- **Language**: C# 
- **Database**: SQL Server (LocalDB/Express)
- **Authentication**: Session-based authentication
- **UI**: Razor Views with Bootstrap

## 📁 Project Structure

```
SIMS/
├── Controllers/          # MVC Controllers
│   ├── AccountController.cs
│   ├── AdminController.cs
│   ├── HomeController.cs
│   ├── InvestigatorController.cs
│   ├── MessagesController.cs
│   └── ReporterController.cs
├── Models/              # Data models
│   ├── ProjectModels.cs
│   └── UserRole.cs
├── Views/               # Razor views
│   ├── Admin/
│   ├── Home/
│   ├── Investigator/
│   ├── Messages/
│   ├── Reporter/
│   └── Shared/
├── Data/                # Database context
│   └── ApplicationDbContext.cs
├── Filters/             # Custom filters
│   └── RoleAuthorizeAttribute.cs
├── wwwroot/             # Static files
│   ├── css/
│   ├── js/
│   ├── lib/
│   └── uploads/
└── Properties/
    └── launchSettings.json
```

## ⚙️ Prerequisites

- [.NET 10.0 SDK](https://dotnet.microsoft.com/download)
- [Visual Studio 2022 Community](https://visualstudio.microsoft.com/vs/community/) or later
- SQL Server Express/LocalDB (included with Visual Studio)

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/SIMS.git
cd SIMS
```

### 2. Configure Database Connection

Update the connection string in `appsettings.json`:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=SecureIMSS;Trusted_Connection=True;TrustServerCertificate=True;"
  }
}
```

### 3. Restore Dependencies

```bash
dotnet restore
```

### 4. Run the Application

**Option A: Using Visual Studio**
1. Open `SIMS.csproj` in Visual Studio 2022
2. Press `F5` or click "Start Debugging"

**Option B: Using .NET CLI**
```bash
dotnet run
```

The application will start at:
- HTTPS: `https://localhost:5001`
- HTTP: `http://localhost:5000`

## 🔐 User Roles & Features

### Admin
- User management
- Role assignment
- System configuration
- Full access to all reports and investigations

### Investigator
- Case management
- Investigation tracking
- Report review and updates
- Evidence management

### Reporter
- Submit new reports
- Track report status
- View own submissions
- Communicate with investigators

## 📦 Dependencies

```xml
<PackageReference Include="Microsoft.Data.SqlClient" Version="6.1.4" />
```

## 🗄️ Database

The application uses SQL Server with the following main components:
- User authentication and authorization
- Role-based access control
- Report and case management
- File upload tracking

Database name: `SecureIMSS`

## 🔒 Security Features

- Session-based authentication
- Role-based authorization using custom `RoleAuthorizeAttribute`
- Secure file upload handling
- HTTPS redirection
- SQL injection protection via parameterized queries

## 🎨 UI Components

The application includes Bootstrap-based responsive UI with:
- Login/Registration pages
- Role-specific dashboards
- Data tables for listing
- Forms for data entry
- File upload interface

## 📝 Configuration Files

- `appsettings.json` - Application configuration and connection strings
- `launchSettings.json` - Development environment settings
- `dotnet-tools.json` - .NET tools configuration

## 🧪 Development

### Build the Project
```bash
dotnet build
```

### Clean Build Artifacts
```bash
dotnet clean
```

### Publish for Deployment
```bash
dotnet publish -c Release -o ./publish
```

## 📤 Uploading to GitHub

After cloning/creating your repository:

```bash
# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - SIMS Application"

# Add remote repository
git remote add origin https://github.com/YOUR_USERNAME/SIMS.git

# Push to GitHub
git push -u origin main
```

## 🚨 Important Notes

⚠️ **Before deploying to production:**
1. Update the database connection string
2. Change authentication secrets
3. Remove sensitive data from `appsettings.json`
4. Configure proper logging
5. Set up HTTPS certificates
6. Review security configurations

## 📄 License

[Add your license information here]

## 👤 Author

[Add your name and contact information]

## 🤝 Contributing

[Add contribution guidelines if applicable]

## 📞 Support

For issues and questions, please open an issue on GitHub.

---

**Note**: This application requires .NET 10.0 runtime. Make sure you have the correct SDK installed before running.
