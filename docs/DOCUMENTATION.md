# Capstone V2[Todo App Deployment]
This file containes a well documented step by step approach on the Pipeline Automation, Infra Provisioning and Deployment of the sample application in the repo.
## Tools and Technologies Used
  - git
  - docker
  - AWS (ECS with Fargate | RDS Mysql | Cloudwatch)

## Approach
I adopted an incremental, step-by-step validation approach to isolate failures and verify each component before introducing additional infrastructure complexity.

## Phase 1 : Local Deployment
- Fork and Clone the Project onto WSL
- Run it Locally using the instructions given in the source repo's readme to see if basic functionality works

## Phase 2: Backend Logging
- Add basic backend server logging using pino and pino-http for http requests and responses(To be further worked on later)
- Run Locally Again to test if responses and requests are logged properly with the appropriate status codes.
- 
## Phase 3: Database Setup
- DB service of choice is RDS since we’re dealing with simple tabular data.
- Setup RDS, hook it up to the local app instance and log to AWS cloudwatch.
- db credentials stored locally in a .env file tentatively for quick testing, to be moved into an appropriate secrets manager after successful testing
