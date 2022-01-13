---
title: "Self Hosted"
date: 2021-12-19T22:41:04-05:00
draft: false
author: "Abe"
tags:
    - Self-Hosted
    - Raspberry-Pi
description: "Self hosted home server"
images:
    - "/images/pi-with-ssd.jpg"
aliases: 
    - /self-host/
    - /2021/12/self-host/

---

This blog is self hosted on a small raspberry pi. Smaller than the size of your hand. I choose [this](https://www.amazon.com/gp/product/B07V5JTMV9/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B07V5JTMV9&linkCode=as2&tag=habet-20&linkId=f44d9fe1209576d61164ee27401025b5) model with a Crucial SSD you can find [here](https://amzn.to/3H57vys). You’ll need a wire like [this](https://www.amazon.com/gp/product/B00XLAZODE/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00XLAZODE&linkCode=as2&tag=habet-20&linkId=02980243c452d2e24be82c3b9df57cd2) to connect them.

- ![pi with lid](/images/pi-with-ssd-covered.jpg)
    
    Lid closed
    
- ![pi with lid open](/images/pi-with-ssd.jpg)
    
    Lid open
    

Raspberry pi sever

The OS of choice is Debian 11 because of its stability. I always prefer to encrypt my hardware, so I have nothing to worry about if it lands in other hands. [This](https://github.com/abe-101/pi-encrypted-boot-ssh) is an easy step-by-step guide to encrypt a headless server.

![debian logo](/images/debian-logo.png)

Debian’s Logo

Stay tuned for follow up posts about self hosted software on the pi.
