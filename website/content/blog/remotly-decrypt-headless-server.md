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

## How to Remotely Decrypt a Headless Server.

My home server uses full disk encryption for all the storage. This poses a problem for a headless server. How can you decrypt it?

## Dropbear

Here's where [dropbear](https://matt.ucc.asn.au/dropbear/dropbear.html) comes in. Dropbear is a small SSH server and client. Think of it as a mini computer used to decrypt the real computer. Dropbear uses the ssh protocol so you can connect over a network. This solution works fine for decrypting the server when your on the local network. You just open a shell and ssh into the dropbear session and put in the password. The setup has been detailed is a [previous](https://habet.dev/blog/raspberry-pi-encrypted-boot-with-ssh/) blog post.

## Remote

The challenge however lies when you are out of the network. How can you decrypt the server remotely? What if you are away and the server crashes? Are you gonna wait till you get home to decrypt it? I don't know about you but l like when things work and when they don't I don't sleep till they are fixed. A better solution is needed.

## Wireguard

This is where whireguard come in. Wireguard is an extremely simple yet fast and modern VPN that utilizes state-of-the-art cryptography. Wireguard allows you to remotely connect to another device. Think of it as a secret tunnel between you and another device at home. Once we are connected to another device at home we can ssh into the Dropbear session to decrypt the server.

## OpenWRT

Which second device should we use? We need a device that will always be on. A WiFi router is perfect for this, it's always on! Though, in order to get wireguard on the router we need a more flexible firmware. For this we can flash it with OpenWRT. The OpenWrt Project is a Linux operating system targeting embedded devices. Here are the [instructions](https://openwrt.org/docs/guide-user/services/vpn/wireguard/automated) to setup Wireguard on the device.


## Conclusion
We now have to ability to remotely decrypt a headless server.
