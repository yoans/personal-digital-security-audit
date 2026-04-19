# Agent Prompt: Device & Network Baseline
*Paste this prompt into Claude, ChatGPT, or any capable AI assistant. The agent will walk you through a device and network security baseline audit.*

---

## Prompt

```
Help me do a device and home network security baseline audit. Walk me through each category by asking questions, then give me a specific fix list sorted by risk and estimated time to fix.

Go through each of these areas:

**1. Primary Laptop/Desktop**
- What OS are you running? (Windows/Mac/Linux, version)
- Is full disk encryption enabled? (BitLocker on Windows, FileVault on Mac)
- What's your screen lock timeout? Does it require a password on wake?
- Are OS updates automatic, or do you manually update?
- What browser do you primarily use? Have you reviewed your extensions recently?
- What applications start automatically when you log in?
- Is anything signed in on this machine that shouldn't be (old accounts, work accounts on personal machines, etc.)?

**2. Phone**
- What phone and OS are you using?
- What's your current passcode type? (6-digit PIN, alphanumeric, just biometric)
- When did you last review which apps have "always on" location access?
- When did you last delete apps you no longer use?
- Is your phone backed up? When was it last backed up?
- Is it backed up with encryption enabled?

**3. Home Router**
- Do you know your router's brand and model?
- Have you ever changed the router's admin login from the default?
- When did the router last get a firmware update? Does it auto-update?
- Do you have a guest network set up?
- Is WPS (Wi-Fi Protected Setup) enabled? (Most should disable this)
- Have you changed your Wi-Fi network name from the factory default?

**4. IoT and Smart Home Devices**
- What smart home devices are on your network? (cameras, smart speakers, smart locks, thermostats, smart TVs, appliances)
- Are these devices on your main network or isolated on a guest network?
- Have you changed the default login credentials on any of them?
- Do you know whether they've received firmware updates recently?

**5. Additional Devices**
- Any other computers, tablets, or secondary phones?
- Any network-attached storage devices (NAS)?
- Any work devices that also have personal accounts on them?

After I've answered, give me:

1. A device inventory table: Device | OS/Firmware | Encryption | Updates | Network | Status

2. A prioritized fix list:
   - **Fix today (under 10 minutes each):** quick wins with high impact
   - **Fix this week:** things that require a little more work
   - **Fix this month:** things that may require purchases or planning

For each fix, give me the specific steps or tell me exactly what to search for to find the setting.

Be specific. "Enable encryption" isn't useful, "Go to Settings → Privacy & Security → FileVault → Turn On" is.
```

---

## What to Do With the Output

1. Save the device inventory table, update it quarterly (Module 8)
2. Run Fing ([fing.com](https://www.fing.com)) on your phone while on your home network, you'll almost certainly find devices you forgot were connected
3. If your router is more than 4 years old and the manufacturer hasn't released firmware updates in 2 years: seriously consider replacing it

---

## Notes

- For Windows encryption status: type "BitLocker" into the Start menu search bar
- For Mac FileVault: System Settings → Privacy & Security → FileVault
- Router admin panel is usually at `192.168.1.1` or `192.168.0.1` in your browser, check your network settings for "Default Gateway" if neither works
- Don't give the AI your router admin password or Wi-Fi credentials
