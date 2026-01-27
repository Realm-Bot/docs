---
label: Tebex
description: Integrate Tebex with Realm Bot to automate in-game reward delivery (e.g., ranks and perks) after a successful store purchase.
order: 97
author:
  - name: Kaii
    avatar: https://avatars.githubusercontent.com/u/72093371?s=96&v=4
  - name: Frazer
    avatar: https://avatars.githubusercontent.com/u/136254012?s=96&v=4
---

# Tebex

Tebex (formerly known as **Buycraft**) is a dedicated webstore and monetization platform used by Minecraft communities to sell **ranks**, **perks**, **cosmetics**, and other digital products. Realm Bot integrates with Tebex to support **automated fulfilment**, allowing eligible purchases to be delivered in-game with minimal staff intervention.

> **Important:** You are responsible for ensuring your store configuration and products comply with all applicable Minecraft / Microsoft monetization requirements, as well as your own server rules and policies.

---

## What This Integration Does

When connected, Realm Bot can fulfil Tebex purchases by delivering configured rewards in your Realm (for example, issuing a purchased rank to the correct player).

This is intended to:
- Reduce manual staff workload (“granting ranks by hand”).
- Improve delivery speed and consistency.
- Provide a clearer audit trail when paired with your moderation/logging workflow.

---

## Requirements

To use the Tebex integration:

- **Realm Bot Premium** must be active.
- You must have a Tebex store with a configured **Game Server**.
- You must obtain your Tebex **Secret Key** (sometimes shown as “Secret Code”) and keep it private.

> **Security Notice:** The Secret Key authorises access to your Tebex server integration. Do not share it publicly, do not paste it in general channels, and rotate it immediately if you believe it has been exposed.

---

## How to Set Up

1.  Create a Tebex account and create a **Game Server** in Tebex.  
    ![Tebex Game Server Setup](/images/tebex/1.png)

2.  Select **Minecraft** as the platform for your webstore.  
    ![Tebex Select Minecraft](/images/tebex/2.png)

3.  Choose **Minecraft: Bedrock Edition**.  
    ![Tebex Select Minecraft](/images/tebex/3.png)

4.  Copy the **Secret Key / Secret Code** only.  
    ![Tebex Secret Key](/images/tebex/4.png)

5.  Open the **Tebex** module inside the Realm Bot Dashboard.  
    ![Dashboard Tebex Module](/images/tebex/dash-5.png)

6.  Enable the module, paste your Tebex **Secret Key**, then select **Save**.

7.  Confirm that both Realm Bot and Tebex show a **Connected** status.  
    ![Connected Status Tebex](/images/tebex/7.png)

---

## Creating Products on Tebex

Once the integration is connected, create products on Tebex (ranks, bundles, subscriptions, etc.) and configure the fulfilment method required by your Realm Bot setup.

Operational recommendations:
- Use clear, consistent product naming (e.g., `Rank: Knight`, `Rank: Emperor`).
- Keep “rank” products separate from “consumable” products (keys, crates, boosts) for easier support.
- Maintain an internal list of products and their intended in-game outcomes for staff reference.

For full Tebex store configuration and product tooling, refer to the official Tebex documentation:
https://docs.tebex.io/

---

## Troubleshooting

### “Not connected” / “Connection failed”
- Re-check that you copied the **Secret Key** (not other identifiers).
- Ensure there are no extra spaces before/after the key when pasted.
- Re-save the module settings after pasting the key.

### Purchases are not delivering
- Confirm the Tebex module remains **Enabled** in the dashboard.
- Confirm the purchase is marked as **Completed** in Tebex.
- Verify the product is configured correctly and maps to the intended in-game reward flow.
- If your Realm Bot environment requires an in-game delivery path (depending on your configuration), confirm the required components are online and operational.

### Incorrect player received the reward
- Ensure the store instructions clearly tell buyers what identity (username / gamertag) must be provided at checkout.
- Avoid ambiguous naming conventions and ensure staff have a consistent process for resolving mis-claims.

If you need support, include:
- Your Tebex store/server name
- A screenshot of the module connection status
- The order ID (or transaction reference) from Tebex
- The expected outcome vs the observed outcome
