# 🏠 Home Network & Office OPSEC Guide (2025 Edition)  
**Privacy, Security & Compartmentalization at Home**

> ⚠️ **Disclaimer – Educational Use Only**  
> This guide is for **personal cybersecurity, privacy defense, and secure home office practices**. It supports ethical use and does not encourage unlawful behavior.

---

## 🎯 Purpose

In 2025, your home is one of your most surveilled and vulnerable environments:
- ISPs log your DNS and activity
- Smart devices can leak data 24/7
- Guests or family members can unknowingly compromise your setup
- Remote work increases exposure of sensitive files and calls

This guide ensures your **home network and office remain secure, compartmentalized, and resistant to leaks** — whether from passive logging, active attack, or behavioral oversights.

---

## 🔐 Core Principles

| Principle | Action |
|----------|--------|
| **Segmentation** | Separate personal, work, and sensitive operations at the network and device level |
| **Hardening** | Secure the router, block outbound tracking, encrypt storage |
| **Monitoring** | Know what's connected and what traffic leaves your network |
| **Minimal trust** | Don’t assume “home = safe”. Design like a hostile network environment |

---

## 🛠️ Router & Network Security

| Task | Notes |
|------|-------|
| **Change default credentials** | Use strong, unique admin passwords. Disable remote management |
| **Firmware updates** | Regularly check for router updates (many don’t auto-update) |
| **Disable WPS, uPnP** | Attack surfaces. Turn them off unless truly needed |
| **Use WPA3 encryption** | Or at minimum WPA2-PSK with strong password |
| **Separate guest Wi-Fi** | Isolate it from LAN access. Use VLAN if possible |
| **Custom DNS** | Use NextDNS, ControlD, or Quad9 instead of ISP DNS |
| **Log monitoring** | Check for unknown devices, excessive outbound traffic

---

## 🧱 Network Segmentation Strategy

| Segment         | Devices |
|-----------------|---------|
| **Main LAN**     | Work PC, home server, printer (if trusted) |
| **Secure VLAN**  | Secure laptop, Tails/Whonix VM host, crypto devices |
| **IoT VLAN**     | Smart TVs, cameras, Alexa, etc – completely isolated |
| **Guest VLAN**   | Visitors, untrusted phones, kids' devices |
| **Air-gapped**   | Devices that should never touch the internet (cold wallets, sensitive backups)

Use a router that supports VLANs (e.g. pfSense, OPNsense, OpenWRT routers, Ubiquiti).

---

## 🔐 Device Security (Home Office Devices)

| Task | Recommendation |
|------|----------------|
| **Full-disk encryption** | Enable on all workstations (FileVault, BitLocker, LUKS) |
| **Separate user accounts** | Never share accounts across family or roles |
| **Camera/mic covers** | Use hardware blockers or tape when not in use |
| **Secure backups** | Use encrypted offline USB or local NAS w/ encryption |
| **Auto-lock timers** | 5 min max on laptops. Require login every time |
| **No personal accounts** | Keep aliases or work profiles off home PCs |

---

## 📡 Smart Device & IoT Hygiene

| Device | Risk | Recommendation |
|--------|------|----------------|
| **Smart TVs** | Voice tracking, ambient data collection | Place on IoT VLAN, disable voice, block internet |
| **Assistants (Alexa, etc)** | Always-on microphones | Don't use, or isolate & monitor traffic |
| **Security cameras** | Cloud access, stream hijack | Use local NVR, VLAN + firewall outbound |
| **Printers** | Known vulnerability vectors | Only connect via USB or secure LAN, never Wi-Fi |
| **Lights, thermostats** | Location/time tracking | Place on IoT VLAN or consider dumb alternatives |

---

## 🔊 Voice, Call & Audio Considerations

- Avoid sensitive calls in rooms with smart devices  
- Use **Noise-cancelling + direction-sensitive microphones**  
- Consider a **Faraday drawer** or shielded box for mobile devices during confidential calls  
- Treat **home assistants as always recording** (because they are)

---

## 🧍‍♂️ Human Habits at Home

| Behavior | OPSEC Tip |
|----------|-----------|
| Letting guests use your devices | Never. Hand them a locked-down guest device or VLAN |
| Leaving devices unlocked | Always lock when stepping away – even at home |
| Mixing personal + work accounts | Separation is safety. Use different browsers or profiles |
| Family accidentally accessing tools | Use app-level PINs, biometric locks, or dual-user setups |
| Sensitive docs visible | Use privacy screens and always clear your desk after use

---

## 📦 Secure Storage at Home

| Item | Storage Option |
|------|----------------|
| **Important files** | Encrypted volume (Veracrypt, LUKS, BitLocker) |
| **USB backups** | Hardware-encrypted drives (e.g. Apricorn, IronKey) |
| **Passwords** | KeePass XC local vaults or offline-only password managers |
| **Documents** | Secure filing cabinet or safe (not fireproof = not secure) |

Bonus: Label drives cryptically, not as "CRYPTO BACKUP" or "TAXES"

---

## 🔄 Routine Maintenance

| Task | Frequency |
|------|-----------|
| Change router/Wi-Fi passwords | Every 3–6 months |
| Review connected devices | Monthly |
| Purge old backups/logs | Every 1–2 months |
| Test backup recovery | Quarterly |
| Reboot network devices | Monthly (flush sessions, rotate IP) |
| Review open ports, firewall rules | Quarterly |

---

## ✅ Home OPSEC Checklist

| Task | Done? |
|------|-------|
| Router locked down, VLANs in use | [ ]  
| Custom DNS and firewall rules active | [ ]  
| IoT devices segmented or isolated | [ ]  
| Devices encrypted and auto-locked | [ ]  
| Smart mics/cams covered or blocked | [ ]  
| Backups encrypted and tested | [ ]  
| Guests use VLAN or temp device only | [ ]  
| Personal/work identities kept separate | [ ]  

---

## 🧭 Final Note

A secure home is more than locks on doors — it’s about **compartmentalization, visibility, and control**.  
Assume your home network is surveilled. Build your systems like you’re on a public Wi-Fi.  
That mindset is your strongest defense.
