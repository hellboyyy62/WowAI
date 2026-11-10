# WowAI

WowAI is a free, independent Windows AI companion prototype for World of Warcraft: Forever (client 1.60.1). It provides a French-language chat overlay so players can ask questions without leaving the game.

## Current prototype

- Windows overlay built with C#/.NET 8, WPF and WebView2.
- A small Lua addon collects a character snapshot using available addon APIs: class, level, faction, location, equipment, inventory, quests, talents and professions.
- Character snapshots are imported through SavedVariables after a reload/logout, or through a manual clipboard export.
- Chat requests are sent to a configured AI provider through an OpenAI-compatible endpoint.
- Player-clicked suggestions can prepare TomTom waypoints. The current prototype can paste chat commands after an explicit click; it does not move the character or perform combat or farming.

## Planned ForeverDB integration

We are requesting developer access to ForeverDB to ground answers in identifiable game data rather than model recollection. This integration is not implemented or approved yet.

The intended workflow is to retrieve relevant records on demand, cache permitted results to reduce requests, retain source/build information, and distinguish observations in Forever from unconfirmed Classic reference data. If the available data supports it, verified coordinates would be used to generate player-requested TomTom waypoints.

Initial feasibility work focuses on class trainer locations and travel connections. Access to these records through ForeverDB's API still needs confirmation. Complete coverage and optimal route calculation are not claimed.

## Data attribution

**Planned data source: [ForeverDB.net](https://foreverdb.net/).** If access is approved, every view displaying ForeverDB-derived data will include a visible source link. ForeverDB data will not be presented as our own or resold.

## Project status

This repository is a public project overview for a personal prototype. The application source and releases are not published here. No game account data, character exports, conversations, API keys or local configuration are included.

WowAI is not affiliated with Blizzard Entertainment or ForeverDB. World of Warcraft belongs to Blizzard Entertainment.
