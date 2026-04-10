# Breach Scenarios
*Real-world attack patterns for training and awareness*

These scenarios are drawn from documented real-world breach patterns. Names and identifying details are fictional. The attack sequences are real.

Use these to calibrate your threat model and test your preparation. After each scenario, check: **if this happened to you today, would your current setup survive it?**

---

## Scenario 1: The SIM Swap

**Target:** A software developer, mid-30s. Active on Twitter/X. Held approximately $45,000 in a cryptocurrency exchange.

**Sequence:**
1. Attacker finds the target's name, phone number, and carrier from a data broker site and a prior data breach that included the carrier name.
2. Attacker calls the mobile carrier, impersonates the target using their name, last 4 of SSN (found in the breach), and billing address (found in public records).
3. Carrier transfers the phone number to an attacker-controlled SIM.
4. Attacker uses SMS "forgot password" to take over the target's email.
5. Via the email, attacker resets the cryptocurrency exchange password.
6. SMS 2FA on the exchange goes to the attacker's now-controlled phone number.
7. Full withdrawal of all funds in under 90 minutes. Irreversible.

**Why it worked:**
- Carrier used knowledge-based authentication (SSN last 4 + address) — both were available from breaches and public records
- Email was recoverable via SMS
- Exchange used SMS 2FA

