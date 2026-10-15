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
### Proof of Execution

**1. S3 Bucket File Upload:**
<img width="1920" height="1080" alt="Screenshot (3504)" src="https://github.com/user-attachments/assets/8bf5c3e0-4d06-4aca-965c-168a75019037" />

**2. Lambada S3 trigger Upload:**
<img width="1920" height="1080" alt="Screenshot (3505)" src="https://github.com/user-attachments/assets/09cf11ee-ef30-4cd8-a811-242ac6b0626b" />

**3. CloudWatch Execution Logs:**
<img width="1920" height="1080" alt="Screenshot (3506)" src="https://github.com/user-attachments/assets/f99fb0a0-d5e5-4e38-9176-c13296e0c3f3" />


