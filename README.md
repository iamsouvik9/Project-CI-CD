# Simple Notes App
This is a simple notes app built with React and Django.

## Requirements
1. Python 3.9
2. Node.js
3. React

##Steps to complete the project 

1. Go to AWS to create an Ubuntu EC2 instance
---------------------------------------------------------------------------------------------------------------------------------   



<img width="958" alt="2" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/9f6febb4-da40-424c-9795-f4cdcb8a6dce">


----------------------------------------------------------------------------------------------------------------------------------

2. In the security group add inbound rules for the Jenkins local host and also allow port 8000 to access the TO-DO notes app as it runs on port 8000
----------------------------------------------------------------------------------------------------------------------------------


<img width="960" alt="1" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/bd863ae4-072e-44fb-a476-92c6d22aa77d">


----------------------------------------------------------------------------------------------------------------------------------


3. Connect to this EC2 instance by SSH/ Instance connect.
----------------------------------------------------------------------------------------------------------------------------------


 <img width="960" alt="3" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/9b577c34-e77d-4420-ad9d-23c018624e37">

----------------------------------------------------------------------------------------------------------------------------------


4. Install jdk11 necessary to install Jenkins and then install Jenkins in this EC2 instance, then start the Jenkins server
----------------------------------------------------------------------------------------------------------------------------------


<img width="953" alt="4" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/fcfb1878-c900-4766-a0e0-0be427c90dea">

----------------------------------------------------------------------------------------------------------------------------------   

5. Also install Docker int the EC2 instance
----------------------------------------------------------------------------------------------------------------------------------6

   
7. Add user and jenkins to the docker group so that they can also have execution permissions
----------------------------------------------------------------------------------------------------------------------------------  


<img width="953" alt="4" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/cf282b80-d9ca-40b7-8bfa-78d7cd359d9b">



----------------------------------------------------------------------------------------------------------------------------------
7. Open <IP-address-of-EC2-instance>:8080 to access the Jenkins server and install suggested plugins and then login
----------------------------------------------------------------------------------------------------------------------------------


 <img width="959" alt="5" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/7c6bb93f-86b9-45a5-a843-365a8d582efb">


----------------------------------------------------------------------------------------------------------------------------------
8. Create a Declarative pipeline for the entire deployement of the TO-DO Notes app
----------------------------------------------------------------------------------------------------------------------------------


   i) It will clone the git repository to fetch the code
   
   ii) and then it will build images from the Dockerfile
   
   iii) and then that created image will be uploaded to the Docker Hub registry
   
   iv) The image will be fetched from the Docker Hub registry to deploy the application inside a Docker Container
   
   v) Enable Webhooks so that whenever there will be any changesd made in the code repository Jenkins will create a new build every single time
   
   vi) Use Dcoker-compose to start and run an entire app on a standalone host that contains multiple services
   

   <img width="960" alt="6" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/a0c0b0d7-959a-4e36-9945-662cd9228553">



----------------------------------------------------------------------------------------------------------------------------------
10. Jenkins Build Dashboard for Note TO_DO app
----------------------------------------------------------------------------------------------------------------------------------


<img width="960" alt="7" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/56bd54aa-0e1b-4adb-a875-a734eb00c078">


----------------------------------------------------------------------------------------------------------------------------------
11. Accessing the TO-DO Note app on port 8000 of the EC2 server
----------------------------------------------------------------------------------------------------------------------------------


<img width="960" alt="8" src="https://github.com/iamsouvik9/Project-CI-CD/assets/79768737/3c2bb7aa-2db0-45fe-a94a-c0a8df9e04da">


----------------------------------------------------------------------------------------------------------------------------------

----------------------------------------------------------------------------------------------------------------------------------
