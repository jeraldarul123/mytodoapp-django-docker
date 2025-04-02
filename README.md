MyToDoApp - Node.js Dockerized Application
🚀 Project Overview
This project demonstrates how to containerize a Node.js application using Docker and deploy it easily by pushing the image to Docker Hub. The purpose of this project is to understand Dockerization, simplify deployment, and improve the management of the application across various environments.

🛠️ Technologies Used
Node.js (v21): The backend framework used to build the application.

Docker: For containerizing the Node.js application.

Docker Hub: For versioning, distributing, and sharing the Docker image.

📦 Features
Lightweight Node.js server using Alpine Linux for minimal image size.

Exposes port 3000 to interact with the application.

Easy deployment via Docker Hub image.

📋 Installation & Setup
1. Clone the Repository
Clone the repository to your local machine:

bash
Copy
git clone https://github.com/your-username/mytodoapp.git
cd mytodoapp
2. Build the Docker Image Locally
To build the Docker image using the Dockerfile in the current directory:

bash
Copy
docker build -t mytodoapp .
This will create a Docker image tagged as mytodoapp.

3. Run the Container
Run the container and map port 3000 inside the container to port 3000 on your local machine, allowing you to access the app at http://localhost:3000:

bash
Copy
docker run -p 3000:3000 mytodoapp
4. (Optional) Push to Docker Hub
If you'd like to share or deploy your image using Docker Hub, follow these steps:

Log in to Docker Hub:

bash
Copy
docker login
Tag the Image: Replace your-dockerhub-username with your Docker Hub username.

bash
Copy
docker tag mytodoapp your-dockerhub-username/mytodoapp
Push the Image:

bash
Copy
docker push your-dockerhub-username/mytodoapp
Once pushed, you can easily share the image or deploy it to any environment that supports Docker.

🌐 Access the Docker Image
You can find the image for this application on Docker Hub:

Docker Hub - jeraldarul/mytodoapp

🔧 Dockerfile
The Dockerfile used to containerize the application:

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
Docker helps make applications platform-independent, reducing the common "works on my machine" issues.

Containerization simplifies the deployment process, ensuring that the application works the same way across different environments.

Docker Hub offers a central platform for managing and distributing Docker images, making it easy to share and deploy.

🤝 Contributing
If you’d like to contribute to this project, feel free to fork the repository, make changes, and submit a pull request. Contributions are always welcome!

📄 License
This project is open-source and available under the MIT License.

Author:
Jerald Arul
![1742891690008](https://github.com/user-attachments/assets/cf546dae-3ae5-49e3-9efa-23bc72aa887e)
![1742891689041](https://github.com/user-attachments/assets/5fd57f1f-d030-4c59-90eb-c00c2b26af61)
![1742891690892](https://github.com/user-attachments/assets/6e1fe855-95cf-4ec4-b577-420b97096539)

