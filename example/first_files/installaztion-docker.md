## **Install Docker**

##### 

1. ###### **Login into Ec2 Instances Then Run this Commands**

\---

|\*\*#Update The Ec2 instances<br />**sudo apt update -y<br /><br />**#Install Docker<br />**sudo apt install docker.io -y<br /><br />**#Checking docker version<br />**docker --version<br /><br />**#To Check Docker is Running Or Not <br />\*\*sudo systemctl status docker|
|-|





###### **2. Running the Docker**



|ubuntu@ip-172-31-19-46:\~$ *docker run hello-world<br />***# permission denied while trying to connect to the docker API at unix:///var/run/docker.sock<br />**|
|-|





* &#x20;**Now Run This command**

&#x20;

|sudo usermod -aG docker ubuntu|
|-|



&#x20;     **#👉 This command means:**

&#x20;        **=> is used in Linux (like Ubuntu) to give a user permission to use**

&#x20;        **Docker without sudo.**

&#x20;

&#x20;        **=> “Add the user ubuntu to the docker group, so they can run Docker**

&#x20;        **commands without using sudo.”**







###### **3. Local Deployment using Docker”**





&#x20;

|**git clone** https://github.com/Tech-lalitha/Docker\_file.git<br /><br />  ubuntu@ip-172-31-19-46:\~$ **ls<br />**  Docker\_file<br /><br />  ubuntu@ip-172-31-19-46:\~$ **cd Docker\_file<br />**  ubuntu@ip-172-31-19-46:\~/Docker\_file$ **ls<br />**  **README.md  example<br /><br />**  ubuntu@ip-172-31-19-46:\~/Docker\_file$ **cd example<br />**  ubuntu@ip-172-31-19-46:\~/Docker\_file/example$ **ls<br />  first\_files<br /><br />**  ubuntu@ip-172-31-19-46:\~/Docker\_file/example$ **cd first\_files<br />**  ubuntu@ip-172-31-19-46:\~/Docker\_file/example/first\_files$ **ls<br />  Dockerfile  app.py<br /><br /><br />**|
|-|





&#x20;     **==> Run This command**

&#x20;

|docker build -t bhumireddylalitha/my-sec-file:latest .<br /><br />\*\*#Now you will check<br />\*\*docker run -it bhumireddylalitha/my-sec-file:latest<br />**Hello World<br />welcome to our world<br />**|
|-|



&#x20; 



##### **Login into DockerHub**



|#Run this command<br />   **docker login<br />**|
|-|





##### **Now Push the Docker Image into DockerHub**





|**docker push bhumireddylalitha/my-sec-file:latest**|
|-|





##### **Now open Docker Hub in Brower**



&#x20;  # now image get push into docker Hub



































