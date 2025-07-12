# IDS and IPS
IDS (Intrusion Detection System): Detects suspicious activities and alerts the administrator.

IPS (Intrusion Prevention System): Detects and blocks threats in real time.

### Types:
- Network-based (NIDS/NIPS)
    - Monitors entire network traffic.
- Host-based (HIDS/HIPS)
    - Monitors activities on individual hosts.

### Detection Techniques:
- Signature-based: Uses known attack patterns.
- Anomaly-based: Detects deviations from normal behavior.
- Hybrid: Combines both methods.

| Feature  | IDS             | IPS                  |
| -------- | --------------- | -------------------- |
| Action   | Alerts only     | Blocks & alerts      |
| Position | Passive         | Inline (active)      |
| Risk     | No interruption | May block legitimate |

### Limitations:
- False positives/negatives.
- Needs regular updates.

