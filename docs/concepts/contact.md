---
sidebar_label: Contact
sidebar_position: 3
---

# Contact

## What is a Contact?

A **Contact** is a trusted sender assigned to a channel. Emails originating from a Contact bypass Route configurations to reach any address under that channel. For example, if `angry.gazelle@example.com` is a Contact for a_happy.rhino, their emails will always be delivered to `a_happy.rhino@duotail.com`, `_sports`, and `_food` regardless of specific route rules.

## Contact Properties
Each Contact object includes the following properties:

- **Contact Email:** The external, real-world email address of your contact.
- **Contact Name:** A display name used to identify the contact (independent of their email address).
- **Email to Send:** The specific `duotail.com` address you should use as the `Recipient` field when composing an email to this contact.
- **Route (Optional):** A specific route you wish to designate as the "Sender" address for this contact.
- **Notes (Optional):** A field for any personal reminders or extra information regarding the contact.

## Incoming Email Handling
When our system detects an incoming email from a channel contact, it processes the message and delivers it to your inbox immediately.  

![Incoming Contact Flow](/img/concepts/contact/incoming_flow.png)
## Outgoing Email Handling
When the system detects an outgoing email addressed to a channel contact, the following checks are performed before the message is delivered:
1. **Sender Permission Check:** The system verifies that the user has the necessary permissions to send emails from this account.
2. **Inbox Authentication:** The system ensures that the sender's originating inbox matches the designated recipient email address for either the specific Channel or Route.

![Outgoing Contact Flow](/img/concepts/contact/outgoing_flow.png)
 