MyToDoApp - Node.js Dockerized Application
This project demonstrates how to containerize a Node.js application using Docker and push the image to Docker Hub for easy distribution and deployment.

🚀 Project Overview
This is a simple Node.js-based To-Do List application, containerized using Docker. The goal of this project was to understand Dockerization and the benefits it brings to deployment and management across different environments.

🛠️ Technologies Used
Node.js (v21) - The backend framework used for building the application.

Docker - To containerize the application.

Docker Hub - For image distribution and versioning.

📦 Features
A lightweight Node.js server using Alpine Linux for minimal image size.

Exposes port 3000 to interact with the app.

Easy deployment via Docker Hub image.

📋 Installation & Setup
1. Clone the repository:
bash
Copy
git clone https://github.com/your-username/mytodoapp.git
cd mytodoapp
2. Build the Docker image locally:
bash
Copy
docker build -t mytodoapp .
This will build the Docker image using the Dockerfile in the current directory.

3. Run the container:
bash
Copy
docker run -p 3000:3000 mytodoapp
This will run the container and map port 3000 inside the container to port 3000 on your local machine, allowing you to access the app at http://localhost:3000.

4. (Optional) Push to Docker Hub:
If you'd like to push your container image to Docker Hub, follow these steps:

Log in to Docker Hub:

bash
Copy
docker login
Tag the image:

bash
Copy
docker tag mytodoapp your-dockerhub-username/mytodoapp
Push the image:

bash
Copy
docker push your-dockerhub-username/mytodoapp
You can then share the image and deploy it anywhere using Docker.

🌐 Access the Docker Image
You can find the image for this application on Docker Hub:

Docker Hub - jeraldarul/mytodoapp

🔧 Dockerfile
Here's the Dockerfile used to containerize the application:

Dockerfile
Copy
# Use the official Node.js image from Docker Hub
FROM node:21-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose the application port
EXPOSE 3000

# Run the application
CMD ["npm", "start"]
🔑 Key Takeaways
Docker helps make applications platform-independent, reducing the "works on my machine" issue.

Containerization simplifies application deployment across various environments.

Docker Hub offers a central platform for managing and distributing Docker images.

🤝 Contributing
If you'd like to contribute to this project, feel free to fork the repository, make changes, and submit a pull request.

📄 License
This project is open source and available under the MIT License.
