<div align="center">

# WPF User Registration & Profile App

### A multi-page desktop application for account creation, sign-in, and profile display

`C#` · `WPF` · `.NET Framework 4.7.2` · `Entity Framework 6` · `SQL Server` · `XAML`

</div>

## Overview

This project is a compact Windows desktop application demonstrating navigation between sign-in, registration, and profile pages. User information is persisted through an Entity Framework database-first model connected to SQL Server.

## Features

- Sign in with username and password.
- Register a user with username, password, age, phone number, gender, and city.
- Validate user credentials against the database.
- Navigate between WPF pages inside a `NavigationWindow`.
- Display the signed-in user's profile information.
- Persist data with Entity Framework 6 and SQL Server.

## Screen flow

```mermaid
flowchart LR
    SignIn[Page 1: Sign in] -->|New account| SignUp[Page 2: Sign up]
    SignUp --> DB[(SQL Server)]
    SignIn --> DB
    DB -->|Valid credentials| Profile[Page 3: Welcome profile]
```

## Project map

```text
├── Exam.sln
└── Exam/
    ├── MainWindow.xaml       Navigation host
    ├── Page1.xaml            Sign-in page
    ├── Page2.xaml            Registration page
    ├── Page3.xaml            Profile / welcome page
    ├── Model1.edmx           Entity Framework database model
    ├── userInfo.cs           Generated user entity
    └── App.config            Runtime and SQL configuration
```

## Requirements

- Windows 10/11
- Visual Studio 2022 with **.NET desktop development**
- .NET Framework 4.7.2 developer pack
- SQL Server Express or SQL Server

## Run locally

```bash
git clone https://github.com/MostafaMedhat19/Second-Desktop-Project-.git
```

1. Open `Exam.sln` in Visual Studio.
2. Restore NuGet packages.
3. Create or restore the `Profile` database.
4. Replace the `ProfileEntities` connection string in `Exam/App.config` with your SQL Server details.
5. Build and run the `Exam` project.

> The repository contains a machine-specific SQL Server connection string. Update it before running the application on another computer.

## Learning outcomes

- WPF page navigation and event handling.
- Form input and desktop UI layout with XAML.
- Entity Framework database-first integration.
- Reading and writing account records in SQL Server.

## Recommended improvements

- Hash passwords and add stronger input validation.
- Adopt MVVM to separate UI and application logic.
- Add screenshots and automated validation tests.
- Remove `.vs`, `bin`, `obj`, and package artifacts from source control.

## Author

[Mostafa Medhat](https://github.com/MostafaMedhat19)
