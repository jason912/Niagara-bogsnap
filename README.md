# Niagara-bogsnap 📸

[![Niagara 4.14+](https://img.shields.io/badge/Niagara-4.14%2B-blue)](https://www.tridium.com)
[![License: Free](https://img.shields.io/badge/License-Free-brightgreen)](LICENSE)
[![Contact](https://img.shields.io/badge/Contact-WhatsApp-brightgreen)](https://wa.me/8613801909968)

> **Capture a real-time snapshot of your Niagara station's program state — with live values, status, and alarms. Milliseconds, not minutes.**

---

## Why BogSnap vs Station Backup?

| | BogSnap ✅ | Traditional Station Backup ❌ |
|:--|:----------:|:----------------------------:|
| **Speed** | **Milliseconds** (< 100ms) | **Seconds to minutes** |
| **Real-time data** | ✅ Captures live values in JACE memory | ❌ Only saves persisted data |
| **CPU impact** | Negligible | Heavy — full station freeze during backup |
| **Target** | Specific program folders | Entire station |
| **Trigger** | On alarm / on demand | Manual or scheduled |
| **Output** | `.bog` — open in Workbench instantly | `.dist` — requires restore to view |

### The Problem

When an alarm fires, you need to know what the station was doing **at that exact moment** — point values, status flags (OK / alarm / fault / down / stale), program logic flow. A traditional station backup takes **30 seconds to several minutes**, by which time:

- The real-time values have changed
- The transient fault condition has cleared
- You've lost the evidence you needed to diagnose the root cause

### The BogSnap Solution

BogSnap captures the program state in **under 100 milliseconds** — triggered automatically by the alarm itself. The resulting `.bog` file contains:

- Program logic exactly as it was wired
- Live point values at the moment of capture
- Point status conditions (OK, alarm, fault, down, stale)
- Platform service information

The maintenance engineer opens the `.bog` in Workbench remotely — no site visit required.

---

## Quick Start

```bash
# 1. Install gline.pem certificate into your station trust store

# 2. Add bogSnap-rt.jar to your modules/ directory

# 3. Restart station

# 4. Drag a BogSnap component into your program

# 5. Configure target folders to snapshot

# 6. Trigger → .bog files exported to your configured folder

# 7. Open .bog files in Workbench — full logic + values + status
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
| Niagara Network | ❌ (password-protected, snapshot export blocked) |

### Known Limitations

- **Alarm console** — real-time alarm info is lost during conversion
- **History data** — cannot be converted to `.bog` format
- **PX files** — cannot be converted to `.bog` format

---

## Requirements

| Component | Requirement |
|-----------|-------------|
| **Niagara** | 4.14 or later (JACE, Edge, Supervisor) |
| **JAR signing** | Requires gline.pem certificate |

---

## Documentation

| Manual | Description |
|--------|-------------|
| [BogSnap User Manual](docs/BogSnap_UserManualEN.pdf) | Complete usage guide |

---

## Support & Contact

- **Email**: [jason.zhang@gline-net.com](mailto:jason.zhang@gline-net.com)
- **WhatsApp**: [+86 138 0199 0968](https://wa.me/8613801909968)

**Shanghai Gline Net Co., Ltd.** — Your Partner in Smarter Automation

---

© 2026 Shanghai Gline Net Co., Ltd. All rights reserved.
