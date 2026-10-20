# E-Learning Platform

An ASP.NET Core (5.0) MVC web app for an e-learning platform, with user authentication via ASP.NET Identity and a separate Admin area for managing content.

## Stack

- **Framework:** ASP.NET Core 5.0 (MVC + Razor Pages)
- **Auth:** ASP.NET Core Identity
- **ORM / DB:** Entity Framework Core + SQL Server

## Structure

- `IPT_PROJ/Controllers`, `Views` — the public-facing site
- `IPT_PROJ/Areas/Admin` — an admin area with its own controllers and views
- `IPT_PROJ/Areas/Identity` — scaffolded Identity (login/register) pages
- `IPT_PROJ/Entities` — domain models: `Category`, `CategoryItem`, `Content`, `MediaType`, `UserCategory`
- `IPT_PROJ/Data` — `ApplicationDbContext` and EF Core migrations
- `IPT_PROJ/SqlScripts` — seed SQL for category items and media types

## Getting started

### Prerequisites

- [.NET 5.0 SDK](https://dotnet.microsoft.com/download/dotnet/5.0)
- SQL Server (LocalDB or SQL Express works fine for local dev)

### Setup

```bash
git clone https://github.com/D1abol1cal/Elearning-Platform.git
cd Elearning-Platform/IPT_PROJ
```

Update the `DefaultConnection` string in `appsettings.json` to point at your own SQL Server instance, then apply the migrations and run:

```bash
dotnet ef database update
dotnet run
```
