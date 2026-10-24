# Tebex

Tebex is a webstore and monetisation platform used by Minecraft communities to sell ranks, perks, cosmetics, and other digital products. Realm Bot can poll a connected Tebex game server and execute configured fulfilment commands in a Minecraft Bedrock Realm.

> **Important:** Store owners are responsible for complying with applicable Minecraft and Microsoft monetisation requirements and for testing every product before public sale.

## Requirements

- An active Realm Bot Premium subscription
- A Tebex store with a Minecraft Bedrock game server
- A valid Tebex **Secret Key**
- The Tebex module enabled for the correct Realm
- A Relay Account connected to and present in the Realm
- Sufficient in-game permission for each delivery command
- The GameTest Pack and Beta APIs only when a product uses an empty-inventory-slot condition

> **Security Notice:** Keep the Secret Key private. Rotate it immediately if it is exposed.

## How Delivery Works

After the integration has been verified and initialised during connected Realm activity, Realm Bot checks Tebex's online and offline command queues approximately every **30 seconds**.

For each eligible command, Realm Bot:

1. Resolves the target player's identity.
2. Applies configured delays or conditions.
3. Executes the command through the Relay Account.
4. Records delivery information in the selected Discord channel, where configured.
5. Marks a successfully processed queue command as complete.

Delivery is periodic rather than instant. Disconnections, invalid commands, missing permissions, or unmet delivery requirements can delay or prevent fulfilment.

## Set Up Tebex

1. Create a Tebex account and a **Game Server**.
   ![Tebex Game Server Setup](/images/tebex/1.png)
2. Select **Minecraft**.
   ![Tebex Select Minecraft](/images/tebex/2.png)
3. Choose **Minecraft: Bedrock Edition**.
   ![Tebex Select Minecraft](/images/tebex/3.png)
4. Copy the **Secret Key / Secret Code**.
   ![Tebex Secret Key](/images/tebex/4.png)
5. Open **Tebex** in the Realm Bot Dashboard.
   ![Dashboard Tebex Module](/images/tebex/dash-5.png)
6. Enable the module, enter the Secret Key, and save.
7. Select a delivery-log channel.
8. Confirm the integration reports **Connected**.
   ![Connected Status Tebex](/images/tebex/7.png)

## Product Commands

Tebex commands can use the following player placeholders:

- `{player}`
- `{name}`
- `{username}`
- `{uuid}`
- `{id}`

Use the placeholder expected by the command and test it with a controlled purchase. Products may also include a delivery delay.

An **empty inventory slots** condition uses the GameTest Pack to inspect the player's inventory before delivery. Enable Beta APIs and keep the pack current before relying on this condition.

## Operational Guidance

- Test every product with a low-value private package.
- Use explicit player targets and commands supported by Minecraft Bedrock.
- Keep a staff record of each product and its intended outcome.
- Monitor the delivery-log channel and Tebex queue after changes.
- Treat a condition-blocked or failed delivery as requiring staff review; do not assume it will always retry automatically.

## Troubleshooting

### The integration is not connected

- Confirm the Secret Key was copied without additional spaces.
- Re-save the module and confirm Tebex accepts the key.
- Verify the correct Realm is selected.

### A purchase is not delivering

- Confirm the purchase is completed in Tebex.
- Allow at least 30 seconds for the next queue check.
- Confirm the Relay Account is online and has sufficient command privileges.
- Confirm the configured command uses a supported placeholder and valid syntax.
- Check the delivery-log channel and Tebex queue.
- If empty-slot validation is used, confirm the GameTest Pack is current and Beta APIs are enabled.

### The wrong player is targeted

- Confirm the buyer supplied the correct Minecraft gamertag.
- Review the placeholder used by the product command.
- Pause the product until a controlled test identifies the mismatch.

When requesting support, provide the Realm name, Tebex order reference, approximate purchase time, configured outcome, and observed result. Never include the Secret Key.
