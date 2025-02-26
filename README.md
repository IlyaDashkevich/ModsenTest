## Modsen Test Event API

## Installation

# 1. Clone the Repository:
```bash
git clone https://github.com/your-repo/ModsenTestEvent.git
cd ModsenTestEvent
```
# 2. Build and Run Docker Containers:

Ensure you have Docker and Docker Compose installed. Then execute:
```bash
docker-compose up -d
```
This will build and start the necessary containers for the API and database.

# 3. Apply Database Migrations:

Once the containers are running, apply the migrations to initialize the database:
```powershell
Invoke-WebRequest -Uri http://localhost:8080/api/migrations/apply -Method POST 
```
Or you can open Swagger UI and then use Migration Endpoint to initialize the database

# 4. Access the API:

After completing the setup, you can access the API at:

Swagger UI: http://localhost:8080/swagger/index.html

API Endpoint Example: http://localhost:8080/api/events

Environment Variables (Optional)

By default, database connection settings are set inside appsettings.json. However, you can override them using environment variables by modifying docker-compose.yml.

Stopping the Application

To stop and remove all running containers:

docker-compose down

