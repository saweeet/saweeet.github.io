---
title: How I stream content
date: 2022-02-20T12:04:16-05:00
tags:
  - images
series:
  - example posts
---
# Background 

A friend told me about a new way to stream media content for roughly $3-5 per month, depending on the subscription you choose. I immediately tested, and became amazed how good it was. There are a few technical steps involved, but if you're reading this then, you can probably reach out to me with any queries. 

There a few ways to set this up. This guide will take the simplest approach, using three different services:

1. **Real-Debrid**: An online service that performs file hosting and handles content downloading from other sources, such as magnet URLs (including torrents). A magnet URL allows users to download at very high speeds. Real Debrid will host these files on their server.
    
2. **Stremio**: This is the client app you will be using to watch content with. The Stremio app can be downloaded from the Google Play Store or the Apple App Store. You will need to install this app on your TV and/or mobile phone.
    
3. **Torrentio RD**: A Stremio add-on extension that helps you find movies or TV shows. It scrapes torrent sites to find streaming links for the content you search for in Stremio. Note that it does not download content itself; it simply finds relevant links and sends them to Real Debrid, which then downloads the content for you.

# Instructions

 **1. Install Stremio**

- I recommend doing this on your mobile phone first. Download and install Stremio from the Google Play Store, the Apple App Store, or directly from their [official website](https://www.stremio.com/).
- Sign up for the free account.

 **2. Sign Up for Real-Debrid**

- Go to [Real-Debrid's website](https://real-debrid.com/) and register an account.

- Subscribe to a premium plan (I chose the 180-day plan, which costs less than $5 per month).

- Once registered, naviage to `My Devices`, where you should find an **API key**.

![](../images/Pasted%20image%2020241201115128.png)


- Copy and paste this API key to your clipboard.
    

 **3. Install the Torrentio RD Add-on**

- Back on your Stremio app on your mobile phone, go to the **Add-ons** section.

- Search for **Torrentio RD** and install it.
- Find the Torrentio RD add-on and click `Configure`.
- Paste the Real-Debrid API key you copied earlier.

Make sure your mobile phone is connected to your home Wi-Fi. Then, you should be able to search for and watch movies and TV shows using Stremio.

> **Important**: You can only watch media content from a single WAN IP address. The WAN IP address is the IP assigned to your modem by your Internet Service Provider. All devices connected to your home Wi-Fi will use the same WAN IP. In simpler terms, if you're watching content at home, do not simultaneously watch content on a different device outside your home. If your mobile phone is not connected to Wi-Fi, it will use a 4G/5G network and a different IP address. If Real-Debrid detects multiple IP addresses, it might believe you're abusing the system (sharing your credentials with everyone) and block your access.

 **Step 4: Install the Stremio App on Your TV**

- Search for the Stremio app on the Google Play Store and download it.

- After logging into Stremio, you may need to download the Torrentio RD add-on again.
- After clicking `Configure`, you should see an QR code displayed on the TV. Use your mobile phone and scan it.
- Follow the prompts, and the app should automatically configure the API key on your TV.


# Caveats
- Some users choose to use an alias email address and VPN. https://www.youtube.com/watch?v=7Ncye_X6wwc . However, I was comfortable not doing this. Up to you how you would like to proceed.

- The Stremio UI isn't as good as Netflix, Jellyfin, Plex etc. There are free alternatives such as Kodi, but requires further dive. 