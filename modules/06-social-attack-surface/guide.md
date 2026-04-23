# Module 6: Social Attack Surface
*OSINT yourself before someone else does.*

An AI agent doing recon on you will, starting from your name and a general location, find your address history, family members, employer history, phone numbers, email addresses, and likely political and religious affiliations, in under ten minutes, for free, from public sources. Most people have no idea how much is available. This module is about finding out, then reducing it.

**Time required:** 2-3 hours initial audit; data broker removal is ongoing  
**Output:** A clear picture of your public exposure; a removal plan

> **Your next move:** run the searches in this guide on yourself, in a private browser window, before doing anything else. Want exact search strings and a removal plan? Use the [Social Attack Surface agent prompt](/agent-prompts/06-social-attack-surface.md).

---

## What's Available About You Right Now

From data brokers and public records (no hacking required):
- Full legal name and all known aliases
- Current and historical addresses (often 10+ years)
- Phone numbers, current and historical
- Email addresses
- Family members and their relationships
- Employer history
- Associated court records (civil and criminal, public in most states)
- Property records and estimated home value
- Voter registration data (in many US states, this is fully public)
- Vehicle registration (some states)
- Professional licenses

From social media and web presence:
- Photos (yours and tagged photos of you from others)
- Geolocation metadata from photos you posted
- Timeline of where you've been (check-ins, event RSVPs)
- Your relationship network
- Political and religious views (from posts, likes, group memberships)
- Work history, education, skills
- Posts and comments you thought were private but weren't

From data breaches:
- Email addresses and passwords from past breaches
- Security question answers
- Old phone numbers

---

## Step 1: OSINT Yourself

Run these searches as if you were a stranger trying to build a dossier:

**Google searches:**
```
"[Your Full Name]" "[Your City]"
"[Your Full Name]" "[Your Employer]"
"[Your Full Name]" site:linkedin.com
"[Your Full Name]" site:facebook.com
"[Your Full Name]" "[Your Phone Number]"
"[Your Email Address]"
```

