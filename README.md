# Mirth Connect Docker Example

This is an example of how to use Docker Compose to set up a Mirth Connect instance along with a PostgreSQL database.

## Services

The docker-compose.yml file defines the following services:

- mirth-connect: This is the Mirth Connect service. It uses the latest image from NextGen Healthcare. It exposes ports 8080 and 8443. It depends on the db service.
- db: This is the PostgreSQL database service. It exposes port 5432.

Both services use the same environment variables file .env.

## Volumes

The mirth-connect service mounts the ./extensions directory to /opt/connect/custom-extensions in the container. This allows you to add custom extensions to your Mirth Connect instance.

## Networks

Both services are part of the default network.

## Usage

1. Clone this repository.
2. Create a .env file in the root directory and define the necessary environment variables.
3. Run docker-compose up to start the services.

Please ensure Docker and Docker Compose are installed and running on your machine before you try to start the services.

### Default Login Credentials

- Username: admin
- Password: admin

## Ports

The following ports are exposed:

- Mirth Connect: 8080 (HTTP), 8443 (HTTPS)
- PostgreSQL: 5432

## Note

This is a basic example and not intended for production use. For production deployments, consider additional security measures and configurations.
