# Serverless-API-using-Lambda-API-Gateway-


📌 Project 6 – Serverless API using Lambda (Demo-lfunction) & API Gateway (test-api)
📖 Project Overview

This project demonstrates a Serverless architecture using AWS Lambda and API Gateway.
A Lambda function named Demo-lfunction was created and integrated with a REST API named test-api.
A resource /welcome with GET method was configured and deployed to stage QA.
The API successfully invokes the Lambda function and returns a response.

🎯 Objective

Create a Lambda function,

Integrate Lambda with API Gateway,

Create REST API,

Deploy API to stage QA,

Access API using Invoke URL,

🛠️ AWS Services Used

AWS Lambda

Amazon API Gateway (REST API)

IAM Role

🏗️ Architecture

Client → API Gateway (test-api) → Lambda (Demo-lfunction) → Response

No EC2. No server management. Fully serverless.


🔄 Implementation Steps

Step 1: Create Lambda Function

Function Name: Demo-lfunction

Runtime: Python

Code used:



def lambda_handler(event, context):


    return {
    
        'statusCode': 200,
        
        'body': 'Hello from AWS Lambda + API Gateway'
        
    }
    
Step 2: Create REST API

API Name: test-api

Protocol: REST

Endpoint Type: Regional

Step 3: Create Resource

Resource Path: /welcome


Step 4: Create Method

Method: GET

Integration Type: Lambda

Lambda Function: Demo-lfunction

Authorization: None

Step 5: Deploy API

Stage Name: QA

Deploy API

Invoke URL:

https://oe1qhwd83.execute-api.us-east-1.amazonaws.com/QA/welcome


🚀 Final Output
Hello from AWS Lambda + API Gateway
