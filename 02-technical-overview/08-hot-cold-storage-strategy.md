# Hot & Cold Storage Strategy

**Balancing Rapid Access with Long-Term, Cost-Effective Archiving**

Vayu.network's data storage strategy is designed to provide quick, responsive access to recent data for our users and the Vayu Explorer, while securely and cost-effectively archiving our growing historical dataset for long-term analysis.

## Our Multi-Tiered Approach

**1. Hot Storage (PostgreSQL):** All new, validated data points are initially stored in our high-performance PostgreSQL database. We keep approximately one month of data in this "hot" storage layer. This allows for rapid querying, real-time aggregation for the Explorer, and immediate access for any operational needs.

**2. Cold Storage (AWS S3 Glacier):** To manage costs and ensure long-term data preservation, we run a daily data pipeline. This pipeline identifies the oldest partition of data in our PostgreSQL database (e.g., data from 30 days ago) and moves it to AWS S3 Glacier. The data is stored in the efficient Parquet file format, which is ideal for large-scale analytics. This process archives historical data securely while keeping our active database lean and fast.

**3. Decentralized Redundancy (Filecoin):** For an additional layer of security, resilience, and data permanence, we also leverage decentralized storage solutions like Filecoin. By storing backups of our historical data across a distributed, censorship-resistant network, we further protect against data loss and ensure the long-term integrity and availability of our valuable dataset.

This comprehensive storage strategy ensures that our data is managed securely, accessibly, and cost-effectively, providing a reliable foundation for the entire Vayu.network ecosystem. 