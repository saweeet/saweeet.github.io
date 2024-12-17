---
title: My self-hosting Google Photos
date: 2022-02-20T12:04:16-05:00
tags:
  - images
series: []
draft: true
---
# Background

Hitting the 20GB limit that Google provides for all your email and photos was inevitable. When that time came, I started digging around and found two potential solutions:

1. **Immich**
2. **Photoprism**

I tried both, and honestly, they work really well. However, I decided to go with Immich since so many users were raving about how awesome it is.

---

# My Current Setup

1. **Raspberry Pi 4 (Rpi4)** with a 512GB SanDisk
2. **NAS**
3. **Docker**

I won't go into detail about how to set everything up because that's already covered in the [Immich installation guide](https://immich.app/docs/install/docker-compose/). Instead, I'll share my thoughts on using it so far. Right now, I will admit. It's not as smooth sailing as I'd like. But I see a lot of potential, so I’m sticking with it and working on overcoming the obstacles.

After configuring my Docker files and confirming all the containers were running, I could log into the main interface. I had used a folder from my Google Takeout and began uploading all these photos into immich:

```bash
immich upload --album --recursive directory/
```

Next, I'll probably use [immich-go](https://github.com/simulot/immich-go) to import directly from Google Photos.

---

## Hard Symptoms

After running my Docker containers, my Rpi4 would consistently hang or freeze after 3–4 hours. While I could still ping the device, SSH would stop working. Initially, I suspected an insufficient power supply, so I bought a brand-new Rpi4 power adapter. This seemed to resolve the issue temporarily, but after a fresh reboot and another 5–6 hours, the freezing resumed. I connected a monitor and keyboard to the Pi and found the command line blinking mockingly, with no response to my input—as if it were laughing at me after winning a long, heated battle. I came across a [Reddit post](https://www.reddit.com/r/docker/comments/egrkrx/startingstopping_containers_makes_raspberry_pi/) suggesting that the issue could stem from a poor storage drive. However, I’m not entirely convinced, as I’m using a brand-new 512GB SanDisk purchased during a Black Friday sale. While I doubt it’s the culprit, I’m not ruling it out entirely. My real hunch is that the CPU or memory is being throttled due to overuse. When checking Docker stats, I noticed my container was hitting 200% CPU usage, which essentially means two of the four CPU cores were maxed out. 

One additional factor to consider: I removed the fan from the Rpi4 because it was too loud. However, I don’t think the fan was making much of a difference in cooling.


## Troubleshooting steps:

- I'm running a cron job that will log my dmesg entries each hour so I can look for any errors:
```
0 0 * * * dmesg > /var/log/dmesg-$(date +\%Y-\%m-\%d).log
```