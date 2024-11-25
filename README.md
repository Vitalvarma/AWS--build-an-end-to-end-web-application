# AWS - Build an End-to-End Web Application

## Services Used
- AWS Amplify
- AWS Lambda
- Amazon API Gateway
- Amazon DynamoDB
- AWS IAM

![IMG-20241125-WA0004](https://github.com/user-attachments/assets/7dd3200a-e201-4e43-b943-4a4f7575e785)

### Step 1: Amplify
1. Create a ZIP file of `index.html` that I have already prepared in the repository.
2. Create an app in Amplify.
3. Choose the "Without Git Provider" option (existing code).
4. Drag and drop the ZIP file and click on the "Save and Deploy" button.
5. Refresh the page.

![IMG-20241125-WA0002](https://github.com/user-attachments/assets/51d562e3-86ac-4d66-b045-7eee985a2a64)

### Step 2: Lambda Function
1. Navigate to Lambda from the Management Console.
2. Click on the options for your concern.
3. Choose Python 3, since my code is in Python.
4. Replace the code with the content from the Git text document.
5. We will deploy and test the code later.

![IMG-20241125-WA0003](https://github.com/user-attachments/assets/5b302b46-ecdd-45e1-aa16-4c4c3eb75bda)

### Step 3: API Gateway
1. Navigate to API Gateway from the Management Console.
2. Select "Create REST API."
3. Create a method (e.g., POST) and select the Lambda function from the options.
4. Enable CORS since we are connecting Amplify with the Lambda function, which are on different domains.
5. Save the API invoke URL for later use.

### Step 4: DynamoDB
1. Create a table.
2. Add a partition key as `ID`.
3. Save the ARN URL for later use.

### Step 5: IAM for Lambda Function
1. Create a role.
2. Add a policy and include the code from my GitHub repository for the text document execution role policy JSON.
3. Change the table name to match your table name.

### Step 6: Lambda Function Code
1. Deploy and test the code.
2. You should see the result in the DynamoDB table.

### Step 7: Connect Amplify and API Gateway
1. Replace the API invoke URL and ARN.
2. Continue deploying.
