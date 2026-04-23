# Dependency Graph Worksheet
*Module 2 output, map what breaks if each account falls*

Complete your Account Inventory (Module 1) first.

---

## Hub Account Map

For each account you classified as a **Hub**, fill in this table.

| Account | Login Email | Recovery Email | Recovery Phone? | 2FA Type | OAuth: I log into... | If compromised, attacker can reach... | If lost, I permanently lose... | Priority Fixes |
|---|---|---|---|---|---|---|---|---|
| Primary Gmail | | - | 📵 No | App auth | [list services] | [list accounts] | [list losses] | |
| Apple ID | | | | | | | | |
| Personal phone # | N/A | N/A | - | N/A | | [all SMS 2FA] | | |
| Password Manager | | | | | | | | |
| Primary Bank | | | | | | | | |
| | | | | | | | | |

---

## Leaf Account Sample

You don't need to map every leaf in detail, but spot-check a representative sample.

| Account | Login Email | 2FA? | Notes |
|---|---|---|---|
| Netflix | | No | |
| Steam | | App auth | |
| | | | |

---

## Recovery Chain Diagram

Map your personal recovery chain. Fill in the boxes:

```
My most critical accounts:
[ Primary Email: _____________ ]
[ Password Manager: __________ ]
[ Primary Bank: ______________ ]

Each of these resets via:
Primary Email → resets via: [ ________________ ]
Password Manager → resets via: [ ________________ ]
Primary Bank → resets via: [ ________________ ]

My phone number (___________) controls SMS 2FA on:
[ ] ________________
[ ] ________________
[ ] ________________

If an attacker took my phone number, they could access:
[ ] ________________ via SMS reset
[ ] ________________ via SMS 2FA
[ ] ________________ via SMS 2FA
```

---

## Red Flag Tracker

| Account | Red Flag | Severity | Fixed? |
|---|---|---|---|
| Example: Apple ID | SMS 2FA, SIM swap vulnerable | 🔴 Critical | No |
| | | | |
| | | | |
| | | | |

**Severity key:**
- 🔴 Critical, fix this week (hub account + SMS or no recovery)
- 🟡 Important, fix this month
- 🟢 Minor, fix when convenient

---

## SIM Swap Exposure Summary

| Step | Answer |
|---|---|
| How many Hub accounts use SMS as primary 2FA? | |
| How many accounts use phone number as ONLY recovery method? | |
| Have you added a carrier account PIN? | Yes / No |
| Does your carrier offer number lock? | Yes / No / Unknown |
| Is number lock enabled? | Yes / No |

---

*Complete, then move to Module 3: Credential Architecture.*

> **→ [Module 3: Credential & Access Architecture](/modules/03-credential-architecture/guide.md)**

Return anytime: [Module 2 guide](/modules/02-dependency-graph/guide.md) · [Master Checklist](/worksheets/master-checklist.md)

---

*Project Chrysalis is a free public-safety resource published by [Build Beyond Belief](https://buildbeyondbelief.com). For more tools and frameworks designed to make you more resilient, visit [buildbeyondbelief.com](https://buildbeyondbelief.com).*
