# Agent Prompt: Recovery Architecture
*Paste this prompt into Claude, ChatGPT, or any capable AI assistant. The agent will help you build a personal incident response playbook.*

---

## Prompt

```
Help me build a personal incident response playbook, a clear set of procedures I can follow if any of my accounts, devices, or identity are compromised. I want you to work through this with me interactively, not just give me generic advice.

We'll go through three scenarios. For each one, I'll tell you what I would do, and you'll fill in what I'm missing, correct what I'd do wrong, and help me build the actual procedure.

**Scenario 1: Your phone is stolen right now**

Ask me: "Walk me through the first 5 things you'd do if your phone were stolen right now."

I'll answer. Then:
- Tell me what I got right
- Tell me what I missed or would do in the wrong order
- Give me the complete, correct 8-step response procedure for this scenario
- Flag any gaps in my setup that this scenario revealed (e.g., "You mentioned you'd remote wipe but you're not sure Find My is enabled, that needs to be fixed before you close this session")

**Scenario 2: Your email account is compromised**

Ask me: "You just got an alert that someone logged into your email from another country, and you can still get in. Walk me through what you'd do."

I'll answer. Then do the same, validate, correct, give me the complete procedure. Also ask me:
- Do you know where to find the active sessions list in your email?
- Do you know where to find the email forwarding rules?
- Do you have a trusted backup email set up as recovery?

**Scenario 3: Someone has opened a credit card in your name**

Ask me: "You check your credit report and find an account you didn't open. Walk me through what you'd do."

I'll answer. Then give me the specific steps, in order, including which agencies to contact, what documentation to prepare, and what legal protections I have.

After all three scenarios:

**Build my quarterly review cadence**

Ask me:
- How much time can you realistically commit to a security review every 3 months?
- What calendar system do you use?

Then give me a quarterly review checklist tailored to what we've discussed, not a generic list, but one that covers the specific gaps we found today. Format it so I can copy it into a recurring calendar event or task list.

**Run a mini breach drill**

Give me one specific, realistic scenario to walk through as a drill right now, something I haven't done yet. Walk me through it step by step and tell me if I have everything I need to complete it successfully.

At the end of the session, give me my complete playbook as a markdown document I can save, all three scenario procedures, the quarterly checklist, and any outstanding gaps I need to fix.
```

---

## What to Do With the Output

1. **Save the playbook.** Store it somewhere you can access even if your phone and primary devices are unavailable, printed copy in your emergency document folder, or in a secure note in your password manager.
2. **Test Find My / Find My Device right now.** Open the remote location service on another device and verify your devices show up. A remote wipe that's never been tested may not work when you need it.
3. **Share the relevant parts.** Your partner, family members, or emergency contact should know what to do if you're unavailable. The "lost phone" procedure should be known to anyone who might need to act on your behalf.

---

## Things to Resolve Before Running This Session

- Know which email is set as your backup/recovery for your primary account
- Have your backup codes accessible (or know you don't have them, that gap will come up)
- Know whether Find My / Find My Device is currently enabled on your phone
- Know your carrier's account PIN (you'll need it for the stolen phone scenario)

---

## Notes

- The more honestly you answer the scenario questions, the more useful the session is. If you don't know what you'd do, say that. That's the gap to fix.
- If you want to run the stolen phone scenario as a real drill: on an old device you're not using, go through the actual remote wipe process. Knowing the steps from memory is different from having done it.
- The quarterly checklist output from this session should be reviewed against the full Module 8 checklist and updated as your setup evolves.
