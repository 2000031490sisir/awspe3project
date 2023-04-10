# awspe3project
Demonstrating GET and POST functionalities using a serverless web application in AWS
1.	IAM ROLE
Create an with required name and description and attach two policies namely AmazonDynamoDBReadOnlyAccess and AWSLambda_FullAccess.
 
 
2.	AWS LAMBDA
Create a lambda function with required name and add the below code in the source code section in order to integrate the lambda function with dynamodb table that is going to be created on the coming step.
In the Permissions section, use the existing role that was create just now.
 
 
3.	DynamoDB
Create a dynamoDB table with required name and add a partition key with your email as value.
Create one or more items with attributes email, first name and last name. All attributes are considered as string parameters.
 
 
4.	API Gateway
Create a REST API with required name and create a resource with specific name by clicking the Actions tab. Also, Enable CORS.
Create a GET method by changing the Integrationtype to Lambda function from mock(default). Select the name of the created lambda function.
 
 
Add a URL query string parameter for the created API with content type json. Make and confirm the integration request with the created lambda function. Last but not the least, Deploy the API with suitable name.
NOTE:- For API to work without hassles, Enable and update the CORS as needed.
Succeeding steps:-
•	After integrating the lambda function with the REST API, open POSTMAN, an application to test various API requests.
•	As part of the project, we are testing the GET request status.
•	Provide the key and value along with the invoke URL of the deployed API.
 

5.	Amazon S3
NOTE:- we need a specific static website resources to perform this step.
Create a html file with required input to redirect the page to retrieve information stored in the dynamoDB table.
Host the static website by uploading the files into an amazon s3 bucket. Enable static website hosting in order to get a website endpoint for the web application. Do not forget to provide public access to the files and write a bucket policy to display the index file while invoking the endpoint.
 
 
 
Test the GET request status by invoking the serverless web application using the website endpoint. Type your email in the Email input section to display the information related to that partition key in your dynamoDB table.
 
 


