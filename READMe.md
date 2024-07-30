# Cloud Resume API Challenge

This project implements a cloud-based resume using various AWS services, including AWS API Gateway, DynamoDB, Lambda functions, and Amazon S3. The goal is to create a robust and scalable resume application that can be easily updated and accessed via an API.

## Table of Contents

- [Project Overview](#project-overview)
- [Architectural Diagram](#architectural-diagram)
- [Architecture](#architecture)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [How It Works](#how-it-works)
- [GitHub Actions](#github-actions)
- [API Endpoints](#api-endpoints)
- [Project Reference](#project-reference)
- [Submission](#submissions)

## Project Overview

This project allows users to host their resume in the cloud, making it accessible via a RESTful API. The resume data is stored in JSON format within DynamoDB, and changes can be made locally using a code editor like VS Code. The API is designed to fetch the resume data whenever invoked.

## Architectural Diagram
![cloud resume api architecture](<cloud-resume-api architecture.jpeg>)

## Architecture

The architecture consists of the following components:

- **AWS API Gateway**: Serves as the entry point for API requests.
- **AWS Lambda**: Executes the backend logic to fetch data from DynamoDB.
- **Amazon DynamoDB**: Stores the resume data in JSON format.
- **Amazon S3**: Hosts the static content of the resume.
- **GitHub Actions**: Automates deployment and tracks changes.

## Technologies Used

- **AWS Services**:
  - API Gateway
  - Lambda Functions
  - DynamoDB
  - S3 Bucket
- **CI/CD**:
  - GitHub Actions
- **Development Tools**:
  - Visual Studio Code

## Setup Instructions

### 1. Create an AWS Account
If you don’t already have one, [sign up for an AWS account](https://aws.amazon.com/).

### 2. Set Up AWS Services
- **DynamoDB Table**: Create a DynamoDB table to store your resume in JSON format.
- **S3 Bucket**: Set up an S3 bucket to host the static content of your resume.
- **Lambda Function**: Create a Lambda function that connects API Gateway to DynamoDB.
- **API Gateway Configuration**: Configure API Gateway with a GET method to retrieve the resume data.

### 3. Configure GitHub Actions
- **Workflows Setup**: In the `.github/workflows` directory, create workflows to automate deployment and track changes.

### 4. Create Your Resume
- **JSON Document**: Use Visual Studio Code or your favourite code editor to create a JSON document for your resume and save it in your project directory.

### 5. Deploy Changes
- **Push to GitHub**: After making changes, push your updates to GitHub. The GitHub Actions pipeline will automatically deploy these changes to AWS.

## How It Works
- The resume data is populated in DynamoDB in JSON format.
- A Lambda function is created to link DynamoDB with the API Gateway.
- The API Gateway is configured with a GET method that retrieves the JSON document from DynamoDB whenever the API URL is accessed via a browser.
- Any changes made locally to the resume will be reflected in the AWS infrastructure after pushing to GitHub.

## GitHub Actions
GitHub Actions create a CI/CD pipeline that automates the deployment process. This ensures that any changes made to the resume are automatically tracked and deployed to AWS, keeping the API up to date.

## API Endpoint
[My api endpoint](https://6e2pry5iad.execute-api.eu-north-1.amazonaws.com/wanjala)

## Project Reference
[Here](https://cloudresumeapi.dev/)

Design architectural diagram using [Lucid charts for design](https://www.lucidchart.com/pages/landing?utm_source=google&utm_medium=cpc&utm_campaign=_chart_en_tier3_mixed_search_brand_exact_&km_CPC_CampaignId=1484560207&km_CPC_AdGroupID=60168114191&km_CPC_Keyword=lucid%20chart&km_CPC_MatchType=e&km_CPC_ExtensionID=&km_CPC_Network=g&km_CPC_AdPosition=&km_CPC_Creative=442433234360&km_CPC_TargetID=kwd-55720648523&km_CPC_Country=9197737&km_CPC_Device=c&km_CPC_placement=&km_CPC_target=&gad_source=1&gclid=CjwKCAjwnqK1BhBvEiwAi7o0X8YkqH6TH6TN3c7gwZ-yPrEZhpQaBqtjIp9h0bZnZGfr27hA6ENLLxoCUjYQAvD_BwE)

## Submissions
[Here](https://cloudresumeapi.dev/submissions/)