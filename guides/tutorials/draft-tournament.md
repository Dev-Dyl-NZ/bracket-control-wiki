---
layout: default
title: Snake Draft tournament tutorial
description: "Create a Snake Draft tournament in Bracket Control, import players, confirm captains, make live picks, and verify automatically approved five-player rosters."
permalink: /guides/tutorials/draft-tournament/
---
# Create a Draft Tournament, Select Captains, and Draft Players

<video controls playsinline preload="none" poster="{{ '/assets/tutorials/draft-tournament/images/01-confirm-captains.png' | relative_url }}" aria-label="Bracket Control tutorial video" style="display:block;width:100%;max-width:960px;height:auto;aspect-ratio:16/9;">
  <source src="{{ '/assets/tutorials/draft-tournament/draft-tournament.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support HTML5 video. Use the MP4 link below.
</video>

[Watch or download the MP4]({{ '/assets/tutorials/draft-tournament/draft-tournament.mp4' | relative_url }})

> **About the recording:** The walkthrough uses fictional or sample data and simulated Discord connections. Follow the steps on your own connected server, then verify the outcome in the live application and Discord.

For additional draft styles, voice rooms, reserves and substitute workflows, see [Draft tournaments]({{ '/guides/drafts/' | relative_url }}).


[Open printable illustrated tutorial (PDF)]({{ '/assets/tutorials/draft-tournament/draft-tournament-sop.pdf' | relative_url }})

Use this guide to run a two-team Snake Draft in Bracket Control.

Start from **Your tournaments** with the intended Discord server selected. The organizer needs permission to manage tournaments on that server. Each captain signs in with their own Discord account. This demo uses Amber Vale and Brook Lane as captains and eight fictional player tags.

## 1. Organizer — Create the tournament

1. Select **+ Create tournament**. Under **Tournament type**, choose **Draft** and enter a **Tournament name**.
2. Set **Maximum approved teams** to **2** for this demo. Under **Draft Style**, choose **Snake Draft** to reverse the order each round. **Standard (1-for-1)** repeats the same order each round. Both styles give each captain one pick per turn. **Bracket format** sets how the teams compete after the draft. The demo keeps **Double Elimination**.
3. Clear **Repeat this tournament weekly** for a one-off event and enter **Tournament Start Time** in the selected **Tournament timezone**. **Draft Call Opens** and **Draft Call Locks** control when players can join the configured Discord draft voice channel. This demo uses the website import path.
4. Check **I confirm the tournament configuration** and select **Create tournament**. Find your new event under **Upcoming tournaments** and open **Manage Tournament**.

## 2. Organizer — Prepare the player pool

1. Open **Live Draft**. In **Live draft player pool**, enter one eligible player's tag per line under **Player tags**. The demo uses Aster, Birch, Cinder, Drift, Ember, Flint, Gale and Harbor.
2. Select **IMPORT PLAYERS**. Check that the pool shows eight **AVAILABLE FREE AGENTS**. At least two captain teams and four available starter picks per captain are required to start. An optional Discord waiting room can also supply available players.

## 3. Organizer — Select and confirm captains

1. Open **Captain Selection**. If a captain is missing from **Draft Captain Registry**, select **Add New Captain**. Use **Search Discord server members** and **Search Discord**, then select the matching result and choose **Save Captain**. As an alternative identity lookup, enter the **Captain Discord user ID**. The registry can be reused across tournaments.
2. Check the captains for this event. **Select active captains** is the bulk shortcut when you want every active registry entry and they fit the tournament capacity. Choose **Confirm Selected Captains** before starting the draft.
3. Check for **2 captains currently confirmed · 2/2 selected**. Open **Teams & players** to see the confirmed captain teams. Captain selection locks once drafting starts.

![Organizer screenshot. A yellow callout identifies Confirm Selected Captains after both captain checkboxes are selected.]({{ '/assets/tutorials/draft-tournament/images/01-confirm-captains.png' | relative_url }})

## 4. Organizer and captains — Start and make picks

1. **Organizer.** In **Live Draft**, select **START CAPTAIN DRAFT**. Read **Selection order (current turn first)** and the line showing which team **is picking now**.
2. **Captain A.** Open your **Captain Dashboard** in your signed-in session. When **Your turn to pick** appears, locate the player under **Available players** and select their `+` button. Amber selects **Aster +**. Aster appears under **Your team** and leaves the shared pool.
3. **Captain B.** While Amber picks, Brook sees **Waiting for Team Amber** and disabled player buttons. After Amber's pick, Brook sees **Your turn to pick** and **Available players (7)**. Brook selects **Birch +** to end round 1 and still has the first pick of round 2, so Brook selects **Cinder +** next. Amber follows to finish round 2.

![Captain A screenshot. A yellow callout identifies Aster + under Available players while the dashboard says Your turn to pick.]({{ '/assets/tutorials/draft-tournament/images/02-captain-pick.png' | relative_url }})

## 5. Organizer and captains — Check the result

1. **Captains.** Keep following the turn indicator until each team has its captain and four drafted starters. Up to two substitute rounds are available when there are surplus players. This pool has exactly enough starters, so optional picks are skipped.
2. **Captains.** Confirm that the dashboard says **Captain draft completed** and verify the five players under **Your roster**. A valid roster shows **Automatically approved**.
3. **Organizer.** Open **Teams & players** and check both rosters under **Captain registration & draft rosters**. Each should show five starters and **Automatically approved**. When ready to begin competition, the next organizer control is **LOCK ROSTERS & GENERATE BRACKET** under **Overview** → **Ready to start? Bracket controls**.

![Organizer screenshot. A yellow callout outlines the completed roster section with Team Amber and Team Brook marked Automatically approved.]({{ '/assets/tutorials/draft-tournament/images/03-completed-rosters.png' | relative_url }})

The workshop uses the running Bracket Control app and a disposable database. Demo sessions and Discord membership lookups use fictional accounts and simulated Discord responses. Live Discord sign-in, voice automation, and bracket generation are outside the recorded workflow.

The demo stops at completed, automatically approved rosters; it does not record live Discord voice automation or actual bracket play. Next, see [Double Elimination and score reporting]({{ '/guides/tutorials/double-elimination-bo3/' | relative_url }}).
