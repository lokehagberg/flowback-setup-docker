Note that this setup is outdated by 2025-03-24

# Flowback Setup Instructions
## Windows development environment

### Requirements for running windows development environment
- This repository
- Flowback from GitHub: https://github.com/lokehagberg/flowback-backend
- Docker Desktop: https://www.docker.com/products/docker-desktop/
- Microsoft Buildtools: https://visualstudio.microsoft.com/downloads/?q=build+tools
- PostgreSQL 16 Command Line Tools: https://www.enterprisedb.com/downloads/postgres-postgresql-downloads

### Installation
1) Run `docker-compose up -d` in this root directory
2) Move "example.pg_service.conf" to postgres config folder (found using `pg_config` command, check the SYSCONFDIR variable).\
Rename the file to "pg_service.conf"
3) Move "example.flowback_pgpass" to the Flowback root directory, rename the file to ".flowback_pgpass"
4) Create a ".env" folder in Flowback root directory, follow ".env.example" located in Flowback folder
    - By default, set RABBITMQ_BROKER_URL variable to `"amqp://flowback:flowback@localhost:5672/flowback"`

 
