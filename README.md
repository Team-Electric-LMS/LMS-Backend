# LMS Backend

A Learning Management System (LMS) backend built with .NET 9.0 and ASP.NET Core.

## About

This project was originally developed as a collaborative school project and has been forked for personal development and improvement.

## Architecture

The project follows a clean architecture pattern with the following layers:

- **LMS.API** - The main API project with controllers and endpoints
- **LMS.Presentation** - Presentation layer with controllers
- **LMS.Services** - Business logic and service implementations
- **LMS.Infrastructure** - Data access and external services
- **Domain.Models** - Domain entities and models
- **Domain.Contracts** - Domain interfaces and contracts
- **Service.Contracts** - Service interfaces
- **LMS.Shared** - Shared utilities and DTOs

## Getting Started

### Prerequisites

- .NET 9.0 SDK or later
- SQL Server (LocalDB for development)

### Building the Project

```bash
dotnet restore
dotnet build
```

### Running the API

```bash
cd LMS.API
dotnet run
```

The API will be available at `https://localhost:7213` (or as configured in launchSettings.json).

## Configuration

The application uses the following default configuration:

- **Database**: LocalDB with database name `LmsDB`
- **JWT Authentication**: Configured for API authentication
- See `appsettings.json` for detailed configuration

## Architecture Diagram

![diagram](LMS.API/20250917_DGML.png)

## License

This is a personal project. See LICENSE file for details (if applicable).