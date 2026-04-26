# DOCKER
## Install Docker

### 1.Login into Ec2 Instances Then Run this Commands

- Update The Ec2 instances
```bash
        sudo apt update -y
```

- Install Docker
```bash
     bash sudo apt install docker.io -y
```

- Checking docker version
```bash
        docker --version
```

-  To Check Docker is Running Or Not 
```bash
        sudo systemctl status docker .
```

### 2. Running the Docker

    `docker run hello-world `

permission denied while trying to connect to the docker API at unix:///var/run/docker.sock



 - **Now Run This command**
 
```bash
      sudo usermod -aG docker ubuntu
```

👉 This command means:
 - is used in Linux (like Ubuntu) to give a user permission to use
  Docker without sudo.
 - Add the user ubuntu to the docker group, so they can run Docker
  commands without using sudo.



## 3. Local Deployment using Docker”
```bash 
 
**git clone https://github.com/Tech-lalitha/Docker_file.git

  ls
  #Docker_file

  cd Docker_file
  ~/Docker_file$ ls
  #README.md  example

  ~/Docker_file$ cd example
  ~/Docker_file/example$ ls
  #first_files

  ~/Docker_file/example$ cd first_files
  ~/Docker_file/example/first_files$ ls
  #Dockerfile  app.py**
```



- Run This command
```bash
docker build -t bhumireddylalitha/my-sec-file:latest .

#Now you will check
docker run -it bhumireddylalitha/my-sec-file:latest
Hello World
welcome to our world

#seeing docker image with command 
docker images**
```


  

## Login into DockerHub

- Run this command
```bash
    docker login **
```


### Now Push the Docker Image into DockerHub
```bash
docker push bhumireddylalitha/my-sec-file:latest
```

## Now open Docker Hub in Brower

   ==> now image get push into docker Hub

---
## 	Containers 
A container is a lightweight, portable unit of software that packages an application along with everything it needs to run—such as code, libraries, dependencies, and configuration files. This ensures the application works consistently across different computing environments.


## 📦 Simple Definition
> A container is like a ready-to-run box that contains an application and all its requirements.
It eliminates the classic problem:
> “It works on my machine but not on yours.”



## 🧳 Real-Life Analogy: Shipping Containers
Think of software containers like shipping containers used in global trade:
|Shipping Container	|Software Container |
|--------------------|--------------------|
|Carries goods	    |Carries applications   |
|Standardized for transport |	Standardized for deployment |
|Moves easily across ships, trucks, and trains	|  Runs on any system with a container engine |
|Protects contents	 |Isolates applications |


## ⚙️ How Containers Work
Containers use operating system virtualization**.
Instead of running a full operating system:
- they share the host OS kernel
- keeping applications isolated.

### Components of a Container:
- 🧩 Application code 
-	📚 Libraries and dependencies 
- ⚙️ Runtime environment 
- 📝 Configuration files




## 🖥️ Containers vs Virtual Machines
|Feature	|Containers	 |Virtual Machines
|Size	|Lightweight (MBs)	| Heavy (GBs)
|Startup Time	|Seconds	| Minutes
|Performance	| High	| Moderate
|OS Requirement |	Shares host OS |	Requires full OS
|Resource Usage	|Efficient	 |Resource-intensive


 

## 🐳 Popular Container Tools
-  Docker – The most widely used container platform. 
- 	Kubernetes – Automates deployment, scaling, and management of containers. 
- 	Podman – A daemonless alternative to Docker. 
- 	Red Hat OpenShift – An enterprise container platform.




## 🌍 Example Use Case
Imagine you develop a Python web application.
### Without Containers:
- It may fail on another system due to missing libraries or version conflicts. 
### With Containers:
-	You package the app and dependencies into a container. 
-	It runs reliably on any environment—your laptop, a server, or the cloud.

 

## 💡 Simple Real-Life Analogy
-	Image = Recipe 🍲 
-	Container = Cooked food 🍛 
-	Run = Eating / Using 
-	Stop = Keep it aside 
-	Remove = Throw it away 




