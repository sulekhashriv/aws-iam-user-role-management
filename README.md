# aws-iam-user-role-management
AWS IAM user, group, role management and EC2-to-S3 access control project
# AWS IAM User and Role Management

## Project Overview
This project demonstrates AWS Identity and Access Management (IAM), including creating IAM users, groups, roles, and granting secure access to Amazon S3 from an EC2 instance.

## AWS Services Used
- AWS IAM
- Amazon EC2
- Amazon S3
- AWS CLI

## Tasks Completed

### 1. IAM User and Group
- Created IAM group: `CloudSupport-ReadOnly`
- Attached `IAMReadOnlyAccess` policy.
- Created IAM user: `cloud-support-user`
- Added the user to the IAM group.
- Configured MFA.

### 2. IAM Role for EC2
- Created IAM role: `cloud-support-ec2-role`
- Selected EC2 as the trusted service.
- Attached `AmazonS3ReadOnlyAccess`.

### 3. EC2 Role Attachment
- Attached the IAM role to the EC2 instance.
- Verified the active identity using `aws sts get-caller-identity`.

### 4. S3 Access Testing
- Created an S3 bucket.
- Tested S3 access from the EC2 terminal using AWS CLI.
- Troubleshot and resolved an AccessDenied error.
- Verified bucket listing using:

```bash
aws s3 ls
```

## Security Best Practices
- Used IAM roles instead of storing AWS access keys on EC2.
- Applied read-only S3 permissions.
- Enabled MFA for the IAM user.
- Kept S3 Block Public Access enabled.

## Project Outcome
Successfully configured IAM users, groups, and roles and verified EC2-to-S3 access using AWS IAM permissions.

## Skills Demonstrated
AWS IAM | EC2 | S3 | AWS CLI | IAM Policies | Role-Based Access Control | Troubleshooting
