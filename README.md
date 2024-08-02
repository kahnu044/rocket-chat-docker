# Rocket.Chat and MongoDB Docker Compose Setup

This repository contains a Docker Compose configuration for deploying Rocket.Chat with MongoDB.

## Prerequisites

- Docker: [Install Docker](https://docs.docker.com/get-docker/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Usage

1. Clone the Repository:

   ```bash
   git https://github.com/kahnu044/rocket-chat-docker
   cd rocket-chat-docker
   ```

2. Configure Environment Variables:
   Create a `.env` file based on the example provided by the `.env.example` fie and adjust the values as needed.

3. Start the Services:
   Run the following command to start Rocket.Chat and MongoDB:
   ```bash
   docker-compose up -d
   ```
4. Access Rocket.Chat:
   ```bash
   Navigate to http://localhost:3000 or the domain you have configured in your .env file.
   ```
5. Stopping the Services:

   To stop and remove the containers, use:

   ```bash
   docker-compose down
   ```

## Configuration

### Environment Variables

- `MONGO_URL`: MongoDB connection URL.
- `MONGO_OPLOG_URL`: MongoDB oplog URL.
- `ROOT_URL`: The URL to access Rocket.Chat.
- `PORT`: Internal port for Rocket.Chat.
- `HOST_PORT`: External port for Rocket.Chat.
- `DEPLOY_METHOD`: Deployment method.
- `DEPLOY_PLATFORM`: Deployment platform.
- `REG_TOKEN`: Registration token for Rocket.Chat.
- `MONGODB_REPLICA_SET_NAME`: Replica set name.
- `MONGODB_PORT_NUMBER`: MongoDB port number.
- `MONGODB_INITIAL_PRIMARY_HOST`: Initial primary host.
- `MONGODB_INITIAL_PRIMARY_PORT_NUMBER`: Initial primary port number.
- `MONGODB_ADVERTISED_HOSTNAME`: Advertised hostname.
- `MONGODB_ENABLE_JOURNAL`: Enable journaling.
- `ALLOW_EMPTY_PASSWORD`: Allow empty passwords.

## Troubleshooting

- Configuration Errors: Check the Docker Compose logs for errors:
  ```bash
  docker-compose logs
  ```
- Environment Variables: Ensure that all required environment variables are correctly set in your `.env` file.

- Restart Services: If changes are made to the configuration, restart the services:
  ```bash
  docker-compose restart
  ```

## Official Docs for Rocket Chat Docker

[https://docs.rocket.chat/docs/deploy-with-docker-docker-compose](https://docs.rocket.chat/docs/deploy-with-docker-docker-compose)

[https://github.com/RocketChat/Docker.Official.Image/blob/master/env.example](https://github.com/RocketChat/Docker.Official.Image/blob/master/env.example)

## Author

[Kahnu Charan Swain](https://github.com/kahnu044)
