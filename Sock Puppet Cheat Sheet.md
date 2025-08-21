# 🧙 Sock Puppet Cheat Sheet — Secure Alias Identity Creation

> ⚠️ **Disclaimer – Educational Use Only**  
> This guide is intended to help individuals protect their privacy, test systems, and manage compartmentalized digital identities in a responsible, legal, and ethical way. It is **not** for deception, fraud, or illegal activity.

---

## Core rule (one line)
Isolate **Device ⇄ Network ⇄ Identity ⇄ Behavior**. Plan objective, threat model, and burn before creation.

---

## One-line SOP (copy / paste)
Isolated device → private network (public access → VPN/ Tor) → puppet email + alias → temp number (only if required) → verify → enable TOTP/hardware key → seed slowly → monitor → burn on schedule.

---

## Top 5 priorities (do these first)
1. OPSEC plan: objective, threat model, accepted risks, burn date, encrypted OPSEC log.  
2. Device separation: physical burner **or** live OS (Tails) / Whonix VM on separate hardware; verify checksums.  
3. Network separation: public Wi-Fi or separate mobile data → optional VPN → Tor for account creation. Never use home/work IPs.  
4. Credentials: ProtonMail/Tutanota + SimpleLogin/AnonAddy aliases; KeePassXC offline vault.  
5. Auth hardening: enable TOTP and/or YubiKey immediately after verification; treat SMS as temporary.

---

## Minimum ordered checklist (execute in sequence)
1. Create OPSEC plan and burn policy.  
2. Prepare isolated device (burner phone or Tails/Whonix VM).  
3. Acquire isolated network access (public Wi-Fi or prepaid mobile data).  
4. Create puppet email + alias, unique password.  
5. Obtain temp number per decision guide and use only for initial SMS.  
6. Verify service, add TOTP/hardware key, remove phone from profile if allowed.  
7. Seed account: 5–15 benign interactions over days to build credibility.  
8. Monitor signals; rotate or burn on schedule.

---

## Temporary phone numbers — decision & practical SOP

**Selection guide (threat → practicality):**
- **High OPSEC:** cash-bought prepaid physical SIM (best separation if lawful).  
- **Moderate OPSEC:** reputable paid burner apps (Hushed, Burner, MySudo) bought anonymously.  
- **Low OPSEC / convenience:** mainstream VoIP (TextNow, Google Voice) — often blocked.  
- **Avoid for serious use:** free public “receive-SMS” websites.

**Acquisition SOP (step-by-step):**
1. Choose method per threat model; log provider and burn date.  
2. **Cash SIM:** buy with cash at unrelated retailer → insert only in burner device → activate over public Wi-Fi or prepaid data. Confirm local legality.  
3. **Burner app:** register on burner device over Tor/VPN → pay with privacy-preserving method (prepaid/ gift card or lawful crypto) → use app only on burner device.  
4. Use number for initial SMS verification only → immediately provision TOTP or register a YubiKey → remove number from profile if possible.  
5. Set lifecycle (30–90 days). Burn: unlink number, delete/neutralize account, factory reset device, destroy SIM.

**Hard rules:** one number per puppet; never link to your real device, identity, or payment method.

---

## Device & network — practical setup
- **Physical burner:** keep solely for puppet; no personal accounts.  
- **Live OS / VM:** Tails (live USB) or Whonix (VM) on isolated hardware; verify images & signatures.  
- **Network flow:** public Wi-Fi / prepaid mobile data → optional VPN → Tor Browser for account actions.  
- **MAC & IDs:** spoof MAC when supported; disable auto backups/auto-connect features.

---

## Email, aliasing & password hygiene
- Use **ProtonMail** or **Tutanota** for puppet email.  
- Use **SimpleLogin** or **AnonAddy** for per-service aliases.  
- Generate long, unique passwords; store in **KeePassXC** (local vault) on the burner device or encrypted removable storage.  
- Immediately enable **TOTP** and/or **YubiKey** after verification; treat SMS as fallback only.

---

## Image & file hygiene — exact commands to run (practical)
- Inspect metadata:
    exiftool image.jpg
- Remove all metadata (overwrite original):
    exiftool -overwrite_original -all= image.jpg
- Remove GPS only:
    exiftool -overwrite_original -gps:all= -xmp:geotag= image.jpg
- Re-render cleaned image: open cleaned file on burner VM and take a screenshot (removes hidden thumbnails/maker notes). Re-check with `exiftool` to confirm.

---

## Behavioral OPSEC — concrete, actionable rules
- **Timing:** post during local hours consistent with puppet timezone; avoid burst posting.  
- **Style:** change sentence length, punctuation, idioms; use a simple style template and vary it.  
- **Social graph:** add a few benign contacts; make small interactions before outreach.  
- **No cross-linking:** never share cloud links, calendar invites, QR codes, or files that can map to your real identity.  
- **Media hygiene:** never upload original phone photos—use AI-generated or licensed images, clean them, then re-render.

---

## Incident response & burn procedure (precise steps)
1. **Contain:** isolate device from networks; revoke sessions via platform controls if possible.  
2. **Audit:** export a minimal encrypted timeline/log for lessons learned (store separate from identifiers).  
3. **Account actions:** change profile data to neutral, then delete account where safe (note: deletion may be delayed or incomplete).  
4. **Device & SIM disposal:** factory reset phone, securely wipe VM images and keys, physically destroy SIM (cut/shred).  
5. **Post-burn verification:** monitor for residual activity or re-linkage attempts; rotate any related credentials.

---

## Templates (copy / paste)

**Puppet checklist (single line):**

PuppetName | Country | City | AgeRange | Email(proton) | Alias(simplelogin) | Number(provider) | 2FA(TOTP/YubiKey) | BurnDate(YYYY-MM-DD)

**Temp-number SOP (single line):**

Buy cash SIM → activate on burner over public Wi-Fi/Tor → verify → enable TOTP/YubiKey → remove phone from profile → set burn date

---

## Recommended toolset (purpose mapped)
- **Anonymity / OS:** Tor Browser; Tails (live USB); Whonix (VM).  
- **Email & aliases:** ProtonMail; Tutanota; SimpleLogin; AnonAddy.  
- **Temp numbers:** Hushed; Burner; MySudo (paid). Avoid free SMS receivers.  
- **Metadata:** ExifTool (CLI).  
- **Passwords:** KeePassXC (offline vault).  
- **2FA / hardware:** YubiKey + Authenticator apps (TOTP).  
- **Guides:** EFF — Surveillance Self-Defense; PrivacyTools.io for threat modeling.

---

## Quick risk & legal notes
- SMS is interceptable and increasingly blocked by platforms; prefer TOTP / hardware keys for ongoing access.  
- SIM registration and purchase laws vary—verify local regulations before buying/activating unregistered SIMs. Consult legal counsel for sensitive or high-risk operations.  
- This guide is defensive; do not use it to commit illegal acts.

---

## Sources & further reading (authoritative starting points)
Tor Project; Tails Project; ProtonMail / Tutanota; SimpleLogin / AnonAddy; Hushed / Burner / MySudo; ExifTool; KeePassXC; Yubico (YubiKey); EFF Surveillance Self-Defense; PrivacyTools.io. (Check official docs for installation, updates and legal constraints.)

---

## Final one-line rule
Plan first, isolate every identifier, use temp numbers only for verification, migrate to TOTP/hardware keys, clean & re-render media, set & execute a burn plan, and operate within the law and platform policies.
```
