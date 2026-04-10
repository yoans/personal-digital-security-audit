# Personal Digital Security Audit
### *Project Chrysalis*

> "A chrysalis doesn't hide. It transforms. You go in exposed and dependent — you come out resilient. That's the model."

This is an **open, public-safety oriented** framework for individuals who want to audit and harden their digital life against the new era of AI-augmented, agent-driven attacks. It is not a password manager. It is not a scanner. It is a **resilience architecture** — a system for understanding and eliminating single points of failure across your entire digital and physical life.

This project is for everyone, from non-technical users to professionals. It is free, open source, and maintained as a community resource.

---

## Before You Begin: Protect Yourself

> **This guide includes AI agent prompts that ask you to share personal context with an AI assistant. Read this section first.**

**Rule 1: Never share private information with an AI you don't control.**
Hosted AI services (Claude, ChatGPT, Gemini) process your input on their servers. Their privacy policies may permit training on your data, retain your conversations, or expose them in a breach. **Do not paste passwords, SSNs, financial account numbers, recovery codes, or carrier PINs into any hosted AI chat.**

**Rule 2: For the most sensitive work, use a local model.**
A local model runs entirely on your machine. Your data never leaves your device. This is the only way to guarantee privacy when working through these audits with AI assistance.

| Local Model Option | Difficulty | Notes |
|---|---|---|
| **[Ollama](https://ollama.com) + Llama 3** | Easy | One-command install. Runs on Mac, Linux, Windows. |
| **[LM Studio](https://lmstudio.ai)** | Easy | GUI app. Download models and chat locally. No setup. |
| **[Jan](https://jan.ai)** | Easy | Open source desktop app. Clean UI. |

If you don't want to use AI at all — **the module guides are complete standalone resources.** Every module can be worked through without an AI assistant. The prompts are an accelerator, not a requirement.

**Rule 3: Don't make yourself less secure in the process of auditing your security.**
If you're working through Module 1 (account inventory), don't export your password vault to a cloud-synced folder. If you're building a dependency graph, don't put it in an unencrypted Google Sheet that's shared with "anyone with the link." Think about where your audit artifacts live.

---

## The Threat We're Responding To

Traditional cybersecurity advice was written for an era of human attackers and blunt automation. The rules have changed.

Modern AI agents can:
- Build a detailed personal dossier from public data (OSINT) in minutes
- Craft hyper-personalized phishing that passes human intuition checks
- Clone voices and faces to impersonate people you trust
- Chain 10 individually harmless signals into one devastating exploit
- Run persistent, adaptive campaigns 24/7 without fatigue or cost
- Operate through compromised accounts of people in your network

The target isn't your password. It's **your dependency graph** — the chain of accounts, devices, relationships, and services that your life runs on. Destroy one link, and an intelligent agent follows the chain.

**No security system stops a sufficiently sophisticated AI agent. But you can make yourself not worth the effort, and not fragile enough to be destroyed by a single breach.**

This is security by **adaptability** and **resilience**, not security by obscurity.

---

## Project Vision

This repository is the seed of a layered platform:

| Phase | Medium | Status |
|---|---|---|
| **v1 – Guides** | Markdown audit checklist, printable worksheets | 🔨 In progress |
| **v2 – Scored Audit** | Web app with scoring, progress tracking, gamified achievements | Planned |
| **v3 – Community** | Leaderboards, shared configs, red team scenarios, partner prizes | Planned |
| **v4 – AI Copilot** | AI-assisted audit walkthrough, real-time gap analysis | Planned |

The v1 goal is simple: a person with no prior security knowledge reads the guides, works through the modules, and leaves with a materially better security posture and a clear picture of what they're still exposed to.

---

## Framework: The Eight Modules

Each module is an independent audit track. They can be done in any order, but the sequence below is recommended.

### 1. Identity Inventory
*Know every account that exists in your name.*

Most people have 200+ accounts. Many are forgotten. Forgotten accounts are breached silently, and become pivot points into your active life.

- Full account inventory methodology
- Zombie account discovery and deletion
- Email alias strategy (never expose your primary email)
- What "identity" actually means to an AI agent doing recon on you

### 2. Dependency Graph
*Map what breaks if each account falls.*

The question isn't "is this account secure?" It's "if this account is compromised or deleted, what else collapses with it?" Google, Apple ID, GitHub, your phone number — these are identity hubs. Map the blast radius of each.

- Hub vs. leaf account classification
- Single points of failure identification
- Recovery chain audit (if you lose X, can you get it back without Y?)
- Phone number dependency (SIM swap is still the #1 account takeover vector)

### 3. Credential & Access Architecture
*Not just "use a good password manager."*

LastPass is fine. Bitwarden is better. But the architecture matters more than the vendor. How are your credentials organized, backed up, and recoverable without creating new attack surfaces?

- Password manager evaluation criteria
- Hardware key (FIDO2/YubiKey) strategy
- Passkey adoption roadmap
- Emergency access kit — the document that lets your family act if you're incapacitated
- What to do *the day* a breach is announced

### 4. Device & Network Baseline
*Your devices are the edge of your perimeter.*

- Personal device hardening (laptop, phone, tablet)
- Home network audit — router firmware, default credentials, guest networks
- IoT inventory — smart home devices, cameras, locks, appliances
- VPN strategy (when it helps, when it doesn't)
- What a compromised device means vs. a compromised account

### 5. Physical Security Layer
*Attacks don't always start on a screen.*

Physical access is the nuclear option. Mail theft, shoulder surfing, device theft, and social engineering in person are real and underestimated.

- Home office physical security
- Paper document management (shredding, fireproof storage)
- ID document copies and storage
- Travel security posture
- The "lost device" drill

### 6. Social Attack Surface
*OSINT yourself before someone else does.*

An AI agent doing recon on you will find everything public about you in minutes. Most people have no idea what's available. This module is about understanding and reducing your exposure.

- Run your own OSINT report (tools and methodology)
- Public records removal
- Social media footprint audit
- Data broker opt-out workflow
- What can be inferred from what you can't delete

### 7. AI Threat Literacy
*Understanding what agent-driven attacks actually look like.*

This module is educational and scenario-based. Real examples, simulated phishing, deepfake recognition, and the mental models needed to evaluate trust in a world where your "contacts" can be impersonated convincingly.

- Voice cloning and video deepfake awareness
- Spear phishing recognition training (live scenarios)
- AI-generated impersonation: what to trust, what to verify
- The "band of trust" principle — how to authenticate requests that matter
- What "a Mythos-class agent in the wild" actually means and can do

### 8. Recovery Architecture & Ongoing Ops
*Given a breach, how fast can you recover? What's the plan?*

Security isn't a state you reach. It's a cadence. This module covers incident response for individuals and the quarterly/annual review process.

- Personal incident response playbook
- The 24-hour breach drill
- Quarterly security review checklist
- What to do when a family member is compromised
- Maintaining posture as your life changes (new job, new relationship, new devices)

---

## Gamification System (v2)

The audit is structured as a **progression system**. You start wherever you are and improve over time, with concrete recognition for each improvement.

### Security Levels
| Level | Name | Description |
|---|---|---|
| 0 | **Exposed** | Default state for most people |
| 1 | **Aware** | Completed full inventory, knows their attack surface |
| 2 | **Hardened** | No weak default credentials, MFA everywhere critical |
| 3 | **Resilient** | No single points of failure, recovery plan in place |
| 4 | **Antifragile** | Adapts after incidents, helps others, maintains cadence |

### Achievement Examples
- 🗑️ *Ghost Cleaner* — Deleted 10+ zombie accounts
- 🔑 *Key Keeper* — Hardware key on all primary accounts
- 📵 *SIM Defender* — Phone number removed as account recovery on all hubs
- 🗺️ *Mapper* — Completed full dependency graph
- 🧪 *Self-OSINT* — Ran complete recon report on yourself
- 🚨 *Drill Sergeant* — Completed the 24-hour breach drill
- 📦 *Dead Man's Kit* — Emergency access kit created and stored securely
- 🛡️ *Family Shield* — Audited and assisted one family member

### Partner Prizes (Target Partnerships)
The gamification system is designed to support real-world rewards for meaningful progress:

- **YubiKey / Yubico** — Free hardware key at "Hardened" level
- **Bitwarden** — Premium account for completing credential module
- **Backblaze / backup providers** — Free year for completing device module
- **Proton** — Free ProtonMail/VPN upgrade for social attack surface completion
- **Credit monitoring providers** — Free identity monitoring enrollment
- **Cyber insurance providers** — Preferred rates for "Resilient" and above users

---

## What This Is Not

- Not a LastPass replacement — we recommend specific tools but don't build one
- Not a corporate security product — individual and family focus only
- Not fear-based — the goal is competence and calm, not anxiety
- Not a one-time fix — it's a living practice

---

## Project Philosophy

**Security by resilience, not obscurity.** The goal is not to be invisible. It's to not be fragile. A sophisticated AI agent will find out everything findable about you. The question is: does that information give them leverage? Does losing one account cascade into catastrophe? 

**No single point of failure.** At every level — credentials, devices, identity, relationships, access — ask: if this breaks, what breaks with it? Eliminate every "yes."

**Accessible to everyone.** The guides must be usable by a non-technical person. Technical depth is available, but never required. The audience is humans, not sysadmins.

**Open and shared.** Everything here is public, free, and improvable. PSA-class material. If it saves one person from a catastrophic breach, it's worth it.

---

## Roadmap

- [x] v1 Module 1: Identity Inventory guide
- [x] v1 Module 2: Dependency Graph worksheet
- [x] v1 Module 3: Credential Architecture guide
- [x] v1 Module 4: Device & Network baseline checklist
- [x] v1 Module 5: Physical Security guide
- [x] v1 Module 6: Social Attack Surface guide + OSINT self-audit tools
- [x] v1 Module 7: AI Threat Literacy intro + phishing scenarios
- [x] v1 Module 8: Recovery Architecture playbook
- [x] v1 Printable master checklist
- [x] v1 Agent prompts for all 8 modules
- [x] v1 Recommended tools guide
- [x] v1 Breach scenarios
- [x] v1 Docsify site (GitHub Pages)
- [ ] v2 Web app with scoring and achievements
- [ ] v2 Partnership integrations
- [ ] v3 Community platform

---

## Contributing

This is a community resource. Contributions welcome — guides, real-world scenarios, tool reviews, translations, and corrections. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## License

[MIT License](LICENSE) — free to use, share, adapt, and build on.

---

*Project Chrysalis — personal-digital-security-audit — started April 2026*

