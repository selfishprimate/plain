# Database

Database solutions for different data models, scale requirements, and use cases. Choose based on your data structure, query patterns, consistency needs, and scaling requirements.

## Relational Databases (SQL)

Traditional structured databases using tables with predefined schemas and SQL for querying. These databases excel at complex relationships, ACID transactions, and data integrity, making them ideal for applications requiring consistency and complex queries. Choose relational databases when you have structured data with clear relationships, need ACID compliance for transactions, require complex queries with joins, or when data integrity is critical.

### PostgreSQL
Advanced open-source relational database.
- **Best for:** Complex queries, ACID compliance, JSON data
- **Features:** JSONB, full-text search, extensions (PostGIS), row-level security
- **Hosting:** Self-hosted, Supabase, Neon, Railway, Render
- **Pricing:** Free open source, managed from $0/month
- **Use cases:** SaaS apps, financial systems, geospatial apps

### MySQL
World's most popular open-source database.
- **Best for:** Web applications, WordPress, high-speed reads
- **Features:** Replication, partitioning, full-text indexing
- **Hosting:** Self-hosted, PlanetScale, AWS RDS, DigitalOcean
- **Pricing:** Free open source, managed from $0/month
- **Use cases:** Web apps, content management, e-commerce

### SQLite
Lightweight, serverless, self-contained database.
- **Best for:** Embedded apps, local storage, edge computing
- **Features:** Zero-configuration, ACID compliant, tiny footprint
- **Hosting:** File-based, Turso for distributed SQLite
- **Pricing:** Free and open source
- **Use cases:** Mobile apps, desktop apps, testing

### Microsoft SQL Server
Enterprise-grade relational database.
- **Best for:** .NET applications, enterprise Windows environments
- **Features:** Advanced analytics, in-memory tables, machine learning
- **Hosting:** Self-hosted, Azure SQL Database
- **Pricing:** Free Express edition, paid from $931/year
- **Use cases:** Enterprise apps, data warehousing

### MariaDB
MySQL fork with additional features.
- **Best for:** MySQL compatibility with extra features
- **Features:** Better performance, more storage engines
- **Hosting:** Self-hosted, SkySQL
- **Pricing:** Free open source
- **Use cases:** Similar to MySQL

## NoSQL Databases

Non-relational databases designed for flexible schemas, horizontal scaling, and specific data models like documents, key-value pairs, or graphs. NoSQL databases trade some consistency guarantees for flexibility and scale, making them ideal for rapidly evolving applications. Choose NoSQL when dealing with unstructured or semi-structured data, needing horizontal scaling, requiring flexible schemas that change frequently, or when eventual consistency is acceptable.

### MongoDB
Document database with flexible schemas.
- **Best for:** Flexible schemas, rapid development, JSON-like documents
- **Features:** Aggregation framework, full-text search, transactions
- **Hosting:** MongoDB Atlas, self-hosted
- **Pricing:** Free tier 512MB, paid from $57/month
- **Use cases:** Content management, catalogs, real-time analytics

### DynamoDB
AWS's fully managed NoSQL database.
- **Best for:** Serverless applications, auto-scaling needs
- **Features:** Single-digit millisecond latency, auto-scaling, global tables
- **Hosting:** AWS managed only
- **Pricing:** Pay-per-request or provisioned capacity
- **Use cases:** Gaming, IoT, mobile backends

### Cassandra
Distributed wide-column store database.
- **Best for:** High write throughput, time-series data
- **Features:** Linear scalability, no single point of failure
- **Hosting:** Self-hosted, DataStax Astra
- **Pricing:** Open source free, Astra from $25/month
- **Use cases:** IoT data, recommendation engines, messaging

### CouchDB
Document database with sync capabilities.
- **Best for:** Offline-first applications, mobile sync
- **Features:** Multi-master replication, REST API, MapReduce
- **Hosting:** Self-hosted, IBM Cloudant
- **Pricing:** Open source free
- **Use cases:** Mobile apps, offline-first apps

## Key-Value Stores

Simple databases storing data as key-value pairs, optimized for speed and scalability. These databases excel at caching, session management, and real-time features with sub-millisecond response times. Choose key-value stores when you need extremely fast data access, simple data structures without complex relationships, caching layers to reduce database load, or real-time features like leaderboards and counters.

