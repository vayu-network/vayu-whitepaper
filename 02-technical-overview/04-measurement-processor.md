# Measurement Processor

<!-- TODO: rewrite this section with accurate details -->
The measurement processing for Vayu.network begins directly on the Flux device. The device's integrated microcontroller unit (MCU) is responsible for polling the air quality sensors and processing the raw data.

The MCU reads data from the Plantower PM sensor and the Renesas ZMOD4410 TVOC/eCO2 sensor. It then combines these readings with a GPS-derived location and a precise timestamp to create a single data packet. This processing happens locally on the device, ensuring that no raw, unprocessed sensor data is transmitted.

### **An Example Of The Payload:**

The resulting data packet is a clean JSON object, ready for transmission to the mobile app via BLE.

```json
{
  "location": {
    "latitude": 40.7128,
    "longitude": -74.0060
  },
  "timestamp": "2024-10-26T10:00:00Z",
  "sensors": {
    "pm25": 12.5,
    "tvoc": 150.0,
    "eco2": 450.0
  }
}
```

This onboard processing is a key part of our architecture. By handling the initial data aggregation on the device itself, we ensure a consistent data format across the entire network and prepare the data for the next stages of validation and anonymization in the backend. 