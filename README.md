# Z Shelter

**English** · [简体中文](README.zh-CN.md)

**[Play on itch.io](https://alpacewhite.itch.io/z-shelter)** · [GitHub download](https://github.com/AmethystineAlpaca/z-shelter-public/releases/tag/v0.2.3-playtest.4) · [Feedback](https://github.com/AmethystineAlpaca/z-shelter-public/issues)

A single-player survival management game about preparing for a zombie outbreak, surviving at home, and living with your choices.

![The shelter and street at night](assets/night-walker-lights.gif)

Buy supplies on a limited budget before the outbreak. Afterward, manage food and water, repair doors and windows, scavenge nearby locations, and decide how to respond to people at your door. Some choices have consequences that unfold days later.

![Preparation shopping](assets/shop-en.png)

![Events and choices](assets/event-en.png)

## About this prototype

Preparation and survival are playable, with English and Chinese support. I've hit a design wall around the game's hook: what makes someone want to play another day? I'm sharing the current build to hear what feels worth developing further, where it loses your interest, and what makes you want to keep playing. Content and balance are still in progress, with no fixed update schedule.

## Play

1. Under Assets on the [download page](https://github.com/AmethystineAlpaca/z-shelter-public/releases/tag/v0.2.3-playtest.4), choose **ZShelter-macOS-v0.2.3-playtest.4.zip**. GitHub's automatic Source code archives contain only these page materials, not a playable game.
2. Extract the entire ZIP, read **START-HERE-English.txt**, and move **Z Shelter.app** to Applications or another folder before opening it. No Godot installation is needed.
3. This build is not Apple-notarized. If macOS cannot verify the app, follow the included instructions for **System Settings → Privacy & Security → Open Anyway**.
4. Choose **Begin a new journal** and try the optional tutorial. Click scene objects to interact, Esc to go back, and F11 for fullscreen.

Currently **macOS only**. The app includes Apple Silicon and Intel executables; launch verification was performed on Apple Silicon. Windows, Linux, and mobile builds are not currently available.

## Public configuration and event graph

This repository includes a snapshot of the prototype's events, items, shop, actions, world state, event delivery, and balance configuration for reading and discussion. The base package contains **40 events and 96 choices**. These files contain story spoilers.

- [Events](config/events_vr/registry.json): text, choices, prerequisites, and effects.
- [Items](config/registry/items.json) / [Shop](config/shop_catalog.json) / [Balance](config/balance.json).
- [Configuration guide and viewer setup](CONFIG.md).

My **[Event Graph Reviewer](https://github.com/AmethystineAlpaca/event-graph-reviewer)** can visualize the event/choice relationships locally, including AND/OR prerequisites and node details. It is a read-only viewer, not a game simulator or an item editor.

## Feedback

Please use [Issues](https://github.com/AmethystineAlpaca/z-shelter-public/issues) for ideas or bugs. For bugs, include the version, language, in-game day, and reproduction steps. Keep screenshots limited to the game.

This is the public distribution repository for descriptions, screenshots, configuration, downloads, and feedback. Game source remains private; this is not an open-source project. This prototype is free to play. Release and pricing plans for future versions are undecided. See [RIGHTS.md](RIGHTS.md).
