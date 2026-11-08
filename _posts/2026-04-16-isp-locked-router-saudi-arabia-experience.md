---
title: "My Experience with ISP-Locked Routers in Saudi Arabia"
date: 2026-04-16
author: tnebula
description: "A personal account of trying to bypass ISP router restrictions in Saudi Arabia, including technical setup, challenges, and community-sourced solutions."
tags: ["isp", "router", "saudi-arabia", "fiber", "networking", "pppoe", "vlan", "mac-cloning"]
categories: ["Networking", "Tech"]
---


## Intro

I recently became interested in this new [Huawei router](https://consumer.huawei.com/en/routers/wifi-be3-pro/) that I got, so I bought it.

It had many amazing features, but then I noticed it does not connect to the internet when I unplug my old router that my ISP gave me. So it turns out that my ISP locked it to their router, which I was upset about. So I started looking for ways.

I started calling the ISP's technicians, their support number, email, everything, and nothing worked so far. So I'm making this post to document everything that I've done so far and what I will do so that I can help you guys in the future who want to change their locked ISP routers.

This is an ongoing guide on how to bypass your ISP locked router and what can you do about it.

## My Story

So I actually called two technicians and first, and they all did not help me. The one of them actually told me stories. One of them said that some people got a thousand Riyals Router & they just got a technician order and told them: okay, remove this router and put this one.

And then the technician said that they can't, & the technicians couldn't. I felt like they were lying, but I told him:

okay, I know you can do it, you just don't want to.

He said: no, no, no, I seriously can't.

So then I called another technician. But this time I told him about a different issue. I told him that I need a cable fixing. He came, he just did some stuff, organized everything, and I told him, can you remove the old ISP router and make it to this router?

He said, I can't.

And I told him, really? And I kept persuading him.

Then he told me a story, there was one guy who actually bought a router and then called a technician, and so ofc he made an insane amount of trouble, called over their managers and just tried persuading so that they can change their routers. And then they didn't. That's what he told me. Now, I'm not gonna believe it. I'm not gonna believe anything.

I think it's 100% possible to bypass it.

The technicians didn't help. I even asked the support. I told them to give me the PPPoE username and password. He said he doesn't know what that is. At the end, they all told me to go to a branch, which I kind of didn't want to do because they're probably not gonna do anything lol

Now I'm trying to find a way. I already made a [Reddit post](https://www.reddit.com/r/HomeNetworking/comments/1smsctp/isp_locked_router_best_way_to_improve_setup/). I asked for everybody's help. It seems like one guy based on the Reddit post who uses the [STC](https://www.reddit.com/r/HomeNetworking/comments/1mpe6pn/how_can_i_use_my_own_router_with_a_fiber_isp_that/) was able to do it. However, I'm on mobily, a different ISP, so I don't know. I either have to find a way & if I couldn't, I'll probably switch over to STC and check if my one-year contract is over so that I can switch.

## My Setup

I have a fiber connection and my setup looks like this:
Internet → ONT → ISP router → My personal router (with DMZ)

The ISP router seems locked & no bridge mode option, which is why I enabled DMZ.
Also, the technician told me it's not possible to replace the router

### What I’ve tried

- Plugging Ethernet from ONT → personal router directly → ❌ Did not work
- Called ISP (Mobily) → ❌ No solution, technician said it's not possible (but I'm still going to try again)

### My goal

- Avoid double NAT / get full control of routing
- Use my own router properly

### Device Brands and Models


| Position | Brand  | Model Number             | Device Type                              |
| -------- | ------ | ------------------------ | ---------------------------------------- |
| Right    | Huawei | WiFi BE3 Pro (YGJN-BE33) | Wi-Fi 7 Router (Personal Router)         |
| Left     | Huawei | OptiXstar EG8010Hv6-10   | GPON Terminal (ONT)                      |
| Left     | Huawei | LG8245X6                 | Wi-Fi 6 Home Gateway (ISP Locked Router) |

**ISP:** Mobily  
**Country:** Saudi Arabia

### What I’ve tested so far

- ONT → personal router directly: ❌ Did not work
- Called ISP (Mobily): ❌ No solution (will try again)
- Current setup (ONT → ISP router → my router): ✔️ Works (with DMZ)

### What I haven't tried yet (based on suggestions on my [Reddit post](https://www.reddit.com/r/HomeNetworking/comments/1smsctp/isp_locked_router_best_way_to_improve_setup/))

- PPPoE login (username/password): Didn't get it yet
- MAC address cloning: Not tested
- VLAN settings: Not tested (don’t know the ID)

Note: The Reddit post has been removed by the moderators. Not sure why they would since many posts have a similar issue to mine but didn't remove them.

## Update 1: I Finally Found a Fix

So after all that struggle, I switched to another provider called **Salam**. And you won't believe what happened — they sent me a text message on my number with the full PPPoE details. It was meant for the technician lmao. I burst with happiness when I saw it.

I even asked the technician to do it for me and he had no clue what to do. Like bro, it's your job. So I just did it myself.

I opened the ISP router's settings, grabbed the VLAN ID from there, put in the PPPoE credentials from the text message, and boom — it finally worked. My own router, fully connected, no DMZ, no double NAT, nothing. Just straight ONT → my Huawei router.

So yeah, if you're stuck in the same situation: get the PPPoE details (they text them to you), grab the VLAN ID from your ISP router's WAN settings, and you're golden.

> **Correction:** I no longer recommend Salam. Read Update 2 at the end of this post before you switch.
{: .prompt-warning }

## Update 2: Do Not Get Salam

Scratch the recommendation above. **Please do not get Salam.** Their customer service is bad, and I regret switching to them.

Here is what actually happened. I have two lines with Salam. One of them is disconnected, and they are still charging me for it. I opened a support ticket weeks ago. Customer support did reply, and then nothing. Weeks later, still nothing done.

So if you are thinking of getting Salam, do not. The connection itself works fine, but the moment something goes wrong you are stuck with a bill and no one to fix it.

And the PPPoE thing was never special to Salam either. Every newly installed ISP sends the username and PPPoE password by SMS. I only found that out after I got STC. So ask your current ISP for the credentials and check your SMS first. You probably do not need to switch providers at all.

## References

- [How can I use my own router with a fiber ISP that locks their router?](https://www.reddit.com/r/HomeNetworking/comments/1mpe6pn/how_can_i_use_my_own_router_with_a_fiber_isp_that/)
- [ISP locked router, best way to improve setup?](https://www.reddit.com/r/HomeNetworking/comments/1smsctp/isp_locked_router_best_way_to_improve_setup/)