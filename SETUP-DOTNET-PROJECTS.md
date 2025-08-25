# zenwebapi10 Solution

This is a placeholder solution file. Replace this with your actual .NET solution file structure.

## Adding Your .NET Projects

1. **Remove this file** and add your actual solution file (`.sln`)
2. **Add your project directories** containing `.csproj` files
3. **Update the solution file** to reference all your projects
4. **Ensure one project is marked as the startup project** for the web application

## Multi-Project Structure Example

```
zenwebapi10/
├── zenwebapi10.sln
├── src/
│   ├── zenwebapi10.Api/
│   │   └── zenwebapi10.Api.csproj
│   ├── zenwebapi10.Core/
│   │   └── zenwebapi10.Core.csproj
│   └── zenwebapi10.Infrastructure/
│       └── zenwebapi10.Infrastructure.csproj
└── tests/
    └── zenwebapi10.Tests/
        └── zenwebapi10.Tests.csproj
```

## Docker Build

The included Dockerfile is designed to:
- Copy all files (including multiple projects)
- Run `dotnet restore` to restore all project dependencies
- Run `dotnet publish` which will automatically detect and build the startup project
- Create a runtime image with the published output

## GitHub Actions

The CI/CD workflow will:
- Build the Docker image with your multi-project solution
- Push to Google Container Registry
- Deploy to your selected target (Cloud Run or GKE)
