```mermaid
    mindmap
    root((Misconfigured S3 Bucket))
        Spoofing
        Attacker impersonates a legitimate user
        Mitigation: Use IAM roles, enable MFA
        Tampering
        Attacker modifies or deletes data
        Mitigation: Enable versioning, use Object Lock
        Repudiation
        Attacker performs actions without trace
        Mitigation: Enable CloudTrail, use access logs
        Information Disclosure
        Sensitive data exposed to unauthorized users
        Mitigation: Make buckets private, restrict access
        Denial of Service
        Attacker overwhelms the bucket
        Mitigation: Use AWS WAF, monitor access patterns
        Elevation of Privilege
        Attacker gains unauthorized privileges
        Mitigation: Audit IAM roles, use AWS Config