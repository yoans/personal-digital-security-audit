# Agent Prompts

Each file in this folder is a prompt you can paste into Claude, ChatGPT, Gemini, or any capable AI assistant to get interactive, personalized help working through that module.

The prompts are designed to be:
- **Interactive:** the agent asks you questions rather than lecturing
- **Personalized:** outputs are based on your specific situation, not generic advice
- **Actionable:** each session ends with something you can save and act on

---

## Read This First: Privacy

> **Do not make yourself less secure by using these prompts carelessly.**

These prompts ask you to share personal information about your accounts, devices, and habits with an AI. Before you start, decide how you're going to do this safely.

**Option A: Use a local model (recommended for sensitive work)**

A local model runs entirely on your machine. Your data never leaves your device. No company stores it, trains on it, or can be breached to expose it.

| Tool | Difficulty | Notes |
|---|---|---|
| **[Ollama](https://ollama.com) + Llama 3** | Easy | One-command install. Mac, Linux, Windows. Great for all 8 modules. |
| **[LM Studio](https://lmstudio.ai)** | Easy | GUI app. Download a model, start chatting. No command line needed. |
| **[Jan](https://jan.ai)** | Easy | Open source desktop chat app. Clean and simple. |

**Option B: Use a hosted model carefully**

If you use Claude, ChatGPT, or Gemini:
- **Never paste:** passwords, SSNs, financial account numbers, recovery codes, carrier PINs, or master password hints
- **Acceptable to share:** service names (Gmail, Netflix), general device types, general habits, your city
- **Check your provider's data retention policy:** some retain conversations for training by default; some let you opt out
- **Delete the conversation when you're done** if your provider allows it

**Option C: Skip the AI**

The module guides are complete standalone resources. Every module can be worked through without an AI assistant. The prompts are an accelerator, not a requirement.

---

## Prompts

| Module | What the Agent Does | File |
|---|---|---|
| 1, Identity Inventory | Walks you through categories of accounts you may have forgotten; outputs a structured inventory table | [01-identity-inventory.md](01-identity-inventory.md) |
| 2, Dependency Graph | Maps which accounts are hubs and what breaks if each falls; surfaces single points of failure | [02-dependency-graph.md](02-dependency-graph.md) |
| 3, Credential Architecture | Audits your current password manager, 2FA, and emergency access setup; gives prioritized fixes | [03-credential-architecture.md](03-credential-architecture.md) |
| 4, Device & Network | Walks through your laptop, phone, router, and IoT devices; outputs a device table and fix list | [04-device-network.md](04-device-network.md) |
| 5, Physical Security | Assesses mail, documents, in-public habits, travel, and credit freezes; gives green/yellow/red status | [05-physical-security.md](05-physical-security.md) |
| 6, Social Attack Surface | Gives you exact search strings to OSINT yourself; walks through data broker removal and social media audit | [06-social-attack-surface.md](06-social-attack-surface.md) |
| 7, AI Threat Literacy | Runs phishing scenario training; helps you build your personal verification protocol | [07-ai-threat-literacy.md](07-ai-threat-literacy.md) |
| 8, Recovery Architecture | Builds your personal incident response playbook through interactive scenario walkthroughs | [08-recovery-architecture.md](08-recovery-architecture.md) |

---

## How to Use

1. Open the prompt file for the module you're working on
2. Copy the text inside the code block labeled `Prompt`
3. Paste it into your AI assistant of choice
4. Answer the questions honestly, the value is in accurate self-assessment, not performing well
5. Save the output somewhere accessible (your password manager, a secure note, a printed document)

---

## Which AI to Use

For **Modules 1-5** (inventory, mapping, device audit): any capable model works, including local models. These are structured Q&A, even a smaller local model handles them well.

For **Modules 6-8** (social attack surface, AI threat literacy, recovery): a frontier model (Claude, GPT-4-class) produces substantially better scenarios and analysis. If you're comfortable with the privacy tradeoffs, this is where hosted models add the most value.

**For maximum privacy:** Use Ollama with Llama 3 70B (or 8B on lighter hardware). Install: `curl -fsSL https://ollama.com/install.sh | sh && ollama run llama3`.

---

## Privacy Reminder

Every prompt in this folder includes a notes section reminding you what not to share. But the overarching rules are simple:

1. **If it could be used to take over an account, don't type it into a chat**
2. **If you're not sure, use a local model**
3. **If you don't want to use AI, the guides work on their own**

---

## Ready to Start?

Pick the module you're working on right now. The agent prompts are most useful when you have the matching module guide open in another tab.

> **→ New to the audit?** Start with **[Module 1: Identity Inventory](/modules/01-identity-inventory/guide.md)** and use the [Identity Inventory agent prompt](01-identity-inventory.md) alongside it.

Or jump back to the [Home page](/) or [Master Checklist](/worksheets/master-checklist.md).
