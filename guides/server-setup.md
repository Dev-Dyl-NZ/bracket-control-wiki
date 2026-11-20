---
layout: default
title: Discord Server Setup
description: "Connect your Discord server to Bracket Control and use Automatic or Manual Setup to configure optional channels for teams, brackets, drafts and match results."
permalink: /guides/server-setup/
---
# Discord Server Setup

Connect your server, then configure only the features your community uses. **Every Discord channel is optional.** No registration role, player-registration channel or verification message is needed.

## Connect and choose a method

1. Sign in with Discord and open **Your Discord servers**.
2. Connect the server you manage and invite the bot if needed. Server owner or administrator access is required.
3. Open **Complete server setup**, or **Server settings → Open Server Setup**.
4. Choose **Automatic Setup** to create selected resources after review, or **Manual Setup** to select resources you have already created in Discord.

Manual Setup keeps existing channel names and permissions. Existing channels default to **Keep Current Location**; only separately approved moves change their location. Use **Refresh Discord inventory** after making changes in Discord.

## Reconnect a disconnected server

Removing the Bracket Control bot in Discord disconnects the server automatically. It leaves the active server selector, and Discord-dependent registration, notifications, channel updates and draft automation pause. Tournament records, completed brackets, teams and match results are kept. Existing history links still follow the tournament's access settings.

If you still manage the Discord server, open **Your Discord servers**, find it under **Disconnected servers**, and select **Reconnect Discord Bot**. Complete the Discord installation and return to Bracket Control. If someone has already invited the bot back, open **Server settings** and select **Check bot connection**.

Bracket Control keeps the original community and its settings. Review any channel or role warnings in **Server settings** and correct them in Discord or update the saved selections. Reconnecting uses valid existing settings and skips outdated one-off messages. Review any interrupted tournament before continuing.

A permanently deleted Discord server cannot be reconnected. Connect a replacement server as a new community, even if it has the same name. The original tournament history stays with the original Discord server.
## Choose optional channels

| Setting | Purpose |
| --- | --- |
| Team Registration and Management | Captains enter ready-made teams and manage their teams. |
| Tournament Announcements | General tournament announcements. |
| Registered Teams | Approved team lists. |
| Bracket Updates | Bracket images and updates. |
| Standings | Rankings and weekly ladders. |
| Match Results | Results and scoresheets. A channel named #claim-rank can be used here. |
| Staff Approvals | Private staff notifications for team applications. |
| Support Ticket Panel | Entry point for private support tickets. |
| Draft Voice Waiting Room | Optional waiting room for draft voice automation. |

Choose **Not Required** for unused features. Website-only organisers can leave every channel unused. Draft-only communities can configure a waiting room without team-registration or staff-approval channels. Standard tournament communities can choose team registration, announcements and results as needed.

Keep Staff Approvals private. If you enable support tickets, select its panel channel, private category and support staff settings. Choose categories only where needed. Existing configured channels and support settings remain available.

### Understand the category preview

Each category has a short explanation and a list of channels assigned to it. The preview uses your selected Discord names and updates immediately when you change a selection, edit a proposed name or enable or disable Support Tickets. The same grouping appears on **Review & Confirm**.

| Category | Used for |
| --- | --- |
| Bracket Control | Team registration, announcements, approved team lists, brackets, standings and results. |
| Community Support | The public support ticket panel where members ask for help. |
| Staff Management | Private team approvals and staff notifications. |
| Support Tickets | Individual private ticket channels, separate from the public panel. |
| Tournament Voice | The draft waiting room and temporary captain and team voice rooms. |

Check the action beside each resource:

- **Create:** Bracket Control will create a new channel or category after approval. New channels show the selected category, or say they will be created without one.
- **Reuse:** Bracket Control will use the selected existing resource. Existing channels default to **Keep Current Location** and appear under their actual current category.
- **Move — Explicit Approval Required:** An existing channel will move only after its separate acknowledgement and the normal setup confirmation. The acknowledgement names the channel and its original and proposed categories. Permissions are kept without synchronising them to the destination.
- **Not Required:** The resource will not be configured. Disabled optional channels are not created; disabling Support Tickets creates no support channel, ticket category or panel.
- **Created When Needed:** Individual private ticket channels are created only when a member opens a ticket. Existing draft voice automation can create temporary captain and team rooms when required, in the waiting room's actual category. Setup does not create these temporary rooms.

