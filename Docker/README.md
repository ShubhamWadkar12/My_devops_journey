# 🐳 **DOCKER OVERVIEW**

## 🤷‍♂️ What is Docker?

**Docker** is a tool that lets you **package your application along with all its settings, libraries, and tools** into a container so that it **runs exactly the same on any operating system** whether it's Windows, Linux, or Mac.

This solves the common issue:  
> “It works on my machine, but not on yours!”

---

## 📦 Why Use Docker?

- It makes your application portable across different systems.
- You don’t have to worry about OS-specific issues or missing dependencies.
- It saves setup time and reduces bugs caused by environmental differences.

---

## 💡 Real-World Example

- Suppose **User A** builds an app on **Windows** and wants to share it with **User B** who uses **Linux**.
  - 🧑‍💻 **User A** creates a Docker image of the app (a packaged bundle with code + required software).
  - 📤 A shares the Docker image (or uploads it to Docker Hub).
  - 👩‍💻 **User B** downloads the image and runs it using Docker on Linux.
  - ✅ The app works exactly the same on both systems no setup issues, no errors.

---

## 🔁 Summary

| Without Docker              | With Docker                        |
|----------------------------|-------------------------------------|
| App may break on other OS  | App runs the same everywhere        |
| Manual setup needed        | One-time Docker setup               |
| Time-consuming debugging   | Faster development and deployment   |

---

## 📌 Key Terms

- **Docker Image**: A blueprint of your app.
- **Container**: A running instance of the image.
- **Dockerfile**: Instructions to build the image.
- **Docker Hub**: A place to store and share Docker images.

## **🐳 Docker Architecture**
<img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/8a174237-da9f-4b24-bace-ae92a92d4593" />

## Docker Commands

- Docker ps  -> Lists all currently running Docker containers
- sudo apt full-upgrade   -> to update all things
- docker pull (filename)   ->Downloads a Docker image from Docker Hub (or another registry) to your local system
- docker run (filename)  -> Creates and starts a container from a pulled image
- docker ps  -> docker stop (container ID) ---> to stop the server(e.g mysql)

### To write a docker file
- mkdir (folder name) & cd (foldername)
- git clone (repo link)
- delete the previous file and create new one by vim (file name)
- write the following commands in it
```bash
# pull a base image which gives all required tools and libraries
FROM openjdk:17-jdk-alpine

# create a folder where the app code will be stored
WORKDIR /app

# Copy the source code from your HOST machine to your container
COPY src/Main.java /app/Main.java      (source and destination)

# compile the application code
RUN javac Main.java

# run the application
CMD ["java","Main"]
```
- **docker build -t java-app .**
 > ✅ Meaning (Broken Down):
                Part                                     	Meaning
             docker build	              Tells Docker to build an image from a Dockerfile.
              -t java-app	            Tags the image with the name java-app (so you can refer to it later).
                  .	                  The build context, means look in the current directory for the Dockerfile and other app files.
- **docker run java-app**
-  docker build -t java-app .    -> to update the changes in local with sync
-  docker run -d -p 80:80 (filename)    -> to run the app on specific port
-  docker logs (container ifd found via docker ps)    -> to see the ip address the app is running on
-  docker attach (container name)    -> to get live updates of app logs
-  docker exe -it (container name) bash  -> to open interactive terminal
-  docker run -itd ubuntu     -> it(interactive terminal and d means for running in background)

---

# 📝 Node TODO App – Dockerized

This guide helps you containerize the [`node-todo-cicd`](https://github.com/LondheShubham153/node-todo-cicd) project and run it locally using Docker.

---

## 📦 Dockerizing `node-todo-cicd`

### 🔹 1. Clone the Repository

```bash
git clone https://github.com/LondheShubham153/node-todo-cicd.git
cd node-todo-cicd
```

#### 🔹 2. Create a Dockerfile (if not already present)
```bash
# Use the official Node.js image
FROM node:18

# Set the working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy all source code
COPY . .

# Expose the app port (default is 3000)
EXPOSE 3000

# Start the app
CMD ["npm", "start"]
```
### 🔹 3. Build the Docker Image
```bash
docker build -t node-todo-app .
```
### 🔹 4. Run the Docker Container
```bash
docker run -p 8000:8000 node-todo-app
```
### 🔹 5. To stop the Docker image
```bash
docker stop (container ID)
```
---
## Docker Networking
Docker network allows containers to talk to each other, and also to the outside world (like your browser or the internet).

| Types        | Use Case                                                         |
| ----------- | ---------------------------------------------------------------- |
| **bridge**  | Default. Great for connecting containers on the same host.       |
| **host**    | Shares the host network. No isolation. Fastest, but less secure. |
| **none**    | Completely isolated. Useful for testing container-only logic.    |
| **overlay** | For **multi-host** communication (used in Docker Swarm).         |
| **macvlan** | Assigns a **real IP** from your network to a container.          |

---
-  docker network create mynetwork -d (network name)    -> to create a new network
-  docker run -d -p 5000:5000 -e MYSQL_HOST=mysql -e MYSQL_USER=root -e MYSQL_PASSWORD=root -e MYSQL_DB=devops two-tier-backend:latest

### 🔍 Command Breakdown

| Part                         | Meaning                                                                 |
|-----------------------------|-------------------------------------------------------------------------|
| `docker run`                | Run a new Docker container                                              |
| `-d`                        | Run in detached mode (in background)                                    |
| `-p 5000:5000`              | Map port `5000` on your system to `5000` in the container (for access via `localhost:5000`) |
| `-e MYSQL_HOST=mysql`       | Set environment variable. Tells the app the MySQL server name is `mysql` |
| `-e MYSQL_USER=root`        | Sets the MySQL username to `root`                                      |
| `-e MYSQL_PASSWORD=root`    | Sets the MySQL password to `root`                                      |
| `-e MYSQL_DB=devops`        | Sets the MySQL database name to `devops`                               |
| `two-tier-backend:latest`   | The Docker image being used (with `latest` tag)                        |

---
- docker ps -a     -> to check killed images
- docker logs(container name)  -> to check why was the image not created
