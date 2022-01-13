---
title: "Abe's finance"
date: 2022-01-10T11:30:13+05:30
draft: false
img: /images/finance.jpg
description: "Paper Trading WebApp"
images:
    - "/images/finance.jpg"
github: https://finance.habet.dev
featured: /
---


# This was sc50

Building this project challenged my skills. After teaching us python, sql, html css and js it had us build a fully functional web app. A paper trading app. Given just a basic flask app structure with login, logout, price lookup, user database and an error page. We had to build the rest. Which included registering, buying and selling stock, quote, history page and a index page. It was necessary to build more tables in the database to keep track of transactions.

# Deployment

Deploying the project brought on its own set of challenges. The staff at Harvard provide a great step by step guide for how to deploy on Heroku. My first mistake was i followed the old docs [here](https://manual50.readthedocs.io/en/latest/heroku.html). When I should have fallowed [these docs](https://cs50.readthedocs.io/heroku/).
Next using the tool `pgloader` we transfer over from sqlite3 database to a postgresql hosted on heroku. This caused a few query errors. Spent a day going through the logs and sorting it all out. For instance the db in sqlite auto incremented the user id when registering a new user. For some odd reason after the transfer that no more happened. so I had to recreate the table.

# Check it out

The last step was to use my own domain. This was as simple as creating a `CNAME` record on a sub domain.
The only downside is Heroku doesn't provide SSL certificate for free acounts.
The workaround was to enable cloudflares to handle the certificate. the downside is that all traffic from cloudflare to heroku isn't encrypted ☹️  While I don't encourage such practice for this small project I left it as is.

go test your trading skill at [finance.habet.dev](https://finance.habet.dev)
