---
title: Privacy & Security
---

# Privacy & Security

:::tip The Duotail Privacy Manifesto
 **Your data isn't our gold; it's a risk we'd rather not hold.**
:::

Duotail is engineered on the principle of **Data Minimalism**. Our goal is to provide a secure gateway that protects your communication without becoming a point of failure for your privacy. This summary outlines how we handle your information and secure your communications.

---

## 🛡️ Zero-Knowledge Message Persistence

We do not operate like a traditional, permanent email archive. Our gateway acts as a secure, zero-knowledge buffer:

* **Zero-Knowledge Persistence:** We only persist processed emails in a zero-knowledge state using modern cryptographic primitives. Because we do not persist decryption keys, your messages are mathematically inaccessible to everyone — including us or any government entities.
* **Dual-Action Purge Protocol:** To minimize data liability, we provide two layers of deletion:
    1. **On-Demand:** You have the power to manually and permanently delete any encrypted record at any time via your dashboard.
    2. **Automated:** To ensure your digital footprint remains minimal, any message remaining in the buffer is automatically and permanently purged after 30 days.
* **Irrecoverable Deletion:** Once a purge is triggered—whether manually or automatically—the data is wiped from our active infrastructure and is completely unrecoverable.

*For a full technical breakdown of our `X25519`, `AES-256`, and `Argon2id` implementation, please visit our [Encryption Documentation](./data-security).*

---

## 👤 Data Collection Practices

We collect the minimum amount of data required to maintain a secure and trustworthy network:

* **Tiered Verification:** While our Free plan remains anonymous, we require legal name verification for our paid tiers (Basic and Business). This is a critical security measure to prevent identity impersonation and ensure the integrity of the Duotail gateway.
* **Metadata Stripping:** Our gateway automatically scrubs outgoing emails of originating IP addresses and device headers.
* **Service-Only Data:** If information is not strictly necessary for routing or securing your email, we do not store it.

*For a full breakdown of the specific data points we collect for each plan, please see our [Personal Data Inventory](/privacy/personal-data-inventory).*

---

## 🍪 Cookie Policy

We believe your browsing behavior is your own business.

* **Essential Only:** We use essential session cookies only to keep you logged in and secure. 
* **No Tracking:** We do not use profiling scripts, tracking pixels, or cross-site advertising cookies.
* **Not For Sale:** Our revenue is generated through subscriptions, never through the monetization of user data.

*For an exhaustive list of the cookies used across our domains, please see our [Cookie Disclosure](/privacy/cookie-disclosure).*

---

## 🚪 Exit Policy & Sovereignty

You maintain full ownership of your routing logic and your presence on our infrastructure.

* **Portable Configuration:** You are never locked in. You may [download your full email configuration](/tutorials/manage-account#1-download-email-configuration) at any time directly from your **[Account Page](/tutorials/manage-account)**.
* **Account Deactivation:** You may [deactivate your account](/tutorials/manage-account#2-deactivate-account) at any time from your **[Account Page](/tutorials/manage-account)** as well. This instantly terminates all active email routing.
* **Scheduled Data Purge:** Following deactivation, your account enters a decommissioned state. To ensure a complete and irreversible wipe, all encrypted records are purged through our **scheduled data purge process**. This process ensures that data is systematically removed from both active clusters and redundant backups, typically finalized within one week.