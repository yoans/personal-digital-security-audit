# Master Checklist
*Project Chrysalis, complete audit across all eight modules*

Print this. Work through it. Track your progress. You don't have to do it all at once.

---

## How to Use

Work through each module in order if possible, they build on each other. Each module has a full guide at `modules/[number]-[name]/guide.md`.

Mark each item:
- `[ ]`, Not done
- `[~]`, Partially done / in progress
- `[x]`, Complete

**Your current level:**  
`[ ]` 0, Exposed &nbsp; `[ ]` 1, Aware &nbsp; `[ ]` 2, Hardened &nbsp; `[ ]` 3, Resilient &nbsp; `[ ]` 4, Antifragile

---

## Module 1: Identity Inventory

- [ ] Searched all email inboxes for account-creation keywords
- [ ] Exported and reviewed password manager vault
- [ ] Reviewed browser saved passwords on all devices
- [ ] Reviewed 12 months of bank and credit card statements for subscriptions
- [ ] Reviewed connected apps on Google
- [ ] Reviewed connected apps on Apple ID
- [ ] Reviewed connected apps on Facebook (if applicable)
- [ ] Completed category sweep (gaming, health, travel, government, etc.)
- [ ] Built master account list in spreadsheet
- [ ] Ran all email addresses through HaveIBeenPwned
- [ ] Started deleting dormant accounts

**Module 1 complete?** `[ ]` → **You are now: Aware (Level 1)**

---

## Module 2: Dependency Graph

- [ ] Classified all accounts as Hub or Leaf
- [ ] Mapped recovery chain for each Hub account
- [ ] Identified all accounts using SMS as 2FA
- [ ] Identified accounts using phone number as ONLY recovery method
- [ ] Found and flagged old email addresses used for recovery on active accounts
- [ ] Mapped blast radius for each Hub
- [ ] Called carrier and added account PIN / number lock
- [ ] Documented complete dependency map

**Module 2 complete?** `[ ]`

---

## Module 3: Credential Architecture

*Immediate priority:*
- [ ] Password manager installed and active on all devices
- [ ] All new passwords are manager-generated (random, 20+ chars)
- [ ] 2FA enabled on password manager vault
- [ ] 2FA enabled on primary email
- [ ] 2FA enabled on all Hub accounts
- [ ] SMS 2FA removed from Hub accounts (replaced with app or hardware key)

*Short-term:*
- [ ] Authenticator app selected and installed
- [ ] All TOTP codes in authenticator app
- [ ] Backup codes generated and stored for all Hub accounts
- [ ] Hardware key ordered
- [ ] Hardware key registered on primary email (both keys)
- [ ] Hardware key registered on password manager (both keys)
- [ ] Emergency Access Kit created and stored securely
- [ ] Passkeys adopted where offered

**Module 3 complete?** `[ ]` → **You are now: Hardened (Level 2)**

---

## Module 4: Device & Network

*Laptop/Desktop:*
- [ ] Full disk encryption verified on
- [ ] Screen lock set to 2 minutes or less, password required on wake
- [ ] OS auto-updates on
- [ ] Browser extensions audited and pruned
- [ ] Startup apps reviewed

*Phone:*
- [ ] Alphanumeric passcode or strong PIN set
- [ ] App permissions audited: location, microphone, camera, contacts
- [ ] Apps unused for 3+ months deleted
- [ ] Backup verified as current and encrypted

*Router:*
- [ ] Admin password changed from factory default
- [ ] Firmware updated
- [ ] Guest/IoT network enabled
- [ ] WPS disabled
- [ ] SSID changed from default

*IoT:*
- [ ] All network devices inventoried (Fing scan)
- [ ] Default credentials changed on all IoT devices
- [ ] All IoT devices moved to guest network
- [ ] Devices without recent firmware flagged or replaced

---

## Module 5: Physical Security

