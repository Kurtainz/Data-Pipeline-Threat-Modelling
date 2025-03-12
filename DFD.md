```mermaid
    flowchart TD
    A[Start] --> B[Scrape Data]
    B --> C[Get Data from Wikipedia]
    C --> D[Parse HTML with BeautifulSoup]
    D --> E[Parse Data into DataFrame]

    subgraph Scraping and Parsing
        B
        C
        D
        E
    end

    E --> F[Generate Pseudonyms]
    E --> G[Categorize Revenue]
    E --> H[Generalize Locale]
    F --> I[Create DataFrame]
    G --> I
    H --> I

    subgraph Data Transformation
        F
        G
        H
        I
    end

    I --> J[Convert DataFrame to CSV]
    J --> K[Upload CSV to S3 Bucket]
    K --> L[End]

    subgraph Upload to S3
        J
        K
    end