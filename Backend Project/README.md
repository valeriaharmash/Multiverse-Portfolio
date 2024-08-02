<h1>Automation of Financial Documentation Processing</h1> 

> A FastAPI endpoint hosted on Swagger for processing two distinct types of payment files. It downloads and reads specified payment files, custom methods validate data types and formats of all the necessary fields, check if the total amount of fiscal columns match. It ingests data into both Primary and Historical tables of PostgreSQL DB nad dispatches email notifications depending on the outcome of the processing

## Users:
Financial Team Members

## Key Functions for Users:
Financial Team members can process the financial documentation without the need to ask Support Team for help

## Key Features:
- Authentication: The API is inaccessible without proper authentication.
- File Processing: The API can handle two distinct types of payment files, selectable from a dropdown menu.
- Notification system: mails are sent to designated stakeholders based on the outcome of the processing.

## Personal Contributions:

**S** - The legacy flow of processing financial files is quite cumbersome, manually intensive, and prone to error. Financial Team had to send payment files over to Support Team. Support Team had to run legacy Java application locally to process those files, which would take up to an hour for one file. Then Support Team had to take the screensots of the outcome of the processing and email to Financial Team.
    
**T** - Streamline the process: Reduce the required steps for completion, thereby minimizing manual effort. Reduce Processing Time: from one hour for one file to 7 seconds. Optimize Technological Infrastructure: improve operational efficiency by using up-to-date technologies such as Python, Pandas, AWS S3, and SES. Improve Error Handling and Logging. Optimize file management: automatically moving files from ‘to-be-processed/’ to ‘error/’ or ‘success/’ folder within the S3 bucket, which is based on processing outcome, provides a clear visual indication of the status of each file and removes the potential risk of re-processing or overlooking files.Optimize notification system: dispatch automatic notifications.

**A** - First I created SQLAlchemy models that reflect the structure of target DB tables. Then I created methods that download the file from S3, read the file into Pandas DataFrame, callculate all necessary financial sums, ingest data into designated DB tables. Finally I created FastAPI route that accepts the name of the file and the type of file as parameters.

**R** - The result is FastAPI Endpoint that can process two types of the files. It makes sure that values in fiscal columns are correctly formatted and financial sums are correct. It then ingests the data into the DB tables depending on the type of the file. Moves the file ‘error/’ or ‘success/’ folder within the S3 bucket, depending on the oucome of the processing 

#### Legacy State Flow:

![current data flow chart](https://github.com/valeriaharmash/automation_project/assets/116832016/d48db7fa-0f5d-4f6f-b82e-407d6746996f)

#### State Flow after automation:

![detailed_future_flow](https://github.com/valeriaharmash/automation_project/assets/116832016/ab20f452-58a9-4118-b65b-4057fa13264a)



## Technologies

- Language: `Python`
- Database: `MYSQL`
- ORM: `SQLAlchemy`
- Files storage: `S3`
- Data manipulation: `Pandas`
- Running utility tasks: `FastAPI with Swagger for API documentation`
- Email sending service: `SES`
- Testing and Reliability: `Pytest with fixture mocking`

## Competencies

### JF XX.XX

- List the full text of the job function first
- Describe a situation where you demonstrated this job function.
- Summarize the actions you took to accomplish the goal.
- Emphasize the results of this action for your team or your learning.
- Connect the competentcy to this project

### JF XX.XX

- List the full text of the job function first
- Describe a situation where you demonstrated this job function.
- Summarize the actions you took to accomplish the goal.
- Emphasize the results of this action for your team or your learning.
- Connect the competentcy to this project
