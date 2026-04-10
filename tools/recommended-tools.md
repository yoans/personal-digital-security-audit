# Recommended Tools
*Project Chrysalis — curated tools by category*

Every tool listed here is either free, open source, independently audited, or clearly the best option in its category. Paid options are noted. No affiliate relationships.

Last reviewed: April 2026

---

## Password Managers

| Tool | Cost | Open Source? | Audited? | Self-host? | Notes |
|---|---|---|---|---|---|
| **[Bitwarden](https://bitwarden.com)** | Free / $10/yr | ✅ | ✅ | ✅ | **Recommended.** Best balance of security, UX, and portability. Free tier is sufficient for most users. |
| **[1Password](https://1password.com)** | $3/mo | ❌ | ✅ | ❌ | Excellent UX, strong security model, great family plan. Closed source but well-audited. |
| **Apple Keychain** | Free | ❌ | ❌ | ❌ | Acceptable if fully in Apple ecosystem. Does not support passkeys on all platforms. Ties you to Apple as a hub. |
| **KeePass / KeePassXC** | Free | ✅ | ✅ | Local only | Best for users who want local-only storage with no cloud sync. Steeper setup curve. |
| ~~LastPass~~ | — | — | — | — | **Avoid.** Encrypted vaults were stolen in 2022; weak iterations made many vaults crackable. |

**Recommendation:** Bitwarden if you use multiple platforms. 1Password if you prioritize UX and family sharing. KeePassXC if you want zero cloud.

---

## Authenticator Apps (TOTP)

| Tool | Platform | Open Source? | Encrypted Backup? | Notes |
|---|---|---|---|---|
| **[Ente Auth](https://ente.io/auth)** | iOS, Android, Desktop | ✅ | ✅ E2E | **Recommended.** Encrypted backup to their server or self-hosted. Best backup story of any TOTP app. |
| **[Aegis](https://getaegis.app)** | Android only | ✅ | ✅ Local | Strong, reliable, audited. Export/import support. No cloud sync — backup manually. |
| **[Raivo OTP](https://raivo-otp.com)** | iOS only | ✅ | ✅ iCloud | Open source iOS option. iCloud backup (encrypted). |
| **2FAS** | iOS, Android | ✅ | ✅ | Clean UX, cross-platform, good backup. |
| ~~Google Authenticator~~ | — | — | ❌ | Google Authenticator now syncs to Google account — no independent encryption. Keys are accessible to Google. |
| ~~Microsoft Authenticator~~ | — | — | Unclear | Closed source; backup encryption unaudited. |
| ~~Authy~~ | — | — | ❌ | Closed source. Backup keys are accessible on their servers. Not recommended for sensitive accounts. |

---

## Hardware Security Keys (FIDO2 / Passkey)

| Product | Price | NFC? | USB-A | USB-C | Notes |
|---|---|---|---|---|---|
| **[YubiKey 5 NFC](https://www.yubico.com/product/yubikey-5-nfc/)** | ~$55 | ✅ | ✅ | ❌ | **Most widely compatible.** Works with almost all services that support hardware keys. |
| **[YubiKey 5C NFC](https://www.yubico.com/product/yubikey-5c-nfc/)** | ~$55 | ✅ | ❌ | ✅ | Same as above; USB-C for modern laptops. |
| **[Google Titan Key](https://store.google.com/us/category/google-titan-security-key)** | ~$30 | ✅ | ✅ | ✅ | Cheaper. Fewer supported protocols but covers major services. |
| **[OnlyKey](https://onlykey.io)** | ~$48 | ❌ | ✅ | ❌ | Open source hardware and firmware. Supports FIDO2 + additional features. |

**Buy two keys.** Register both on each critical service before relying on either. Keep one accessible and one stored securely.

---

## Breach Monitoring

| Tool | Free? | Monitors passively? | Notes |
|---|---|---|---|
| **[HaveIBeenPwned](https://haveibeenpwned.com)** | ✅ | ✅ (with free account) | The standard. Check all your email addresses. Enable notifications. |
| **[Firefox Monitor](https://monitor.mozilla.org)** | ✅ | ✅ | Powered by HIBP; clean UI, dashboard. |
| **[Bitwarden built-in](https://bitwarden.com)** | ✅ (premium feature) | ✅ | Checks your vault passwords against breach databases. Worth the $10/yr premium. |

---

## Data Broker Removal

| Tool | Cost | Brokers Covered | Notes |
|---|---|---|---|
| **[Incogni](https://incogni.com)** | ~$70/yr | 180+ | **Recommended for most users.** Good coverage, transparent reporting, automated re-removal. |
| **[DeleteMe](https://joindeleteme.com)** | ~$130/yr | 750+ | More thorough, human-verified, quarterly reports. Worth the higher cost for high-exposure individuals. |
| **[Kanary](https://www.kanary.com)** | ~$90/yr | 200+ | Strong monitoring and alerts when you reappear. |
| **Manual opt-outs** | Free | All | Time-consuming but free. Use [JustDeleteMe](https://justdeleteme.com) as a starting point. |

**Start with manual opt-outs on the top 5–10 brokers.** If your exposure is medium or high (found on 3+ brokers), an automated service is worth the cost.

---

## Network Scanning

| Tool | Platform | Free? | Notes |
|---|---|---|---|
| **[Fing](https://www.fing.com)** | iOS, Android | ✅ | **Recommended.** Fast, clear, shows device names and types. Best for home network inventory. |
| **[Advanced IP Scanner](https://www.advanced-ip-scanner.com)** | Windows | ✅ | Good Windows option. Shows MAC addresses, open ports. |
| **[nmap](https://nmap.org)** | All platforms | ✅ | Command-line. Most powerful. Requires familiarity with the tool. |
| **[LanScan](https://www.iwaxx.com/lanscan/)** | macOS | ✅ | Simple, clean macOS option. |

---

## VPN

| Tool | Cost | Audited? | Logs? | Notes |
|---|---|---|---|---|
| **[Mullvad](https://mullvad.net)** | ~$5/mo | ✅ | ❌ No logs | **Recommended.** Anonymous accounts (no email required to sign up). Flat-rate, audited. |
| **[ProtonVPN](https://protonvpn.com)** | Free / $10/mo | ✅ | ❌ No logs | Free tier is genuinely usable. Swiss-based. Same org as ProtonMail. |
| **[IVPN](https://www.ivpn.net)** | ~$6/mo | ✅ | ❌ No logs | Less known but excellent; also supports anonymous accounts. |
| Any VPN without a published third-party audit | — | ❌ | Unknown | **Avoid.** "No logs" claims without audits are unverifiable. |

**Reminder:** A VPN is useful for public WiFi and ISP privacy. It doesn't protect you from a compromised device, phishing, or misconfigurations.

---

## Email Aliasing

| Tool | Free Tier? | Open Source? | Notes |
|---|---|---|---|
| **[SimpleLogin](https://simplelogin.io)** | ✅ (10 aliases) | ✅ | **Recommended.** Aliases forward to your real address. Widely used, solid. Now part of Proton. |
| **[Addy.io (formerly AnonAddy)](https://addy.io)** | ✅ | ✅ | Generous free tier. Good API for power users. |
| **Apple Hide My Email** | ✅ (iCloud+) | ❌ | Convenient within Apple ecosystem. Limited to Apple-signed-in browsers/apps. |
| **Fastmail aliases** | Paid | ❌ | Good if you already use Fastmail. Clean integration. |

---

## Identity OSINT Tools

| Tool | Use | Cost | Notes |
|---|---|---|---|
| **[HaveIBeenPwned](https://haveibeenpwned.com)** | Email breach check | Free | Run every email address you've ever used |
| **[WhatsMyName](https://whatsmyname.app)** | Username search across ~600 platforms | Free | Web-based, no install |
| **[Sherlock](https://github.com/sherlock-project/sherlock)** | Username search (command-line) | Free, open source | More comprehensive than WhatsMyName; requires Python |
| **[TinEye](https://tineye.com)** | Reverse image search | Free / paid | Find where your photo appears online |
| **[Google Images](https://images.google.com)** | Reverse image search | Free | Drag image in; broader index than TinEye |

---

## Credit & Identity Monitoring

| Service | Cost | What It Does | Notes |
|---|---|---|---|
| **[AnnualCreditReport.com](https://www.annualcreditreport.com)** | Free | Full credit reports from all 3 bureaus | Check all three quarterly |
| **Experian free monitoring** | Free | Alerts on changes to Experian report | Useful baseline |
| **[Credit Karma](https://www.creditkarma.com)** | Free | Monitoring on TransUnion and Equifax | Good free monitoring; ad-supported |
| Paid credit monitoring | $15–40/mo | Wider monitoring, identity theft insurance | Often included with credit cards — check yours |

**Credit freezes are free and more protective than monitoring.** See Module 5. Monitor AND freeze — they serve different purposes.

---

## Physical Security

| Product | Purpose | Approx Cost |
|---|---|---|
| **Micro-cut shredder** | Document destruction | $80–150 |
| **Cross-cut shredder** | Document destruction (minimum acceptable) | $30–50 |
| **Fireproof document bag or safe** | Physical document storage | $30–200 |
| **USB data blocker (PortaPow)** | Block data on public USB charge ports | $10 |
| **Laptop privacy screen filter** | Block shoulder surfing | $20–40 |
| **Kensington cable lock** | Deter opportunistic laptop theft | $30–50 |

---

*Tools added or updated? Open a PR or issue. Tool landscape changes — keeping this current matters.*
