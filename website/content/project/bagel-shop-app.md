---
title: "Bagel Shop App"
date: 2022-01-10T11:30:13+05:30
draft: true
author: "Abe"
img: /images/bagel-shop.png
description: "A simple secure web app for groups to submit food orders. OTP email confirmation."
images:
    - "/images/bagel-shop.png"
github: https://github.com/abe-101/bagel-shop
featured: https://breakfast.habet.dev
---

## CS50x Final Project
As part of Harvards CS50x course we had to build our own project. I chose to solve a real world problem. We have a local study group that orders breakfast together. The problem is how can each member select what they want? This app attempts to solve it.

## Bagel Shop App

The app is built using Python and Flask which depends on the Jinja template engine.
The idea behind the app is simple, allow members to select breakfast for the week. The web app will send out an email with everyone's choice of breakfast.

![menu](/images/bagel-shop.png)

The app was built with security in mind. Inspired by the course's teacher, [David J. Malan](https://twitter.com/davidjmalan), who gave a great lecture on security. You can watch it in 4K HDR on [CS50's website](https://cs50.harvard.edu/x/2022/weeks/cybersecurity/).

Members will need to provide a real email address. The app confirms its authenticity by sending out a OTP (one time password) to the member. The app will not send out orders of members who have not verified their account. Check the blog post where I detail the technical process of setting up OTP authentication.

![menu](/images/otp.png)

The app also prevents malicious users from submitting the wrong information or putting in the wrong email/password.

![menu](/images/invalid.png)

Go try it out  at [breakfast.habet.dev](https://breakfast.habet.dev)
