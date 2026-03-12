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

* **Cryptographic Sovereignty:** We only persist processed emails in a **zero-knowledge state** using modern cryptographic primitives. 
* **No Decryption Keys:** Because we do not persist the decryption keys, your messages are mathematically inaccessible to everyone—including our engineers and any government entities.
* **Permanent Purge:** You have the power to permanently delete encrypted records from our system at any time. Once deleted, they are unrecoverable.

*For a full technical breakdown of our $X25519$, $AES-256$, and $Argon2id$ implementation, please visit our [Encryption Documentation](./data-security).*

---

## 👤 Data Collection Practices

We collect the minimum amount of data required to maintain a secure and trustworthy network:

* **Tiered Verification:** While our Free plan remains anonymous, we require legal name verification for our paid tiers (Basic and Business). This is a critical security measure to prevent identity impersonation and ensure the integrity of the Duotail gateway.
* **Metadata Stripping:** Our gateway automatically scrubs outgoing emails of originating IP addresses and device headers.
* **Service-Only Data:** If information is not strictly necessary for routing or securing your email, we do not store it.

---

## 🍪 Cookie Policy

We believe your browsing behavior is your own business.

* **Essential Only:** We use essential session cookies only to keep you logged in and secure. 
* **No Tracking:** We do not use profiling scripts, tracking pixels, or cross-site advertising cookies.
* **Not For Sale:** Our revenue is generated through subscriptions (The Architect and The Sovereign plans), never through the monetization of user data.

---

## 🚪 Exit Policy & Sovereignty

You maintain full ownership of your routing logic and your presence on our infrastructure.

* **Portable Configuration:** You are never locked in. You may download your full email configuration and whitelist settings at any time directly from your **Account Page**.
* **Account Deactivation:** You may deactivate your account at any time via your dashboard. This instantly terminates all active email routing.
* **Scheduled Data Purge:** Following deactivation, your account enters a decommissioned state. To ensure a complete and irreversible wipe, all encrypted records are purged through our **automated cleanup cycles**. This process ensures that data is systematically removed from both active clusters and redundant backups, typically finalized within one week.