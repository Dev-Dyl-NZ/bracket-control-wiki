---
layout: default
title: Discord Slash Commands
description: "Learn how to use Bracket Control Discord slash commands for tournament creation, team registration, score reporting, standings and server command synchronization."
permalink: /guides/discord-commands/
---
# Discord Slash Commands

This guide applies to the global commands introduced in application PR #167 once the production release is verified. Commands are available in connected Discord servers, subject to server permissions. They are not available in direct messages.

## Available commands

| Command | Purpose |
| --- | --- |
| `/tournament create` | Organisers and administrators open a short-lived authenticated tournament draft. |
| `/tournament list` | Browse tournaments you are allowed to view. |
| `/register` | Choose an open team tournament and register or manage a team. |
| `/score report` | Select your tournament, team and match, then open the secure reporting page. |
| `/score status` | See outstanding reports, confirmations and disputes. |
| `/bracket` | Open a visible tournament bracket. |
| `/standings` | Open visible tournament standings. |

## Organisers and captains

Tournament creation requires confirmation in the authenticated website editor. Choose a new or existing series and review the competition settings before creating the tournament.

Team registration uses the existing registration form, rules and privacy checks. Registrations remain subject to organiser approval. Score reporting uses the existing captain dashboard, evidence requirements and opponent confirmation. A command cannot automatically approve a team or finalize a score.

Responses are private. Sign in using the Discord account entitled to perform the action; a shared link does not grant access.

## Server administrators

Open [Bracket Control](https://app.devdylnz.com/app/) and select **Server Management → Discord Commands**. This page displays synchronization status, available commands, the last successful global synchronization and errors. Use **Sync Commands** to request reconciliation if needed.

Commands are registered globally. New connected servers do not need a separate command installation. Older copies are retired after the global definitions are verified. Discord controls client propagation and server-specific command permissions.

If commands are missing, verify the server connection, the installation scopes (`bot` and `applications.commands`) and Discord's server command permissions. Use Sync Commands if the status is not current. No Message Content privileged intent is required for slash commands.
