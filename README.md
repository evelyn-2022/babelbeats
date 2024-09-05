# BabelBeats

## Project Deployment

🎉 The web application BabelBeats is live and accessible at https://babelbeats.rocks/

> [!CAUTION]
> I've temporarily taken down the server and database because they're too expensive and I'm just a poor student 🥲. But I'll redeploy the app once version 1 is ready for release.

### Deployment Details

- **Frontend**: Hosted on AWS S3 and distributed via CloudFront, providing a global Content Delivery Network (CDN) that caches content at edge locations to reduce latency and ensure fast load times for users.

- **API**: Deployed using AWS Elastic Container Service (ECS) with an Application Load Balancer, ensuring high availability and efficient traffic management by automatically distributing incoming traffic across multiple targets.

- **Database**: The application uses Amazon RDS with a PostgreSQL database for robust and reliable data management.

- **User Authentication**: Managed with AWS Cognito, offering secure and scalable user sign-up, sign-in, and access control. It supports both email and social media account authentication, providing a flexible and user-friendly experience.

- **SSL Certificate**: Secured with an SSL certificate managed by AWS Certificate Manager (ACM) to ensure secure data transmission and encryption.

## Docker Setup

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
   docker-compose --env-file .env.dev -f docker-compose.dev.yml up --build
   ```

   This command will build the Docker images and start the containers.

3. Accessing the Services

   - Web Client: Accessible at http://localhost:3000
   - Server: Accessible at http://localhost:8080

### Testing Mode

The testing mode mimics deployment environment by building the frontend into a static package (`dist`) and packaging the Java server into a JAR file. Nginx acts as a reverse proxy, routing requests to the frontend service for static assets and the API service for backend logic.

1. Start the Environment

   Use Docker Compose to build and run the services.

   ```bash
   docker-compose --env-file .env.test up --build
   ```

   This command will build the Docker images and start the containers.

2. Accessing the Services

   - Web Client: Accessible at http://localhost
   - Server: Accessible at http://localhost:8080
