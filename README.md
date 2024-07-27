# BabelBeats

## Getting Started

### Development Mode

In development mode, both the server and web client support hot reloading.

To start the project in the development environment, follow these steps:

1. Clone the Repository

   ```bash
   git clone https://github.com/evelyn-2022/babelbeats.git
   cd babelbeats
   ```

2. Start the Environment
   Use Docker Compose to build and run the services.

   ```bash
   docker-compose -f docker-compose.dev.yml up --build
   ```

   This command will build the Docker images and start the containers.

3. Accessing the Services

   - Web Client: Accessible at https://localhost:3000
   - Server: Accessible at https://localhost:8080

4. Important Note on SSL Certificates
   For development purposes, we use self-signed SSL certificates. This means the browser may flag the connection as insecure. We recommend using the Firefox browser, as it allows you to easily add exceptions for self-signed certificates.
