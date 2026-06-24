---
title: "Free Save Wizard Alternatives and How to Use Them: Re-Sign, Re-Region, and Edit PS4 Saves"
date: 2025-06-01
description: "Learn how to use Discord bots as free Save Wizard alternatives to re-sign, re-region, and mod PS4 saves. This guide covers features, commands, required files, and how to get started — all without paying for Save Wizard."
comments: true
author: tnebula
categories: [PlayStation, Save Modding]
tags: [ps4, ps5, save wizard, re-sign, re-region, discord bot, game saves, save modding, cusa codes]
image: https://i.imgur.com/mgRLjR6.png
image_alt: "Minimalist black and white thumbnail featuring white silhouette icons of PS5 on the left and PS4 on the right, with a glowing Discord logo at the center in a square icon style. Below is bold white text reading 'Free Alternatives to Save Wizard.' The design is high-contrast, modern, and tech-focused, ideal for gaming-related blog content."
hidden: true
---

## What is Save Wizard?

For those who don't know, Save Wizard is a paid tool that lets you mod your PS4 game saves. You can do things like:

- Add infinite money
- Unlock cosmetics
- Max out XP or levels

In simple terms, Save Wizard lets you edit your save data directly — adding cheats, unlocking content, modifying stats or currency.

---

## What are these alternatives to Save Wizard?

Basically, these are free alternatives to Save Wizard. These alternatives are available on Discord and offer similar functions for free by using Discord as their platform.

---

## Where can I find them?

They're on Discord, and there are a bunch of Discord communities that have them. Here are the communities I know so far with the bots:

