---
sidebar_position: 1
sidebar_label: Welcome
---

# Welcome to our Duotail Documentation 

Let's discover our **Email Proxy Service in less than 5 minutes**.

## Purpose

**Our mission is simple: to provide every user with total control over their inbox and how they receive email.**

We're convinced that every person deserves a curated inbox. To make that a reality, we provide our full suite of incoming email controls to all our customers, free of charge.

## Key Concepts

To get the most out of our services, it is important to understand these three core concepts:
- **Channel**: A channel acts as an "umbrella" for all email addresses starting with its name. For example, owning the channel `a_happy.rhino` gives you control over `a_happy.rhino@duotail.com`, `a_happy.rhino_sports@duotail.com`, and `a_happy.rhino_food@duotail.com`. More details can be found in the [channel guide](/concepts/channel).

- **Route**: A Route defines the rules for incoming emails. The text following the last underscore in an address is the Route ID. For example, in `a_happy.rhino_food@duotail.com`, `food` is the route. If a route rule allows `deliciousgrass.com`, any emails from that domain will be delivered to your inbox. More details can be found in the [route guide](/concepts/route).

- **Contact**: A Contact is a trusted sender assigned to a channel. Emails originating from a Contact bypass Route configurations to reach any address under that channel. For example, if `angry.gazelle@example.com` is a Contact for a_happy.rhino, their emails will always be delivered to `a_happy.rhino@duotail.com`, `_sports`, and `_food` regardless of specific route rules. More details can be found in the [contact guide](/concepts/contact).

## What You'll Need

As our service is in its early stages, our domain is still being recognized by major email providers. To ensure you receive our communications, please whitelist `duotail.com` in your email settings. This will prevent our messages from being incorrectly flagged as junk.

[Gmail Guide](/tutorials/white-list-domain#whitelist-in-gmail) &nbsp;&nbsp;&nbsp;&nbsp; [Outlook Guide](/tutorials/white-list-domain#whitelist-in-outlook)

## Getting Started

To try our service, you can sign up for a free account. Upon successful registration, you will own the channel `a_<your_username>`. For example, a user named `happy.rhino` would own the channel `a_happy.rhino`, which means all the emails starting with `a_happy.rhino` at `duotail.com`.

[How to register a free account](/tutorials/register)

## Get Support

We are happy to assist you with any issues or answer any questions you may have. You can reach us through these two main channels:

- Technical support: `support@duotail.com`
- Other concerns: `contact@duotail.com` 
