# Anomaly Detection Engine

**A Multi-Faceted Approach to Filtering Invalid Data**

To protect the integrity of the Vayu.network dataset, we employ a sophisticated, multi-layered anomaly detection engine. This system runs continuous checks to filter out invalid data, whether from malfunctioning sensors or malicious actors attempting to defraud the system.

## User & Device Validation

*   **Account Uniqueness:** Standard checks are in place to prevent single users from creating multiple accounts, including monitoring for overlapping IP addresses or device identifiers.
*   **Secure Authentication:** Users will be required to use secure login methods to access their accounts.
*   **Hardware Attestation:** In future firmware versions, we plan to implement a cryptographic attestation system where each Flux device can prove its authenticity to the network, making it extremely difficult to spoof hardware.

## Measurement Integrity

*   **Logical Sensor Values:** The system flags sensor readings that are physically improbable (e.g., negative PM2.5 values, extreme and sudden spikes inconsistent with environmental context).
*   **Cross-Sensor Correlation:** Data from the PM2.5, TVOC, and eCO2 sensors are analyzed for expected correlations. For example, a sudden spike in PM2.5 without a corresponding change in other sensors might be flagged for review.
*   **Environmental Context:** Data is cross-referenced with known environmental data. A sensor reporting high pollution in an area known to have clean air (or vice-versa) would be flagged.

## Location & Movement Analysis

*   **GPS Spoofing Prevention:** The system analyzes location data for signs of spoofing. This includes checking for physically impossible "jumps" in location, movement patterns that are too perfect (e.g., perfect straight lines or circles), and speeds that are inconsistent with human behavior (e.g., a device that is always moving at a constant speed).
*   **Stationary Device Detection:** While stationary measurements are valuable, the system is designed to detect if a device is attempting to earn rewards by reporting the same location data for extended, unrealistic periods.
*   **Indoor/Outdoor Plausibility:** GPS data is analyzed to determine the likelihood that a device is actually indoors, as claimed.

## Community & AI Oversight

*   **Community Flagging:** The Vayu Explorer will feature a system for community members to anonymously flag data points that appear suspicious, adding a crucial layer of human oversight.
*   **AI-Driven Analysis:** Beyond these explicit rules, our system uses machine learning models to identify complex patterns and novel anomalies that may indicate sophisticated fraud attempts.

These safeguards, combined with an active moderation team, help us maintain a healthy and trustworthy data ecosystem where genuine contributors are rewarded and the dataset remains valuable for everyone. 