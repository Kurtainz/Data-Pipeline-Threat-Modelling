# MITRE ATT&CK Summary

### 1. Initial Access
#### Technique: Exploit Public-Facing Application (T1190)

The attacker identifies and exploits a misconfigured S3 bucket that is publicly accessible.

Example: Scanning for S3 buckets with weak or no access controls.

### 2. Discovery
#### Technique: Cloud Infrastructure Discovery (T1580)

The attacker enumerates cloud resources, such as S3 buckets, to identify misconfigurations.

Example: Using tools like s3scanner or manual methods to find publicly accessible buckets.

### 3. Collection
#### Technique: Data from Cloud Storage Object (T1530)

The attacker collects sensitive data from the misconfigured S3 bucket.

Example: Downloading files containing customer information, intellectual property, or other sensitive data.

### 4. Exfiltration
#### Technique: Exfiltration Over Web Service (T1567)

The attacker exfiltrates the collected data to an external server or cloud storage under their control.

Example: Uploading stolen data to another S3 bucket or external server.

### 5. Impact
#### Technique: Data Destruction (T1485)

The attacker may delete or corrupt data in the S3 bucket to disrupt operations.

Example: Deleting critical files or overwriting them with malicious content.

```mermaid
    flowchart TD
        A[Attacker] --> B["Reconnaissance: Cloud Infrastructure Discovery (T1580)"]
        B --> C["Weaponization: Prepare Exploit Tools"]
        C --> D["Delivery: Exploit Public-Facing Application (T1190)"]
        D --> E["Exploitation: Access Misconfigured S3 Bucket"]
        E --> F["Installation: Data from Cloud Storage Object (T1530)"]
        F --> G["Command and Control: Exfiltration Over Web Service (T1567)"]
        F --> H["Actions on Objectives: Data Destruction (T1485)"]

        style A fill:#d70d0d,stroke:#333,stroke-width:2px