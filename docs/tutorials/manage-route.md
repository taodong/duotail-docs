---
sidebar_label: Manage Routes
sidebar_position: 4
---

# Manage Routes
:::info 
**Routes** are a core feature of our platform and one of the key elements that set our service apart from others. If you are new to the system, we highly recommend reading our [Route Guide](/concepts/route) to get started.
:::

## Summary
**Route Management** is located within the **Channel** section of each individual channel page. In addition to managing specific routes, this section includes a **Channel Settings** segment at its top. Here, users can view or update global channel configurations, which serve as the default values for every new route created within that channel.

To access the Route Management section, simply click the `Manage` or `Initialize` button for any channel listed on your Home Page.
![Sample Channel Section](/img/tutorials/manage-route/sample-channel-section.png)
## Route Table
The **Route Table** is the central component of the Channel section, displaying all existing routes configured under the current channel.  
Each row in the table provides a summary of a specific route's configuration:  
- **Route ID:** The unique identifier for the route.  
- **Description:** A user-defined label or note describing the route's purpose.  
- **Recipient:** The destination email address where messages passing through this route are delivered.  
- **Type:** The specific classification of the route - `Subscription` or `One Shot`.  
- **Status:** The current state of the route - `Enabled`, `Disabled`, or `Locked`.
- **Actions:** - Management tools available for the route.

## Update Default Channel Settings

You can modify your default configurations by clicking the `Edit Channel Settings` button. The following settings are available in the configuration window:
![Update Channel Settings Window](/img/tutorials/manage-route/update-channel-settings.png)
- **Channel Name:** The unique identifier for the current channel. This is a read-only field.  
- **Sender Name:** The default name displayed on all outgoing emails sent through this channel. If this field is left empty (the default state upon initialization), the system will use your name when registered.  
- **Channel Email:** A dropdown menu that allows you to change the channel's destination to any verified email address associated with your account.

:::warning Security Note
We actively monitor sender names for compliance. To prevent phishing and fraud, any attempt to misguide recipients by using a deceptive sender name will result in immediate account suspension.
:::

## Create Routes
You can create a route by clicking the `Add Route` button located below the bottom of the `Route Table`. The `Add Route` configuration window features two tabs: `Essential` and `Permissions`.

### Route Essentails
![Add Route Essential](/img/tutorials/manage-route/add-route-essential.png)
The **Essential** tab contains the primary fields required to create a route:
- **Route ID:** A unique identifier for the new route.
- **Description:** A brief note explaining the purpose of the route.
- **Recipient:** A dropdown menu to select the destination email address where messages received via this route will be delivered.
- **Type:** A dropdown menu to select the route logic—either `Subscription` or `One Shot`.

### Route Permissions
![Add Route Permissions](/img/tutorials/manage-route/add-route-permissions.png)
The **Permissions** tab allows you to configure specific access rules for the route. You can manage two types of permissions: `Domain Permissions` and `Email Permissions`.

#### Adding a Permission
To add a new rule, enter the following details and click the **`+`** button:
- **Name (Optional):** A label to help you identify the permission.
- **Value:** The specific domain (e.g., example.com) or the full email address you wish to manage.
- **Type:** A dropdown menu to specify whether the value is a `Domain` or an `Email`.

#### Managing Permissions 
A permission is successfully added once it appears as a "pill" on the tab. You can control the behavior of each permission by toggling its status:  
- **Allowed (Green Pill):** Emails from the specified domain or address are permitted to pass through the route.  
- **Rejected (Gray Pill):** Emails from the specified domain or address will be automatically blocked. 

You can switch between `Allowed` and `Rejected` status simply by clicking on the permission pill.

To understand how our system determines whether an email is permitted when multiple overlapping permissions exist, please refer to our [Route Guide](/concepts/route) for a detailed explanation of the decision hierarchy

#### Removing a Permission
To permanently delete a permission from the route, click the **`x`** icon located at the right end of the permission pill.

:::tip Empty Permission Subscription
We recommend leaving permissions undefined when creating a new **Subscription** route. If no explicit permissions are set, the system will automatically permit the first incoming email it receives. This is particularly useful for handling automated confirmation or verification emails generated by third-party services.
:::

## Update Routes
You can update a route's configuration by clicking the 'Update' button located in the 'Actions' column of the 'Route Table'.

## Related Topics

You may also want to check out the following related topics

[Route Guide](/concepts/route)