# AWS Lambda with S3 Trigger

## 1. Open Lambda Service

```text
Services → Lambda
```

---

## 2. Create Lambda Function

Click:

```text
Create Function
```

---

## 3. Configure Function

- Enter function name
- Select runtime

Recommended:

```text
Python
```

---

## 4. Open Code Section

You will see:

```text
lambda_function.py
```

---

## 5. Add Print Statements

Example:

```python
import json

def lambda_handler(event, context):

    print("Lambda Triggered")
    print("File uploaded successfully")

    return {
        'statusCode': 200,
        'body': json.dumps('Hello from Lambda!')
    }
```

---

## 6. Deploy Function

Click:

```text
Deploy
```

---

## 7. Add S3 Trigger

Click:

```text
Add Trigger
```

Select:

```text
Source → S3
```

Choose bucket.

Event type:

```text
All object create events
```

---

## 8. Upload File to S3

Go to S3 bucket and upload:
- image
- pdf
- text file

---

## 9. View CloudWatch Logs

Go to:

```text
Monitor → View CloudWatch Logs
```

Open latest log stream.

---

# Lambda Workflow

```text
Upload File to S3
         ↓
S3 Trigger Activated
         ↓
Lambda Function Executes
         ↓
Print Statements Generated
         ↓
CloudWatch Logs Store Output
```

---

# Services Used

| Service | Purpose |
|---|---|
| Lambda | Serverless compute |
| S3 | File storage |
| CloudWatch | Logs and monitoring |
| Trigger | Automatic execution |