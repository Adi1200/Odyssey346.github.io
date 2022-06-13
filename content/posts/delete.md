---
title: "Delete your old internet past"
date: 2022-06-06T10:14:48+02:00
draft: false
readingTime: true
tags: ["privacy", "guide"]
---

## My experience getting my information off of the Internet
Recently I decided to learn about tools you can use to ~~stalk~~ find out information about Internet users, and I've been using them to find information I've published about myself on the internet that I really shouldn't have. So, in this post I will show off the tools I used and my technique to finding information about myself that I've published on the internet, and find old accounts, so that you can stay safe on the internet.

## Tools (prerequisites)
Before you start, you'll need to install the following tools.
- [Sherlock](https://sherlock-project.github.io)
- [Holehe](https://github.com/megadose/holehe)

Done? Then continue.

## How to use Holehe
Holehe is a tool that allows you to figure out what sort of services are attached to an email address. So, here's what I want you to do:
1. type in: ``holehe --only-used your@email.address``
2. find services attached to your email that you don't use. Go on that service and try to reset your pass, and log in.
3. Check [JustDeleteMe.xyz](https://justdeleteme.xyz) and search that service. Check how hard it is to delete your account on there. If you can't find that service on JustDeleteMe, try looking around in for example Account Settings or something similar.
4. Delete your account!

Note that you can't use Holehe in bulk like ``holehe --only-used my@email.address myother@email.address``. You will have to do this:
```
holehe --only-used my@email.address
holehe --only-used myother@email.address
```
## Now, what do we use Sherlock for?
Sherlock is a tool that searches various services for a username. Here's how you'd use it:
1. Make sure you're in the directory with Sherlock
2. type this: ``py sherlock --timeout 10 username1 username2 username3 etc``. Note that if you're on Linux it might be ``python`` instead of ``py``.
3. Try to log in to a service you'd like to remove yourself from with your username. If you can't, try every email you've used in your life to reset your password. If they let you reset your password with just your username, you're probably in luck.
4. Once again, check [JustDeleteMe.xyz](https://justdeleteme.xyz) and search that service on there, and look at the instructions. If you can't find that service on JustDeleteMe, look around and try to find a way to delete your account on there.

## The Holehe trick
Here's the thing you should do with Holehe: check EVERY email you've used in your life.

Doesn't matter if it's an email you "used once", just check it with Holehe. It's a very efficient way to delete your old Internet past.

Another trick is to sherlock the email username. If your email username is something common like email@gmail.com or something, then there's probably no reason to. But if your email username is somewhat unique like hunter2269@gmail.com, then it's probably worth running Sherlock on hunter2269. It's especially worth it when it's gmail because some sites generate a username based on your Gmail when you do Google SSO, and they usually have your full name on there because of your Google account.

### Further reading
There's a site called [Epieos](https://epieos.com) that requires login, but, allows you to see details about a Google account from an email that has a Google account attached to it. If your email is Gmail then it's definitely got a Google account attached to it. I recommend you get an account on there, and type in your email. Epieos can also find a Skype account from that email, and it also runs Holehe on it (although, it seems like they lack some results). I highly recommend you check it out.

#### Contact
If there's anything wrong with this article, or something you need help with, you can contact me by pressing the message bubble on the left side (or the chat button on the top of the site if you're on mobile).

<script src="https://utteranc.es/client.js"
        repo="Odyssey346/Odyssey346.github.io"
        issue-term="pathname"
        label="comment"
        theme="preferred-color-scheme"
        crossorigin="anonymous"
        async>
</script>