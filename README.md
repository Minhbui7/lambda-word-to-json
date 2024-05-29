# lambda-word-to-json
Convert the tables in a Word Document into json format and ingest the new document into Amazon Kendra

The Lambda function will scan the Word Document file, detect tables, convert the tables into JSON data, insert the json text into the word document.
The new modified document is ingested into kendra for retrieval by a LLM using Kendra as datasource for RAG and increase accuracy by providing JSON-formated text. 
The Lambda is automatically triggered by an S3 event trigger when a new word document is PUT in the S3 bucket (with extension docx).

```
