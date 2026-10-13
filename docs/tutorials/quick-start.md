---
sidebar_label: Quick Start
sidebar_position: 0
---

# Quick Start: Your Dashboard

The **Dashboard** is the first page you see after signing in. Everything you need for day-to-day use is on this one page, so you can create an email address, receive email, and send email without learning the rest of the application first.

This guide assumes you have already [registered an account](/tutorials/register) and confirmed your email.

## A Tour of the Dashboard

![The Duotail dashboard with its action buttons, Activity, Inboxes and Send Pending sections](/img/tutorials/quick-start/dashboard-full-layout.png)

From top to bottom, the dashboard shows:

| Area | What it is for |
|---|---|
| **Notices** | Short messages about what just happened, such as a new email address being ready. Most can be closed with the **×** on the right. |
| **Action buttons** | **Create Email Address**, **Allow Incoming Emails** and **Add Inbox**. Hover over a button to see a short tip. |
| **Activity → Listening Now** | Email addresses that are temporarily open to a new sender. Only shown while at least one is open. |
| **Activity → Recent Emails** | Your five latest emails and what happened to each one. **View all in History** opens the full list. |
| **Inboxes** | Your inboxes. Each one has a **main email** address and a **recipient**, which is your own email address where Duotail delivers your mail. |
| **Send Pending** | Emails you wrote that are waiting for you before they can go out. Only shown on a paid plan, and only when something is waiting. |

:::info What a free account can do
A free account can receive emails and reply to them. Starting a new email and adding more inboxes require a paid plan. On a free account the **Add Inbox** button and the **Send Pending** section are not shown, and a notice with an **Upgrade** link appears at the top of the dashboard.
:::

### Two Words You Will See Often

- **Inbox** – a group of email addresses that all start with the same name. For example, the inbox `a_happy.rhino` owns `a_happy.rhino@duotail.com` (its main email) and every address that starts with `a_happy.rhino_`. Other pages of this documentation call an inbox a [channel](/concepts/channel).
- **Email address** – an extra address inside an inbox that you create for one purpose, such as `a_happy.rhino_news@duotail.com`. Other pages call this a [route](/concepts/route).

Duotail does not store a mailbox for you to open. Email that is allowed through is forwarded to the **recipient** address of the inbox, so you keep reading and writing email in the mail app you already use.

### Before You Start: Check Your Inbox Is Ready

Look at the **Inboxes** table. An inbox can be used when its row shows a **Manage** button. If you see another button instead, click it first:

- **Activate** – your own email address is not confirmed yet. Follow the confirmation link we emailed you.
- **Initialize** – the inbox needs a one-time setup. One click completes it.

Until this is done, a yellow notice above the table tells you which inboxes cannot receive email yet.

## 1. Create an Email Address

There are two ways to get a new email address. Use the first for everyday needs; use the second when you want a whole new inbox with its own main email.

### Option A: Create Email Address

Use this when you need an address to give out, for example when signing up for a website or a newsletter.

1. Click **Create Email Address**. The **New Email Address** window opens.
2. **Address** – type a short name for the address, such as `news`. You can use lowercase letters, numbers and periods, up to 20 characters. The full address is shown as you type, for example `a_happy.rhino_news@duotail.com`. If you have more than one inbox, first choose which inbox the address belongs to.
3. **Delivery** – choose which of your own email addresses should receive the mail. This step only appears if you have more than one confirmed email address.
4. **Purpose** – choose how strict the address should be:
   - **Permission Enforced** – best for subscriptions, online shopping, or membership sign-ups. The first email that arrives is let through and its sender is remembered; other senders are blocked until you allow them.
   - **Cold Reach Allowed** – lets one email through from each person you have not heard from before. Use it for an address you hand out to people, such as on a business card.

   ![The Purpose step of the New Email Address window, with Permission Enforced selected](/img/tutorials/quick-start/new-email-purpose.png)
5. **Details** – describe what you will use the address for (up to 30 characters). For a Permission Enforced address you can also note who you expect to hear from.
6. **Confirm** – check the summary and click **Finish**.

