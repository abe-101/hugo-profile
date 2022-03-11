---
title: "How to Remotely Decrypt a Headless Server"
date: 2022-03-22T09:35:54-05:00
draft: true
author: "Abe"
tags:
    - Self-Hosted
    - Raspberry-Pi
    - Nextcloud
description: "Nextcloud: integrated on-premises content collaboration platform"
images:
    - "/images/nextcloud-dashboard.png"

---

## How to Remotely Decrypt a Headless Server.

My home server uses full disk encryption for all the storage. This poses a problem for a headless server. How can you decrypt it?

## Dropbear

Here's where [dropbear](https://matt.ucc.asn.au/dropbear/dropbear.html) comes in. Dropbear is a small SSH server and client. Think of it as a mini computer used to decrypt the real computer. Dropbear uses the ssh protocol so you can connect over a network. This solution works fine for decrypting the server when your on the local network. You just open a shell and ssh into the dropbear session and put in the password.

## Remote

Thie challenge lies when you are out of the network. How can you decrypt the server? What if I'm on vacation and the server restarts, are you gonna wait till you get home to set it up again? I don't know about you but l like when things work and when they don't I don't rest to i fix them. So i needed a better solution.

## Wireguard

This is where whireguard come in. Wireguard is an extremely simple yet fast and modern VPN that utilizes state-of-the-art cryptography. We can use wireguard to remotely connent to a device on the local network. Therby enableing us to ssh into the dropbear to decrypt the server.

## OpenWRT

Which 2nd device should we use? Why not make use the WiFi router. It's always on. inorder to use wireguard on the router i had to flash it with OpenWRT

## Conclusion
