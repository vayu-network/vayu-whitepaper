# Vayu Explorer

**Visualizing the World's Indoor Air Quality**

The Vayu Explorer is the public-facing window into the Vayu.network. It is a powerful, interactive map that visualizes the vast amount of indoor air quality data collected by the global fleet of Flux devices, making this once-invisible data accessible and understandable to everyone.

## The Indoor Air Quality Map

### Data Pipeline & H3 Hexagon Aggregation

Vayu.network uses a sophisticated data pipeline that continuously streams validated measurements from our primary database. This pipeline processes the data, aggregating individual data points into H3 hexagons at various resolutions. For each hexagon, it calculates and regularly updates the average levels of PM2.5, TVOC, and eCO2, storing them in a dedicated database that powers the Explorer.

The air quality levels are categorized using a simple, color-coded system to provide an at-a-glance understanding of the environment. While the exact thresholds will be refined based on scientific standards (like those from the WHO and EPA), the classification will be similar to this:

*   **Green:** Good
*   **Yellow:** Moderate
*   **Orange:** Unhealthy for Sensitive Groups
*   **Red:** Unhealthy
*   **Purple:** Very Unhealthy
*   **Maroon:** Hazardous

## Interactive Map Features

### Filtering and Sorting

The Vayu Explorer is designed to be a powerful tool for discovery. Users will be able to filter and sort the map data based on several criteria:

*   **Location Search:** Users can search for any address, city, or point of interest to see the indoor air quality data in that area.
*   **Data Layers:** Users can switch between different data layers to visualize PM2.5, TVOC, or eCO2 levels independently.
*   **Time Frame:** The explorer will allow users to view data across different time scales, from a "live" view of the last 24 hours to historical trends over the past week, month, or year.
*   **Location Type (Future):** As our dataset grows, we aim to introduce filtering by location type (e.g., residential, office, commercial) based on aggregated, anonymized data patterns.

The Vayu Explorer transforms raw, complex sensor readings into actionable, easy-to-understand insights, empowering individuals, researchers, and businesses to make healthier decisions about their indoor environments. 