---
title: "How to Get Google Services on Huawei (microG & Aurora Store)"
date: 2026-02-16
author: tnebula
categories: ["Android", "Tutorials"]
tags: [huawei, google-services, microg, aurora-store, emui]
description: "A comprehensive guide to installing MicroG and Aurora Store to use Google apps on Huawei devices running EMUI or HarmonyOS."
image: /assets/Huawei/GoogleServices/cover.png
---

## What is this guide?

This guide shows you how to install **microG Services** together with the **Aurora Store**. This combination allows you to use most Google-dependent apps on Huawei devices (EMUI / HarmonyOS) that don't come with Google Mobile Services (GMS) pre-installed.

Whether you're a tech expert or a complete beginner, this guide is designed for you.

---

## ⚡ The Quick Guide (For Power Users)

If you already know your way around Android and just need the links, here is the summary.

1.  **Download microG**: [GitHub Release (Look for -hw.apk)](https://github.com/microg/GmsCore/releases)
2.  **Download Aurora Store**: [Official Website](https://www.auroraoss.com/files/AuroraStore/Release/huawei)
3.  **Install Both**: Install the Latest APKsa for Both.
4.  **Permissions**: Open microG → Self-Check → **Grant ALL permissions**.
5.  **Done**: Login to Aurora Store and start downloading apps.

---

## 📘 The Detailed Guide (Step-by-Step)

If you want a walkthrough with pictures and more explanation, follow this section.

### Step 1: Download and Install microG

**What is it?** microG is the brains of the operation. It tricks apps into thinking your phone has official Google Services installed.

1.  **Download the APK**: Go to the microG GitHub releases page.
    -   **Link**: [microG GmsCore (GitHub)](https://github.com/microg/GmsCore/releases)
    -   **Important**: Scroll down to "Assets" and find the file ending in `-hw.apk` (this version is optimized for Huawei).

    ![microG Download Page](/assets/Huawei/GoogleServices/microg-download.png){: .w-75 .shadow .rounded-10 }

2.  **Install**: Tap on the downloaded file. If prompted, allow installation from your browser.

3.  **Grant Permissions (Crucial Step)**:
    -   Open the **microG Settings** app.
    -   Tap on **Self-Check**.
    -   You will see a list of checkboxes. Use my Settings in the picture Below & allow the permission it asks for.
    -   **Goal**: Make sure you do the same as the image below

    > **Why?** If you don't do this, some apps may have delayed notifications or doesn't send you notifications at all.

    ![microG Permissions Self-Check](/assets/Huawei/GoogleServices/microg-permissions.jpg){: .w-75 .shadow .rounded-10 }

### Step 2: Install Aurora Store

**What is it?** Aurora Store is your new **Open Source** "Play Store." It connects directly to Google's servers so you can download official apps.

1.  **Download**: Go to the official website.
    -   **Link**: [AuroraOSS Huawei](https://www.auroraoss.com/files/AuroraStore/Release/huawei)
    -   Download the Latest Release

    ![Aurora Store Website](/assets/Huawei/GoogleServices/aurora-download.png){: .w-75 .shadow .rounded-10 }

2.  **Install**: Open the APK and install it.

3.  **Setup**:
    -   Open the app and follow the welcome screen.
    -   When asked for permissions (Installer, Storage, etc.), grant them all. This allows the store to install apps automatically for you.

### Step 3: Login and Use

You have two choices when you open the store:

1.  **Google Login**: Use your real Google account. (Recommended)
    -   *Pros*: Access your paid apps and wishlist.
    -   *Cons*: Small risk of Google limiting the account (haven't seen a case, but possible).
2.  **Anonymous Login**: Use a secure, anonymous account.
    -   *Pros*: Safer, no tracking.
    -   *Cons*: Can't download paid apps & some downtimes.

Once you're in, search for an app (like Gmail or Google Maps) and install.

---

## FAQ & Troubleshooting

-   **"Installation Failed"**: Make sure you downloaded the `-hw` version of microG.
-   **"Notifications aren't working"**: Go back to microG Settings > Cloud Messaging and make sure it's turned ON.
-   **"Can I use Google Pay?"**: Unfortunately, no. Google Pay requires strict security checks that usually fail on devices without official GMS.

---

## 🤝 Community & Support

A big thank you to the following communities for supporting this guide. If you need more help or want to discuss Huawei devices, consider joining them:

-   **Huawei Subreddit Discord** - [Join their Discord](https://discord.gg/YE98uMgNQx)

---

## References

-   [Reddit: How to get Google Services the safest way](https://www.reddit.com/r/Huawei/comments/1pxsukm/how_to_get_google_services_the_safest_way/)
-   [AuroraOSS Official Site](https://auroraoss.com/)
-   [Reddit: How to use Huawei devices without Google](https://www.reddit.com/r/Huawei/comments/ie71hk/article_how_to_use_huawei_devices_without_google/)

![Not AI](/assets/img/Written-By-Humans-Not-By-AI-Badge-black.png){: .right }
