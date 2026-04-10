# Module 8: Recovery Architecture & Ongoing Ops
*Given a breach, how fast can you recover? What's the plan?*

Security isn't a state you reach. It's a cadence. This module assumes you will be breached — because eventually you will be — and builds the systems to detect it fast, respond correctly, and recover fully. It also establishes the lightweight ongoing practice that keeps your posture from decaying.

**Time required:** 2–3 hours to build your playbook; 30 minutes quarterly after that  
**Output:** A personal incident response playbook; a quarterly review cadence

---

## Personal Incident Response Playbook

### Scenario A: Device Lost or Stolen

**Immediate (within 30 minutes):**
1. Remote wipe the device
   - iPhone/Mac: [icloud.com/find](https://www.icloud.com/find) → Erase
   - Android: [google.com/android/find](https://www.google.com/android/find) → Erase
   - Note: If you disabled Find My, you cannot do this. Enable it now.
2. Change passwords for all accounts that had active sessions on that device
3. On each of those accounts: revoke active sessions ("sign out all other devices")
4. If the device had authenticator app codes: those codes are still valid. Log into each service and either:
   - Re-enroll a new authenticator, OR
   - Revoke the old one if you have another device or backup codes
5. If it was a phone: call your carrier immediately to suspend the number and prevent SIM fraud

**Short-term (within 24 hours):**
- File a police report (creates a paper trail for insurance and provides documentation if the device is used in a crime)
- Contact your carrier about insurance claim if applicable
- Review your email and financial accounts for any activity in the window between device loss and remote wipe

**Prevention check:** After you resolve this — did you have Find My enabled? Were backup codes accessible? Did you know which accounts were active on that device? Fill the gaps found.

---

### Scenario B: Account Compromised

**Signs:** Unexpected login notifications; contacts reporting odd messages from you; locked out of an account; unfamiliar activity in account history.

**Immediate:**
1. Attempt recovery immediately — use your backup codes, recovery email, or authenticator app
2. If recovered: change password immediately to a new unique one
3. Revoke all active sessions on that account (usually under Security settings)
4. Review the activity log: what did they access? What did they send? When did the breach start?
5. Remove any OAuth apps or connected services you don't recognize

**Secondary sweep:**
- If the compromised account was used for SSO anywhere, treat those accounts as potentially compromised too
- If the same password was used elsewhere: change it everywhere (this should not be possible if you followed Module 3)
- If the compromised account is email: check for email forwarding rules added by the attacker (a common persistence technique: they set up forwarding before you recover access)
- Check for new connected apps, recovery email or phone changes, and 2FA changes in your account settings

**Notify:**
- Contacts who may have received messages from the account during the breach
- If it's a financial account: contact the institution directly

---

### Scenario C: Identity Used Fraudulently

**Signs:** Credit application denial when you didn't apply; unfamiliar accounts on your credit report; debt collectors for debts you don't recognize; government benefits denied because they've already been claimed.

**Steps:**
1. **Place a fraud alert** at Experian — this is free and they are required to notify Equifax and TransUnion
   - [experian.com/fraud-alert](https://www.experian.com/fraud-alert) — valid 1 year, renewable
   - A fraud alert requires lenders to verify your identity before opening new credit
2. **Escalate to a credit freeze** if you haven't already (see Module 5) — this is stronger than a fraud alert
3. **File an Identity Theft Report** at [IdentityTheft.gov](https://www.identitytheft.gov) — this generates an official FTC report and a personal recovery plan; it also provides documentation that helps dispute fraudulent accounts
4. **File a police report** — required by many creditors and financial institutions before they'll remove fraudulent accounts
5. **Document everything:** screenshots, dates, account numbers, all correspondence
6. **Contact each institution** where fraudulent accounts were opened — provide your FTC Identity Theft Report and police report. Each has a fraud dispute process.
7. **Request your credit reports** from all three bureaus: [annualcreditreport.com](https://www.annualcreditreport.com) — review for any other unfamiliar accounts

---

## The 24-Hour Breach Drill

**Do this once.** Pick your most critical account — your email or password manager. Pretend, right now, that you have completely lost access.

Work through these questions:
1. Do you have backup codes? Where are they? How long would it take to find them?
2. Do you have a recovery email set up? Can you still access it?
3. Do you have a hardware key registered? Where is it?
4. If all recovery options fail, what is the account's official recovery process? Have you ever tried it?
5. If you genuinely cannot recover this account, what do you lose permanently?

**Most people fail this drill.** That's the point. The gaps you find are the things to fix — before a real incident forces it.

---

## Quarterly Review Checklist

Set a calendar reminder. 30 minutes, four times per year.

**Accounts & Credentials:**
- [ ] Any accounts in recent breach notifications? (Check HaveIBeenPwned for recent breaches)
- [ ] Any new accounts to add to your master inventory?
- [ ] Any dormant accounts to delete?
- [ ] Password manager master password: still strong? Still memorized?
- [ ] Hardware keys: still accounted for? Both of them?
- [ ] Backup codes: still accessible for all hub accounts?
- [ ] Any accounts still using SMS 2FA that could be upgraded?

**Devices & Network:**
- [ ] Any new devices on your home network? (Run Fing scan)
- [ ] Router firmware checked?
- [ ] Any devices that need OS updates?
- [ ] Emergency Access Kit: still accurate? Still accessible to your trusted person?

**Identity & Social:**
- [ ] Any new public records or data broker listings to remove?
- [ ] Social media privacy settings still configured correctly?
- [ ] Any changes to your public footprint since last review?

**Recovery & Planning:**
- [ ] Any major life changes since last review? (See below)
- [ ] Family member check-in: anyone in your household need a security review?
- [ ] Incident Response Playbook: still accurate? Phone numbers current?

---

## Life Change Triggers

Always re-audit when:

**Job change (starting or leaving):**
- Remove personal accounts from work devices before you leave
- Rotate passwords for any service accessed from work equipment
- Check whether work Google/Microsoft account was connected to personal services
- Remove work contacts from your personal emergency protocols

**Relationship change (new partner or separation):**
- Shared account inventory: streaming, utilities, household apps
- Shared device review: is their device logged into your accounts?
- Location sharing: which apps have you shared location with this person?
- Separation: rotate passwords, revoke OAuth grants, check for unknown connected apps

**Moving:**
- Update address at financial institutions, government agencies, and any service that mails you
- Forward mail but watch for address change fraud: USPS sends confirmation of address changes; if you receive one you didn't request, contact USPS immediately
- Watch for mail redirection fraud in the first 60 days after a move

**Death in the family:**
- Estate account management is a major attack vector — fraudulent access to deceased persons' accounts is common
- Execute the Emergency Access Kit process
- Notify major financial institutions; close or memorialize social media accounts per the deceased's wishes

**Kids getting devices:**
- Add their devices to your network inventory
- Establish device security baselines before handing over
- Add them to your dependency map: their accounts may connect to family accounts

---

## Checklist

- [ ] Incident Response Playbook written for Scenarios A, B, and C
- [ ] 24-Hour Breach Drill completed; gaps found and addressed
- [ ] Remote wipe tested or verified active on all devices
- [ ] Quarterly review calendar event created
- [ ] One family member walked through basic recovery planning
- [ ] Emergency Access Kit verified accessible

---

## Tools

| Tool | Use | Link |
|---|---|---|
| iCloud Find My | Remote wipe Apple devices | [icloud.com/find](https://www.icloud.com/find) |
| Google Find My Device | Remote wipe Android | [google.com/android/find](https://www.google.com/android/find) |
| IdentityTheft.gov | FTC identity theft report and recovery plan | [identitytheft.gov](https://www.identitytheft.gov) |
| AnnualCreditReport.com | Free credit reports from all three bureaus | [annualcreditreport.com](https://www.annualcreditreport.com) |
| Experian Fraud Alert | Fraud alert (notifies all three bureaus) | [experian.com/fraud-alert](https://www.experian.com/fraud-alert) |
| HaveIBeenPwned | Ongoing breach monitoring | [haveibeenpwned.com](https://haveibeenpwned.com) |

---

## Agent Prompt
Build your personal incident response playbook with AI assistance: [`agent-prompts/08-recovery-architecture.md`](../../agent-prompts/08-recovery-architecture.md)

---

*You've completed the eight modules. Return to the [master checklist](../../worksheets/) or review your [Security Level](../../README.md#gamification-system-v2) progress.*
