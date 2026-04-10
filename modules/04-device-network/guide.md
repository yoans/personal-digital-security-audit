# Module 4: Device & Network Baseline
*Your devices are the edge of your perimeter.*

Strong credentials mean nothing if your device is compromised. A keylogger on your laptop captures your master password before encryption touches it. A compromised router intercepts everything before it reaches your VPN. Start from the hardware you sit on.

**Time required:** 2–4 hours  
**Output:** A device inventory with hardening status; a list of specific fixes

---

## Laptop / Desktop

### Encryption
Full disk encryption ensures that if your device is stolen, the data is unreadable without the PIN/password.

- **Windows:** BitLocker — check status: Start → Settings → Privacy & Security → Device Encryption (or search BitLocker)
- **Mac:** FileVault — check: System Settings → Privacy & Security → FileVault
- Both are on by default on modern hardware, but verify — some OEM Windows installs disable it

### Screen Lock
- Auto-lock after **2 minutes** of idle. More is too long.
- Require password on wake (not just closing the lid)
- Windows: Settings → Personalization → Lock Screen → Screen timeout
- Mac: System Settings → Lock Screen

### OS and Software Updates
- Enable automatic OS updates
- Browser: auto-updates are on by default; verify in settings
- Other software: prioritize anything that touches the internet (email clients, Zoom, etc.) — update within 7 days of a release

### Browser
- Use Firefox or Chrome — both have strong security teams and frequent updates
- **Extensions:** every extension can read your web traffic. Audit now:
  - Chrome: `chrome://extensions/`
  - Firefox: `about:addons`
  - Remove anything you didn't intentionally install or haven't used recently
  - Suspicious? Google it — browser extension malware is common
- Review what's signed in on this browser. Should everything be logged in here?

### Review Auto-Startup Apps
What runs when you start your machine? Anything unfamiliar is worth investigating.
- Windows: Task Manager → Startup tab
- Mac: System Settings → General → Login Items

---

## Phone

### Passcode
- Minimum: 6-digit PIN
- Better: alphanumeric passcode (4-6 words or mixed characters)
- Note: biometric (fingerprint/Face ID) is convenient but courts can compel it; a passcode cannot be compelled in most US jurisdictions

### Encryption
- iOS: encrypted by default with a passcode
- Android 6.0+: encrypted by default; verify in Settings → Security → Encryption

### App Permissions Audit
Review which apps have access to:
- **Location (always on):** Settings → Privacy → Location Services — every "always" is a potential tracking vector
- **Microphone:** Settings → Privacy → Microphone
- **Camera:** Settings → Privacy → Camera
- **Contacts:** Settings → Privacy → Contacts
Remove permissions that don't make obvious sense for what the app does.

### App Purge
Delete apps you haven't opened in 3 months. Dormant apps still run background processes, may still have live permissions, and receive updates that could introduce vulnerabilities.

### Backup
- **iOS:** iCloud backup (encrypted) or local backup via Finder/iTunes (use encrypted backup option)
- **Android:** Google One backup; verify it's actually running
- Verify your backup is current: Settings → [Apple ID] → iCloud → iCloud Backup (or Android equivalent)

---

## Home Router

Your home router is the gateway for every device on your network. Default credentials and unpatched firmware are in most attacker playbooks.

