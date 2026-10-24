# Member Gate

Member Gate evaluates players as they join a Realm and removes those who match configured entry rules. It is intended for communities that apply platform restrictions or cautious profile-based onboarding.

> **Important:** Profile signals can be incomplete or private and may produce false positives. Member Gate should support, not replace, staff review and a clear appeal process.

## How Rules Work

- A Realm can have up to **20 rules**.
- Each rule can contain up to **10 conditions**.
- All conditions within a rule must match before the rule triggers.
- Users on the Realm Bot allowlist are exempt.
- Actions are recorded in the configured Automod logging channel.

Although the dashboard may display Kick and Ban choices, current rule enforcement removes matching players with a **kick**. Do not rely on a Ban selection for persistent enforcement.

Realm Bot may also apply additional account-consistency checks while Member Gate is enabled. These checks are intentionally not exposed in detail.

## Available Conditions

Rules can evaluate:

- **Device includes** or **device excludes**
- **Gamerscore above** or **below** a selected value
- **Followers above** or **below** a selected value
- **Following above** or **below** a selected value

Supported platform information may include Android, iOS, Windows, Xbox, PlayStation, and Nintendo where it is available from the connection.

## Private Title History

Member Gate can require public Xbox game and app history. If this profile signal is private, Realm Bot may be unable to confirm device context and may remove the player.

Players affected by this reason should follow [Private Title History troubleshooting](../Troubleshooting/private-title-history.md).

## Requirements

- An active Realm Bot Premium subscription
- Member Gate enabled for the correct Realm
- A Relay Account connected to and present in the Realm
- Access to the player's Xbox profile information
- A Discord Automod destination for enforcement records

The GameTest Pack is not required for Member Gate.

## How to Set Up

1. Open **Member Gate** in the Realm Bot Dashboard.
   ![Member Gate Configuration](/images/member-gate.png)
2. Enable the module and select an Automod destination.
3. Configure whether private title history should be checked.
4. Create a clearly named rule and add only the conditions required for that policy.
5. Save the rule, then test with both a permitted and a deliberately non-matching account.

## Recommended Configuration

- Start with one conservative rule and review its logs before adding more.
- Prefer device rules for explicit platform policies.
- Avoid aggressive gamerscore or social thresholds for communities with new or younger accounts.
- Publish entry requirements and provide an appeal route.

## Troubleshooting

### Rules do not trigger

- Confirm Member Gate is enabled for the selected Realm.
- Confirm the Relay Account is online and receiving join events.
- Check that every condition in the rule is intended to match.
- Confirm the player is not allowlisted.

### Legitimate players are removed

- Review the exact rule recorded in the Automod log.
- Relax profile thresholds or test one condition at a time.
- Check whether Xbox privacy settings are hiding required profile data.
- Add a verified trusted player to the allowlist where appropriate.
