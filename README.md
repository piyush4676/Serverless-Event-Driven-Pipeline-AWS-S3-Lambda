# Serverless Event-Driven Pipeline: AWS S3 & Lambda

## 📋 Overview
This project showcases serverless architecture concepts by building an event-driven workflow. Whenever an object (file) is uploaded to an Amazon S3 storage bucket, it automatically triggers an AWS Lambda function, demonstrating serverless scaling and CloudWatch logging.

## 🏗️ Architecture & Workflow
1. **Storage (Amazon S3):** Created a dedicated S3 bucket to act as the event source.
2. **Compute (AWS Lambda):** Developed a serverless function using **Python** (`lambda_handler`) that executes on-demand without provisioning or managing underlying servers.
3. **Event Notification Trigger:** Configured an S3 event notification rule (`All object create events`) to automatically invoke the Lambda function upon file uploads.
4. **Monitoring & Observability (Amazon CloudWatch):** Automatically captured execution logs, metrics, and trace data in CloudWatch to audit serverless events in real time.

## 🛠️ Key Skills Demonstrated
* Designing event-driven, serverless architectures.
* Writing Python runtime functions for AWS Lambda.
* Configuring cross-service integrations (S3 bucket triggers to Lambda).
* Monitoring and debugging cloud applications using Amazon CloudWatch logs.

## 🐍 Code Sample (`lambda_function.py`)
```python
import json

def lambda_handler(event, context):
    print("Received S3 event:", json.dumps(event))
    return {
        'statusCode': 200,
        'body': json.dumps('Hello from my AWS Lambda function!')
    }
<img width="1920" height="1080" alt="Screenshot (3504)" src="https://github.com/user-attachments/assets/6d64f6f3-2cc8-40ad-ba7d-0b85b70320e8" />
