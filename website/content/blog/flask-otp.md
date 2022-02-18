---
title: "Flask Otp"
date: 2022-01-23T22:27:51-05:00
draft: true 
author: "Abe"
tags:
    - Python
    - Web App
    - Flask
description: "Integrate OTP in flask application"
images:
    - "/images/otp.png"
---

## What is OTP

> A one-time password (OTP), also known as a one-time PIN, one-time authorization code (OTAC) or dynamic password, is a password that is valid for only one login session or transaction, on a computer system or other digital device. OTPs avoid several shortcomings that are associated with traditional (static) password-based authentication; a number of implementations also incorporate two-factor authentication by ensuring that the one-time password requires access to something a person has (such as a small keyring fob device with the OTP calculator built into it, or a smartcard or specific cellphone) as well as something a person knows (such as a PIN).
 > <cite>[^1]</cite>


[^1]:  [Wikipedia](https://en.wikipedia.org/wiki/One-time_password)


## veryfy form

``` html
{% extends "layout.html" %}

{% block title %}
    OTP Verification
{% endblock %}

{% block main %}
 <form action = "/validate" method="post">   
     <h4> OTP has been sent to the email {{ email }}. Please check the email for the confirmation.</h4>  
    Enter OTP(One-time password): <input type="text" name="otp">  
    <input type="submit" value="Submit">  
 </form>  
{% endblock %}
```
