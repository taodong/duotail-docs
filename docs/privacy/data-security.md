---
id: data-encryption-protocol
title: Data Security & Encryption
sidebar_label: Encryption Protocol
sidebar_position: 1
---

# The Duotail Encryption Protocol

At the heart of our **Zero-Knowledge** architecture is a non-custodial encryption flow. We have engineered our system so that we cannot read your messages, even if we were compelled to. 

Below is the technical breakdown of how your data is protected from the moment it enters our gateway.

---

## 🛰️ Encryption Flow Overview

![Duotail Encryption Flow](/img/privacy/encryption-flow.png)

---

## 🔐 Technical Implementation

Our protocol is divided into three distinct phases: Identity Generation, Message Protection, and Secure Retrieval.

### Phase 1: Key Generation & Registration
We use a derived-key architecture to ensure we never store your master secret.
1. **User Entropy:** The customer provides a unique combination of **three words** associated with a **Key Name**.
2. **Key Derivation:** Our system applies the **Argon2id** hashing algorithm and **X25519** elliptic curve cryptography to generate a high-entropy encryption key. 
3. **Storage:** Only the **Key Name** and the derived **Encryption Key** are stored in our secure database. Your original three words are never persisted.

### Phase 2: Message Protection (The Airlock)
When an email enters our gateway, it is neutralized and secured before it touches our disk.  
4. **Encryption:** Before the system saves any email content, it is encrypted using the **AES-256** algorithm in GCM mode, utilizing the key generated in Phase 1.  
5. **Association:** Once the encrypted `.eml` file is stored in our file system, we record which **Key Name** was used to secure it. This creates a link without exposing the content.  

### Phase 3: Secure Retrieval
Retrieval is a "Just-in-Time" process. The decryption key exists only in memory for the duration of your request.  
6. **Challenge:** When you request a download, our system retrieves the **Key Name** and prompts you for the associated **three words**.  
7. **Re-Generation:** Using your provided words, the system re-runs the **Argon2id** and **X25519** process to reconstruct the **Decryption Key**.  
8. **Decryption & Delivery:** The system loads the encrypted file, performs the decryption in a transient memory state, and streams the original file to you. 

---

## 🛡️ Why This Matters

* **No Persistence of Secrets:** Because we do not store your "three words," we have no way to reconstruct your decryption key. 
* **Mathematical Inaccessibility:** Without your unique words, the stored `.eml` files are mathematically indistinguishable from random noise.
* **Transient Memory:** Decryption keys are generated on-the-fly and are never written to permanent storage.

---

## ❓ Security FAQ
* **What if I lose my three words?**  
Because Duotail is a zero-knowledge system, we do not have a "backdoor" to your data. If you lose your three words, any messages already encrypted with that specific key become **permanently inaccessible**. We cannot reset the key for existing files because we never held the secret to begin with.

* **Can I change my encryption settings?**
Yes. You maintain full control over your security configuration via your **Account Page**. You can update your encryption key at any time by providing a a new **Key Name** and a new set of **Three Words**. 
    - *Future Emails:* All incoming emails received after the update will be secured using your new credentials.
    - *Legacy Emails:* Messages previously encrypted will still require the original words used at the time of their arrival.

* **What algorithms do you use?**  
We rely on industry-standard primitives: **AES-256** for data at rest, and **Argon2id** with **X25519** for key derivation.