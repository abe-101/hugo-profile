---
title: "How to Remotely Decrypt a Headless Server"
date: 2022-03-22T09:35:54-05:00
draft: true
author: "Abe"
tags:
    - Self-Hosted
    - Raspberry-Pi
    - WireGuard
    - OpenWrt
description: "Demonstrates how to remotely decrypt a headless server"
images:
    - "/images/"

---

## Intro
In this article I detail how I use Dropbear, Wireguard, an OpenWrt router and a WiFi plug to remotly unlock my fully encrypted headless server.
I prefer to have all my digital content saved on an encrypted drive.
This poses a problem for my home server that has no screen.
How can I unlock it?

- Dropbear
- WireGuard
- OpenWrt Router
- A Wifi Plug

## Dropbear

For this I looked into [dropbear](https://matt.ucc.asn.au/dropbear/dropbear.html).
Dropbear is a small SSH server and client.
Think of it as a mini-computer used to decrypt the real computer.
Dropbear uses the ssh protocol so I can connect from another computer over your local network.
You just open a shell and ssh into the dropbear session and put in the password.
The setup for a Raspberry pi is detailed in [another](https://habet.dev/blog/raspberry-pi-encrypted-boot-with-ssh/) blog post.

## Remote

The challenge I faced was when I was out of the network.
How can I unlock the server remotely?
What if I was away and the server rebooted?
I can't afford to wait till I get home to unlock it.
I needed a better solution.

## Wireguard

This is where wireguard comes in.
Wireguard is an extremely simple yet fast and modern VPN that utilizes state-of-the-art cryptography.
Wireguard allows you to remotely connect to another device.
Think of it as a secret tunnel between you and the other device.
So if I can connect to another device on the local network, we can ssh into the Dropbear session to decrypt the server.

## OpenWRT

Which second device should be used?
I need a device that will always be on.
A WiFi router is perfect for this, it's always on!
Though, to get wireguard on the router, I needed a more flexible firmware.
For this, I went with OpenWRT.
The OpenWrt Project is a Linux operating system targeting embedded devices.
Here are the [instructions](https://openwrt.org/docs/guide-user/services/vpn/wireguard/automated) to set up Wireguard on the device.


## Conclusion
I now have to ability to unlock my headless server from anywere in the world.
