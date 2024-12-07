# WordPress with MariaDB Using Docker Compose

Welcome to your WordPress and MariaDB setup! This repository provides an easy-to-use configuration for hosting a WordPress website backed by a MariaDB database using Docker Compose.

## Table of Contents

1. [Description](#description)
2. [Quickstart](#quickstart)
3. [Usage](#usage)
   - [Configuration](#configuration)
4. [Contact](#contact)

## Description

This repository includes a Docker Compose setup for quickly launching a WordPress instance with a MariaDB database. It simplifies the process of setting up and maintaining a WordPress site with an underlying database.

Key features:

- **Containerized Deployment**: Run WordPress and MariaDB reliably using Docker.
- **Environment Variable Configuration**: Easily customize credentials and database details via a `.env` file.
- **Scalable & Portable**: Run locally or deploy on a remote server/VM.

## Quickstart

### Prerequisites

Ensure you have the following tools installed:

- [Docker](https://www.docker.com/products/docker-desktop)
  - Docker Compose is included with Docker 20.10 and later. If you have an older version, follow the [official instructions](https://docs.docker.com/compose/install/) to install Docker Compose as a plugin.

1. Clone this repository:

   ```bash
   git clone https://github.com/PascalNehlsen/wordpress-container
   cd minecraft-server
   ```

2. Create a `.env` file from the example configuration:

   ```bash
   cp example.env .env
   ```

3. Edit the `.env` file to set your desired configuration (see [Configuration](#configuration)).

4. Start the WordPress and MariaDB containers:

   ```bash
   docker compose up -d
   ```

5. Access your WordPress site:

   - Open your browser and navigate to `http://localhost:8080` (or your server's IP if running remotely).
   - Now you can configure the Admin panel.

6. To stop the server, use:

   ```bash
   docker compose down
   ```

## Usage

### Configuration

The [example.env](./example.env) file allows you to customize the WordPress and MariaDB setup. Below is a list of the environment variables and their functions:

| Variable             | Description                                        | Possible Values | Required |
| -------------------- | -------------------------------------------------- | --------------- | -------- |
| `WORDPRESS_USER`     | Username for the WordPress admin account.          | user            | Yes      |
| `WORDPRESS_PASSWORD` | Password for the WordPress admin account.          | password        | Yes      |
| `DATABASE_NAME`      | Name of the MariaDB database used by WordPress.    | wordpress       | Yes      |
| `DATABASE_HOST`      | Hostname of the database (matches the db service). | db              | Yes      |

### Updating the Setup

To modify the configuration, edit the `.env` file and restart the containers:

    ```bash
    docker compose down
    docker compose up -d
    ```

## Contact

- Pascal Nehlsen - [LinkedIn](https://www.linkedin.com/in/pascal-nehlsen) - [mail@pascal-nehlsen.de](mailto:mail@pascal-nehlsen.de)
- Project Link: [https://github.com/PascalNehlsen/wordpress-container](https://github.com/PascalNehlsen/wordpress-container)
