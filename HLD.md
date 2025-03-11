```mermaid
    flowchart TD
        A[Wikipedia Page] --> B[Web Scraper]
        B --> C[Data Processing]
        C --> D[Processed Data]
        D --> E[AWS S3 Bucket]

        subgraph Web Scraper
            B1[requests Library] --> B2[BeautifulSoup]
        end

        subgraph Data Processing
            C1[Generate Pseudonyms] --> C2[Categorize Revenue]
            C2 --> C3[Generalize Locale]
            C3 --> C4[Create DataFrame]
        end

        subgraph AWS S3
            E1[Upload CSV] --> E2[Store in S3 Bucket]
        end