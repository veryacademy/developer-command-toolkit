# Docker Commands

This guide outlines various docker commands.

- **Build and start docker**
    ```
    docker compose up -d
    ```

- **Build and start docker from a specified docker-compose.yml file**
    ```
    docker compose -f ./infrastructure/docker-compose.yml up --build -d
    ```

- **Access Docker Contianer Terminale**
  
    1. Find the Container Name or ID:
    ```
    docker ps
    ```
    2. Use docker exec to Access the Container
    ```
    docker exec -it <container_name_or_id> /bin/bash
    ```
