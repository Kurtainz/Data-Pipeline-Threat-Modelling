```mermaid
    sequenceDiagram
        participant Attacker
        participant S3Bucket

        Note over Attacker,S3Bucket: Scenario: Misconfigured S3 Bucket

        Attacker->>S3Bucket: Scans for public/misconfigured buckets
        S3Bucket-->>Attacker: Returns bucket details (if misconfigured)

        Attacker->>S3Bucket: Attempts to access bucket (e.g., list objects)
        S3Bucket-->>Attacker: Grants access (if misconfigured)

        Attacker->>S3Bucket: Downloads sensitive data or uploads malicious files
        S3Bucket-->>Attacker: Successfully performs action
