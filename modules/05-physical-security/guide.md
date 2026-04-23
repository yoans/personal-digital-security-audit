# Module 5: Physical Security
*Attacks don't always start on a screen.*

Physical access bypasses most digital security controls. An attacker with 60 seconds alone with your unlocked device, or access to your mail, or knowledge of what's in your trash, has options no firewall can stop. Physical security is unglamorous and consistently neglected.

**Time required:** 1-2 hours to audit; some purchases may be needed  
**Output:** Physical security gaps identified and addressed

> **Your next move:** walk your home, mailbox, wallet, and travel kit while you read. Want a guided assessment with green/yellow/red status? Use the [Physical Security agent prompt](/agent-prompts/05-physical-security.md). Track items in the [Master Checklist](/worksheets/master-checklist.md).

---

## Mail & Documents

### Incoming Mail
Mail theft is a direct path to identity fraud. New credit cards, bank statements, insurance documents, and government correspondence all arrive by mail.

- **Locked mailbox:** Use one. If your current mailbox is unlocked, replace the lock or upgrade the box.
- **PO Box:** For highest-sensitivity mail (IRS, financial institutions, legal), a PO Box prevents theft entirely.
- **USPS Informed Delivery:** Free service that emails you preview images of your incoming mail each morning. You know what's coming before it arrives, and you'll know if something expected didn't arrive. Register at [informeddelivery.usps.com](https://informeddelivery.usps.com).
- Go paperless wherever possible. Bank statements, utility bills, and investment statements sent by email are far harder to steal.

### Outgoing Mail
Never put outgoing mail in an unsecured residential mailbox (the raised-flag method). Anyone walking by can take it. Use a USPS collection box or hand to a postal worker.

### Shredding
Anything with your name + any sensitive identifier (account number, SSN, DOB, address, signature) must be shredded before disposal.

- **Minimum:** cross-cut shredder (~$40)
- **Better:** micro-cut shredder (~$80-150), produces confetti-sized pieces that cannot be reconstructed
- **Shred:** bank statements, credit card offers, medical paperwork, old IDs, boarding passes, utility bills, tax documents (after retention period), prescription labels

