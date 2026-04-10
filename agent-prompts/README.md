# Agent Prompts

Each file in this folder is a prompt you can paste into Claude, ChatGPT, Gemini, or any capable AI assistant to get interactive, personalized help working through that module.

The prompts are designed to be:
- **Interactive** — the agent asks you questions rather than lecturing
- **Personalized** — outputs are based on your specific situation, not generic advice
- **Actionable** — each session ends with something you can save and act on

---

## Prompts

| Module | What the Agent Does | File |
|---|---|---|
| 1 — Identity Inventory | Walks you through categories of accounts you may have forgotten; outputs a structured inventory table | [01-identity-inventory.md](01-identity-inventory.md) |
| 2 — Dependency Graph | Maps which accounts are hubs and what breaks if each falls; surfaces single points of failure | [02-dependency-graph.md](02-dependency-graph.md) |
| 3 — Credential Architecture | Audits your current password manager, 2FA, and emergency access setup; gives prioritized fixes | [03-credential-architecture.md](03-credential-architecture.md) |
| 4 — Device & Network | Walks through your laptop, phone, router, and IoT devices; outputs a device table and fix list | [04-device-network.md](04-device-network.md) |
| 5 — Physical Security | Assesses mail, documents, in-public habits, travel, and credit freezes; gives green/yellow/red status | [05-physical-security.md](05-physical-security.md) |
| 6 — Social Attack Surface | Gives you exact search strings to OSINT yourself; walks through data broker removal and social media audit | [06-social-attack-surface.md](06-social-attack-surface.md) |
| 7 — AI Threat Literacy | Runs phishing scenario training; helps you build your personal verification protocol | [07-ai-threat-literacy.md](07-ai-threat-literacy.md) |
| 8 — Recovery Architecture | Builds your personal incident response playbook through interactive scenario walkthroughs | [08-recovery-architecture.md](08-recovery-architecture.md) |

---

## How to Use

1. Open the prompt file for the module you're working on
2. Copy the text inside the code block labeled `Prompt`
3. Paste it into your AI assistant of choice
4. Answer the questions honestly — the value is in accurate self-assessment, not performing well
5. Save the output somewhere accessible (your password manager, a secure note, a printed document)

---

## Which AI to Use

Any capable frontier model works. For sensitive context:
- **Avoid pasting real passwords, SSNs, or financial account numbers** — ever, in any chat
- For the Social Attack Surface module: you'll be asked for your name and city — this is fine in a private chat session, but be aware of your AI provider's data retention policies
- Claude and GPT-4-class models handle the scenario-based modules (6, 7, 8) particularly well

---

## Privacy Note

These prompts ask you to share personal context with an AI assistant. What you share is subject to that provider's privacy policy. For the most sensitive work:
- Use a model running locally (Ollama + Llama 3 or similar) if you're privacy-conscious
- Or use the module guides directly without the AI prompts — they're complete standalone resources
