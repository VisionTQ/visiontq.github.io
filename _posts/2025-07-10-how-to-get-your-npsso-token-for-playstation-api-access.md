---
title: How to Get Your NPSSO Token for PlayStation API Access
date: 2025-07-10
author: tnebula
categories:
  - psntools
tags:
  - npsso
  - psnawp
  - psn-api
  - psn
  - token
  - privacy
  - playstation
image: https://i.imgur.com/7z6R31U.png
description: Learn how to extract your NPSSO token to access private PlayStation APIs like PSNAWP. This guide covers what NPSSO is, what data it can access, potential risks, safe tools, and how to automate the process.
---

## Get NPSSO to Access PlayStation APIs

> ⚠️ **Need help or have questions?**  
> Join our Discord server and ask in the support channels: [Nebula0 - Discord](https://nebula0.com/discord)  
> This guide is community-maintained. If you're unsure about any step, it's safer to ask first.  
{: .prompt-warning }

The NPSSO token lets you access private PlayStation APIs like [PSNAWP](https://github.com/Tustin/psnawp). These APIs can be used to:

- View user profile info
- Check friends list and online status
- Get trophy data
- Access game metadata
- Track PSN activity
- & more

---
## Get Your NPSSO Token

1. Log in to [playstation.com](https://www.playstation.com/) using your browser. (Log out then log back in to refresh the Token)
2. Then go to this link to extract your token:[https://ca.account.sony.com/api/v1/ssocookie](https://ca.account.sony.com/api/v1/ssocookie)

You’ll see:

```json
{ "npsso": "your_64_character_token_here" }
```

Copy the token. it should be valid for 60 days.

---
## What NPSSO Can Access

The NPSSO token gives limited access to your PlayStation account data. According to [psntools.com](https://www.psntools.com/outreach/privacy-policy), here’s what it can and cannot access:

| Data Point                              | Accessed |
|----------------------------------------|----------|
| Account/Login Email                    | ✅ Yes   |
| Account/Login Password                 | ❌ No    |
| Personal Profile Picture               | ✅ Yes   |
| Real Name                              | ✅ Yes   |
| Account Devices                        | ✅ Yes   |
| Credit Cards / Payment Details         | ❌ No    |
| All Transactions History               | ✅ Yes   |
| 2-Step Verification Phone Number       | ❌ No    |
| Exact Date of Birth                    | ✅ Yes   |
| Verification Status                    | ✅ Yes   |
| Cart Items                             | ✅ Yes   |

This information helps clarify what level of privacy is maintained when using your NPSSO for third-party API tools.

---
## ❓ Frequently Asked Questions

### Q1: Are there any risks if someone gains access to my NPSSO?

Yes, if someone gets your NPSSO token, they can extract sensitive account data. This includes your transaction history, real name, profile picture, date of birth, and other details tied to your PSN identity.

Even though they can’t directly log in or change your password, they **can log your transaction IDs**. If they contact Sony support pretending to be you and provide these transaction details, they may be able to **recover your account through social engineering**.

⚠️ Never paste your NPSSO on untrusted websites. Treat it like a password. Only use it with safe, known tools, ideally open-source ones you can inspect.

---

### Q2: Can I use NPSSO with official PlayStation services?

No. NPSSO is only used with **unofficial, reverse-engineered APIs** like:

- [`psn-api`](https://github.com/Tustin/psn-api)
- [`psnawp`](https://github.com/Tustin/psnawp)
- Other tools that simulate PlayStation’s internal requests

You **cannot** use NPSSO with Sony’s official API endpoints or developer portals, since Sony has not made any public-facing API that supports it. NPSSO is meant for internal cookie-based session auth. These tools just repurpose it for personal use.

---

### Q3: Is there an easier way to get my NPSSO without copying it manually every time?

Yes. You can simplify the process by creating & using a **browser extension**. You can create one that:

- Detects when you're signed into `playstation.com` or signs you in.
- Extracts the NPSSO cookie from your current session
- Displays or copies the token instantly

This makes it much faster than manually visiting the NPSSO URL each time.

⚠️ **Only use trusted tools**. never use apps or websites that ask for your NPSSO unless they are open-source or verifiable (e.g. hosted on GitHub). Avoid exe files or applications that offer cosmetic changes like custom avatars if they require your `NPSSO` or your `pdccws_P`



## Safe open source tools

[PSNToolBot](https://github.com/hzhreal/PSNToolBot) - Discord bot used to mainly add PlayStation 3 avatars to shopping cart, and obtain PlayStation account id from username. Made by [@hzhreal](https://github.com/hzhreal)

More safe tools will be added soon.
