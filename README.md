# Todo API DotNET

This is a test project designed to explore dotnet core and the entity framework.

## Run application

Instructions to run the application and the docker-compose configuration development environment.

``` sh
# Run application: http://localhost:5015
dotnet run

# Run docker (for development environment)
docker-compose up -d

# Shut down docker
docker-compose down

# Remove database data
sudo rm -rf ./docker-data
```

## Initalize new application

Steps to recreate this application and its configuration.

``` sh
# Create dotnet application
dotnet new webapi --use-controllers -o todo-api-dotnet

# Initalize gitignore
dotnet new gitignore

# Add entity framework tools
dotnet tool install --global dotnet-ef
dotnet add package Microsoft.EntityFrameworkCore.Design
dotnet add package Npgsql.EntityFrameworkCore.PostgreSQL
```

## Connect to pgsql using Adminer

Access adminer: [localhost:8080](localhost:8080)

Access postgres: [localhost:5432](localhost:5432)

|    **Key**   |  **Value** |
|:------------:|:----------:|
| **System**   | PostgreSQL |
| **Server**   |     db     |
| **Username** |  postgres  |
| **Password** |  password  |
| **Database** |    todo    |
