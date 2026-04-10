# Agent Prompt: AI Threat Literacy
*Paste this prompt into Claude, ChatGPT, or any capable AI assistant. The agent will run a structured threat literacy training session with you.*

---

## Prompt

```
Run an AI threat literacy training session with me. I want to understand what AI-augmented attacks actually look like in 2026, practice recognizing manipulation attempts, and build a personal verification protocol.

Structure the session in four parts:

**Part 1: Accurate Threat Model (briefing, not fear-mongering)**

Start by giving me a clear, specific description of what Mythos-class AI agents can actually do as of 2026 — what's documented, not speculative. Cover:
- What they can find about a person from public sources alone
- What spear phishing looks like when it's AI-generated and personalized
- What voice cloning and video deepfakes currently look like — realistic capabilities, not sci-fi
- What they cannot do reliably yet

Be specific. Vague threat descriptions aren't useful. If a capability is documented, say what it is. If something is overstated by the media, say that too.

**Part 2: Phishing Scenario Training**

Present me with 3 scenarios. For each one:
1. Show me the scenario as it would appear to me (email text, voicemail description, text message)
2. Ask: "What would you do? Would you click, call, or comply? Why or why not?"
3. Wait for my response
4. Debrief: what were the tells, what should I have caught, what's the correct response

Scenarios should cover:
- A spear phishing email that references real details (ask me for my employer name and use it)
- A voice message from someone claiming to be a family member with an urgent financial request
- A text message alert claiming unusual activity on a financial account

Make the scenarios realistic — not obviously fake. The goal is to test my actual detection, not give me something a 10-year-old would spot.

**Part 3: Deepfake Recognition**

Describe for me — in specific, practical terms — the current tells to look for in a live deepfake video call. Then tell me honestly how long these heuristics will remain reliable.

Then give me 3 questions I can ask in any suspicious call that would be difficult for a deepfake or impersonation to answer convincingly.

**Part 4: Personal Verification Protocol**

Help me design my personal verification protocol. Ask me:
1. Who are the 2-3 people in my life whose impersonation would be most dangerous to me?
2. How do I normally communicate with each of them?
3. What would be an "out of pattern" request from each of them?

Then help me design:
- A backup contact channel for each person (if normal channel is unavailable)
- A verification phrase or signal I should establish with each — something not in any public record, not mentioned online, known only to us
- My 3 personal rules for verification — specific to how I live and who I communicate with

At the end of the session, summarize:
- My current threat detection calibration (where I was sharp, where I fell for it)
- My completed verification protocol
- The 2 habits I should build going forward
```

---

## How to Get the Most From This Session

**Before you start:** Tell the agent your employer name so the phishing scenario is realistic. Don't name your actual family members — use "my sibling" or "my parent."

**During the scenarios:** Respond the way you actually would, not the way you think you're supposed to. The value is in accurate self-assessment, not performing well.

**After the session:** Write down your 3 personal verification rules somewhere you'll remember them. Then — critically — have a short in-person or private call with your 1-2 verification anchor people and agree on the verification phrase. The phrase is only useful if both parties know it.

---

## Notes

- This module works best with a model that can simulate realistic social engineering. Claude and GPT-4 are both capable of generating convincing phishing scenarios for training purposes.
- The verification phrase should never be written in any chat log, cloud document, or email thread — agree on it verbally
- If you're skeptical about voice cloning: 30-second audio samples from voicemails, videos, or podcast appearances are sufficient for current voice cloning tools. Anyone with a public voice profile is already cloneable.
