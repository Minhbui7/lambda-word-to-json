# lambda-word-to-json
Convert the tables in a Word Document into json format and ingest the new document into Amazon Kendra

The Lambda function will scan the Word Document file, detect tables, convert the tables into JSON data, insert the json text into the word document.
The new modified document is ingested into kendra for retrieval by a LLM using Kendra as datasource for RAG and increase accuracy by providing JSON-formated text. 
The Lambda is automatically triggered by an S3 event trigger when a new word document is PUT in the S3 bucket (with extension docx).

The steps are as follow:
1. Create Lambda function
   You will need to specify the Kendra index ID and ARN details in the Lambda code. 
3. Create Lambda layer for Docx library and attach it to Lambda
4. Modify Lambda execution role to give S3 and Kendra permissions
5. Create an S3 bucket
6. Configure S3 event triggers on PUT actions to invoke Lambda
7. Test by uploading a Docx document to S3 bucket
   
Details instructions WIP
