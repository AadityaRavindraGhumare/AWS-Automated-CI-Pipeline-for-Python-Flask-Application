# AWS Automated CI Pipeline for Python Flask Application

## Project Overview

This project demonstrates the implementation of an automated Continuous Integration (CI) pipeline for a Python Flask application using AWS CodePipeline, AWS CodeBuild, GitHub, and Docker.

The pipeline integrates source code management with automated build execution, allowing code changes pushed to GitHub to trigger the build process automatically.

## Architecture

**Workflow:**

GitHub → AWS CodePipeline → AWS CodeBuild → Docker Image Build

### AWS Services Used

| Service | Purpose |
|---|---|
| AWS CodePipeline | Automates pipeline orchestration |
| AWS CodeBuild | Executes build commands |
| GitHub | Source code repository |
| AWS Systems Manager Parameter Store | Secure storage of Docker credentials |
| Docker | Container image creation |

### Development Technologies

- Python 3.11
- Flask
- Docker
- Ubuntu
- YAML
- Git and GitHub

## Project Implementation

### 1. GitHub Repository Integration

Connected the GitHub repository to AWS CodeBuild using the GitHub integration.

Repository:  
https://github.com/AadityaRavindraGhumare/aws-devops-zero-to-hero

### 2. AWS CodeBuild Configuration

Created a CodeBuild project with:

- Compute: EC2
- Provisioning: On-demand
- Environment image: AWS Managed Image
- Operating System: Ubuntu
- Runtime: Standard
- Build environment: Docker container
- Python runtime: 3.11

### 3. Buildspec Configuration

Configured build commands using YAML to automate:

- Python dependency installation.
- Docker authentication using securely stored credentials.
- Navigation to the application directory.
- Docker image creation.

### 4. AWS CodePipeline Configuration

Created a pipeline with two stages:

**Source Stage**
- GitHub integration through GitHub App.
- Source code retrieval.
- Automatic triggering through repository changes.

**Build Stage**
- AWS CodeBuild integration.
- Execution of buildspec commands.
- Docker image build process.
- Build status monitoring.

## Execution Results

The pipeline was successfully executed.

- GitHub source stage: Succeeded.
- AWS CodeBuild stage: Succeeded.
- Latest pipeline execution: Succeeded.
- Build environment: Ubuntu.
- Application: Python Flask.

## Key Learning Outcomes

- AWS CI pipeline implementation.
- GitHub and AWS integration.
- AWS CodeBuild configuration.
- AWS CodePipeline orchestration.
- Docker image creation.
- Buildspec YAML configuration.
- Secure credential management.
- Automated build execution and monitoring.

## Screenshots

Add your implementation screenshots to a folder named `screenshots/`.

Suggested screenshots:

1. AWS CodeBuild project configuration.
2. GitHub repository integration.
3. Buildspec configuration.
4. AWS CodeBuild successful execution.
5. AWS CodePipeline architecture.
6. Successful pipeline execution.

## Future Enhancements

- Add automated testing.
- Push Docker images to Amazon ECR.
- Implement AWS CodeDeploy.
- Deploy the application on Amazon EC2 or ECS.
- Add security scanning to the pipeline.
- Implement a complete CI/CD workflow.

## Author

**Aaditya Ghumare**

B.Tech Computer Engineering Student

Interested in AWS Cloud, DevOps, Docker, CI/CD, and Cloud Infrastructure.

GitHub: https://github.com/AadityaRavindraGhumare

---

⭐ If you find this project useful, feel free to explore the repository and share feedback.

#AWS #DevOps #CloudComputing #CI #Docker #Python
