```mermaid
graph TD;
    A[Wikipedia SSE Stream (RecentChanges API)];
    B[Event Ingestion Service (Kafka Producer)];
    C[Kafka Cluster (Topic: wikipedia_events)];
    D[Language Filtering Service (Kafka Consumer)];
    E[Statistics Aggregation Service (Kafka Consumer)];
    F[Filtered Events Topic (Optional)];
    H[Discord Bot Service];
    I[Persistent Storage (Redis/MongoDB/PostgreSQL)];
    J[Discord Users (Commands: !recent, !setLang, !stats)];
    
    A --> B
    B --> C
    C --> D
    C --> E
    D --> F
    F --> H
    E --> I
    I --> H
    H --> J

```