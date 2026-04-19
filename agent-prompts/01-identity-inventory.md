# Agent Prompt: Identity Inventory
*Paste this prompt into Claude, ChatGPT, or any capable AI assistant. The agent will walk you through building a complete account inventory.*

---

## Prompt

```
I need help building a complete inventory of every account associated with my digital identity. I want you to act as a thorough assistant, ask me questions to uncover accounts I may have forgotten, then help me organize the results into a usable format.

Start by asking me:
1. What email addresses do you actively use?
2. What email addresses have you used in the past, even if abandoned?
3. What phone numbers have you had in the last 10 years?

After I answer, walk me through these categories one at a time, asking if I have accounts in each. Don't lecture, just ask, let me answer, and log what I confirm:

- Email providers (Gmail, Outlook, Yahoo, AOL, Hotmail, school, work, old domains)
- Social media (Facebook, Instagram, Twitter/X, LinkedIn, TikTok, Snapchat, Pinterest, Reddit, Tumblr)
- Banking and finance (banks, credit cards, investment accounts, crypto, PayPal, Venmo, CashApp, Zelle)
- Shopping (Amazon, eBay, Etsy, Target, Walmart, old retail accounts, subscription boxes)
- Streaming and entertainment (Netflix, Spotify, Apple Music, Hulu, Disney+, YouTube Premium, gaming platforms)
- Gaming (Steam, PlayStation Network, Xbox Live, Nintendo, Battle.net, Epic, old MMOs or mobile games)
- Health and fitness (insurance portals, MyFitnessPal, Strava, gym apps, telehealth, pharmacy accounts)
- Travel (airlines, hotels, car rental, Airbnb, booking sites, travel credit cards)
- Work and professional (GitHub, Slack, Jira, LinkedIn, old employers' tools, freelance platforms)
- Government and utilities (IRS, DMV, Social Security, utility providers, local government portals)
- News, forums, and communities (paywalled sites, hobby forums, Discord servers, newsletters with accounts)
- Other subscriptions or services I haven't covered

For each account I confirm, add it to a running list with these columns:
- Service
- Email address used
- Approximate year created
- Status (Active / Dormant / Unknown)
- Whether I've logged in in the last year (Yes / No / Unsure)

When we've finished all categories, output the full list as a markdown table. At the end, flag any services I mentioned where I don't know the email used, those are the ones worth searching for in my inbox.
```

---

## What to Do With the Output

1. Copy the generated table into a spreadsheet (Google Sheets, Excel, or a secure local file)
2. Add two columns: **Criticality** (Hub / Leaf) and **2FA Enabled:** you'll fill these in during Module 2
3. Run every email address in the table through [HaveIBeenPwned.com](https://haveibeenpwned.com)
4. For any dormant accounts: delete them using [JustDeleteMe.com](https://justdeleteme.com)

---

## Notes

- Do not paste actual passwords into the AI chat
- This is a discovery exercise, accuracy matters more than speed
- If the AI misses a category relevant to your life (professional licenses, church platforms, parenting apps, etc.) add it manually
