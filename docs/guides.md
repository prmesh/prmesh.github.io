# 📡 Recommended Configuration Settings for Puerto Rico Mesh

To help maintain a **healthy and stable Meshtastic mesh network** across Puerto Rico, we recommend the following configuration settings for your devices.

These settings are based on the collective experience of this community and best practices shared by others like Mountain Mesh. They’re meant to keep traffic clean, extend battery life, and improve long-range communications.

> ⚠️ These recommendations may evolve as the network grows.

---

## 🛰️ Radio Configuration

### 🔧 Device Settings

| Option                   | Recommended Value         | Notes                                                                                          |
|--------------------------|---------------------------|------------------------------------------------------------------------------------------------|
| **Role**                 | `CLIENT` or `CLIENT_MUTE` | `CLIENT_MUTE` is ideal for listen-only nodes. See [Deployment Scenarios](https://youtu.be/htjwtnjQkkE) |
| **Node Info Interval**   | `10800` (every 3 hours)   | Reduces network traffic while still providing basic visibility.                               |

---

### 📍 Position Settings

| Option                    | Recommended Value      | Notes                                                             |
|---------------------------|------------------------|-------------------------------------------------------------------|
| **Smart Positioning**     | `True`                 | Devices will use GPS if available, fallback otherwise.            |
| **Broadcast Interval**    | `3600` (every hour)    | Helps update nearby nodes without flooding the network.           |
| **GPS Update Interval**   | `1800` (every 30 mins) | Useful for mobile nodes.                                          |
| **Position Flags**        | Disable unused flags   | Fixed nodes should disable all unnecessary position flags.        |

---

### 📶 LoRa Radio

| Option            | Recommended Value | Notes                                                                 |
|-------------------|-------------------|----------------------------------------------------------------------|
| **Hop Limit**     | `5`               | Avoid increasing beyond `6`. Keeps routing sane and efficient.       |
| **Ignore MQTT**   | `True`            | Useful for routers in isolated areas or avoiding MQTT echo.          |
| **OK to MQTT**    | `True`            | Enable if you want your node to appear on tools like [MeshMap.net](https://meshmap.net) |

---

## 🧩 Module Configuration

### 📊 Telemetry

| Option                           | Recommended Value | Notes                                                               |
|----------------------------------|-------------------|---------------------------------------------------------------------|
| **Device Metrics Interval**      | `3600` (1 hour)   | Use `1800` for testing new node behavior.                           |
| **Environment Metrics Interval** | `3600` (1 hour)   | Can be disabled if not using environmental sensors.                 |
| **Power Metrics Enabled**        | `False`           | Only needed for I²C-based external sensors, not built-in voltage.   |

> 🔌 Disable unused telemetry modules to conserve bandwidth and power.

---

### 🧭 Neighbor Info

| Option              | Recommended Value |
|---------------------|-------------------|
| **Neighbor Info**   | `False`           |

This module has limited utility in recent firmware versions. Disable unless needed for debugging.

---

## ℹ️ Want to Learn More About Meshtastic?

Visit the official Meshtastic site for detailed docs, firmware updates, and community links:

👉 [meshtastic.org](https://meshtastic.org)

---

_This guide is community-maintained. If you spot outdated info or want to suggest an improvement, reach out to us!_
