```mermaid
    graph TD
    A[Data Source: Wikipedia] --> B{Data Extraction and Parsing};
    B --> C{Data Transformation};
    C --> D[Data Storage: S3 Bucket];

    subgraph Data Extraction and Parsing
        B
    end

    subgraph Data Transformation
        C
    end

    subgraph Data Storage
        D
    end