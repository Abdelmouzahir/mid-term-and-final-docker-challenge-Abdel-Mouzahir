# Learning Outcomes for Docker Challenges
## Abdel Mouzahir
### 000891579
## Challenge 1 - Simple web server for static web pages
- Basics of Docker: Understand how to use Docker to create and manage containers.
- Docker Image Creation: Learn how to build a Docker image using a Dockerfile.
- Container Deployment: Deploy a Docker container and access the served content through a browser.
- Version Control with Git and GitHub: Use Git and GitHub to manage code versions and collaborate with others.
- Documentation and Reporting: Write a comprehensive report documenting the steps taken, including screenshots and explanations.

## Challenge 2 - Creating a dynamic application
- Docker Compose: Introduce the concept of Docker Compose for orchestrating multiple containers.
- Containerization of NodeJS Application: Dockerize a NodeJS application using a Dockerfile.
- Service Orchestration: Use Docker Compose to define and manage multiple services (e.g., NGinx, API server).
- Testing and Troubleshooting: Verify that all services are running correctly and troubleshoot any issues that arise.
- Submission and Documentation: Submit the project repository's URL and provide a detailed report on the steps taken, including screenshots and explanations.

## Challenge 3
For Docker Challenge 3, we were tasked with connecting an NGINX app to a simple database and displaying the information. The challenge involved setting up .env variables and writing a docker-compose file, as these were not provided in the initial package. The docker-compose file specifies how to build and run the services for the database, API, and NGINX, with proper environment variables and volume mounting. After configuring these files, we used docker-compose up --build to build and run the containers. Once running, we could access the app at localhost:8080 to view the database items in JSON format. Troubleshooting involved ensuring correct file paths and matching environment variables between the .env file and the docker-compose file. If issues arise, commands like docker-compose logs can help diagnose problems.

## Challenge 4
For Docker Challenge 4, we were tasked with scaling up the application built in Challenge 3. Initially, when accessing http://localhost:8080/api/stats with the app running, the hostname remained consistent across multiple requests, confirming a single instance was handling them. To scale the application, we modified the docker-compose file to allow Docker to manage ports dynamically rather than explicitly declaring them. This enabled us to scale the application using the command docker-compose up --scale node-service=3 -d. After scaling, we observed that the hostname changed with each request, indicating multiple instances were now handling the requests. Running docker-compose ps confirmed that three instances of the node-service were running successfully. This process allows you to scale your application effectively as needed.