### Redis
In-memory data structure store.
- **Best for:** Caching, sessions, real-time features
- **Features:** Pub/sub, transactions, Lua scripting, persistence options
- **Hosting:** Redis Cloud, AWS ElastiCache, Upstash
- **Pricing:** Open source free, managed from $0/month
- **Use cases:** Caching, queues, leaderboards, sessions

### Memcached
High-performance distributed memory caching.
- **Best for:** Simple caching needs
- **Features:** Simple key-value, multi-threading
- **Hosting:** Self-hosted, AWS ElastiCache
- **Pricing:** Open source free
- **Use cases:** Database query caching, session storage

### KeyDB
Faster Redis-compatible database.
- **Best for:** High-performance Redis alternative
- **Features:** Multi-threading, Redis compatible
- **Hosting:** Self-hosted, KeyDB Cloud
- **Pricing:** Open source free
- **Use cases:** Same as Redis with better performance

## Graph Databases

Databases optimized for storing and querying highly connected data as nodes and relationships. Graph databases excel at traversing relationships and finding patterns in connected data, making complex relationship queries simple and performant. Choose graph databases when working with social networks, recommendation engines, knowledge graphs, fraud detection systems, or any domain where relationships between entities are as important as the entities themselves.

### Neo4j
Leading graph database platform.
- **Best for:** Connected data, recommendations, knowledge graphs
- **Features:** Cypher query language, ACID compliant, graph algorithms
- **Hosting:** Neo4j Aura, self-hosted
- **Pricing:** Community free, Aura from $65/month
- **Use cases:** Social networks, recommendations, fraud detection

### ArangoDB
Multi-model database (document, graph, key-value).
- **Best for:** Mixed data models in one database
- **Features:** AQL query language, ACID transactions
- **Hosting:** ArangoDB Oasis, self-hosted
- **Pricing:** Open source free, Oasis from $175/month
- **Use cases:** Mixed workloads, microservices

### Amazon Neptune
Fully managed graph database service.
- **Best for:** AWS ecosystem, enterprise graphs
- **Features:** Gremlin and SPARQL support
- **Hosting:** AWS managed only
- **Pricing:** Pay per instance hour
- **Use cases:** Knowledge graphs, identity graphs

## Time-Series Databases

Databases specifically designed for handling time-stamped data with high write throughput and time-based queries. These databases optimize storage and querying for metrics, events, and measurements that change over time. Choose time-series databases when dealing with IoT sensor data, application metrics, financial market data, monitoring and observability systems, or any data where time is the primary axis for queries and aggregations.

### InfluxDB
Purpose-built for time-series data.
- **Best for:** Metrics, events, real-time analytics
- **Features:** Time-series functions, retention policies
- **Hosting:** InfluxDB Cloud, self-hosted
- **Pricing:** Free tier available, paid from $250/month
- **Use cases:** IoT monitoring, DevOps metrics

### TimescaleDB
PostgreSQL extension for time-series.
- **Best for:** Time-series with SQL needs
- **Features:** PostgreSQL compatible, automatic partitioning
- **Hosting:** Timescale Cloud, self-hosted
- **Pricing:** Open source free, cloud from $100/month
- **Use cases:** IoT, monitoring, financial data

### Prometheus
Open-source monitoring system with TSDB.
- **Best for:** Metrics and alerting
- **Features:** Pull model, PromQL, alerting
- **Hosting:** Self-hosted, Grafana Cloud
- **Pricing:** Open source free
- **Use cases:** System monitoring, alerting

## Serverless Databases

Databases that automatically scale compute and storage based on demand, charging only for actual usage. These services eliminate capacity planning and handle all infrastructure management, perfect for variable workloads. Choose serverless databases when building serverless applications, dealing with unpredictable traffic patterns, wanting to minimize operational overhead, or when you need automatic scaling without managing infrastructure.

### Fauna
Globally distributed serverless database.
- **Best for:** Serverless apps, global distribution
- **Features:** ACID transactions, global consistency
- **Pricing:** Free tier, pay-per-use
- **Use cases:** Serverless apps, edge computing

