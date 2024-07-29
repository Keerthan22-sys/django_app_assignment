# Django_app_assignment - DeepLogic AI

 **Description**:- The project is about displaying the list of the available courses.
 
 **Added functionality**: Added a search feature in the project that makes it easy for users to use. (Added API - /searchCourse)

 **Instructions on how to run the application locally**

 1) Clone this repository in your system
 2) Navigate to the project folder - i.e cd Application
 3) The project is built using the framework - Django/Python
 4) To install Python & Django in your system, run - "pip install python" & "pip install django"
 5) To run the project locally, run this command - "python3 manage.py runserver 0.0.0.0:8080"
 6) Once you browse to "localhost:8080", you can see the application running.


**Instructions on how to deploy the application to AWS Lambda**

***Creating Docker Image***
1) To create a Docker file in your project folder, execute - "docker init"
2) The "docker init" command creates the necessary files to build and run docker containers and image.
3) Add a requirements.txt file in the project that specifies the dependencies configurations.
4) Run "docker compose up --build" to start our application inside the docker container.
5) Build our application using "docker build --platform=linux/amd64 -t keerthan_assignment ."
6) Then push our built docker to the docker registry - "docker push keerthan222/keerthan_assignment"
7) The above command creates the docker image runs the image and sees the output in the desired port.
8) This ensures that our Docker image includes all necessary dependencies and configurations for running the application.

***AWS deployment part***

****Prerequisites****

	1.	AWS Account: Ensure you have an AWS account.
	2.	AWS CLI: Install and configure the AWS CLI.
	3.	Docker: Ensure Docker is installed on your machine.
	4.	AWS SAM CLI: Install the AWS SAM (Serverless Application Model) CLI.
	5.	AWS Lambda Docker Image Support: Your Docker image must meet AWS Lambda’s requirements.

***Step-by-Step Instructions***

***Step 1: Dockerize Your Django Application (verify that our Django application has docker files)***

***Step 2: Create a group and users in the AWS Management Console.***

***Step 3: Push our Docker Image to Amazon ECR (Elastic Container Registry - Similar to Docker hub registry but in AWS cloud space)***
- Create an ECR Repository
- Authenticate Docker to our ECR
- Tag our Docker Image
- Push our Docker Image to ECR

***Step 4: Create a Lambda Function Using the Docker Image***
- Create a Lambda function

***Step 5: Set Up API Gateway***
- Create an API Gateway
- Create an Integration
- Create a Route
- Deploy the API
- Grant API Gateway Permission to Invoke Lambda

***Step 6: Test Your Application***
- Find our API Gateway Endpoint - "aws apigatewayv2 get-apis"
- Access Your Django Application - Open your browser and navigate to https://<api_id>.execute-api.us-west-1.amazonaws.com/dev.

**This should bring up our Django application.**