### Change the Admin Password
Factory default admin passwords (often "admin/admin" or printed on the label) are public knowledge.
1. Find your router's admin IP: usually `192.168.1.1` or `192.168.0.1`, or check your network settings for "Default Gateway"
2. Log in with current credentials (check the label if you've never changed them)
3. Change the admin password to a strong, unique one — store it in your password manager

### Update Firmware
Many routers never auto-update. Check your router manufacturer's site or the admin interface for firmware updates. If your router model hasn't had a firmware update in 2+ years — consider replacing it.

### Guest Network
- Enable a separate guest network (most modern routers support this)
- Put all IoT devices (smart speakers, cameras, locks, TVs) on the guest network, not your main network
- This limits lateral movement if an IoT device is compromised — it can't reach your laptop

### Disable WPS
WPS (Wi-Fi Protected Setup) has a known brute-force vulnerability. Disable it in your router admin settings. You don't need it.

### Change the Default SSID
Your SSID (Wi-Fi network name) broadcasts your router model by default (e.g., "NETGEAR_2G"). This tells attackers which vulnerabilities to try. Change it to something that doesn't identify your hardware, carrier, or home address.

---

## IoT Devices

Smart home devices — cameras, speakers, locks, thermostats, TVs, appliances — are consistently the weakest device class. They often ship with weak defaults, receive infrequent updates, and are forgotten once set up.

### Inventory your network
Run a network scanner to see every device connected. Most home users are surprised.
- **Fing** (iOS/Android): easy, clear — [fing.com](https://www.fing.com)
- **Advanced IP Scanner** (Windows, free)
- **nmap** (if you know the command line)

### For each IoT device:
- [ ] Is the default login changed? (If not, do it now — every device has a known default)
- [ ] Is it on the guest/IoT network, not the main network?
- [ ] When did it last receive a firmware update?
- [ ] Does it have a cloud component? (If the company goes under or gets acquired, does it still work? Does it still have access to your network?)

**If a device hasn't had a firmware update in 2+ years and isn't end-of-support by the manufacturer: treat it as potentially compromised.** Consider replacing or isolating it.

---

## VPN

VPNs are useful for specific situations, not a catch-all fix.

**VPNs help with:**
- Public WiFi (coffee shops, airports, hotels) — prevents snooping on open networks
- Hiding your traffic from your ISP
- Accessing geo-restricted content

**VPNs don't help with:**
- Websites you're logged in to — they see your identity regardless
- Malware on your device
- Phishing
- A compromised router on your own network

**Trusted no-log providers (audited):**
- [Mullvad](https://mullvad.net) — anonymous, no account needed, audited, flat-rate
- [ProtonVPN](https://protonvpn.com) — open source, audited, free tier available

Avoid VPNs without published third-party audits.

---

## Device Inventory Table

Build and maintain this:

| Device | Type | OS / Firmware | Encryption On? | Auto-Update? | Network | Last Checked |
|---|---|---|---|---|---|---|
| Personal laptop | Laptop | Windows 11 | ✅ BitLocker | ✅ | Main | 2026-04 |
| iPhone 16 | Phone | iOS 19 | ✅ | ✅ | — | 2026-04 |
| Home router | Router | Netgear v3.2 | — | ❌ | — | Never |
| Ring doorbell | IoT | Unknown | — | Unknown | ⚠️ Main | Never |

---

## Checklist

**Laptop/Desktop:**
- [ ] Full disk encryption verified on
- [ ] Screen lock set to 2 minutes or less
- [ ] Auto-updates on
- [ ] Browser extensions audited
- [ ] Reviewed what's signed in

**Phone:**
- [ ] Alphanumeric passcode or strong PIN
- [ ] App permissions reviewed (location, mic, camera, contacts)
- [ ] Apps not used in 3 months deleted
- [ ] Backup verified as current

**Router:**
- [ ] Admin password changed from default
- [ ] Firmware updated
- [ ] Guest network enabled
- [ ] WPS disabled
- [ ] SSID changed from default

**IoT:**
- [ ] All devices inventoried via network scanner
- [ ] All defaults changed
- [ ] All IoT devices on guest network
- [ ] Devices without recent firmware updates flagged

---

## Tools

| Tool | Use | Link |
|---|---|---|
| Fing | Network device scanner (mobile) | [fing.com](https://www.fing.com) |
| Advanced IP Scanner | Network scanner (Windows) | [advanced-ip-scanner.com](https://www.advanced-ip-scanner.com) |
| Mullvad VPN | Privacy VPN, audited | [mullvad.net](https://mullvad.net) |
| ProtonVPN | VPN with free tier, audited | [protonvpn.com](https://protonvpn.com) |

---

## Agent Prompt
[`agent-prompts/04-device-network.md`](../../agent-prompts/04-device-network.md)

**Next:** [Module 5 — Physical Security](../05-physical-security/guide.md)