**Image search:**
- Upload your profile photo to [Google Images](https://images.google.com) and [TinEye](https://tineye.com) (reverse image search)
- This shows every site where that photo appears and any similar photos, relevant if you've used the same photo across services

**Breach check:**
- [HaveIBeenPwned](https://haveibeenpwned.com), all your email addresses
- Firefox Monitor, ongoing monitoring

**Username search:**
- [Sherlock](https://github.com/sherlock-project/sherlock), open source CLI tool that searches 300+ sites for a username
- [WhatsMyName](https://whatsmyname.app), web-based alternative

**Data broker spot check:**
Visit and search your name on these manually to gauge your exposure:
Spokeo, Whitepages, Radaris, BeenVerified, Intelius, Instant Checkmate, TruthFinder, MyLife, FamilyTreeNow

---

## Step 2: Data Broker Removal

Data brokers aggregate and sell your personal information. You have the legal right to opt out. It's tedious but effective over time.

**Manual removal (free):**
Each broker has an opt-out form, typically buried deep in their site. Search: `[broker name] opt out` or `[broker name] remove my information`.

Top 20 to prioritize:
Spokeo, Whitepages, Intelius, BeenVerified, Radaris, US Search, MyLife, Pipl, FamilyTreeNow, Addresses.com, AnyWho, CheckPeople, ClustrMaps, IdCrawl, Instant Checkmate, PeekYou, PublicInfoServices, SearchPeopleFree, TruthFinder, ZabaSearch

Track your submissions in a spreadsheet, many re-list you after 30-90 days and you'll need to re-submit.

**Automated removal (paid):**
Services that submit opt-outs on your behalf and re-submit when you're re-listed:

| Service | Annual Cost | Notes |
|---|---|---|
| **Incogni** (Surfshark) | ~$70/yr | Covers 180+ brokers, good transparency reporting |
| **DeleteMe** | ~$130/yr | Long-established, human verification, detailed reports |
| **Kanary** | ~$90/yr | Strong monitoring, notifies when you reappear |

Worth it if your time has any value. These services don't cover everything, but they dramatically reduce the surface.

**Realistic expectation:** You will not disappear. The goal is raising the cost and difficulty of building a useful dossier on you. Every source you remove is a data point an attacker has to go without.

---

## Step 3: Social Media Audit

For each platform you're on, review:

**Privacy settings:**
- Who can see your posts? (Public / friends / custom)
- Who can see your friends/followers list?
- Who can see your check-ins and tagged locations?
- Who can see posts you're tagged in?
- Who can search for you by email/phone?
- Is your profile photo reverse-searchable? Consider using a different photo on public vs. personal accounts.

**Past posts:**
- Location data in posts, was auto-location tagging on? Many old posts may have precise location embedded
- Old posts that expose information you'd rather not have public (home address, workplace, family member names, opinions you no longer hold)
- Photos posted that contain visible addresses, license plates, or location clues in the background

**Specific platform guides (search for current instructions as these change):**
- Facebook: Settings & Privacy → Privacy Shortcuts
- Instagram: Settings → Account → Privacy
- LinkedIn: Settings → Privacy, note: LinkedIn is a significant professional OSINT source and most of it is intended to be public; focus on what you can control
- Twitter/X: Settings → Privacy and Safety

---

## Step 4: Reduce Future Exposure

**Email aliases:**
Never give your real email address to services you don't fully trust. Use an alias, when that alias gets spammed or breached, you delete it and create a new one, without any impact on your real address.

- **SimpleLogin:** open source, aliases forwarded to your real address, free tier, [simplelogin.io](https://simplelogin.io)
- **Apple Hide My Email:** works within Apple ecosystem, easy
- **Fastmail + aliases:** good if you pay for Fastmail

**Phone number:**
- Don't give your real mobile number to every service. Use a **Google Voice** or **Hushed** number as your "public" number for signups and services.
- Keep your real carrier number for people who actually need to reach you.

**Real-time location:**
- Don't post photos at a location while you're still there
- Disable location metadata in your phone's camera: Settings → Camera → GPS/Location (varies by OS)
- Review which apps have continuous location tracking and disable where unnecessary (see Module 4)

**Separate personas where appropriate:**
If you maintain a professional presence and personal social presence, consider using different usernames that aren't cross-linkable. Don't use the same avatar across both.

---

## Checklist

**OSINT audit completed:**
- [ ] Google searches run on your name + city, email, phone
- [ ] Reverse image search done on your common profile photo
- [ ] All email addresses checked on HaveIBeenPwned
- [ ] Username search run on Sherlock or WhatsMyName
- [ ] Top 5 data brokers checked manually for your info

**Removal in progress:**
- [ ] Manual opt-outs submitted to top 20 brokers (or automated service enrolled)
- [ ] Removal submissions tracked in a spreadsheet or tool

**Social media hardened:**
- [ ] Privacy settings reviewed on all active platforms
- [ ] Old location-tagged posts reviewed
- [ ] Auto-location tagging on posts disabled going forward

**Ongoing exposure reduced:**
- [ ] Email alias strategy in place for new signups
- [ ] Public phone number separate from real carrier number
- [ ] Camera location metadata disabled
- [ ] USPS Informed Delivery active (if not done in Module 5)

---

## Tools

| Tool | Use | Link |
|---|---|---|
| HaveIBeenPwned | Breach check for email addresses | [haveibeenpwned.com](https://haveibeenpwned.com) |
| Sherlock | Username search across 300+ platforms (CLI) | [github.com/sherlock-project/sherlock](https://github.com/sherlock-project/sherlock) |
| WhatsMyName | Web-based username search | [whatsmyname.app](https://whatsmyname.app) |
| TinEye | Reverse image search | [tineye.com](https://tineye.com) |
| SimpleLogin | Email aliasing | [simplelogin.io](https://simplelogin.io) |
| Incogni | Automated data broker removal | [incogni.com](https://incogni.com) |
| DeleteMe | Automated data broker removal + reports | [joindeleteme.com](https://joindeleteme.com) |
| Google Voice | Free second phone number | [voice.google.com](https://voice.google.com) |

---

## Agent Prompt
[Agent Prompt: Social Attack Surface](/agent-prompts/06-social-attack-surface.md)

**Next:** [Module 7: AI Threat Literacy](/modules/07-ai-threat-literacy/guide.md)

---

*Project Chrysalis is a free public-safety resource published by [Build Beyond Belief](https://buildbeyondbelief.com). For more tools and frameworks designed to make you more resilient, visit [buildbeyondbelief.com](https://buildbeyondbelief.com).*