Automatic Setup offers creation and reuse. Manual Setup only selects existing resources; enabling tickets or draft voice still allows their existing workflows to create channels later when needed. Review the grouped actions before approving the existing confirmation checkbox.

### Fit your existing server structure

Every configured channel has a **Category for ...** dropdown. It lists the server's existing categories, optional recommended Bracket Control categories in Automatic Setup, **No Category**, and **Keep Current Location** for existing channels. The current location is shown beneath each existing channel's selection.

For a migrating community, select your existing channels and leave **Keep Current Location** selected. No reorganisation or permission changes are needed. For new channels, choose a compatible existing category or an optional recommended category. Unused proposed categories will not be created. Manual Setup uses only existing channels and categories.

Changing a category moves the channel between the proposed layout groups immediately. On **Review & Confirm**, check each existing channel's current and destination categories. Each move needs its own unchecked acknowledgement as well as the normal setup confirmation. Existing channel names and permissions stay unchanged.

Moves are blocked if the destination has a different visibility audience, if permissions cannot be verified, or if the bot or approving administrator cannot view and manage the channel and destination. Choose Keep Current Location or correct permissions directly in Discord; setup never synchronises existing channel permissions for you. Draft waiting rooms cannot move while a draft is live, and existing temporary voice rooms are never relocated by setup.

The public support panel has its own channel location. The separate **Support Tickets** category still controls where private ticket channels are created when members request help. Staff Approvals remains private to authorised tournament staff; choosing a support role does not grant tournament administration access.

### Support ticket closure settings

After setup, open **Server Management → Support Tickets → Support Ticket Settings** to manage tickets for that Discord server. The following options are enabled by default:

| Setting | What it does |
| --- | --- |
| **Send closure DM** | DMs the ticket creator a closure confirmation with the server, ticket number and closure time. |
| **Attach ticket transcript** | Includes a downloadable `.txt` conversation transcript in that DM; requires closure DMs to be enabled. |
| **Allow members to reopen via DM** | Includes a **Reopen Ticket** button for the original creator; requires closure DMs to be enabled. |
| **Automatically delete closed ticket channels** | Removes the Discord channel immediately after a complete, encrypted transcript is successfully archived and verified, provided no preservation hold blocks deletion. |

These settings apply per server. Turning off automatic channel deletion keeps closed ticket channels until an administrator explicitly manages them; it does not switch to delayed automatic deletion. If archiving or integrity verification fails, the bot preserves the channel for review. Failed Discord DM delivery does not prevent a completed ticket closure or an otherwise safe channel cleanup.

Support staff can manage tickets without inheriting tournament-administration permissions. Authorised administrators can reopen closed tickets through the dashboard.

## Review and finish

1. Continue to **Optional messages** and choose whether to publish the team-registration message.
2. Review **Support Ticket Configuration**; leave tickets disabled if unused.
3. Select **Review Configuration** and check the proposed actions.
4. Check the confirmation, then select **Apply Configuration**.
5. Select **Go to Dashboard** when setup completes.

If setup was interrupted before simplification, review a new plan. Existing roles, channels and messages are not automatically deleted. For a current interrupted plan, confirm **Resume setup** after any displayed Discord wait.

The bot needs permissions only for features you use: text publishing needs channel access, sending messages, embeds, attachments and message history. Creating channels needs Manage Channels and View Audit Log. Draft voice also needs Connect and Move Members. Support ticket privacy checks remain in place.

## Players and rules

Bracket Control displays a compact [website legal acknowledgement]({{ '/guides/legal-acknowledgement/' | relative_url }}). Discord Global Player Registration roles and channels are no longer required. Individual Player Acceptance is no longer required. Organisers communicate and enforce their own community and tournament rules.

Team registration, approvals, captain dashboards, drafting, substitutes, brackets, reporting, publishing and support continue normally.

## Illustrated references and downloads

These earlier illustrations remain available. Some show retired registration or acceptance screens; follow the current guidance above.

The [original Discord Server Setup PDF]({{ '/assets/guides/server-setup/Bracket_Control_Discord_Server_Setup_Guide.pdf' | relative_url }}) is still available. Its screenshots may show an earlier setup screen. Use this page for current channel requirements and button instructions.
