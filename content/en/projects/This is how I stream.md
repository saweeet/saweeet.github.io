---
title: This is how I stream
date: 2021-12-31
tags:
  - images
series:
  - media
---
# Background 

**Important Update**

In a recent [X post](https://x.com/realdebrid/status/1859673163681960169?s=46&t=v7hlI5j-ie2ub28ChSkAKw), Real-Debrid (RD) announced enhanced anti-piracy measures, which could cause some content to stop working. However, four weeks later, I’m still not experiencing any issues.

As an alternative to Real-Debrid, I’ve heard Torguard is a good option and works natively with Stremio too.

For now, I plan to continue using RD until my subscription runs out or the service stops working, then decide whether to switch to Torguard.


---

A friend told me about a new way to stream 4k media content for roughly $3-5 per month, depending on the subscription you choose. I immediately tested it, and became amazed how good it was. There are a few technical steps involved, but if you're reading this then, you can probably reach out to me with any queries. 

There a few ways to set this up. This guide will take the simplest approach, using three different services:

1. **[Real-Debrid](https://real-debrid.com)**: An online service that performs file hosting and handles content downloading from other sources, such as magnet URLs (including torrents). A magnet URL allows users to download at very high speeds. Real Debrid will host these files on their server.
    
2. **[Stremio](https://www.stremio.com)**: This is the client app you will be using to watch content with. The Stremio app can be downloaded from the Google Play Store or the Apple App Store. You will need to install this app on your TV and/or mobile phone.
    
3. **[Torrentio RD](https://torrentio.strem.fun/)**: A Stremio add-on extension that helps you find movies or TV shows. It scrapes torrent sites to find streaming links for the content you search for in Stremio. Note that it does not download content itself; it simply finds relevant links and sends them to Real Debrid, which then downloads the content for you.

# Instructions

 **1. Install Stremio**

- I recommend doing this on your mobile phone first. Download and install Stremio from the Google Play Store, the Apple App Store, or directly from their [official website](https://www.stremio.com/).
- Sign up for the free account.

 **2. Sign Up for Real-Debrid**

- Go to [Real-Debrid's website](https://real-debrid.com/) and register an account* [1].

- Subscribe to a premium plan (I chose the 180-day plan, which costs less than $5 per month).

- Once registered, navigate to `My Devices`, where you should find an **API key**.

![](../images/Pasted%20image%2020241201115128.png)


- Copy and paste this API key to your clipboard.
    

 **3. Install the Torrentio RD Add-on**

- Make sure you are signed in your Stremio app on your mobile phone
- Visit https://torrentio.strem.fun/ and under Debrid Provider, click on Real Debrid
- Paste the RealDebrid API Key under the `RealDebrid API Key` that you copied in Step 2.

At this stage you should now be able to test this. Make sure your mobile phone is connected to your home Wi-Fi. Then, using Stremio, try searching and watching a few movies and TV shows using Stremio. 

> **Important**: 
> -  If you're watching content at home, do not simultaneously watch content on a different device outside your home.
> - You can only watch media content from a single WAN IP address. The WAN IP address is the IP assigned to your modem by your Internet Service Provider. All devices connected to your home Wi-Fi will use the same WAN IP. 
> - If your mobile phone is not connected to Wi-Fi, it will use a 4G/5G network and a different WAN IP address. 
> - If Real-Debrid detects multiple IP addresses, it might believe you're abusing the system, that is, sharing your credentials with everyone and block your access.

 **Step 4: Install the Stremio App on Your TV**

- Search for the Stremio app on the Google Play Store and download it.

- After logging into Stremio, you may need to download the Torrentio RD add-on again.
- After clicking `Configure`, you should see an QR code displayed on the TV. Use your mobile phone and scan it.
- Follow the prompts, and the app should automatically configure the API key on your TV.

The Stremio client UI does not have as good as Netflix, Jellyfin, Plex etc. There are free alternatives such as Kodi, but requires a lot further technical dive. For 4K content, you need to have a good internet download speed. I have a 100mbps down and do not have any issues streaming.
# Notes
[1] Some users choose to use an alias email address and VPN. See https://www.youtube.com/watch?v=7Ncye_X6wwc However, I was comfortable not doing this. Up to you how you would like to proceed.
