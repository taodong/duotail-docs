---
sidebar_label: Manage Account
sidebar_position: 7
---

# Manage Account

## Summary
The **Manage Account** page is your central hub for updating your personal profile, managing your subscription, and verifying the email addresses associated with your account.

![Manage Account Page](/img/tutorials/manage-account/manage-account-page.png)

## Account Profile
In the top section, you can manage your basic identity and security settings:
- **Account Name:** Displays the name currently associated with your account.

### Change Name
Click `Change Name` button to update your display name. Since the sender name configured at the `Channel` or `Route` level takes precedence over your `Account Display Name`, updating your name here will not change the sender name for your existing channels or routes.
![Update Name](/img/tutorials/manage-account/update-name.png)

### Change Password
Use `Change Password` button to update your account login password. You must provide both your current and new passwords to complete this change. Please note that submitting a password update will automatically log you out of your account on all devices.

![Update Password](/img/tutorials/manage-account/update-password.png)

### Update Encryption Words
You can rotate your encryption credentials at any time. This is a powerful security feature that ensures your future communications are protected by fresh keys.

#### How to Update
Click the "Update Encryption Words" button.
![Update Encryption Key](/img/tutorials/manage-account/update-encryption-words.png)
A window will appear with two sections: Key Name and File Encryption Words. Fill in your new details and click Save.
![Update Encryption Key](/img/tutorials/manage-account/update-encryption-words-form.png)

#### Understanding the Form Fields
If you are new to zero-knowledge encryption, here is exactly what these fields do:

1. **Key Name**  
    Think of this as a public label for your secret words.  
    *What it does:* It helps you remember which set of words you are currently using. If you have multiple keys over time, this label tells you which one to use when downloading a specific email.
    *Rules:* Maximum 8 characters. Use only letters and numbers (e.g., key2026, youguess). It's case insensitive.
2. **File Encryption Words**  
    These are your private master keys.   
    *What it does:* Our system takes these three words and uses them as the "ingredient" to mathematically build a lock for your emails.   
    *Our Privacy Promise:* We never store these words. They exist only in your mind or your password manager.   
    *Rules:* Each word must be 12 characters or fewer. You can use letters, numbers, and special characters (like !@#$). These are case-sensitive (e.g., "Apple" is different from "apple").

:::important The "Future-Only" Rule
When you update your encryption words, the following happens:
    - New Emails: All emails arriving after the update will be locked with your new words.   
    - Old Emails: Any emails currently in your buffer were locked with your previous words. To download them, you will still need to provide the words associated with the old `Key Name`.
:::

***

#### 🛠️ Technical Transparency
Curious about the math? For a full technical breakdown of how we use `Argon2id` and `X25519` to turn your three words into a zero-knowledge lock, visit our **[Data Encryption Protocol](/privacy/data-encryption-protocol)** page.

### Deactivating Your Account

We believe that true data sovereignty includes the right to leave. If you decide to move on from Duotail, you can manage your departure and data portability directly from your dashboard.

#### 1. Download Email Configuration
Before deactivating, we recommend exporting your routing logic. 

* **Action:** Click the **"Download My Data"** button in your account settings.
* **Result:** You will receive a JSON file containing all your channel configurations, route premissions, and all existing contacts. This ensures you can recreate your routing logic on another platform if needed.

![Download Email Configuration](/img/tutorials/manage-account/download-data.png)

#### 2. Deactivate Account
Deactivating your account is an immediate and final action regarding your email routing.

* **Process:** Click **"Deactivate Account"**. For your security, a confirmation window will appear requiring you to enter your password to authorize the request.
![Deactivate Account](/img/tutorials/manage-account/deactivate-account.png)
![Deactivate Account Form](/img/tutorials/manage-account/deactivate-account-form.png)

:::warning
* **Immediate Effect:** Once confirmed, you will be logged out immediately. All active email gateways associated with your account will cease to function instantly.
* **Data Purge:** Your account information and encrypted records will be marked for deletion. All data will be permanently removed from our active infrastructure and backups during our next scheduled data purge process.
:::

## Subscription Management
![Subscription Section](/img/tutorials/manage-account/subscription-section.png)
This section provides details regarding your current service tier:

- **Plan:** Displays your current plan level (e.g., FREE BASIC).
- **Renewal Date:** Displays the date your subscription is scheduled to renew. Please note that a renewal date is not applicable to the FREE plan.

### Unsubcribe
We are currently refining our automated unsubscription process. In the meantime, please send your unsubscription request directly to our support team at `support@duotail.com`. We will manually downgrade your plan or delete your records as requested.

Clicking the `Unsubscribe` button will display a similar notification. **We sincerely apologize for any inconvenience this manual process may cause and appreciate your patience.**

## Manage Emails
![Emails Section](/img/tutorials/manage-account/email-list.png)
You can link multiple email addresses to your Duotail account to use with various channels. All your emails will be listed under the **Emails** section. 

- **Primary Email:** Labeled with a green `primary` tag. This is your main contact address for account notifications.
- **Unverified Email:** Labled with a yellow `unverified` tag. This is an email address that has not yet been confirmed. Clicking the 'Verify Email' button will trigger a new confirmation email to be sent to that address.

### Add Email
Use the `Add Email` button to link a new email address to your account. Upon submission, the new email will appear in the Emails list with a yellow `unverified` tag.

### Verify Email
For any unverified address, click `Verify Email` button to trigger a confirmation email. You must verify an email before it can be used for channel routing.

### Change Primary Email
You can update your primary email address by clicking the `Make Primary` button located next to any non-primary email address.