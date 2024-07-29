# BabelBeats

## Project Deployment

🎉 The web application BabelBeats is live and accessible at https://babelbeats.rocks/

### Deployment Details

- Frontend: Hosted on AWS S3 with distribution through CloudFront. This setup provides a Content Delivery Network (CDN) that improves performance by caching content at edge locations globally, reducing latency and ensuring fast load times for users.

- API: Deployed using AWS Elastic Container Service (ECS) with an Application Load Balancer. This configuration ensures high availability and efficient traffic management, automatically distributing incoming application traffic across multiple targets.

- Database: The application uses Amazon RDS with a PostgreSQL database for robust and reliable data management.

- User Authentication: Managed using AWS Cognito, which provides secure and scalable user sign-up, sign-in, and access control. The application supports federated authentication, including Google login, allowing users to sign in using their existing social media or identity provider credentials.

- SSL Certificate: Secured with an SSL certificate managed by AWS Certificate Manager (ACM) to ensure secure data transmission and encryption.

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

### Production Mode

1. Start the Environment

   Use Docker Compose to build and run the services.

   ```bash
   docker-compose up --build
   ```

   This command will build the Docker images and start the containers.

2. Accessing the Services

   - Web Client: Accessible at http://localhost
   - Server: Accessible at http://localhost:8080
