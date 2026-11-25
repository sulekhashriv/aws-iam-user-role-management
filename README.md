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

## Screenshots
<img width="1654" height="960" alt="EC2 attached role" src="https://github.com/user-attachments/assets/626367bf-05a9-437c-b2a4-33470c3354aa" />
<img width="1537" height="960" alt="IAM S3 Terminal output" src="https://github.com/user-attachments/assets/a0b0e2a0-ffa5-47a5-903b-2ae68d17facc" />
<img width="1531" height="960" alt="IAM user" src="https://github.com/user-attachments/assets/12fc2543-5b0b-416b-8ac0-ed1098e164f1" />
<img width="1444" height="960" alt="IAM USer group" src="https://github.com/user-attachments/assets/7a4bfb3e-164c-4d28-99ee-f539d9addf1c" />
<img width="1501" height="960" alt="IAM role cloud-support-ec2 role" src="https://github.com/user-attachments/assets/4b8c7197-8301-441b-9414-f32693373154" />


