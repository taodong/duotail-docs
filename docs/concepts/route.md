---
sidebar_label: Route
sidebar_position: 2
---

# Route

## What is a Route?

A **Route** defines the rules for incoming emails. The text following the last underscore in an address is the Route ID. For example, in `a_happy.rhino_food@duotail.com`, `food` is the route. If a route rule allows `deliciousgrass.com`, any emails from that domain will be delivered to your inbox.

## Route Email

A Route Email is an address structured as `<channel_id>_<route_id>@duotail.com`. For an incoming email to pass through a route, it must comply with either the specific rules of that route or the general rules of the channel to which it belongs.

### Permissions
Whether an incoming email is delivered to a user is determined by a combination of three types of permissions at the route level:

- **Domain Permission:** This permission applies to a specific domain and all its subdomains. It can be set to either `Enabled` or `Disabled`. For example, if deliciousgrass.com is enabled, emails from both `deliciousgrass.com` and `em.deliciousgrass.com` are permitted.  
- **Email Permission:** This permission applies to a specific email address. It can be either `Enabled` or `Disabled`. For example, if `spmail@em.deliciousgrass.com` is disabled, all emails from that specific address will be blocked.  
- **Stamp List:** Any email addresses included in the Stamp List are automatically blocked.  

:::note Reply Handling
If you reply to any email received through a route, an `Email Permission` for that sender will be automatically added to the route settings. This ensures that their future messages are always permitted.
:::


## Route Type

There are two types of routes available for our users: subscription route and one-shot route.

### Subscription Route
A **Subscription Route** is designed to help users manage their email subscriptions effectively. It allows for the creation of comprehensive rules to tailor incoming email permissions specifically for subscription scenarios. Subscription route allows only **Domain Permission** and **Email Permission**. 

#### First Email Auto Permission
When a new Subscription Route is created, we recommend leaving the permissions undefined initially. If no permissions are set, the first email to reach the route will be automatically permitted. Furthermore, the host domain of that email will be added to your permission list with the status set to "Enabled." This feature is specifically designed to ensure that third-party confirmation emails reach your inbox without delay.

#### Subscription Route Incoming Email Decision Hierarchy
When multiple permissions are set within a subscription route for emails from the same domain, the final decision is determined by a hierarchical "top-down" logic. The system searches for the most specific match first, moving to more general rules only if a match isn't found.

**The Decision Hierarchy**
1. **Exact Email Match:** The system first checks if the specific email address is listed. If a match is found, the email is `Allowed` or `Denied` based on that specific setting.

2. **Full Domain Match:** If there is no specific email match, the system checks for a rule matching the exact domain (e.g., `example.com`). If a rule exists, it is applied immediately.

3. **Ancestor Domain Match:** If no full domain match exists, the system looks for the closest ancestor domain (e.g., if the email is from `sub.example.com`, it looks for a rule for `example.com`).

4. **Final Fallback:** If no matches are found at any level, the email is `Denied` by default.

![Subscription Permission Logic](/img/concepts/route/sub_permission_logic.png)

#### Disabled Subcription Route
If a subscription route is set to `Disabled`, any incoming emails directed to that specific route address are automatically trashed.

### One-Shot Route 
A **One-Shot Route** is designed to handle "serendipity" style interactions, such as those originating from networking events or public inquiries. Under this route, only the first email from a new sender is delivered to your inbox.

In addition to standard domain and email permissions, the One-Shot Route utilizes a built-in **Stamp List** to track previous senders. Once a sender has messaged you, they are added to this list and subsequent emails from them are blocked. To allow a follow-up email from a specific sender, you can simply remove their address from the Stamp List.

**Example:** Suppose `hug` is a One-Shot Route under the channel a_happy.rhino.

- If a new sender, `angry.gazelle@example.com`, sends an email to this route, the message will be delivered.

- However, any subsequent emails from `angry.gazelle@example.com` will be automatically discarded.

#### One-Shot Route Incoming Email Decision Hierarchy
A One-Shot Route determines whether an email is delivered using the following hierarchy:

1. **Permission Check:** The system first follows the same [decision hierarchy as a Subscription Route](#subscription-route-incoming-email-decision-hierarchy), checking all domain and email-level permissions. If an explicit "Enabled" permission is found, the email is delivered immediately.

2. **Stamp List Check:** If no explicit permission is found in Step 1, the system checks the Stamp List. The email will be delivered only if the sender’s address is not already present on the list.

#### Disabled One-Shot Route
If a One-Shot route is set to `Disabled`, any incoming emails directed to that specific route address are automatically trashed.

#### Locked One-Shot Route
To protect against the risk of a One-Shot email address being leaked or falling into the wrong hands, these routes can be `Locked`.

When a route is locked, the system skips the Stamp List check and performs a Permission Check only. In this state, only emails from senders with explicit `Enabled` permissions will be delivered; all other incoming emails will be blocked.
