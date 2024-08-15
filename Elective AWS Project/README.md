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

- [Lambda Functions](https://github.com/valeriaharmash/elective_aws/tree/main/lambdas):
`PublishMessagesFunction`: Publishes messages to an SNS topic.
`ProcessMessagesFunction`: Processes messages from SQS queues. It reads messages and performs actions based on their type, such as storing them in a database.

- [Step Function Definition](https://github.com/valeriaharmash/elective_aws/blob/main/stacks/process-messages-workflow/statemachine/process_messages.asl.json):
The state machine defined in `asl.json` orchestrates the workflow by specifying tasks and parallel branches:
`PublishMessages`: Task state that invokes the PublishMessagesFunction.
`ProcessMessages`: Parallel state with branches for processing notifications and alert messages using the ProcessMessagesFunction.

- IAM Roles:
Defined IAM roles and policies to provide the necessary permissions for Lambda functions to interact with SNS, SQS, and Secrets Manager.

- [CloudFormation Template](https://github.com/valeriaharmash/elective_aws/blob/main/stacks/process-messages-workflow/template.yml):
The `template.yml` file defines all resources, including Lambda functions, IAM roles, and Step Function, using AWS SAM (Serverless Application Model).

- [Makefile](https://github.com/valeriaharmash/elective_aws/blob/main/Makefile):
The Makefile is used to streamline the setup, publishing, and deployment processes:
`Setup`: Automates the creation of S3 buckets and uploading necessary stacks and applications. It includes checks to ensure all required variables are set.
`Publish`: Manages the publishing of the application to AWS Serverless Application Repository, ensuring the version does not already exist.
`Deploy`: Handles the deployment of CloudFormation stacks, including parameter management and template adjustments for different environments.
`Delete`: Provides a mechanism to delete stacks and handle clean-up.

**R** - The final application integrates AWS services into a complete workflow. The Makefile I created streamlines the setup and deployment processs. It ensures that all necessary components are configured correctly and allows for easy management of the deployment lifecycle. The application demonstrates my ability to work with AWS serverless components and manage complex deployments.

[Check out code for Messaging Workflow on GitHub](https://github.com/valeriaharmash/elective_aws)

#### Data Flow Diagram:
<img width="1082" alt="Screenshot 2024-08-15 at 1 32 04 PM" src="https://github.com/user-attachments/assets/58dde97f-e2d3-4562-ab92-c345e94924ee">

#### Step Function View from AWS Console:
<img width="522" alt="Screenshot 2024-08-15 at 1 35 59 PM" src="https://github.com/user-attachments/assets/b8286869-b438-4c28-9ea3-b0f8025d2a4a">

## Technologies:
- Language: `Python`
- Database: `PostgreSQL`
- Event-Driven Computing: `AWS Lambda, Step Function, SecretManager, CloudWatch, SNS, SQS`
- Cloud Services: `AWS Cloud`
- Deployment Orchestration: `AWS CloudFormation, AWS SAM`

## Competencies
### JF 4.3: Is able to build, manage and deploy code into the relevant environment
##### Situation:
In this project, I undertook the challenge of building, managing, and deploying a serverless architecture using AWS services. My objective was to design cloud-based workflow that integrated AWS SNS, SQS, and Step Function to efficiently handle message processing and data ingestion. This involved setting up and automating the deployment of Lambda functions, Step Functions, and related resources.

##### Actions:
- Code Development: I wrote Python code for two Lambda functions, common layer, postgres layer etc.
- Workflow Orchestration: I designed and implemented the state machine in asl.json, which orchestrated the workflow by defining tasks.
- Resource Definition: I used AWS SAM to define all necessary resources in the template.yml file, including Lambda functions, IAM roles, and Step Function.
- Makefile Integration: I created a Makefile to automate various deployment steps:
    - Setting up S3 buckets and uploading stacks and application files.
    - Publishing the application to AWS Serverless Application Repository.
    - Deploying CloudFormation stacks with appropriate parameters for different environments.
- Deployment: Executed the Makefile to ensure all steps were completed correctly, including environment checks, deployment of resources, and version management.

##### Results:
The Makefile automated the deployment process, minimizing manual errors and saving time. This automation facilitated rapid iterations and updates, improving development efficiency. Additionally, it enhanced my understanding of AWS services and cloud deployment practices, leading to better management of complex cloud-based workflows.

##### Connection to Project:
This project directly demonstrates my competency in building, managing, and deploying code into relevant environments. By creating a serverless architecture and automating deployment processes with a Makefile, I showcased my ability to integrate and manage AWS services efficiently.

### JF 6.6: Shows initiative for solving problems within their own remit, being resourceful when faced with a problem to solve
##### Situation:
In this project, I needed to deploy a serverless architecture integrating AWS SNS, SQS, and Step Functions. The challenge was to ensure the deployment process was efficient and error-free, given the complexity of managing multiple AWS services and resources.

##### Actions:
To address this, I created a Makefile to automate the deployment and management of resources. The Makefile included steps for setting up S3 buckets, packaging Lambda functions, deploying CloudFormation stacks, and publishing applications. I also defined checks and validations within the Makefile to ensure all required variables were set and dependencies were correctly configured.

##### Results:
The implementation of the Makefile reduced manual errors and streamlined the deployment process. It saved significant time by automating repetitive tasks and enabled quicker iterations and updates. This approach improved the overall efficiency of the development workflow and enhanced my ability to manage and deploy complex cloud-based architectures effectively.

##### Connection to Project:
This competency was demonstrated through the initiative to automate the deployment process in the project. By creating a Makefile to handle complex deployment tasks, I solved the problem of manual errors and inefficiencies, showcasing resourcefulness and problem-solving skills within the context of deploying a serverless architecture with AWS services.


