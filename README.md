# Cloud Storage and Security Monitoring on AWS

## Project Overview

This project demonstrates fundamental cloud security practices using Amazon Web Services (AWS). It focuses on securing cloud storage, controlling user permissions, and investigating AWS activity using CloudTrail.

## Objectives

- Secure cloud storage using Amazon S3.
- Protect stored data with server-side encryption.
- Apply least-privilege access using AWS IAM.
- Investigate AWS account activity using CloudTrail.
- Document security findings and recommendations.

## AWS Services Used

| Service | Purpose |
|---|---|
| Amazon S3 | Stores the sample security report |
| AWS IAM | Manages users, groups, and permissions |
| AWS CloudTrail | Records AWS activity for security investigations |

## Security Controls Implemented

### 1. Amazon S3

- Created a private S3 bucket.
- Kept Block Public Access enabled.
- Enabled default server-side encryption using SSE-S3.
- Uploaded a sample security report.

### 2. AWS IAM

- Created an IAM user and group.
- Configured permissions for the project bucket.
- Allowed listing bucket contents and reading project files.
- Tested access using the IAM user.
- Applied the principle of least privilege.

### 3. AWS CloudTrail

- Explored CloudTrail Event History.
- Investigated a `ConsoleLogin` event.
- Reviewed the event identity, timestamp, source IP, and login result.
- Examined a `PutBucketEncryption` event associated with the project bucket.

## Investigation Findings

- The reviewed console login event showed a successful login by an IAM user.
- The project's S3 bucket had default encryption enabled using SSE-S3.
- CloudTrail contained an event associated with the bucket's encryption configuration.
- Additional investigation is needed to determine whether unfamiliar activity is authorized.

## Security Recommendations

- Follow the principle of least privilege.
- Keep S3 Block Public Access enabled.
- Maintain appropriate encryption settings.
- Review CloudTrail events for unexpected activity.
- Protect AWS credentials and enable multi-factor authentication.
- Monitor AWS usage and costs.

## Key Learnings

- S3 storage security and encryption.
- IAM users, groups, and permissions.
- Least-privilege access control.
- CloudTrail event analysis.
- Basic cloud security investigation.

## Architecture Diagram

This diagram illustrates the IAM access controls, S3 security configuration, and CloudTrail management-event investigation used in this project.

[View the AWS Security Architecture Diagram (PDF)](aws_architecture_diagram.pdf)


## Disclaimer

This project was created for educational purposes. Findings are limited to the AWS configurations and events examined during the project.

## Author

**Sameeha Shajahan**

Cybersecurity Learner | Cloud Security | SOC Analysis

- GitHub: [SAMEEHASHAJAHAN](https://github.com/SAMEEHASHAJAHAN)
- LinkedIn: [Sameeha Shajahan](https://linkedin.com/in/sameeha-shajahan-4582093b8)
