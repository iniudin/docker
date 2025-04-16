# Curated Docker Compose for Local Development (PostgreSQL, RabbitMQ, Redis)
This repository offers a ready-to-use `docker-compose.yml` for quickly spinning up PostgreSQL, RabbitMQ, and Redis for local development. It's tailored for projects that depend on these core services.

## Key Benefits

* **One-Command Launch:** Start all services together with a single command.
* **Developer-Friendly Defaults:** Pre-set configurations optimized for local use.
* **Customizable Setup:** Easily adjust ports, volumes, and environment variables in the `docker-compose.yml`.
* **Seamless Integration:** All services are networked for straightforward inter-service communication.

## Getting Started

1. **Clone this repository:**
  ```bash
  git clone https://github.com/iniudin/docker
  cd docker
  ```

2. **Configure environment variables:**

   Copy the example environment file and adjust values as needed:
   ```bash
   cp .env.example .env
   ```
   Edit the `.env` file to set credentials, ports, and other settings for PostgreSQL, RabbitMQ, and Redis. These variables are automatically loaded by `docker-compose.yml`.

3. **Start the services:**
    ```bash
    docker-compose up -d
    ```
    The `-d` flag runs the containers in detached mode (in the background).

4. **Access the services:**

    * **PostgreSQL:**
        * Host: `localhost`
        * Port: `5432` (default, can be configured in `.env`)
        * Default User/Password: Set in the `.env` file (see `POSTGRES_USER`, `POSTGRES_PASSWORD`).

    * **RabbitMQ:**
        * Management UI: `http://localhost:15672` (default, can be configured in `.env`)
        * Default Guest User/Password: Set in `.env` (see `RABBITMQ_DEFAULT_USER`, `RABBITMQ_DEFAULT_PASS`)
        * AMQP Port: `5672` (default, can be configured in `.env`)

    * **Redis:**
        * Host: `localhost`
        * Port: `6379` (default, can be configured in `.env`)

**Note:** Refer to `.env.example` for all available environment variables and their descriptions.