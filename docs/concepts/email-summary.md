---
sidebar_label: Email Summary
sidebar_position: 4
---

# Email Summary

## What is an Email Summary?
An **Email Summary** is a system-generated table inserted at the beginning of every incoming email, providing a concise overview of the message's original content. This summary is automatically removed when you reply, ensuring the external recipient never sees it.

We include the Email Summary for two key reasons:
- **Enhanced Visibility:** Standard email headers are often insufficient—especially on mobile platforms—for quickly identifying key details.
- **Transparency and Security:** We believe users have the right to know what might be hidden within a message. The summary notifies you of "invisible" elements, such as whether the email contains tracking pixels or insecure links.

## Email Summary Contents
An **Email Summary** consists of three primary sections: **Sender Details**, **Email Alerts**, and **Action Shortcuts**.

**Sample Email Summary**
![Sample Email Summary](/img/concepts/email-summary/sample_summary.png)

### Sender Details
This section provides a brief overview of the source of the message:
- **Sender Name:** The name associated with the sender's email account.
- **Sender Email:** The original email of the sender.
- **Email Entrance:** The specific Channel or Route address that received the email.

### Email Alerts
Alerts are displayed only when "invisible" or potentially risky elements are detected:  
- **Tracked:** The email contains tracking pixels designed to monitor when you open the message.
- **Insecure Link:** The email contains URLs that do not use the secure `https` protocol.
- **Insecure Domains:** When insecure links are detected, the system lists the specific domains associated with them for your review.

### Action Shortcuts
Action Shortcuts are one-click links that allow you to instantly update how the system handles future emails from this sender. The available shortcuts vary based on the [Route Type](/concepts/route#route-type):

- **Allow Next:** Permits exactly one additional email from this sender. 
- **Allow Future:** Whitelists the sender to allow all future emails.
- **Unsubsribe from Domain:** Silently blocks all future emails from the sender’s (exact) domain.
- **Unsubcribe from Email:** Silently blocks all future emails from this specific email address.
