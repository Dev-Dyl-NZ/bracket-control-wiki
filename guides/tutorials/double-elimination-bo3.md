---
layout: default
title: Double Elimination BO3 tutorial
description: "Create a Double Elimination tournament in Bracket Control with BO3 winners and finals, BO1 losers, captain score reporting, and a Grand Final bracket reset."
permalink: /guides/tutorials/double-elimination-bo3/
---
# Bracket Control | Double Elimination BO3 and Captain Score Reporting

<video controls playsinline preload="none" poster="{{ '/assets/tutorials/double-elimination-bo3/images/01-tournament-settings.png' | relative_url }}" aria-label="Bracket Control tutorial video" style="display:block;width:100%;max-width:960px;height:auto;aspect-ratio:16/9;">
  <source src="{{ '/assets/tutorials/double-elimination-bo3/double-elimination-bo3.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support HTML5 video. Use the MP4 link below.
</video>

[Watch or download the MP4]({{ '/assets/tutorials/double-elimination-bo3/double-elimination-bo3.mp4' | relative_url }})

> **About the recording:** The walkthrough uses fictional or sample data and simulated Discord connections. Follow the steps on your own connected server, then verify the outcome in the live application and Discord.

Captains can skip setup and use the short [Captain score reporting tutorial]({{ '/guides/tutorials/captain-score-reporting/' | relative_url }}). For broader configuration options, see [Tournament creation]({{ '/guides/tournament-creation/' | relative_url }}) and [Match results]({{ '/guides/match-results/' | relative_url }}).


[Open printable illustrated tutorial (PDF)]({{ '/assets/tutorials/double-elimination-bo3/wiki-instructions.pdf' | relative_url }})

Use this walkthrough to set up a four-team Double Elimination tournament, run BO3 in the winners bracket and grand final, with BO1 in the losers bracket, and verify that confirmed results advance the correct teams. Start at **Your tournaments** with the intended Discord server selected. The organizer needs tournament management access. Each captain needs the Discord account linked to the assigned team.

## 1. Create the tournament

1. Select **+ Create tournament**. Leave **Tournament type** on **Standard Team**, enter a **Tournament name**, and choose **Double Elimination** in **Bracket format**. The demo uses four under **Maximum approved teams**, clears **Repeat this tournament weekly**, and sets **Tournament start (Pacific/Auckland)**. Use the date and timezone for your event.
2. Under **Grand Finals**, select **1–2 matches (bracket reset)**. Leave **Split Participants — start half in the losers bracket** clear so every team starts in the winners bracket.
3. Open **Advanced match settings (optional)**. Set **Winners bracket format** to **Best of 3**, keep **Losers bracket format** at **Best of 1**, and set **Grand Final format** to **Best of 3**. The observed defaults are Best of 3, Best of 1, and Best of 1 respectively. The settings apply to each bracket section, and this form has no individual-round selector. **Grand Final format** also applies to the **RESET FINAL**.
4. Check **I confirm the tournament configuration** and select **Create tournament**. The success message includes **Open tournament dashboard**.
5. When all four starting rosters are approved, open **Overview** and expand **Ready to start? Bracket controls**. Select **LOCK ROSTERS & GENERATE BRACKET**, accept the prompt, and select **View bracket**. The demo begins with four ready teams.

![Callout 1 highlights the BO3, BO1, and BO3 selections under Advanced match settings.]({{ '/assets/tutorials/double-elimination-bo3/images/01-tournament-settings.png' | relative_url }})

## 2. How captains report scores

1. Sign in with the Discord account linked to your team. Under **Captain Dashboard**, choose **Score Reporting**. Under **Active matches**, find your opponent and check the tournament and round.
2. If your team won the current game, attach its evidence using **One scoresheet (required)** and select **Report Win**. The field accepts PNG, JPEG, WebP, or PDF up to 10 MB. Follow **Report game 1**, **Report game 2**, and **Report game 3** as they appear. The form takes one scoresheet per win. The app derives the series score from confirmed game winners.
3. Check for **Game 1 · reported** and **Waiting for the opposing captain to confirm or dispute your report.** The series score stays unchanged until the game is confirmed.
4. In the opposing captain’s session, open **View Game 1 Scoresheet**. Select **Confirm Result** if it is correct. If the result is wrong, enter a **Dispute reason** and select **Dispute Result**. A dispute pauses the series for administrator resolution. Routine confirmation needs only the opposing captain.
5. Repeat for every game played, with the winner’s captain reporting each one. Harbor Falcons win Games 1 and 3 and Copper Owls win Game 2. After each confirmation the series reads **1–0**, **1–1**, and finally **2–1** in match order. In the BO3 sweep, Summit Foxes report Games 1 and 2 against Tidal Rays. The second confirmation closes the series at **2–0**, with no Game 3. In a BO1 match, the first confirmed game closes the series **1–0** for the winner.
6. Under **Match History**, look for **Match complete · Winner: [team] · Bracket updated**. The winning team reaches two confirmed game wins in BO3.

![Callout 2 marks Report Win with one demo scoresheet attached.]({{ '/assets/tutorials/double-elimination-bo3/images/02-captain-submission.png' | relative_url }})

![Callout 3 marks the report awaiting confirmation, with the score still at 0–0.]({{ '/assets/tutorials/double-elimination-bo3/images/03-report-pending.png' | relative_url }})

## 3. Follow the bracket and verify advancement

Open **Bracket** and use the confirmed score plus the next match cards to track both teams.

| Confirmed result | Next position |
| --- | --- |
| Harbor Falcons 2–1 Copper Owls in **W1 · MATCH 01** | Falcons advance to **W2 · MATCH 01**. Owls drop to **L1 · MATCH 01**. |
| Copper Owls 0–1 Tidal Rays in **L1 · MATCH 01** | Rays advance to **L2 · MATCH 01**. The Owls have two series losses and are eliminated. |
| Harbor Falcons 0–2 Tidal Rays in **GRAND FINAL** | Both teams now have one series loss. The same teams appear in **RESET FINAL**. |
| Harbor Falcons 2–0 Tidal Rays in **RESET FINAL** | Falcons win the tournament. |

Dropping a game in BO3 changes the series score. Losing the series adds one match loss. With the bracket-reset setting, the undefeated side can win the tournament in the first final. The lower-bracket side must win that final to force a reset.

![Callout 4 marks the updated bracket. Falcons appear in W2 and Owls in L1 after the 2–1 result.]({{ '/assets/tutorials/double-elimination-bo3/images/04-bracket-advancement.png' | relative_url }})

![Callout 5 marks the Reset Final with both finalists populated after Tidal Rays win the first final.]({{ '/assets/tutorials/double-elimination-bo3/images/05-reset-final.png' | relative_url }})

## Demo verification

The current app ran against disposable PostgreSQL with fictional teams, synthetic scoresheets, and separate organizer and captain browser sessions. Discord authentication and membership were simulated. The rehearsal and recorded run verified tournament creation, mixed BO3/BO1 settings, report submission, opponent confirmation, a 2–1 result, a 2–0 winners-bracket sweep, a 1–0 losers-bracket result, advancement, elimination, and the reset path. Live Discord sign-in and notifications, administrator dispute resolution, and a first-final win by the undefeated team were outside the recorded demo.

This is a demonstrated mixed-format example: **BO3** for the winners bracket and grand final, **BO1** for the losers bracket. It does not mean every Double Elimination tournament automatically uses those settings.
