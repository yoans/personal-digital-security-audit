# Module 1: Identity Inventory
*Know every account that exists in your name.*

Most people have 200+ accounts. Many are forgotten. Forgotten accounts get breached silently and become pivot points into your active life. You cannot protect what you don't know exists.

**Time required:** 2-4 hours for the initial inventory. 15 minutes quarterly after that.

**Output:** A master account list you'll use in every other module.

---

## Steps

### Step 1: Search your inboxes
Search all email addresses (present and past) for these strings:
```
"verify your email"
"welcome to"
"account created"
"confirm your account"
"your account has been"
"thanks for registering"
"thanks for signing up"
```
Export or log every service name that appears. Don't filter yet, just collect.

### Step 2: Export your password manager
If you use a password manager: export the vault to CSV temporarily, add services to your list, then delete the export file securely. If you don't have one, this is column proof you need one (see Module 3).

### Step 3: Check browser saved passwords
Chrome: `chrome://password-manager/passwords`
Firefox: `about:logins`
Safari: Settings → Passwords
Edge: `edge://password-manager/passwords`

### Step 4: Review bank and credit card statements
12 months of statements. Every recurring charge is an account. Subscriptions you forgot about may have credentials that haven't been rotated in years.

### Step 5: Review connected apps on your identity hubs
These are services you've authorized to access your Google or Apple account:
- **Google:** [myaccount.google.com/connections](https://myaccount.google.com/connections)
- **Apple:** [appleid.apple.com](https://appleid.apple.com) → Security → Apps Using Apple ID
- **Facebook:** Settings → Apps and Websites
- **Twitter/X:** Settings → Security → Connected Apps

### Step 6: App store purchase history
Every app you've downloaded that requires an account:
- **iOS:** App Store → Account → Purchased
- **Android:** Play Store → Account → Order History

### Step 7: Category sweep
Force yourself to think through these categories for forgotten accounts:
- Old email providers (Hotmail, AOL, Yahoo, school/work addresses)
- Gaming (Steam, PlayStation, Xbox, old MMOs, mobile games)
- Shopping (Amazon, eBay, Etsy, old retail accounts)
- Health & fitness (MyFitnessPal, Strava, old gym apps)
- Forums and communities (Reddit, Discord servers, hobby forums)
- Travel (airlines, hotels, car rentals, booking sites)
- News and media (subscriptions, paywalled sites)
- Finance (investment accounts, crypto, old banks, PayPal, Venmo)
- Old work / school accounts (still accessible?)

---

## Build Your Account List

Create a spreadsheet or table with these columns:

| Service | Email Used | Username | Status | Criticality | 2FA? | Notes |
|---|---|---|---|---|---|---|
| Gmail | you@gmail.com | - | Active | Hub | App | Primary identity |
| MyFitnessPal | you@gmail.com | username123 | Dormant | Leaf | No | Breached 2018 |
| Old Hotmail | old@hotmail.com | - | Forgotten | Leaf | No | May still exist |

**Status:** Active / Dormant (haven't used in 1yr+) / Unknown  
**Criticality:** Hub (controls other accounts) / Leaf (stands alone), you'll refine this in Module 2

---

## Actions After Inventory

**Delete what you don't need.** Zombie accounts are liabilities.
- Start with: [JustDeleteMe.com](https://justdeleteme.com), rates how easy it is to delete accounts on hundreds of services
- For services not listed: search `[service name] delete account` or `[service name] close account`
- If a service won't let you delete: change the email and password to something random and log out

**Check for past breaches.**
- Run every email address through [HaveIBeenPwned.com](https://haveibeenpwned.com)
- Any breached service: rotate that password immediately; if you reused it elsewhere, rotate those too

**Note patterns.** Which email address is on hundreds of accounts? That becomes a target. That awareness feeds Module 2 and Module 6.

---

## Tools

| Tool | Use | Link |
|---|---|---|
| HaveIBeenPwned | Check email addresses for known breaches | [haveibeenpwned.com](https://haveibeenpwned.com) |
| JustDeleteMe | Delete account guides for hundreds of services | [justdeleteme.com](https://justdeleteme.com) |
| Google Security Checkup | Review connected apps, recent access, 2FA status | [myaccount.google.com/security-checkup](https://myaccount.google.com/security-checkup) |
| Firefox Monitor | Breach monitoring, free | [monitor.mozilla.org](https://monitor.mozilla.org) |

---

## Agent Prompt
Use an AI agent to help surface accounts you've forgotten: [Agent Prompt: Identity Inventory](/agent-prompts/01-identity-inventory.md)

---

## Checklist
- [ ] Searched all inboxes for account creation emails
- [ ] Exported password manager (and deleted the export)
- [ ] Reviewed browser saved passwords
- [ ] Reviewed 12 months of bank/card statements
- [ ] Reviewed connected apps on Google, Apple, Facebook
- [ ] Completed category sweep
- [ ] Built master account list
- [ ] Ran all email addresses through HaveIBeenPwned
- [ ] Started deleting dormant accounts

**Next:** [Module 2: Dependency Graph](/modules/02-dependency-graph/guide.md)

---

*Project Chrysalis is a free public-safety resource published by [Build Beyond Belief](https://buildbeyondbelief.com). For more tools and frameworks designed to make you more resilient, visit [buildbeyondbelief.com](https://buildbeyondbelief.com).*
