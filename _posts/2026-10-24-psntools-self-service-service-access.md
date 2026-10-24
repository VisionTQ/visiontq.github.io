---
title: "Access your services"
date: 2026-10-24 19:16:00 +0300
author: tnebula
categories: [psntools]
tags: [psn-tools, self-service, playstation, npsso]
description: "Log in to self-service with your order ID and marketplace username, or use the magic link from your order."
hidden: true
---

Self-service is for services you bought for your own PlayStation account, such as profile changes or avatar unlocks. You can log in two ways: with your order details, or with the magic link from your order.

## Step 1: Go to the self-service page

Go to [modding.psntools.com](https://modding.psntools.com). On the **What Did You Buy?** page, choose **Something For My Own Account**.

![What Did You Buy screen with Something For My Own Account highlighted](/assets/psn-tools/self-service/service-access-card.png){: .w-100 .shadow .rounded-10 }

## Step 2: Choose how to log in

### Option 1: Log in with your order details

1. Open your order and copy the **Order ID**.
2. On the **Access Your Services** page, paste the Order ID into the **Order ID** field.
3. Enter your **marketplace username** in the **Your Marketplace Username** field.
4. Click **Access My Services**.

![Order page with the Order ID highlighted](/assets/psn-tools/self-service/service-access-order-id.png){: .w-100 .shadow .rounded-10 }

![Access Your Services form with the Order ID and Marketplace Username fields highlighted](/assets/psn-tools/self-service/service-access-form.png){: .w-100 .shadow .rounded-10 }

When the order is verified, you will see **Successfully verified order ownership**.

![Access Your Services form filled in with the success message](/assets/psn-tools/self-service/service-access-success.png){: .w-100 .shadow .rounded-10 }

### Option 2: Use the magic link

If your order has a magic link, you can skip the form. Open your order and copy the link in the **Login** field, then open it in your browser. No password is needed.

![Order page with the magic link in the Login field highlighted](/assets/psn-tools/self-service/service-access-magic-link.png){: .w-100 .shadow .rounded-10 }

The link in the screenshot is only an example. Use the link from your own order.

> **Important:** The magic link is tied to the first person who opens it. Do not share it.

## Step 3: Connect your PlayStation account

Before you can use your services, connect your PSN account with an NPSSO token.

1. Get a fresh NPSSO token. If you do not have one, see [Get your NPSSO token](https://docs.psntools.com/account-billing/your-account/npsso-token).
2. Paste it into the **NPSSO Token** field on the **Your Services** page.
3. Click **Connect Account**.

> **Note:** Use a fresh token. If it is older than about 20 minutes, sign out of PlayStation, sign back in, and copy it again.

![Your Services page with the NPSSO Token field and Connect Account button highlighted](/assets/psn-tools/self-service/service-access-npsso.png){: .w-100 .shadow .rounded-10 }

After your account is connected, the **Entitlements Summary** shows what you can use. The list depends on what you bought, and each item shows how many uses are remaining.

## Next steps

- [Profile Modding](/posts/psntools-self-service-profile-modding/)
- [Avatar Adding](/posts/psntools-self-service-avatar-adding/)
