# Cloud-account-onboarding-task-1

1. Overview
This project documents the setup of IAM, MFA, and AWS CLI for accessing the Dev Sandbox environment. It also follows the team's tagging and naming conventions.

# 1. IAM Setup
- **User Name:** nisha-dev
- **Policy Attached:** AmazonEC2ReadOnlyAccess
- **Region:** ap-south-1 (Mumbai)
- **Purpose:** Read-only access to view EC2 instances for cost reporting.
- Access Key was created for CLI authentication.
## 2. MFA Configuration
- **Device:** Virtual MFA using Google Authenticator App
- **Steps:** IAM > User > Security Credentials > Assign MFA Device > Scan QR Code
- MFA is enabled to secure the account. Login is not possible without the mobile code.

## 4. AWS CLI Installation & Verification

Check version:
```bash
aws --versionConfigure CLI:bashaws configure
# Region: ap-south-1
# Output: jsonVerify Access:bashaws sts get-caller-identityOutput shows User ID and Account ID, which confirms the Dev Sandbox access is working.

