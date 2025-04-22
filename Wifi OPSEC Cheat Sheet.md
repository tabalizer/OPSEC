# 📡 Wi-Fi Tracking & Metadata Leakage Guide

> ⚠️ **Disclaimer – Educational Use Only**  
> This content is for **educational and informational purposes**. It is designed to help users protect their privacy and defend against digital surveillance. It is **not** a guide for evading lawful monitoring or engaging in illegal activity. Use responsibly and legally.

---

## 🎯 Purpose

Wi-Fi is a massive privacy risk — even when you're not connected. Devices constantly **broadcast identifiers**, **probe for known networks**, and **leak movement patterns**. This guide shows how to **detect**, **block**, and **mitigate** those risks.

---

## 🚨 Key Wi-Fi Risks

| Threat | Description |
|--------|-------------|
| **Passive Tracking** | Devices broadcast probe requests looking for known networks ("Home Wi-Fi", "CafeXYZ"). Observers can track movement based on this. |
| **MAC Address Logging** | Your device’s unique MAC can be logged at airports, malls, or by adversaries for movement correlation. |
| **Hotspot Impersonation** | Attackers set up fake hotspots with familiar names (e.g., "Starbucks Free WiFi") to intercept connections. |
| **Metadata Leakage** | Even encrypted traffic leaks timestamps, DNS requests, and device identifiers. |
| **Auto-Connect Dangers** | Devices can silently join known networks without consent, exposing you to MITM attacks. |

---

## 🧱 Countermeasures

### ✅ **1. Keep Wi-Fi Off When Not in Use**
- Manually disable Wi-Fi in **Settings**, not just the Control Center (especially on iOS).
- Avoid "smart" auto-connect features unless critically needed.
- Use **Airplane Mode** with Wi-Fi disabled to ensure full radio silence.

### ✅ **2. Use Private MAC Addressing**
- Modern phones randomize MAC per network. **Ensure it’s on**:
  - iOS: Settings > Wi-Fi > [Network] > Private Wi-Fi Address → Enabled
  - Android: Varies, but usually under Wi-Fi > Network > Privacy > Random MAC
- For sensitive use, **forget all saved networks** and never reuse SSIDs.

### ✅ **3. Clear Out Saved Networks**
- Devices constantly search for saved SSIDs. Purge your list:
  - iOS: Reset Network Settings (Settings > General > Transfer/Reset > Reset Network Settings)
  - Android: Manually forget or use system reset

### ✅ **4. Avoid Public Wi-Fi**
- If you must use it:
  - Always tunnel traffic through a **reliable VPN**
  - Avoid entering passwords or accessing sensitive services
  - Disable **Auto-Join** after use

### ✅ **5. Rotate Device Identifiers**
- Change device name:  
  iOS: Settings > General > About > Name → Set to “Phone” or similar  
  Android: Settings > About Phone > Device Name

### ✅ **6. Monitor Device Activity**
- Use built-in **App Privacy Reports** (iOS) or **NetGuard/TrackerControl** (Android) to detect background connections
- Consider using **Faraday bags** to block all signals when physical OPSEC is required

---

## 🔧 Advanced Options

| Tool/Method | Function |
|-------------|----------|
| **WiFi Analyzer** | Scan nearby networks, detect rogue access points (Android only) |
| **Wireshark** | Capture traffic over known networks for anomaly detection |
| **Kismet** | Detect devices probing for SSIDs and analyze signal behavior (Linux) |
| **Faraday Bag** | Hardware solution — blocks all RF signals, including Wi-Fi |

---

## 🚩 Real-World Use Cases

| Scenario | Risk | Mitigation |
|----------|------|------------|
| **Crossing borders** | Phone probes for “Home Wi-Fi” | Reset network settings before entry |
| **Attending protest** | Passive MAC logging | Random MAC + Wi-Fi off |
| **Using hotel Wi-Fi** | Rogue DHCP / MITM risk | VPN + custom DNS |
| **Running aliases** | Device name reveals real identity | Use neutral device name like “iPhone” |

---

## 🧼 Routine Hygiene Checklist

- [ ] Wi-Fi off unless actively needed  
- [ ] MAC randomization on  
- [ ] Device name anonymized  
- [ ] Saved networks cleared monthly  
- [ ] VPN always-on for Wi-Fi use  
- [ ] Check app activity reports  

---

## 🧭 Final Advice

If you’re serious about OPSEC:
- Use **mobile data + VPN** whenever possible.
- Treat all public Wi-Fi as **hostile**.
- Wi-Fi is never “just connectivity” — it’s **a location tracker**, **a behavioral map**, and **a fingerprint**.

---
