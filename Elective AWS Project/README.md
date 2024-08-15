<h1>Serverless Messaging Workflow with AWS Lambda, Step Function, SNS and SQS</h1>

>  This project was developed to enhance my skills with AWS services, specifically SQS and SNS, and to practice deploying a complete cloud-based workflow. The architecture includes a Lambda function that publishes messages to an SNS topic, which then distributes these messages to different SQS queues based on their type. Another Lambda function processes the messages from the SQS queues, handling them accordingly and ingesting them into a database. The entire process is orchestrated by an AWS Step Function, which coordinates the flow of messages through the different components.

## Users:
The users of this system are developers or DevOps engineers responsible for managing and processing messages. They might work in roles that involve handling large volumes of data or events.

## Key Functions for Users:
This project automates the workflow of message processing in a cloud environment. It provides a solution for handling messages from SNS to SQS, processing them with Lambda functions, and storing results in a database. This automation helps streamline operations, reduces manual intervention, and improves overall efficiency.
The inspiration for this project came from a desire to deepen my understanding and practical skills with AWS SQS and SNS. The goal was to create a comprehensive, serverless architecture that showcases my ability to integrate and manage various AWS components in a real-world scenario.

## Key Features:
- AWS Step Function: Orchestrates the flow of messages through different stages of processing.
- SNS Topic: Publishes messages that are distributed to different SQS queues based on message type.
- SQS Queues: Handles and organizes incoming messages for processing.
- Lambda Functions: Publishes messages to SNS and processes messages from SQS, ensuring efficient and automated handling of data.


## Personal Contributions:

**S** - The application I developed is a serverless workflow for processing SNS messages using AWS services. I created this program to enhance my skills with AWS services like SQS and SNS, and to practice deploying a complete cloud-based workflow. The goal was to build a scalable and automated solution that handles message distribution and processing.
    
**T** - The overall structure of the application involves a Lambda function publishing messages to an SNS topic, which then distributes these messages to various SQS queues based on their type. Another Lambda function processes messages from these queues and ingests them into a database. Prior to building the program, I designed a setup to manage the various components and ensure they worked well together.

**A** - The implementation involved several steps:

- Lambda Functions:
`PublishMessagesFunction`: Publishes messages to an SNS topic.
`ProcessMessagesFunction`: Processes messages from SQS queues. It reads messages and performs actions based on their type, such as storing them in a database.

- Step Function Definition:
The state machine defined in `asl.json` orchestrates the workflow by specifying tasks and parallel branches:
`PublishMessages`: Task state that invokes the PublishMessagesFunction.
`ProcessMessages`: Parallel state with branches for processing notifications and alert messages using the ProcessMessagesFunction.

- IAM Roles:
Defined IAM roles and policies to provide the necessary permissions for Lambda functions to interact with SNS, SQS, and Secrets Manager.

- CloudFormation Template:
The `template.yml` file defines all resources, including Lambda functions, IAM roles, and Step Function, using AWS SAM (Serverless Application Model).

- Makefile Integration:
The Makefile is used to streamline the setup, publishing, and deployment processes:
`Setup`: Automates the creation of S3 buckets and uploading necessary stacks and applications. It includes checks to ensure all required variables are set.
`Publish`: Manages the publishing of the application to AWS Serverless Application Repository, ensuring the version does not already exist.
`Deploy`: Handles the deployment of CloudFormation stacks, including parameter management and template adjustments for different environments.
`Delete`: Provides a mechanism to delete stacks and handle clean-up.

**R** - The final application integrates AWS services into a complete workflow. The Makefile I created streamlines the setup and deployment processs. It ensures that all necessary components are configured correctly and allows for easy management of the deployment lifecycle. The application demonstrates my ability to work with AWS serverless components and manage complex deployments.

