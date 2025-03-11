```mermaid
    flowchart TD
        A[Start] --> B[Scrape Data]
        B --> C[Get Data from Wikipedia]
        C --> D[Parse HTML with BeautifulSoup]
        D --> E[Parse Data into DataFrame]
        E --> F[Generate Pseudonyms]
        E --> G[Categorize Revenue]
        E --> H[Generalize Locale]
        F --> I[Create DataFrame]
        G --> I
        H --> I
        I --> J[Convert DataFrame to CSV]
        J --> K[Upload CSV to S3 Bucket]
        K --> L[End]

        subgraph Scraping and Parsing
            B --> C --> D --> E
        end

        subgraph Data Transformation
            E --> F
            E --> G
            E --> H
            F --> I
            G --> I
            H --> I
        end

        subgraph Upload to S3
            I --> J --> K
        end