### PlanetScale
Serverless MySQL-compatible database.
- **Best for:** Scalable MySQL without complexity
- **Features:** Branching, non-blocking schema changes
- **Pricing:** Free tier 5GB, paid from $29/month
- **Use cases:** Modern web apps, SaaS

### Neon
Serverless PostgreSQL with branching.
- **Best for:** Development workflows, serverless Postgres
- **Features:** Branching, autoscaling, point-in-time recovery
- **Pricing:** Free tier 3GB, paid from $19/month
- **Use cases:** Development, staging, production

### Upstash
Serverless Redis and Kafka.
- **Best for:** Edge functions, serverless caching
- **Features:** Global replication, REST API
- **Pricing:** Free tier, pay-per-request
- **Use cases:** Edge caching, rate limiting

## Cloud-Native Databases

Databases built from the ground up for cloud environments, offering deep integration with cloud services, automatic scaling, and managed operations. These databases often include additional features like real-time sync, offline support, and integrated authentication. Choose cloud-native databases when building cloud-first applications, needing tight integration with other cloud services, wanting real-time synchronization across clients, or when you prefer fully managed solutions with minimal configuration.

### Firebase Realtime Database
NoSQL cloud database with real-time sync.
- **Best for:** Real-time collaborative apps
- **Features:** Real-time sync, offline support
- **Hosting:** Google Cloud
- **Pricing:** Free tier 1GB, pay-as-you-go
- **Use cases:** Chat apps, collaborative tools

### Firestore
Document database with real-time sync.
- **Best for:** Mobile and web apps
- **Features:** Real-time sync, offline support, queries
- **Hosting:** Google Cloud
- **Pricing:** Free tier generous, pay-per-use
- **Use cases:** Mobile apps, real-time apps

### Azure Cosmos DB
Globally distributed multi-model database.
- **Best for:** Global apps, multiple data models
- **Features:** Multiple APIs, global distribution
- **Hosting:** Azure managed
- **Pricing:** Pay per RU/s
- **Use cases:** Global apps, IoT

### Supabase
Open-source Firebase alternative with PostgreSQL.
- **Best for:** Full-stack apps wanting open source
- **Features:** Real-time, auth, storage, edge functions
- **Pricing:** Free tier 500MB, paid from $25/month
- **Use cases:** SaaS, mobile apps, real-time apps

## Embedded Databases

Lightweight databases that run within your application process rather than as separate servers. These databases are perfect for desktop applications, mobile apps, and embedded systems where you need local data storage without network dependencies. Choose embedded databases when building offline-first applications, desktop or mobile apps, need zero-configuration data storage, or when you want to avoid the complexity of client-server architecture.

### RocksDB
Embeddable persistent key-value store.
- **Best for:** Embedded storage engines
- **Features:** High performance, compression
- **Pricing:** Open source free
- **Use cases:** Storage engines, blockchain

### LevelDB
Fast key-value storage library.
- **Best for:** Embedded applications
- **Features:** Ordered mapping, compression
- **Pricing:** Open source free
- **Use cases:** Chrome browser, Bitcoin Core

### Realm
Mobile database with sync.
- **Best for:** Mobile applications
- **Features:** Object database, sync, encryption
- **Pricing:** Free local, Atlas Device Sync paid
- **Use cases:** Mobile apps, offline-first

## Selection Criteria

Critical factors to evaluate when choosing a database for your application. These criteria help you match data requirements with database capabilities while considering operational complexity and total cost of ownership.

Consider these factors:

- **Data Model:** Structured vs. semi-structured vs. unstructured
- **Query Patterns:** Simple lookups vs. complex queries vs. analytics
- **Consistency:** Strong vs. eventual consistency
- **Scale:** Data size and growth projections
- **Performance:** Latency and throughput requirements
- **Geographic Distribution:** Single region vs. global
- **Development Experience:** Query languages, SDKs, tooling
- **Operational Overhead:** Managed vs. self-hosted
- **Cost Model:** Fixed vs. usage-based pricing
- **Ecosystem:** Integration with other tools and services

---

*Choose a database that fits your data model and query patterns. Start with managed services to reduce operational overhead, and consider migration paths as you scale.*