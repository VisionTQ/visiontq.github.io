---
title: "Leaked: Full Internal PlayStation Account Closure Criteria"
date: 2025-06-01
description: A leaked internal list from PlayStation Support reveals the full criteria for PSN account closures, suspensions, and bans. Also with how support agents handle each case behind the scenes.
comments: true
author: tnebula
categories:
  - psntools
tags:
  - psn
  - bans
  - sony support
  - salesforce
  - customer service
  - compromised account
  - chargeback
  - suspension
image: https://i.imgur.com/A2yfQ9n.png
image_alt: Internal PlayStation dropdown showing account closure reasons
hidden: true
---

So this is something interesting I got my hands on - a leaked reason list used by PlayStation Support. I received it thanks to a few people who chose to stay anonymous, so I won’t mention their names here.

They gave me an image showing the PlayStation support screen, and the alias shown on it was **"NP-PACMAN"**.

The links involved seem to be:

> [https://sie-calypso.lightning.force.com](https://sie-calypso.lightning.force.com)  
> [https://sie-calypso.lightning.force.com?](https://sie-calypso.lightning.force.com?)

These lead to a Salesforce Lightning instance, which is used by **Sony Interactive Entertainment (SIE)** - yep, the company behind PlayStation. If you don’t know what Salesforce is: it's basically a cloud platform a lot of companies use to manage things like customer support, internal systems, and business operations.

Here’s what the domain tells us:

- `lightning.force.com`: That’s the main Salesforce domain for custom internal apps.
- `sie-calypso`: This is SIE’s custom subdomain. “Calypso” could be a codename for one of their systems or environments.

If you try visiting the link, you’ll just see a login screen - it’s private and locked down for SIE staff or partners. Basically, not meant for public use.

> I also posted this on Reddit if you want to see the PACMAN image directly: [Reddit – r/PlayStation](https://www.reddit.com/r/playstation/s/wFUmpLU34D)

## PlayStation Outsources Support

Sony outsources their customer support. Meaning, the people who help you when you contact PlayStation support are not Sony employees - they’re from third-party companies.

## Leaked Reasons for PSN Account Actions

Here’s the raw list of ban or suspension reasons that can happen to PlayStation Network (PSN) accounts. It includes notes on how bans are handled and what you can (or can’t) do about them:

---

**1. Account Closure**  
You’ll need to call support and ask to cancel the account closure. Sometimes they’ll ask for an ID card.

**2. Chargeback**  
You need to go to the link for appealing chargebacks and pay the money you reversed.

**3. Community Standard Abuse**  
You need to log in on the appeal site and appeal the suspension.

**4. Compromise**  
You’ll have to send in your ID card to prove you’re the real owner of the account.

**5. Customer Withdrawal**  
Same thing - you’ll need to send in your ID card.

**6. Dormant Account**  
You need to call support. This is what they call the "100 year ban."

**7. Exploitation / Hacking**  
If you installed a jailbreak or hacked games, they probably won’t unban you unless someone else logged into your account without permission.

**8. Fraud**  
You need to call them a lot. This kind of ban is random and different agents handle it differently based on what they told me.

**9. Harassment**  
No luck for this one. They won’t unban the account unless you claim it was hacked, and even then, they might not remove the suspension.

**10. Inappropriate OID**  
This usually means a temporary ban. If it’s a permanent one, you’ll need to appeal it on the site.

**11. Legal**  
You’ll need to seek legal help. This kind of ban happens when your PSN account is involved in a criminal investigation or used as evidence in a legal case.

**12. Offensive Content**  
If the ban is permanent, they won’t remove the suspension.

**13. Unauthorized Email Use**  
You’ll need to call support for this one.

**14. Underage**  
You’ll need a legal guardian to handle it. They may ask for an ID card from the guardian to proceed.

---

## How Can This Leak Affect Sony’s Support System or Public Trust?

Leaks like this can shake things up for Sony and how people see their support, especially since exposing internal tools and project details can give hackers ideas on how to attack or trick both players and staff.

## Why Am I Posting This?

I know some people might ask, “If leaks can help hackers or hurt Sony, then why are you sharing this?”

It's Simple really: information like this is already out there. Keeping it hidden doesn’t make it disappear. A lot of players get banned and never get a clear answer why, or even how bans actually work. This post is to bring clarity and not chaos.

I’m not leaking passwords, logins, or anything dangerous. I'm just showing what kind of reasons are floating around in the system and how people are told to deal with them. If anything, this helps legit users understand what they’re up against, especially when support feels confusing.

That’s all for now. The list might expand or change later, but this is what I’ve seen leaked so far.
