# Kill Chain Attack Description: Data Anonymisation ETL Pipeline Scenario 1: Misconfigured S3 bucket leads to data exposure
 
 ## Stages of the Attack
 
 ### Reconnaissance
 The attacker uses tools like s3scanner, bucket-stream, or manual searches to find S3 buckets with weak or misconfigured permissions. They may also search for exposed buckets through public datasets, GitHub repositories, or misconfigured logging systems.
 
 ### Weaponization
 The attacker develops or customizes scripts to enumerate and access the contents of the misconfigured bucket. They may also prepare tools to exfiltrate data or inject malicious content.
 
 ### Delivery
 The attacker uses their tools to connect to the S3 bucket and list its contents. If the bucket is publicly accessible, they can directly access it via HTTP requests.
 
 ### Exploitation
 The attacker downloads sensitive data from the bucket or uploads malicious files (e.g., ransomware or backdoors). They may also modify or delete data to disrupt operations.
 
 ### Installation
 The attacker uploads malicious scripts or tools to the bucket for later use. They may also use the bucket as a staging area for exfiltrated data.
 
 ### Command and Control (C2)
 The attacker uses the bucket to store command-and-control scripts or exfiltrated data. They may also use the bucket to distribute malware to other systems.

 ### Actions on Objectives
 The attacker exfiltrates sensitive data (e.g., customer information, intellectual property). They may also encrypt the data and demand a ransom for its release.