- [https://discord.gg/fnntcGCC6z](https://discord.gg/fnntcGCC6z)
- [https://discord.gg/psbot](https://discord.gg/psbot)  
  If this one doesn't work, then use the Permanent Link:  
  `https://discord.gg/dyapjAPdCT`

This section will keep being updated with more links.

---

## Why is it on Discord?

Discord is a popular communication and community platform that also supports bots, which are programs that automate tasks. These bots run inside Discord, so users don’t have to install random applications - they only need Discord, which is available on PC, browser, and mobile. They just use the commands on Discord, making it accessible and easy to use for everyone.

---

## What does the bot do?

These bots help you modify PlayStation game saves by allowing you to re-sign and re-region them, among other features. The bots use a jailbroken PS4 in the backend to process encrypted saves — but you as the user do not need a jailbroken console. All you do is upload your saves.

---

## What are the features of this bot?

- Re-sign saves and re-region them.
- Decrypt encrypted saves.
- Change the picture of encrypted saves.
- Change the titles of encrypted saves.
- Convert game saves from PS4 to PC or vice versa (some games require extra conversion).
- Add quick cheats to your games.
- Apply Save Wizard quick codes to your saves.
- And more.

For more information, check [https://github.com/hzhreal/HTOS/blob/main/README.md](https://github.com/hzhreal/HTOS/blob/main/README.md)

---

## Re-sign

Re-signing means taking a save file that belongs to someone else and changing its account ID or "username" so it works on your PlayStation account. 

For example, let's just say you found a save on the internet or your friend has a save with a cosmetic you want or has a lot of stuff in a game and you want to use that exact save, you cannot just copy it directly because it’s tied to their account. You must re-sign the save with your own account ID so the PlayStation system recognizes it as yours. Every PlayStation account has a hidden **account ID** — a unique, unchangeable number that stays the same even if you change your username. The re-signing process uses this ID, not your visible username.

---

## Re-region

Re-regioning means changing the region code of a save so it matches your account's region. Basically, re-regioning changes the region of a save file. Let’s say you downloaded a save from someone who has the US version of the game, but your game is the EU version. Even though it’s the same game, it won’t load unless the region matches.

You can tell the region of the save by the CUSA code using [orbispatches](https://orbispatches.com/). It shows up like this:

```text
CUSA12345
```

Here is an example table of the same game but multiple regions/different CUSA numbers:

**Red Dead Redemption 2:**

- [CUSA08519](https://orbispatches.com/CUSA08519), [CUSA15698](https://orbispatches.com/CUSA15698) → EU
- [CUSA08568](https://orbispatches.com/CUSA08568) → JP
- [CUSA03041](https://orbispatches.com/CUSA03041) → US

They are the same game but different regions for the save. Re-signing isn't enough and won't work for your game. That's why you have to re-region it. And if you do re-region it, it doesn't matter what previous region it was. It will still work on your own region.

If your game and the save have different CUSA codes, you need to re-region it to match.

---

## Does This Really Work on PS5?

Sort of. PS5 saves can’t be copied to the USB like PS4 saves, but some games support a feature called 'cross-save'. That means the PS5 version of the game can read your PS4 save of the same game.

So you can re-sign or re-region a PS4 save, then load it into the PS5 version of a game that supports cross-save. It's limited, but it works for games that have that feature.

I'll make a separate blog or article later explaining cross-save in much detail.

---

## What You Need Before You Start

- A Discord server with one of the Save bots (There are many, and it doesn’t matter which one you use. Just make sure they support slash commands.)
- A USB flash drive to move saves between your console and phone or PC.
- If you’re on mobile: a USB adapter to connect your flash drive to your phone.
- A way to upload your saves. You can upload saves directly to the bot in Discord, but this is important: if the file is large or giving errors, just upload it to Google Drive and share the link. Make sure your link is set to "anyone with the link can view/edit".

---

# Getting Started

## Threads

Click the create thread button in the channel that the bot's message is in. Then you will get pinged or mentioned by the Discord bot in a new thread. After that, you can use the commands there.

**Disclaimer:**  
If you get "The application did not respond," it means the bot is not online. Ping the moderators or the bot admin for help.

Now, after you are in the new thread, use this command:

```text
/ping
```

to check if the bot is working and online.

Next, it depends on what you want. Do you want to re-region, re-sign, or other? Check the TOC (Table of Contents).

---

## Re-sign Command

Now type in the thread:

```text
/resign
```

There will be optional buttons that pop up after writing the command. One of them is:

```text
playstation_id:
```

Click on it. After that, it should look like this:

```text
/resign playstation_id:
```

Now type in your PlayStation username.

Once you've linked your PSN ID, you can simply use `/resign`[^psn] — no need to include your username again.

The bot will then reply with:

> Please attach at least two encrypted save files that you want to upload (.bin and non-bin). Or type 'EXIT' to cancel command.

So now attach 2 save file pairs in your CUSA folder, either straight on Discord or upload them to Google Drive and share the link.

Example of a save pair (one encrypted `.bin` and its matching non-bin file):  
`SAVEDATASGTA50000` & `SAVEDATASGTA50000.bin`

They’re usually found in:

```text
PS4/SAVEDATA/{account ID}/{CUSAXXXX}/{files}
```

Done. That’s it for re-signing.

### 🖼 Visual Walkthrough

![Visual tutorial showing the full resign process from command to upload and response](https://i.imgur.com/OmscS4X.jpeg){: .w-75 .shadow .rounded-10 }

This image shows how the full resign process looks visually — from typing the command to uploading your save files and getting the final result.

---

## Re-region Command

Type this command:

```text
/reregion
```

There will be optional buttons that show up again. One of them is:

```text
/reregion playstation_id:
```

Type your PlayStation username if the bot doesn't already remember it.

If your PSN is already linked, just type `/reregion`[^psn] directly.

Now the bot will reply with:

> **Re-region process: Upload encrypted files from YOUR region**  
> Please attach two encrypted save files that you want to upload (.bin and non-bin). Or type 'EXIT' to cancel command.

So now upload 2 save file pairs from **your region**. Either upload them to Discord or drop a Google Drive link.

Example:  
`SAVEDATASGTA50000` & `SAVEDATASGTA50000.bin`

Found in:

```text
PS4/SAVEDATA/{account ID}/{CUSAXXXX}/{files}
```

After that, it’ll ask for the save from the **foreign region** (the save you’re trying to convert to match your version of the game).

Once both are uploaded, the bot will process them and return the converted version in a ZIP file or sometimes a Google Drive folder link.

---

# Extra Commands

Now for the rest of the commands or features I [mentioned earlier](#what-are-the-features-of-this-bot). Most of these are optional unless you want to customize your save — like changing the image, title, or editing it for PC.

---

## Decrypt Command

This command gives you the raw, decrypted version of your save.

Now just decrypting the save doesn’t make it human-readable — it only removes Sony’s encryption. Some games need extra work, like converting file formats or going through a second decryption layer.

If the game is known in the bot’s [database](https://github.com/hzhreal/HTOS/tree/main?tab=readme-ov-file#functionalities), then the bot will handle the second-layer decryption too.

Once decrypted, you can use a save editor for that specific game. Also, decrypted saves can be used on PC (for games that support it).

Here’s how you use it:

```text
/decrypt
```

After that, options will show up on your Discord client. Hit enter and it should auto-fill like this:

```text
/decrypt include_sce_sys:
```

### What is `include_sce_sys:`?

That’s just asking if you want to include the system files from the save. Choose either `True` or `False`. These system files sometimes aren’t needed but you can include them if you’re doing full manual editing.

If the game has an extra encryption layer and the bot knows how to handle it, it’ll also ask if you want that removed.

##  Encrypt Command

This command re-encrypts your decrypted save so it works again on PlayStation.

It’s mainly used after editing a decrypted save or when you want to resign a save to a different account. The bot will take your modified files, rebuild the save folder, and apply Sony’s encryption again.

Here’s how you use it:

```text
/encrypt
```

After that, options will show up on your Discord client. Hit enter and it should auto-fill like this:

```text
/encrypt upload_individually: upload_sce_sys: account_id:
```

### What do the options mean?

* **upload\_individually:**
  Set this to `True` if you want to upload each file one by one (or all at once).
  Set to `False` if you already have the folder structure ready.

* **upload\_sce\_sys:**
  Choose `True` to include the original `sce_sys` folder in the encryption.
  Some games need this; others don’t — it depends on what you're editing.

* **account\_id:**
  Enter the Account ID you want the save to be signed to.
  This is how you resign the save to your own account.

Once you've filled in the options, follow these steps:

1. Upload the original PS4 save folder first (including `.bin` and metadata files).
   ![encrypt 1](https://raw.githubusercontent.com/That-Kidd/ps-resources/main/crc/pics/encrypt_1.jpg){: .w-75 .shadow .rounded-10 }

2. Then upload the modified, decrypted files you want to encrypt.
   ![encrypt 2](https://raw.githubusercontent.com/That-Kidd/ps-resources/main/crc/pics/encrypt_2.jpg){: .w-75 .shadow .rounded-10 }

3. The bot will process everything and give you back the encrypted save file.
   ![encrypt 3](https://raw.githubusercontent.com/That-Kidd/ps-resources/main/crc/pics/encrypt_3.jpg){: .w-75 .shadow .rounded-10 }

If you didn’t enter an Account ID or skipped that part, you’ll need to resign the save later before it works on your console


## ❓ FAQ (Community Answers)

These are questions I personally asked one of the bot hosters [**@That_kidd**](https://discord.com/users/285251932505767936) on Discord. Here's what he had to say:

---

### 🔹 Q1: Are there any risks to using these bots or Save Wizard?

> There’s not really any risks when using the bots or Save Wizard — at least not offline.  
>  
> Cheating in **online games** always carries a risk of punishment or bans. But for **offline single-player saves**, no action is taken against your account.  
>  
> As far as I know, no one has ever been banned for using these tools offline.  

---

### 🔹 Q2: Is the bot open source? How reliable is it?

> Yes — the bot is open-source. That means other people can host their own versions, contribute to it, and build on the code.  
>  
> I host one myself and try to keep it up as much as I can.  
>  
> The HTOS Discord has decent support too.

---

### 🔹 Q3: Can modified saves carry over into online games?

> In some games, yes. It depends on the game.  
  
 For example:
 - **Monster Hunter**  
 - **Dark Souls / Bloodborne / Elden Ring**  
 - **Dragon Ball Xenoverse**
 - **Ghost of Tsushima: Legends mode**
  
 These games use your save data for online play.  
  
 For **Dark Souls/Elden Ring**, if you edit the wrong stuff, you can get banned — but only on their servers, not your PSN account.  
(Credit - [nox_23](https://discord.com/users/346434189404405760) for the list)

---

### 🔹 Q4: Does the bot remember my account ID forever?

> No — it only stores your **most recent account ID**.  
>  
> When you re-sign to a different account, the previous one gets deleted.



# Notes & References

[^psn]: Once your PSN ID is linked, the bot remembers you using your **Discord ID + PlayStation account ID** (not your visible PSN username).  
Even if you change your PSN username, your **account ID stays the same** — and that’s what the bot uses to track your saves.  
This is why you don't need to re-link your PlayStation ID after changing your username.
