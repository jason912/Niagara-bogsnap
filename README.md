# Niagara-bogsnap 📸

[![Niagara 4.14+](https://img.shields.io/badge/Niagara-4.14%2B-blue)](https://www.tridium.com)
[![License: Free](https://img.shields.io/badge/License-Free-brightgreen)](LICENSE)
[![Contact](https://img.shields.io/badge/Contact-WhatsApp-brightgreen)](https://wa.me/8613801909968)

> **Capture a real-time snapshot of your Niagara station's program state — with values, status, and alarms.**

---

## What Is It?

BogSnap takes a point-in-time snapshot of your Niagara station's program logic and saves it as a `.bog` file. Open it in Workbench to review exactly what the station was doing at that moment — program connections, point values, status conditions (OK, alarm, fault, down, stale), and platform service info.

### Typical Use Case

An alarm triggers → BogSnap automatically saves the program logic + real-time point data → emails the `.bog` file to the maintenance engineer → engineer analyzes the snapshot remotely without visiting the JACE.

---

## Quick Start

```bash
# 1. Install gline.pem certificate into your station trust store

# 2. Add bogSnap-rt.jar to your modules/ directory

# 3. Restart station

# 4. Drag a BogSnap component into your wiresheet

# 5. Configure the target folders to snapshot

# 6. Trigger → .bog files are exported to your configured folder

# 7. Open .bog files in Workbench to review
```

---

## Tested Networks

| Network | Status |
|---------|:------:|
| MQTT Network | ✅ |
| BACnet Network | ✅ |
| Modbus Network | ✅ |
| SNMP Network | ✅ |
| oBIX Network | ✅ |
| Niagara Network | ❌ (password-protected) |

### Known Limitations

- **Alarm console** — real-time alarm info is lost during conversion
- **History data** — cannot be converted to .bog format
- **PX files** — cannot be converted to .bog format

---

## Requirements

| Component | Requirement |
|-----------|-------------|
| **Niagara** | 4.14 or later |
| **JAR signing** | Requires gline.pem certificate |

---

## Documentation

| Manual | Description |
|--------|-------------|
| [BogSnap User Manual](docs/BogSnap_UserManualEN.pdf) | Complete user manual |

---

## Support & Contact

- **Email**: [jason.zhang@gline-net.com](mailto:jason.zhang@gline-net.com)
- **WhatsApp**: [+86 138 0199 0968](https://wa.me/8613801909968)

**Shanghai Gline Net Co., Ltd.** — Your Partner in Smarter Automation

---

© 2026 Shanghai Gline Net Co., Ltd. All rights reserved.
