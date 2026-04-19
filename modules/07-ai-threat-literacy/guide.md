# Module 7: AI Threat Literacy
*Understanding what agent-driven attacks actually look like.*

In April 2026, Anthropic's Project Glasswing demonstrated that frontier AI models can autonomously find zero-day vulnerabilities in every major operating system and browser, including a 27-year-old OpenBSD bug that survived human review and millions of automated tests. The same capabilities that patch critical infrastructure can be turned toward individuals.

This module is about accurate mental models, not fear. If you understand what AI-augmented attacks actually do, you can reason about what actually stops them, and what doesn't.

**Time required:** 1-2 hours reading + scenario practice  
**Output:** Calibrated threat model; personal verification protocol

---

## What Mythos-Class Agents Can Actually Do (As of 2026)

Be specific. Vague fear is useless. These are documented capabilities:

**Autonomous vulnerability discovery:**
- Find previously unknown security flaws in major OS and browser code, without human guidance
- Chain multiple individually minor vulnerabilities into a full system compromise
- Generate working exploits, not just identify flaws but automate their use

**Targeted personal reconnaissance:**
- Build a detailed personal dossier from public OSINT in minutes: full name, address history, family members, employer, phone numbers, email addresses, social connections, political/religious inference
- Cross-reference breach databases to recover historical passwords and security question answers
- Map your dependency graph before you've done Module 2

**Social engineering at scale:**
- Write spear phishing emails that reference your real name, real employer, real recent activity, and your manager's real name, no generic "Dear Customer"
- Craft pretexts that fit your specific professional and personal context
- Operate simultaneously against many targets with no fatigue or cost

**Voice and video impersonation:**
- Clone a voice convincingly from ~30 seconds of audio (your voicemails, podcast appearances, videos)
- Generate real-time deepfake video in a live call with current tooling
- Impersonate family members, colleagues, or authority figures in ways that pass casual human judgment

**Persistence and adaptability:**
- Run continuously across multiple platforms, accounts, and time zones
- Adapt tactics based on responses, if one approach fails, try another
- Operate through compromised accounts of people in your network as proxies

---

## What AI Agents Cannot Do Reliably (As of 2026)

Accurate threat modeling means knowing the limits, too:

- Cannot beat a hardware security key (FIDO2), hardware keys verify the actual domain cryptographically, not the apparent one; they cannot be phished
- Cannot override a credit freeze, a credit freeze works at the bureau level regardless of what information an attacker holds
- Cannot access accounts that don't exist or are not connected to anything
- Cannot perfectly impersonate someone in a sustained, probing conversation with unexpected questions, there are still tells, and pre-established verification protocols can expose them
- Cannot always operate without traces, log analysis can detect agent-driven attacks
- Cannot recover deleted accounts or data that has been genuinely purged

**The implication:** The defenses in this guide work. Hardware keys, no single points of failure, credit freezes, and verification protocols are all effective against even sophisticated AI-augmented attacks. You are not powerless.

---

## Phishing in the AI Era

**Old phishing:** Generic greeting. Obvious typos. Urgent tone. A suspicious link. Easy to spot if you're paying attention.

**New phishing:** Your name. Your bank (because they know your bank from breach data or OSINT). Reference to a recent transaction. Your manager's name in the CC line. A domain that looks right at a glance. Possibly a voice message from someone who sounds like a family member.

