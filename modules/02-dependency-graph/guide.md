# Module 2: Dependency Graph
*Map what breaks if each account falls.*

The question isn't "is this account secure?" It's "if this account is compromised or deleted, what else collapses with it?" Most people discover their entire digital life is balanced on 2–3 identity hubs they haven't thought carefully about.

**Time required:** 1–2 hours  
**Prerequisite:** Module 1 account list

**Output:** A dependency map and a list of single points of failure to eliminate.

---

## Key Concepts

**Hub account** — If compromised, an attacker can take over many other accounts via password reset, SSO, or shared credentials. Losing it destroys your access to dependent services. Examples: primary email, phone number, Apple ID, Google account, password manager.

**Leaf account** — Stands alone. Losing it doesn't cascade. Examples: a streaming service, a forum account, a pizza app.

**Recovery chain** — Account A can reset B, which can reset C. If A is taken, C is gone even if C has a strong password and 2FA.

**Blast radius** — The total scope of damage if a given account is compromised.

---

## Steps

### Step 1: For each account in your list, answer:

1. **"If someone controlled this account, what else could they access?"**
   - Can it reset passwords for other accounts?
   - Is it used as a login for other services (SSO/OAuth)?
   - Does it contain recovery codes or sensitive info that unlocks other accounts?

2. **"If I lost access to this account TODAY, what else would I lose?"**
   - What accounts have their password reset email sent here?
   - What apps are connected via this account's SSO?
   - What would become unrecoverable?

3. **"What does this account reset via?"** (email address, phone number, backup code)

4. **"What 2FA method does this account use?"** (hardware key, authenticator app, SMS, none)

### Step 2: Map your recovery chains

Trace every path an attacker could use to get from one account to your most critical ones.

**Common dangerous chains:**
- Phone number → SMS code → primary email → everything else
- Old forgotten email → password reset link → banking account
- Work Google account → personal accounts signed in on same browser

### Step 3: Identify SIM swap exposure

SIM swap is the #1 account takeover vector. An attacker calls your carrier, impersonates you, and gets your phone number moved to their SIM. They then receive every SMS 2FA code sent to that number.

Audit: **How many critical accounts use SMS as a 2FA or recovery method?**

Any hub account using SMS 2FA is SIM-swap vulnerable.

---

## Build Your Dependency Map

Extend your Module 1 account list with these columns:

| Account | Type | Resets Via | 2FA Method | If Compromised, Attacker Can Access | If Lost, I Also Lose |
|---|---|---|---|---|---|
| Gmail | **Hub** | Recovery phone + backup email | App auth | All Google services, everything that resets here | 40+ accounts |
| Apple ID | **Hub** | Email + phone | SMS ⚠️ | All Apple services, App Store purchases, iCloud | iCloud backup, all iOS apps |
| Personal phone # | **Hub** | Carrier | — | Any account using SMS 2FA | SMS-based 2FA everywhere |
| Netflix | Leaf | Gmail | SMS | Nothing | Just Netflix |

---

## Red Flags to Fix

**Priority 1 (fix this week):**
- [ ] SMS 2FA on your primary email
- [ ] SMS 2FA on your password manager  
- [ ] SMS 2FA on your bank or investment accounts
- [ ] Phone number is the *only* recovery method for your primary email

**Priority 2 (fix this month):**
- [ ] One email address on 200+ accounts with no aliasing strategy
- [ ] No backup codes stored offline for any hub account
- [ ] Old email address you no longer control used as recovery for active accounts
- [ ] Work account linked as recovery for personal accounts

**Priority 3 (fix when you can):**
- [ ] Any hub account with no 2FA at all
- [ ] Recovery chains longer than 3 hops

---

## Phone Number Hardening

Your phone number is often the weakest hub. Steps to reduce exposure:

1. **Add a carrier PIN/passcode** — call your carrier and add a PIN required to make account changes. All major US carriers support this.
2. **Enable number lock** — T-Mobile and Verizon offer explicit SIM lock features.
3. **Remove SMS 2FA from hub accounts** — replace with an authenticator app or hardware key (see Module 3).
4. **Consider a Google Voice or silent VoIP number** as the "public" number you give to services — keep your real SIM number private.

---

## Tools

| Tool | Use | Link |
|---|---|---|
| Google Security Checkup | Review which apps have access to your Google account | [myaccount.google.com/security-checkup](https://myaccount.google.com/security-checkup) |
| Apple ID Connected Apps | Review OAuth grants | [appleid.apple.com](https://appleid.apple.com) |
| Twitter/X Connected Apps | Review third-party app access | Settings → Security → Connected Apps |

---

## Agent Prompt
Use an AI agent to help map your dependencies: [Agent Prompt — Dependency Graph](/agent-prompts/02-dependency-graph.md)

---

## Checklist
- [ ] Mapped recovery chain for every hub account
- [ ] Identified all accounts using SMS 2FA
- [ ] Identified SIM-swap-vulnerable accounts
- [ ] Listed blast radius for each hub
- [ ] Found any old email address used as recovery for active accounts
- [ ] Found any recovery chain loops
- [ ] Built dependency map table
- [ ] Prioritized red flags for Module 3 action

**Next:** [Module 3 — Credential & Access Architecture](/modules/03-credential-architecture/guide.md)
