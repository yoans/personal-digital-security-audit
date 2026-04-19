# Agent Prompt: Dependency Graph
*Paste this prompt into Claude, ChatGPT, or any capable AI assistant. The agent will help you map which accounts are hubs and what breaks if each one falls.*

---

## Prompt

```
I've completed a basic account inventory and I need help mapping out my dependency graph, which of my accounts are "hubs" that could cascade into others if compromised, and which are standalone "leaf" accounts.

Here is my account list:
[PASTE YOUR MODULE 1 ACCOUNT TABLE HERE]

For each account, I want you to ask me:
1. What email address is used for password reset?
2. What phone number is used for 2FA or recovery (if any)?
3. Is this account used to log into other services (Google, Apple, Facebook SSO)?
4. Do I have 2FA on this? If so, what type? (SMS / authenticator app / hardware key / none)
5. If I lost access to this account today, what else would I lose access to?

Work through each account systematically. Don't rush, some of these answers will surface things I haven't thought about.

After we've been through all accounts, give me:

1. A dependency map table with columns: Account | Type (Hub/Leaf) | Resets Via | 2FA Method | Blast Radius (what collapses if this falls)

2. A list of my single points of failure, accounts where losing access or having it compromised would cause disproportionate damage

3. A red flag list, prioritized by severity:
   - Any hub accounts using SMS as 2FA (SIM swap vulnerable)
   - Any account where the phone number is the ONLY recovery method
   - Any old email addresses I don't control used as recovery for active accounts
   - Any account with no 2FA at all that has high blast radius

4. My recovery chain: trace the path an attacker would take to get from my most vulnerable account to my most critical one

Be direct. If something is a critical gap, say so clearly.
```

---

## What to Do With the Output

1. Add the dependency map table to your account inventory spreadsheet
2. Sort the red flag list, tackle Priority 1 items (SMS on hubs) this week in Module 3
3. Call your mobile carrier this week and add an account PIN and/or number lock, even before you fix the 2FA

---

## Notes

- If you have more than ~20 accounts, work through the hub accounts first (email, phone, Apple/Google ID, password manager, banking), these are the ones that matter most
- Your phone number often appears as a hidden hub even if it's not an "account", include it explicitly in the analysis
- Do not paste passwords into the AI chat
