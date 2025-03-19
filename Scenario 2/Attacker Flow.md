```mermaid
    sequenceDiagram
    participant Attacker
    participant TargetWebsite
    participant WebScraper
    participant DataProcessor
    participant S3Bucket

    Note over Attacker,TargetWebsite: Scenario: Malicious Data Injection

    Attacker->>TargetWebsite: Injects malicious content (e.g., scripts, fake data)
    TargetWebsite-->>WebScraper: Serves malicious content to the scraper

    WebScraper->>DataProcessor: Passes malicious content for processing
    DataProcessor-->>WebScraper: Processes malicious content (e.g., stores in DataFrame)

    WebScraper->>S3Bucket: Uploads processed data (including malicious content)
    S3Bucket-->>WebScraper: Successfully stores data

    Note over DataProcessor,S3Bucket: Malicious content remains undetected