- [ ] Locked mailbox or PO Box for sensitive mail
- [ ] USPS Informed Delivery active
- [ ] Cross-cut or micro-cut shredder in use
- [ ] Critical documents in fireproof/water-resistant storage
- [ ] Critical documents scanned and stored encrypted
- [ ] Social Security card is NOT in wallet
- [ ] Screen privacy filter when working in public
- [ ] Never leave device unattended policy established
- [ ] Public USB avoided (or data blocker on hand)
- [ ] Find My / Find My Device active on all devices
- [ ] Remote wipe procedure known
- [ ] **Credit freeze: Experian** `[ ]`
- [ ] **Credit freeze: Equifax** `[ ]`
- [ ] **Credit freeze: TransUnion** `[ ]`
- [ ] **ChexSystems freeze** `[ ]`

---

## Module 6: Social Attack Surface

- [ ] Google searches run on yourself (name + city, name + employer, email, phone)
- [ ] Reverse image search done on common profile photo
- [ ] All emails checked on HaveIBeenPwned
- [ ] Username search run (Sherlock or WhatsMyName)
- [ ] Top data broker sites checked for your info
- [ ] Manual opt-outs submitted to top 20 brokers (or automated service enrolled)
- [ ] Removal submissions tracked
- [ ] Privacy settings reviewed on all active social platforms
- [ ] Auto-location tagging on posts disabled
- [ ] Old location-tagged posts reviewed
- [ ] Email alias strategy in place for new signups
- [ ] Public phone number separate from real carrier number
- [ ] Camera location metadata disabled

---

## Module 7: AI Threat Literacy

- [ ] Read capabilities section (what AI agents can and can't do)
- [ ] Worked through all three phishing scenarios
- [ ] Understood the three-part structure of every phishing attempt
- [ ] Identified 2-3 verification anchor people
- [ ] Established backup contact channel with each anchor
- [ ] Established verification word/phrase with each anchor (in person or private call)
- [ ] Written and stored personal verification rules (3 rules)
- [ ] Shared Band of Trust concept with at least one family member

---

## Module 8: Recovery Architecture

- [ ] Incident response playbook written for: device lost/stolen
- [ ] Incident response playbook written for: account compromised
- [ ] Incident response playbook written for: identity used fraudulently
- [ ] 24-Hour Breach Drill completed; gaps addressed
- [ ] Remote wipe verified active on all devices
- [ ] Quarterly review calendar event created (4x/year)
- [ ] Emergency Access Kit verified accessible to trusted person

**Module 8 complete?** `[ ]` → **You are now: Resilient (Level 3)**

---

## Level 4: Antifragile

These aren't one-time items, they're habits and practices.

- [ ] Quarterly review completed at least once
- [ ] One family member or friend walked through the audit with your help
- [ ] One incident occurred and was handled using your playbook
- [ ] Posture updated after a major life change (job, relationship, move)
- [ ] At least one module guide improved or contribution made to the project

---

## Quick Stats (fill in after Module 1)

| | Count |
|---|---|
| Total accounts inventoried | |
| Dormant accounts deleted | |
| Hub accounts identified | |
| Accounts with hardware key | |
| Accounts still on SMS 2FA | |
| Data broker opt-outs submitted | |
| Devices inventoried | |
| IoT devices moved to guest network | |

---

## You finished. Now help one other person.

Most people will never see a guide like this on their own. The single highest-leverage thing you can do after completing your own audit is hand it to one other person who would not have found it.

- Send it to a parent, sibling, partner, or friend: `https://chrysalis.buildbeyondbelief.com`
- Share on LinkedIn or your platform of choice with a one-line note about why you did it
- Open an issue on the repo with anything you'd improve

---

*Project Chrysalis is a free public-safety resource published by [Build Beyond Belief](https://buildbeyondbelief.com). For more tools and frameworks designed to make you more resilient, visit [buildbeyondbelief.com](https://buildbeyondbelief.com).*

*Repo: [github.com/yoans/personal-digital-security-audit](https://github.com/yoans/personal-digital-security-audit)*
