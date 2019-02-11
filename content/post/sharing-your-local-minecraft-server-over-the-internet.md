+++
title = "Guide: Sharing Your Local Minecraft Server Over the Internet"
description = "This guide will show you how to share your local Minecraft game with your online friends for free"
date = "2016-01-11"
+++

This guide will show you how to share your local Minecraft game with your online friends for free.

Local Minecraft games only works with people connected to the same network.
It runs locally on your computer and it's not accessible through the internet.

What we need is a public Internet address that our friends can connect to. The solution to this: `ngrok`!

#### Step 1
You need to sign up for an ngrok account at [ngrok.com](https://ngrok.com/). Don't worry it's free.

#### Step 2
Visit the ["Download and Installation"](https://ngrok.com/download) section and download the ``ngrok`` binary.
Follow the simple three step installation guide.

#### Step 3
You need to save your authentication token to your installation of ``ngrok``.
Sign in to your [ngrok dashboard](https://dashboard.ngrok.com/).
Navigate to the directory where you put ngrok in your terminal and run this command:
``./ngrok authtoken <YOUR-TUNNEL-AUTHTOKEN>``

#### Step 4
Launch Minecraft.
Click "Open for LAN" and remember the port number.

#### Step 5
Go back to your terminal and run:
``ngrok tcp <PORT-NUMBER>``
E.g.
``ngrok tcp 60442``

You should see ngrok sharing your local Minecraft game on the Internet.

Your server is now available at ``0.tcp.ngrok.io:45097``.

Now your friends can connect to your server by pressing "Direct Connect" and entering your ngrok address.