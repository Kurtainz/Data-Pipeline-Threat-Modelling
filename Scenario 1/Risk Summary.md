 | Risk ID | Description                                         | Severity | Likelihood | Impact | Mitigation Plan                                       |
 |---------|-----------------------------------------------------|----------|------------|--------|-------------------------------------------------------|
 | R1      | Publicly accessible S3 bucket                       | High     | High       | High   | Ensure S3 buckets are private by default              |
 | R2      | Sensitive data exposure due to misconfiguration     | High     | High       | High   | Enable S3 Object Lock to prevent tampering            |
 | R3      | Data tampering or deletion                          | High     | Medium     | High   | Regularly back up data to a secure location           |
 | R4      | Lack of monitoring for bucket access                | Medium   | High       | High   | Enable AWS CloudTrail to log all S3 bucket activities |
 | R5      | Insufficient access controls                        | High     | High       | High   | Use IAM roles and policies to enforce least privilege |