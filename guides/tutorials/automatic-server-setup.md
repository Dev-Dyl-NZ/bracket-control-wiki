---
layout: default
title: Automatic Server Setup tutorial
description: "Follow the Automatic Server Setup tutorial in Bracket Control to configure optional Discord channels, review the proposed layout, and verify saved settings."
permalink: /guides/tutorials/automatic-server-setup/
---
# Bracket Control | Automatic Server Setup Wizard

<video controls playsinline preload="none" poster="{{ '/assets/tutorials/automatic-server-setup/images/01-open-wizard.png' | relative_url }}" aria-label="Bracket Control tutorial video" style="display:block;width:100%;max-width:960px;height:auto;aspect-ratio:16/9;">
  <source src="{{ '/assets/tutorials/automatic-server-setup/automatic-server-setup.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support HTML5 video. Use the MP4 link below.
</video>

[Watch or download the MP4]({{ '/assets/tutorials/automatic-server-setup/automatic-server-setup.mp4' | relative_url }})

> **About the recording:** The walkthrough uses fictional or sample data and simulated Discord connections. Follow the steps on your own connected server, then verify the outcome in the live application and Discord.

For a full reference on optional channels, permissions and reconnecting a bot, see [Discord Server Setup]({{ '/guides/server-setup/' | relative_url }}).

Use Automatic Setup to configure the optional Discord channels and messages your tournament community needs. The wizard runs on a Discord server you already manage..

**Before you start.** Sign in to Bracket Control with Discord. You need Administrator or Manage Server access, a connected Bracket Control bot with access to the resources you plan to use, and the setup wizard enabled. Creating channels requires the bot's **Manage Channels** and **View Audit Log** permissions. If the server is unconnected, open **Your Discord servers**, select **Connect server**, and use **Invite bot**. If the bot is already installed, use **Connect installed bot**.

## 1. Open the wizard

Open **Your Discord servers** and select **Complete server setup** on the connected server you want to configure. To reopen the wizard later, use **Server settings** → **Open Server Setup**. The wizard starts at **Welcome to Bracket Control!**

![Complete server setup on the connected demo server]({{ '/assets/tutorials/automatic-server-setup/images/01-open-wizard.png' | relative_url }})

## 2. Choose Automatic Setup

Select **Automatic Setup** to create or reuse selected Discord resources after reviewing them. Choose **Manual Setup** if you want to select channels and categories you have already created. The example opens **Automatic Setup — Discord Channels**.

![Automatic Setup and Manual Setup with Automatic Setup highlighted]({{ '/assets/tutorials/automatic-server-setup/images/02-choose-automatic.png' | relative_url }})

## 3. Choose channels and categories

Open **Bracket Updates** and select **Create bracket-updates**. Keep the **Proposed name: Bracket Updates** and the recommended category in **Category for Bracket Updates**. Select an existing resource by name to reuse it. A reused channel defaults to **Keep Current Location**. You can also choose **No Category** for a channel.

Leave other channels set to **Not Required** and **Enable Support Tickets** clear for this example. Every channel is optional, including the draft waiting room. Under **Proposed layout**, check that `#bracket-updates` appears under the **BRACKET CONTROL** category, then select **Continue**.

![Create bracket-updates in the Bracket Updates list]({{ '/assets/tutorials/automatic-server-setup/images/03-choose-channel.png' | relative_url }})

![Proposed layout showing the category and bracket-updates channel]({{ '/assets/tutorials/automatic-server-setup/images/04-proposed-layout.png' | relative_url }})

## 4. Decide whether to publish a message

On **Optional messages**, **Publish or update the Team Registration and Management message** requires a team-registration destination. **Allow replacement of a tracked message confirmed deleted by Discord** applies to a previously tracked message. Leave both unchecked for this example and select **Continue**.

![Optional messages with both choices clear]({{ '/assets/tutorials/automatic-server-setup/images/05-optional-messages.png' | relative_url }})

## 5. Review Support Ticket Configuration

Leave **Enable Support Tickets** clear in this example. If you enable tickets, choose a public panel channel, a private ticket category and a support staff role. Review whether the wizard should publish the support panel. Select **Review Configuration** to open **Review & Confirm**.

![Support Ticket Configuration with tickets disabled and Review Configuration available]({{ '/assets/tutorials/automatic-server-setup/images/06-support-tickets.png' | relative_url }})

## 6. Review and apply

Check the **Create**, **Reuse** and **Not Required** entries that appear in your plan. Check channel locations and any messages selected for publication. A proposed move for an existing channel requires its own approval. In the example, the plan creates a category and one channel and leaves message publication off.

Select **I approve these exact assignments, resource actions and selected message publications**, then select **Apply Configuration**.

![Review and confirm with the approval checkbox highlighted]({{ '/assets/tutorials/automatic-server-setup/images/07-review-and-approve.png' | relative_url }})

## 7. Confirm completion

Look for **Discord Server Setup Complete** and **Bot connected**. Select **Manage Discord Settings** and confirm that **Discord Settings (Global)** shows `#bracket-updates` under **Bracket Updates**. Select **Tournament dashboard** and check that **Your tournaments** opens for the same server. **Go to Dashboard** on the confirmation screen takes you straight to the dashboard.

After a live setup, also confirm in Discord that the expected channel is in the intended category and visible to the intended members.

![Setup complete with Manage Discord Settings highlighted]({{ '/assets/tutorials/automatic-server-setup/images/08-setup-complete.png' | relative_url }})

![Saved bracket-updates destination in Discord Settings]({{ '/assets/tutorials/automatic-server-setup/images/09-verify-saved-channel.png' | relative_url }})

![Your tournaments dashboard for the same sample server]({{ '/assets/tutorials/automatic-server-setup/images/10-dashboard-ready.png' | relative_url }})

The demo used the current frontend with a local synthetic API. It verified the wizard screens, approval gate, completion response, saved destination readback and dashboard handoff. Live Discord sign-in, bot installation, permissions, channel creation and message delivery require a separate live test.

For other walkthroughs, open the [video tutorials library]({{ '/guides/tutorials/' | relative_url }}).
