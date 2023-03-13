# docker_master

## CI/CD Deployment for SpringBoot Application

### Developed by: Shrawan Kumar Thakur
### GitHub link: https://github.com/shrawanthakur16/docker_master.git

Project:
In this project, we implemented a CI/CD (Continuous Integration/Continuous Deployment) pipeline for the development, deployment, and continuous monitoring of a “Spring Boot” application respectively. The flow of all the stages step-by-step is termed as a “Pipeline”. For this purpose, we used open-source tools, such as “Jenkins”, “Github” and “Docker” (for monitoring purpose). 
“AWS EC2” instance has been used for the hosting the application on the server. 


### Technology Stack 
￼ ￼ ￼

• CI/CD :- Refers to a set of development practices that enable the rapid and reliable delivery of code changes, while DevOps is a collection of ideas, practices, processes, and technologies that allow development and operations 
teams to work together to streamline product development. 

• Github :- A web-based interface that uses Git, the open source version control software that lets multiple people make separate changes to web pages at the same time. 

• Docker:-An open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. 
By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production. 

• Jenkins:-A Java-based open-source automation platform with plugins designed for continuous integration. It is used to continually create and test 
software projects, making it easier for developers and DevOps engineers to integrate changes to the project and for consumers to get a new build. 

• AWS:-Amazon Elastic Compute Cloud(AmazonEC2) provides scalable computing capacity in the Amazon Web Services (AWS) Cloud. Using Amazon EC2 eliminates your need to invest in hardware up front, so you can develop and deploy applications faster. You can use Amazon EC2 to launch as many or as few virtual servers as you need, configure security and networking, and manage storage. Amazon EC2 enables you to scale up or down to handle changes in requirements or spikes in popularity, reducing your need to forecast traffic. 



### SPRINT PLANNING 
	•	The spring planning for the above application from development to deployment phase has been conducted in 15 days, which includes two sprints of 7 and 8 days respectively. A total number of 2 story points has been covered in total, which are divided in 1 and 1 in both the sprints. Each story has 4 tasks respectively.  
	
Prerequisites:  -> A GitHub account to store the source code. 
-> A Jenkins server with admin access. -> An AWS account to create an EC2 instance.
-> Basic knowledge of Spring Boot, AWS EC2, and Jenkins.  1. Sprint 1 (7 Days/ 1 Story) :-

Task 1: Clone the GitHub repository: Clone the repository containing the source code of the Spring Boot application to the local system. This will be used by Jenkins to build the application and create a deployment package. 

Task 2: Install necessary plugins:  Install the following plugins in the Jenkins server :- 
-> Maven Integration Plugin 
-> Git plugin  These plugins will be used to build the application and fetch the source code from the GitHub repository.

Task 3: Create a Jenkins job:
-> Create a new Jenkins job by navigating to Jenkins Dashboard > New Item > Freestyle project.
-> In the Source Code Management section, select Git and provide the URL of the GitHub repository where the code is stored.  -> In the Build section, select Invoke top-level Maven targets and provide the necessary Maven goals to build the application. For example, clean install.  
￼ 

Task 4: Configure AWS EC2 instance: 
-> Create an EC2 instance in the AWS account and configure the security group to allow HTTP traffic on port 8080. 
-> Install Java and Tomcat on the EC2 instance to run the Spring Boot application. 

2. Sprint 2 (8 Days/ 1 Story) :- 
Task 1: Install AWS CLI: 
-> Install the AWS CLI on the Jenkins server to automate the deployment process. 

Task 2: Configure AWS credentials: 
-> Add the AWS access key and secret key to the Jenkins server using the AWS CLI. 

Task 3: Create a deployment job: 
Create a new Jenkins job to deploy the Spring Boot application to the EC2 instance. In this job, configure the following steps :- 
-> Fetch the latest deployment package from the Jenkins workspace.
-> Copy the deployment package to the EC2 instance using the AWS CLI. -> Start the Tomcat server on the EC2 instance to run the application. 

Task 5: Test the deployment: 
-> Run the deployment job and check if the application is deployed successfully on the EC2 instance. Access the application using the public IP address of the EC2 instance. 
