

![image](https://github.com/user-attachments/assets/7dabafec-a908-4c95-b2f7-c11f52de9afb)

Flow:
1. User invoked a REST API and provides a prompt to API GW.
2. API GW sents prompt as an Event to Lambda
3. Prompt + Inference Parameteres (past of Lmabda code) sent to AWS Bedrock
4. AWS Bedrock interacts with Stability AI model to generate the Image
5. Image stored in S3
6. Generate a pre signed URL and send it to API GW which is sent to the user
7. User uses the Pre-signed URL to acccess the object

Implementation Steps:

1. Request access to models
2. 
