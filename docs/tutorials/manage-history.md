---
sidebar_label: Manage History
sidebar_position: 6
---

# Manage History

## Summary
The **History Page** is the centralized hub where all emails processed through your channels and routes are collected. This area allows you to review records and recalibrate your route configurations based on actual traffic.

![Free Plan History](/img/tutorials/manage-history/history-free-user.png)

All email records from the past 30 days are directly accessible here. While we provide complimentary storage for 60 days for all processed emails, records older than 30 days must be manually retrieved. To request older records, please contact `support@duotail.com`.

:::note Privacy Note
We never view your email content without your explicit permission. Furthermore, once a record is deleted through the History page, it is removed permanently from our systems.
:::

##The History Table
The central component of this section is the **History Table**, which lists every email sent or received by your account over the last 30 days. Each row contains the following details:

- **ID:** Our internal email ID. Please provide this ID when submitting inquiries or support requests regarding a specific record.
- **From:** The email address found in the `From` field of the message.
- **To:** The email address found in the `To` field of the message.
- **Subject:** The subject line of the email.
- **Date:** The date and time the email was processed by our system.
- **Status:** The current processing status (e.g., Sent, Saved, or Blocked).
- **Actions:** Available tools for the record, including `Download` and `Delete`.

:::tip Pro Tip
If a field is too long to fit in the table, only the beginning will be displayed. Simply hover your mouse over the field to reveal the full value.
:::

### Email Processing Statuses
If an email is processed successfully, you will see one of the following statuses applied to your email record:
- **Sent:** The email was successfully delivered to the intended recipient.
- **Saved:** The email was not delivered to your inbox but has been securely stored in our system for your review.
- **Blocked:** The email was silently intercepted and deleted based on your configuration rules.

In rare cases where the system fails to process a record (e.g., corrupted email content), the status will reflect the error, and you will be given the option to download the original file for manual review.

### Download Email
If an email is stored in our system, a `Download` button will appear in the Actions column. Clicking this allows you to download the email in .eml format, which can be opened by almost all local mail clients.

### Delete Email
If an email is stored, a `Delete` button will also be available. Clicking this deletes the file permanently; no recovery is possible after this action.

## Storage Policy
We store all processed emails as a safeguard in case of system delivery issues.

- **Free Plan:** Emails that do not meet your defined rules are Blocked to reduce operational costs.
- **Paid Plans:** Emails that do not meet defined rules are Saved, allowing you to review them later.

**Sample History Table of Paid Plan**
![Paid Plan History](/img/tutorials/manage-history/history-paid-user.png)