A green notice confirms that your new address is ready. Click **Copy email address** in the notice to copy it, then paste it wherever you need it.

![Green notice showing the new address with a Copy email address link](/img/tutorials/quick-start/new-email-ready-banner.png)

:::tip
You can create as many addresses as you like. Still, you do not need a new one for every website. We recommend keeping one address per purpose, such as one for all your newsletters and another for online shopping, and reusing it for every sender of that kind. Each time you give the address to a new sender, use [Allow Incoming Emails](#option-c-allow-incoming-emails) to let that sender in.
:::

### Option B: Add Inbox (Paid Feature)

Use this when you want a separate inbox with its own main email address, for example to keep work and personal email apart.

1. Click **Add Inbox**. The button is shown on a paid plan once you have a confirmed email address.

   ![The Add Inbox window with Email, Channel and Identity Channel fields](/img/tutorials/quick-start/add-inbox-form.png)
2. **Email** – choose which of your own email addresses receives the mail for this inbox.
3. **Channel** – type the name of the inbox. It must be 5–30 characters, using lowercase letters, numbers and dots, and it cannot start or end with a dot. The name is prefixed with `a_`, so `happy.rhino` becomes `a_happy.rhino@duotail.com`.
4. **Identity Channel** – if this checkbox is shown, tick it to create an address without the `a_` prefix. See [Identity Channel](/concepts/channel#identity-channel) for what this means.
5. Click **Submit**.

The new inbox appears in the **Inboxes** table. If its row shows **Initialize**, click it to finish the setup. Use **Copy Email** on the row to copy the main email address.

:::note
Only your contacts can send email to an inbox's main email address. To let someone reach it, [create a contact](#option-a-create-a-contact) for them.
:::

## 2. Receive Email

Duotail blocks email by default and lets through only what you have allowed. There are three ways to allow a sender. Whichever you choose, the email is delivered to your recipient address and listed under **Recent Emails**.

| You want to… | Use |
|---|---|
| Always receive email from a person you trust, on any address of an inbox | [Create a contact](#option-a-create-a-contact) |
| Decide exactly which senders an email address accepts | [Configure the email address](#option-b-configure-the-email-address) |
| Let one new sender through for a short time, such as a sign-up confirmation | [Allow Incoming Emails](#option-c-allow-incoming-emails) |

### Option A: Create a Contact

A **contact** is a sender you trust. Email from a contact always reaches the inbox's main email and every other address in that inbox.

1. In the **Inboxes** section, click **Create a contact** in the blue notice above the table. The **Create Contact** window opens.
2. **Who is this?** – fill in:
   - **Email to Send** – a short name of your choice. It becomes the address you write to when you want to email this contact, in the form `2_<name>@duotail.com`.
   - **External Email** – the contact's real email address.
   - **Name** – a name to recognize the contact by (5–30 characters).

   ![The Who is this? step of the Create Contact window](/img/tutorials/quick-start/create-contact-who.png)
3. Click **Next**.
4. **Where does it live?** – choose the inbox (**Channel**) the contact belongs to. **Route** and **Notes** are optional.
5. Click **Finish**. A short message confirms that the contact was created.

If you have closed the blue notice, reload the page to bring it back, or click **Manage** on the inbox and add the contact from its **Contacts** section. See [Manage Contacts](/tutorials/manage-contact) for viewing, changing and deleting contacts.

### Option B: Configure the Email Address

Every email address you create has its own list of permitted senders. You can edit that list at any time.

1. In the **Inboxes** table, click **Manage** on the inbox that owns the address.
2. Find the address in the table and open it for editing.
3. Add the sender's domain (for example `example.com`) or exact email address to its permissions and save.

The full walkthrough, including how to block a sender again, is in [Manage Routes](/tutorials/manage-route#route-permissions).

:::tip
A new **Permission Enforced** address needs no configuration for its first sender. The first email that arrives is let through and that sender's domain is permitted from then on.
:::

### Option C: Allow Incoming Emails

Use this when you are about to give an existing address to a new sender and expect an email soon, for example a confirmation email after signing up on another website.

1. Click **Allow Incoming Emails**. The **Turn On Listening** window opens.
2. **Which address should we watch?** – choose the address the email will be sent to. If you have more than one inbox, choose the inbox first.
3. **How soon do you expect it?** – choose **30 minutes**, **1 hour** or **8 hours**. You can also note who the email is from.

   ![The Turn On Listening window asking how soon the email is expected](/img/tutorials/quick-start/turn-on-listening.png)
4. Check the summary and click **Finish**.

A yellow notice confirms that we are listening, and the address appears under **Activity → Listening Now**. From there you can **Copy Email** to paste the address into the other website, or **Turn Off** to stop early.

The next email from a new sender to that address is delivered, and that sender is permitted from then on. Listening then stops by itself. It also stops when the time you chose runs out.

:::tip Choose the shortest time
Pick the shortest time in which you expect the email. The shorter the window, the less chance an unwanted sender gets through.
:::

Good to know:

- Only **Permission Enforced** addresses that already have at least one permitted sender are listed. A brand-new address does not need this step because it already accepts its first sender.
- Each inbox can listen on one address at a time. Turning on a new one replaces the current one; you are warned before this happens.
- If the window says you need an address first, [create one](#option-a-create-email-address) and choose **Permission Enforced**.

## 3. Send Email (Paid Feature)

:::info
Starting a new email requires a paid plan. On a free plan you can still reply to any email you received through Duotail.
:::

You send email from your own mail app, not from the dashboard. Instead of writing to a person's real address, you write to their Duotail contact address, which starts with `2_`. Duotail then delivers your email to the real address and shows your Duotail address as the sender, so your own email address stays private.

Always send from the **recipient** email address of the inbox. Email sent from any other address is not delivered.

### Option A: Send to an Existing Contact

1. Find the contact's **Email to Send** address. Click **Manage** on the inbox, then open its **Contacts** section. The address looks like `2_matt.kansher@duotail.com`.
2. In your own mail app, write a new email to that address and send it.

The email appears under **Recent Emails** with the status **Sent**.

### Option B: Send First, Add the Contact Later

You do not have to create a contact before writing. Make up a `2_` address on the spot and Duotail holds your email until you tell it who the address belongs to.

1. In your own mail app, write an email to a new address of the form `2_<name>@duotail.com`, for example `2_matt.kansher@duotail.com`, and send it.
2. Open the dashboard. The email is listed in the **Send Pending** section.
3. Click **Send** on its row. The **Create Contact** window opens with the **Duotail Contact Address** already filled in.

   ![The Create Contact window with the Duotail Contact Address already filled in](/img/tutorials/quick-start/send-pending-create-contact.png)
4. Enter the contact's **External Email** (their real address) and a **Name**, then click **Next**.
5. Choose the inbox the contact belongs to and click **Finish**.
6. If you are asked for your **File Encryption Words**, enter your three encryption words. See [Understanding Encryption Fields](/tutorials/manage-account#understanding-the-form-fields) if you are unsure what these are.

The email leaves the **Send Pending** list and is sent. A notice asks you to check the **History** page for its final status. From now on, emails to that `2_` address are sent straight away, as in Option A.

The other buttons on a pending row:

- **View** – read the email before deciding.
- **Delete** – discard the email without sending it.

:::note Monthly sending limit
Your plan includes a monthly number of emails you can send this way. If you have reached it, a notice tells you so when you click **Send**, and the email stays in **Send Pending** until the limit resets next month.
:::

## Where to Go Next

- [Manage Routes](/tutorials/manage-route) – fine-tune who can reach each email address.
- [Manage Contacts](/tutorials/manage-contact) – view, change and delete contacts.
- [Manage History](/tutorials/manage-history) – see every email and download or delete it.
- [Manage Account](/tutorials/manage-account) – your profile, email addresses, encryption words and subscription.
- [White List Our Domain](/tutorials/white-list-domain) – make sure emails from Duotail are not treated as junk.
