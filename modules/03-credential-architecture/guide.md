# Module 3: Credential & Access Architecture
*Not just "use a good password manager."*

The vendor matters less than the architecture. How your credentials are organized, backed up, and recoverable determines whether you can survive a breach, or a forgotten master password. This module builds a system.

**Time required:** 2-3 hours to set up; ongoing maintenance is minimal  
**Output:** A working credential system with no single points of failure

---

## Password Manager

You need one. Browser password storage is not a password manager, it's a convenience feature with weak encryption and no portable backup.

**Recommended:**

| Manager | Why | Cost |
|---|---|---|
| **Bitwarden** | Open source, independently audited, generous free tier, self-hostable, passkey support | Free / $10/yr premium |
| **1Password** | Excellent UX, strong security model, good for families | $3/mo |
| **Apple Keychain** | Convenient if fully in Apple ecosystem, acceptable, but ties you to Apple as a hub | Free |

**Avoid:**
- LastPass, multiple breaches including encrypted vault theft; slow, insufficient response
- Browser-only storage (Chrome, Firefox built-in), not portable, no 2FA on the vault itself
- Reusing passwords, one breach exposes everything

**What your password manager must do:**
- Encrypt the vault locally before syncing (zero-knowledge)
- Support 2FA on the vault login itself
- Allow export and backup
- Run on all your devices

---

## 2FA Hierarchy

Use the strongest available method. From best to worst:

| Method | Phishing Resistant? | SIM Swap Resistant? | Notes |
|---|---|---|---|
| **Hardware key (FIDO2/passkey)** | ✅ Yes | ✅ Yes | Best. Requires physical key. |
| **Authenticator app (TOTP)** | ❌ No | ✅ Yes | Good. Real-time codes. |
| **TOTP in password manager** | ❌ No | ✅ Yes | Convenient, but merges vault + 2FA into one target |
| **Email OTP** | ❌ No | Depends | Use only as fallback |
| **SMS** | ❌ No | ❌ No | Avoid on anything important |

**Phishing resistant** means the 2FA cannot be intercepted by a fake login page, FIDO2/hardware keys verify the actual domain cryptographically.

**Authenticator app recommendations:**
- **Ente Auth:** open source, encrypted backup, works offline, top pick
- **Aegis** (Android only), open source, good backup options
- **Raivo** (iOS only), open source
- Avoid Google Authenticator and Microsoft Authenticator for portability/backup reasons unless you've verified their backup encryption

---

## Hardware Keys (FIDO2 / YubiKey)

A hardware key is a physical USB/NFC device. To log in, you insert it and touch it. It cannot be phished, it verifies the actual domain you're on before signing.

**When to use:** On your most critical hub accounts, email, password manager, financial accounts.

**Getting started:**
- Buy two keys (one primary, one backup stored securely). Don't have only one.
- Compatible with Google, Apple, Microsoft, GitHub, Bitwarden, Coinbase, many banks
- Register both keys on each service before relying on them
- [Yubico](https://www.yubico.com) YubiKey 5 NFC is the most widely supported option ($55)

---

## Passkeys

Passkeys are the FIDO2 standard implemented into app and web logins. They're phishing-resistant by design and are becoming the default on major platforms.

**Adopt passkeys everywhere they're offered.** When a service offers "sign in with passkey," take it.

**Where to store passkeys:**
- Your password manager (Bitwarden, 1Password), portable, not locked to a device
- Apple Keychain, Google Password Manager, convenient but platform-tied

---

## Emergency Access Kit

This answers: *"If I'm incapacitated or dead, can someone I trust access what they need?"* and *"If I forget my master password, can I recover without losing everything?"*

**The kit contains:**
- Your password manager name and account email
- A hint for your master password (NOT the password itself, a hint only you and your trusted person would understand)
- Location of your hardware keys
- Recovery codes for: primary email, authenticator app, password manager
- Your critical account list (service names and usernames, no passwords)
- Step-by-step instructions for what to do first in an emergency
- Your carrier PIN (masked or split)

**Storage:**
- One physical copy: fireproof container or with your attorney
- One encrypted digital copy: stored separately from your main vault (a second encrypted drive, a trusted attorney, a sealed letter in safe deposit box)

**Never:** store the emergency kit in the same place or vault it's meant to recover access to.

---

## Breach Response Protocol

When a service you use announces a data breach:

1. **Change the password for that service immediately:** don't wait for the service to force it
2. **Check if you reused that password anywhere:** if yes, change it everywhere
3. **Enable 2FA on that service if not already on**
4. **Check HaveIBeenPwned** to see if your email shows up in the specific breach
5. **Monitor connected accounts:** if the breached service was used for SSO anywhere, check those accounts for unusual activity over the next 30 days
6. **Watch for phishing:** breach victims are immediately targeted with follow-on phishing using data from the breach

---

## Checklist

**Immediate:**
- [ ] Password manager installed and active on all devices
- [ ] All new passwords generated by the manager (random, 20+ characters)
- [ ] 2FA enabled on password manager vault login
- [ ] 2FA enabled on primary email
- [ ] 2FA enabled on all hub accounts (from Module 2)
- [ ] SMS 2FA removed from hub accounts and replaced with app or hardware key

**Short-term:**
- [ ] Authenticator app selected and installed
- [ ] All TOTP codes migrated to authenticator app
- [ ] Backup codes for all hub accounts generated and stored
- [ ] Hardware key ordered and registered on critical accounts (both primary and backup)
- [ ] Emergency Access Kit created and stored securely

**Ongoing:**
- [ ] New account? Unique password from manager. 2FA on.
- [ ] Breach announced? Protocol above.
- [ ] Quarterly: check for accounts still using SMS 2FA or reused passwords

---

## Tools

| Tool | Use | Link |
|---|---|---|
| Bitwarden | Password manager (recommended) | [bitwarden.com](https://bitwarden.com) |
| Ente Auth | Authenticator app with encrypted backup | [ente.io/auth](https://ente.io/auth) |
| Aegis | Authenticator app, Android, open source | [getaegis.app](https://getaegis.app) |
| Yubico | Hardware security keys | [yubico.com](https://yubico.com) |
| HaveIBeenPwned | Breach check + monitoring | [haveibeenpwned.com](https://haveibeenpwned.com) |
| 2FA Directory | Check which sites support what 2FA types | [2fa.directory](https://2fa.directory) |

---

## Agent Prompt
Use an AI agent to audit your current setup and get a prioritized action list: [Agent Prompt: Credential Architecture](/agent-prompts/03-credential-architecture.md)

**Next:** [Module 4: Device & Network Baseline](/modules/04-device-network/guide.md)

---

*Project Chrysalis is a free public-safety resource published by [Build Beyond Belief](https://buildbeyondbelief.com). For more tools and frameworks designed to make you more resilient, visit [buildbeyondbelief.com](https://buildbeyondbelief.com).*