### Document Storage
Keep originals of critical documents in a fireproof, water-resistant container or safe:
- Passport
- Birth certificate
- Social Security card (don't carry this in your wallet)
- Property deed / lease
- Vehicle title
- Will, trust documents, power of attorney
- Insurance policies
- Vaccination records

**Scan everything above.** Store encrypted copies in your password manager (Bitwarden supports file attachments) or an encrypted folder in your cloud storage. This lets you recover if the originals are lost.

---

## In Public

### Screen Privacy
- **Privacy screen filter** on your laptop if you work in cafes or open offices. Cheap ($20-40), effective, eliminates shoulder surfing entirely.
- Position your screen away from foot traffic when possible.
- Be aware of cameras, security cameras and phone cameras record at high resolution.

### Device Unattended
**Never leave your device unattended.** A 30-second window is enough to install a hardware keylogger or boot from a USB drive.

Common justification: "I'm just getting a coffee refill." That's exactly how long it takes. Take your device or lock it, don't assume the brief absence is safe.

If you must leave a laptop in a space briefly:
- Windows: `Win + L` to lock immediately
- Mac: `Ctrl + Cmd + Q` or close the lid (set to lock on sleep)
- Enable a login password on wake before relying on this

### PIN Entry
Be aware of who's behind you when entering PINs, passwords, or passcodes, ATM, phone, laptop, door code. Tilt your screen toward you or use your hand to shield the keypad.

### USB Charging
**Public USB charging ports can deliver malware.** This is called "juice jacking." Avoid public USB ports or use a USB data blocker (PortaPow, ~$10) which passes power but blocks data lines. Better: carry your own AC charger or a power bank.

---

## Travel

### Before You Leave
- Enable Find My (Apple) or Find My Device (Google) and verify it works
- Know your remote wipe procedure, practice it on a device you're wiping anyway
- Ensure your device has a strong passcode (not just biometric)
- Back up your device the day before travel

### With Your Device
- Keep devices with you, not in checked luggage
- Consider a cable lock for your laptop in hotel rooms (Kensington lock slots are on most laptops)
- Hotel room safes offer convenience, not security, they are not rated for theft resistance
- **Better: keep high-value items with you**

### Border Crossing
At international borders, your devices may be inspected and searched without a warrant in many jurisdictions (including returning to the US). Know your rights and risk tolerance.

Options for high-risk travel:
- **Travel device:** a separate laptop/phone with minimal data, nothing you can't afford to have inspected or seized
- **Clean device:** wipe and restore a device specifically for the trip; restore your data when you're home
- Log out of sensitive accounts before crossing; re-authenticate after

### Public WiFi
Use your phone's mobile hotspot instead of public WiFi when handling sensitive tasks. If you must use public WiFi, use a VPN (see Module 4).

---

## Credit Freeze

A credit freeze is one of the highest-leverage physical identity protection steps available. It prevents new credit lines from being opened in your name, even if an attacker has your SSN.

- **Free** at all three major bureaus
- Does not affect your existing credit or credit score
- You temporarily lift it when applying for credit, then re-freeze
- Do it now if you haven't

**Freeze at:**
- Experian: [experian.com/freeze](https://www.experian.com/freeze)
- Equifax: [equifax.com/personal/credit-report-services/free-credit-freeze](https://www.equifax.com/personal/credit-report-services/free-credit-freeze)
- TransUnion: [transunion.com/credit-freeze](https://www.transunion.com/credit-freeze)

Also freeze at:
- **ChexSystems:** used by banks for checking/savings accounts: [chexsystems.com/security-freeze](https://www.chexsystems.com/security-freeze)
- **NCTUE:** used by some utility providers: [nctue.com](https://www.nctue.com)

Store your freeze PINs in your password manager.

---

## Checklist

**Mail & Documents:**
- [ ] Locked mailbox or PO box for sensitive mail
- [ ] USPS Informed Delivery active
- [ ] Cross-cut shredder in use for sensitive documents
- [ ] Critical documents in fireproof container
- [ ] Critical documents scanned and stored encrypted

**In Public:**
- [ ] Screen privacy filter on laptop (or habit of positioning screen)
- [ ] Never leave device unattended in public
- [ ] Aware of shoulder surfing on PIN/password entry
- [ ] Not using public USB charging ports unprotected

**Travel:**
- [ ] Find My / Find My Device active
- [ ] Remote wipe procedure known
- [ ] Travel device policy in place for high-risk destinations

**Credit & Identity:**
- [ ] Credit freeze placed at Experian, Equifax, TransUnion
- [ ] ChexSystems freeze placed
- [ ] Freeze PINs stored in password manager

---

## Tools

| Tool | Use | Link |
|---|---|---|
| USPS Informed Delivery | Mail preview notifications | [informeddelivery.usps.com](https://informeddelivery.usps.com) |
| Experian Freeze | Credit freeze | [experian.com/freeze](https://www.experian.com/freeze) |
| Equifax Freeze | Credit freeze | [equifax.com/personal/credit-report-services/free-credit-freeze](https://www.equifax.com/personal/credit-report-services/free-credit-freeze) |
| TransUnion Freeze | Credit freeze | [transunion.com/credit-freeze](https://www.transunion.com/credit-freeze) |
| PortaPow USB Blocker | Blocks data on USB charge cables | Available on Amazon |

---

## Agent Prompt
[Agent Prompt: Physical Security](/agent-prompts/05-physical-security.md)

**Next:** [Module 6: Social Attack Surface](/modules/06-social-attack-surface/guide.md)

---

*Project Chrysalis is a free public-safety resource published by [Build Beyond Belief](https://buildbeyondbelief.com). For more tools and frameworks designed to make you more resilient, visit [buildbeyondbelief.com](https://buildbeyondbelief.com).*