**What stops this:**
- Carrier account PIN (an attacker doesn't know it, and KBA questions are bypassable — a PIN is not)
- Carrier number lock (T-Mobile, Verizon offer this)
- Email recovery not linked to phone number alone
- Cryptocurrency exchange using hardware key (FIDO2) instead of SMS 2FA
- Even app-based TOTP (not SMS) would have blocked the exchange takeover

**Chrysalis modules:** 2 (SIM swap exposure), 3 (2FA upgrade), 5 (credit/carrier hardening)

---

## Scenario 2: Credential Stuffing into a Bank

**Target:** A retiree, 60s. Uses the same password on about 40 accounts. One of those accounts — a retail loyalty program — was breached in 2019. She never changed the password because she didn't know.

**Sequence:**
1. The retail breach database is sold on a criminal forum. Millions of email/password pairs.
2. Automated tools test those credentials at scale against thousands of services.
3. Her email + password combination works on her bank's login page. (She reused the password.)
4. The bank uses no 2FA — just username and password.
5. Attacker logs in, adds a new external transfer account, waits 24 hours (standard bank transfer delay — the attacker knows this), and transfers $12,000.
6. She gets a notification the following morning.

**Why it worked:**
- Password reuse across services
- Bank had no 2FA requirement
- She had no breach monitoring active — didn't know the 2019 breach affected her

**What stops this:**
- Unique password for every account (a password manager makes this zero-effort)
- HaveIBeenPwned monitoring on her email — would have flagged the 2019 breach the day it was indexed
- 2FA on the bank (many banks now offer this — some require you to opt in)

**Chrysalis modules:** 1 (account inventory, breach check), 3 (password manager, unique passwords), 8 (breach response protocol)

---

## Scenario 3: AI-Assisted Spear Phish → Corporate Credential → Personal Account Pivot

**Target:** A marketing manager, early 40s. Uses their work laptop for some personal browsing. Same password for work email and their personal email.

**Sequence:**
1. Attacker uses public LinkedIn profile to identify the target's employer, manager's name, and recent company announcement (a product launch, mentioned in a press release).
2. AI generates a highly personalized phishing email: "Hi [name], [manager's name] asked me to loop you in on the compliance review for [product launch]. Please access the secure review portal and confirm your credentials: [link]."
3. The link is a convincing mock of the company's SSO login page — a domain with a one-character typo.
4. Target enters work credentials. Attacker now has them.
5. Using work credentials, attacker accesses the company email system.
6. In previously received emails, target's personal Gmail address is visible.
7. Target used the same password for work and personal Gmail. Password reset + SMS 2FA (SIM swap of the phone number visible in their work email signature) = personal Gmail taken.
8. Personal Gmail contains bank statements. Bank account targeted via account recovery.

**Why it worked:**
- Public OSINT (LinkedIn, press release) enabled a convincing, personalized pretext
- No domain check habit before entering credentials
- Password reuse across work and personal
- Phone number in work email signature was exploitable for SIM swap

**What stops this:**
- Domain verification before entering credentials — the one-character typo domain would have caught it
- A hardware key (FIDO2) on the work login — it would have refused to sign in to the typo domain
- Unique passwords (work email ≠ personal email)
- Phone number absent from public email signatures, or non-real-carrier number used
- Phishing awareness training — this is a textbook pretexting attack; recognizing the pattern is the first defense

**Chrysalis modules:** 3 (hardware key as phishing defense), 6 (OSINT exposure, phone number hygiene), 7 (spear phish recognition)

---

## Scenario 4: Voice Clone Family Emergency

**Target:** A parent, 50s. Their adult child had been on a service trip abroad the previous year and had done a video interview that was posted publicly online — about 4 minutes of audio available.

**Sequence:**
1. Attacker identifies the target via their child's social media: parent's name, hometown, and relationship visible in a tagged photo.
2. Child's voice cloned from the publicly posted video — 30 seconds of audio is sufficient.
3. Target receives a call: it sounds like their child. "Mom, I got robbed. My phone is broken and I'm borrowing someone's phone. I need you to wire $800 so I can get to the airport. Please don't tell dad yet — I'm embarrassed."
4. Target wires $800 via a money transfer service.
5. Two days later, the real child calls from their actual phone. Neither robbery nor trip had occurred.

**Why it worked:**
- Child's voice was publicly available and convincing when cloned
- Urgency + emotional framing bypassed rational evaluation
- No pre-established verification protocol in the family
- Request to keep it private removed the second-opinion check

**What stops this:**
- **A pre-established family verification code** — a word or phrase known only to the family, agreed on in person, that an attacker couldn't know
- The habit of calling back on a known number — any legitimate stranded person can be called back at a hotel or on a borrowed phone via a number you look up independently
- Awareness that voice cloning is real and accessible — understanding this possibility makes the emotional override less likely to work
- Any request to *not* tell someone else is itself a red flag

**Chrysalis modules:** 7 (AI threat literacy, Band of Trust protocol)

---

## Scenario 5: The Quiet Account Takeover

**Target:** A freelance consultant, late 30s. Has a forgotten Dropbox account from 2013 with a simple password. Dropbox was breached in 2012 — the database was circulated online years later.

**Sequence:**
1. Attacker obtains the 2012 Dropbox breach database (freely available on dark web forums).
2. Tests the credential pair — email + password — against current-day services. Dropbox itself has long since forced a password reset. But the target reused that password on an older forum account.
3. That forum account's profile lists a secondary email address the target used in 2013.
4. That old email address is still accessible — the target forgot about it — and uses the same password.
5. Inside the old email: an airline account confirmation. The attacker resets the airline account and collects 85,000 frequent flyer miles.
6. The target doesn't notice for 8 months.

**Why it worked:**
- Old, forgotten account with reused password
- Old email address still active, still accessible with old credentials
- No breach notifications active on the secondary email

**What stops this:**
- Zombie account deletion — a forgotten account that still exists is still an attack surface
- HaveIBeenPwned monitoring on all email addresses — the 2012 Dropbox breach is indexed; a notification would have surfaced it
- Unique passwords — if the email/password pair didn't work anywhere else, the chain breaks at step 2

**Chrysalis modules:** 1 (zombie account discovery and deletion, breach monitoring)

---

## Using These Scenarios

**For personal reflection:** After each scenario, run the "what stops this" section against your own setup. If the defense listed isn't in place, that's a priority for the corresponding module.

**For family conversations:** These scenarios are concrete and non-technical enough to share with family members who aren't going to read a security guide. The voice clone scenario works particularly well for parents and older relatives.

**For training:** Use the [Module 7 agent prompt](/agent-prompts/07-ai-threat-literacy.md) to generate personalized versions of these scenarios — customized to your employer, your relationships, and your real account patterns.

---

*More scenarios to be added. Real documented cases welcome — submit via PR with all identifying details removed or fictionalized.*
