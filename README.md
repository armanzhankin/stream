```mermaid
graph TD
    A[Wikipedia SSE Stream] --> B[Event Ingestion Service]
    B --> C[Kafka Cluster]
    C --> D[Language Filtering Service]
    C --> E[Statistics Aggregation Service]
    D --> F[Filtered Events Topic (Optional)]
    F --> H[Discord Bot Service]
    E --> I[Persistent Storage]
    I --> H
    H --> J[Discord Users]