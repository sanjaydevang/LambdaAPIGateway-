# LambdaAPIGateway-

# AWS Lambda and API Gateway: Celsius to Fahrenheit Converter

This project demonstrates how to create a serverless API using AWS Lambda and API Gateway. The API converts Celsius temperatures to Fahrenheit. The setup includes a Lambda function written in Python that performs the conversion and returns the result as a JSON response. 

## Project Structure

- `lambda_function.py`: Contains the main code for the Lambda function.
- `README.md`: Project documentation with step-by-step setup instructions.

## Prerequisites

- AWS Account
- Access to AWS services such as Lambda, API Gateway, and CloudWatch
- Basic knowledge of AWS Lambda and API Gateway

## Step-by-Step Setup

### 1. Create the Lambda Function

1. Go to the **AWS Lambda Console**.
2. Create a new Lambda function, name it `CelsiusToFahrenheitConverter`, and choose **Python 3.x** as the runtime.
3. Enter the code provided in `lambda_function.py` in the Lambda function editor.
4. Deploy the function after saving the code.

### 2. Set Up API Gateway

1. Go to **API Gateway Console** and create a **REST API**.
2. Create a new resource called `/temperature`.
3. Add a **GET method** to `/temperature` and integrate it with the Lambda function.
4. Enable **Lambda Proxy Integration** in the integration settings.

### 3. Deploy the API

1. Deploy the API to a stage (e.g., `dev111`).
2. Copy the Invoke URL for testing:
   ```plaintext
   https://<your-api-id>.execute-api.<region>.amazonaws.com/dev111/temperature?celsius=25
