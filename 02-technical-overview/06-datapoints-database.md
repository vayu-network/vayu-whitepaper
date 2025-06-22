# Datapoints Database

Once a data packet from a Flux device has been successfully validated by our anomaly detection engine, the reliable measurement is passed on to our core datapoints database.

This database is the central, trusted repository for all valid air quality measurements collected by the network. From here, several asynchronous processes are initiated:

*   **Data Aggregation:** The individual data points are aggregated into larger geographical units using the H3 hexagonal system. This process calculates average PM2.5, TVOC, and eCO2 levels for each hexagon, which is essential for visualizing data on the Vayu Explorer and for providing meaningful insights through our API.
*   **Data Archiving:** After a set period, the raw, validated data points are moved from the active database to a long-term, cost-effective cold storage solution. This ensures we have a complete historical archive for future analysis while keeping the active database optimized for performance. 