**What doesn't change:** The mechanism. Phishing always involves:
1. Creating urgency or fear (act now or lose access / there's a suspicious charge)
2. Asking you to take an action (click, call, provide credentials, approve a transfer)
3. Providing a path that they control (a link, a phone number, a QR code)

**The baseline rule:** Any unsolicited communication asking you to take an action involving access, money, or sensitive information should be verified through a channel you initiated, not the one they provided.

---

## Spear Phishing Scenarios (Practice)

Read each scenario. Decide what you'd do. Then read the debrief.

---

**Scenario 1: The IT Email**
> From: helpdesk@[your-employer-domain-with-a-typo].com  
> Subject: Your account is scheduled for deactivation  
> "Hi [your name], we've detected unusual sign-in activity on your account. Your access will be suspended in 24 hours unless you verify your credentials at the link below., IT Security Team"

*What makes this dangerous:* Correct name, legitimate-looking sender on a quick read, urgency, plausible IT activity.  
*The tell:* The domain is slightly wrong. Hover over every link before clicking, look at the actual URL.  
*What to do:* Do not click. Navigate directly to your employer's IT portal. Call IT support using a number from your company directory, not this email.

---

**Scenario 2: The Family Emergency Voice Message**
> You receive a voicemail from a number you don't recognize. The voice sounds like your sibling. "Hey, [your name], it's me. My phone got stolen while I was traveling. I need you to send $400 via Venmo to get a flight home. I can't call from my hotel. Please do this as soon as you can. I'll pay you back right away."

*What makes this dangerous:* Voice cloning is convincing. The story is plausible. The urgency prevents careful thinking.  
*What to do:* Do not send money. Call your sibling's real number. Contact a mutual family member. The real person, if stranded, will understand verification. Any pressure against verification is a red flag.

---

**Scenario 3: The Unusual Login Alert**
> Text message: "Chase alert: unusual sign-in from [city you've never been to]. If this wasn't you, call 1-800-[number] immediately to secure your account."

*What makes this dangerous:* SMS is expected from banks. The city creates urgency. The number provided is controlled by the attacker.  
*What to do:* Do not call that number. Open your bank app directly or call the number on the back of your card. Access your account directly and check for real activity.

---

## Deepfake Recognition

Current heuristics, these improve with each model generation, so don't rely on them indefinitely:

- **Unnatural eye movement or blinking:** deepfake models have historically struggled with realistic blinking and gaze
- **Lighting inconsistencies around hair edges:** the boundary between face and hair is computationally hard
- **Audio/lip sync mismatch:** small desync on words with tight lip movements (b, p, m)
- **Unnatural stillness:** the head and body movement of real video is complex; deepfakes can appear slightly rigid
- **Ask an unexpected question:** "Quick, tell me your dog's name" or anything that requires retrieval from real memory plus natural delivery often exposes a generated response

**The lasting defense:** These heuristics age. The protocol below doesn't.

---

## Band of Trust: Your Verification Protocol

Define this now, before you need it. Write it down. Share it with your trusted people.

**Identify 2-3 people who are your verification anchors:** family members or close friends you would contact in an emergency.

**For each, establish:**
1. A backup contact channel (if my phone is gone, I'll reach you at...)
2. A verification word or phrase, something you've agreed on in person, that neither of you has ever typed online, that you would both recognize but an AI building a profile on you couldn't know

**The protocol in practice:**
- Any request involving money, access, or sensitive action, regardless of how legitimate it looks or sounds, that comes through a channel you didn't initiate gets verified through a channel you control
- "Can I verify this with a quick call/text through our normal channel?", legitimate senders will not be offended
- Any pushback against verification is itself a red flag

**Write your 3 personal rules:**
1. I will never transfer money based on any single digital communication, regardless of who it appears to be from.
2. I will verify any unexpected request involving my accounts by going directly to the service, not using any link or number provided in the message.
3. I will use [your verification protocol] for any request from a trusted contact that falls outside normal patterns.

---

## Checklist

- [ ] Read the capabilities section, understand what AI agents can and can't do
- [ ] Read through the three phishing scenarios; could you have spotted each one?
- [ ] Understood the three-part structure of every phishing attempt (urgency → action → controlled path)
- [ ] Identified your 2-3 verification anchor people
- [ ] Established a backup contact channel with each
- [ ] Established (in person or via a channel not associated with your normal digital profile) a verification word/phrase with each
- [ ] Written your 3 personal verification rules
- [ ] Shared the Band of Trust concept with at least one family member

---

## Further Reading

- [Anthropic, Project Glasswing](https://www.anthropic.com/glasswing), official documentation of what Mythos-class models can do
- [Anthropic, Frontier Red Team Blog](https://red.anthropic.com/2026/mythos-preview), technical details on autonomous vulnerability discovery
- CISA Phishing Guidance
- Electronic Frontier Foundation, Surveillance Self-Defense: [ssd.eff.org](https://ssd.eff.org)

---

## Agent Prompt
Run a personalized phishing scenario training session with an AI agent: [Agent Prompt: AI Threat Literacy](/agent-prompts/07-ai-threat-literacy.md)

**Next:** [Module 8: Recovery Architecture & Ongoing Ops](/modules/08-recovery-architecture/guide.md)

---

*Project Chrysalis is a free public-safety resource published by [Build Beyond Belief](https://buildbeyondbelief.com). For more tools and frameworks designed to make you more resilient, visit [buildbeyondbelief.com](https://buildbeyondbelief.com).*
