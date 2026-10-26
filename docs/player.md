---
id: admin-tools
name: Admin tools
summary: Tools for test servers. Administrators list players, mods and placed pieces, give items and reread settings from the Mods screen.
needs: server
settings:
  - key: enabled
    default: false
    meaning: Turns on the administrator actions and the command file. Keep it off on a server people play on.
    applies: at-once
---

- Administrators get actions on the mod's page of the Mods screen.
- They list the players online, the loaded mods and the last pieces placed.
- They give items to themselves or to another player, at most 10000 at a time.
- They make a mod read its settings again.
- A command file runs lines on the server without anyone joining.

## Who may use the actions?

Only administrators, and only after an administrator turns `enabled` on. Until
then the actions show as off.

## How does the command file work?

The file is `mod-data/admin-tools/commands.txt` beside the game. Add a line,
such as `admin-tools world`, and save. Within a second, the line runs as the
server's console. `<mod id> help` lists a mod's actions.

Each line runs once. The line and its answer go to
`logs/enshwick/mods/admin-tools.log`.

## Install

Admin tools comes in enshwick.zip, and the
[install guide](https://enshwick.github.io/docs/guides/install/) shows where to
put it. It runs on enshwick.

## Settings

You change this value in the game, as the
[settings guide](https://enshwick.github.io/docs/guides/change-mod-settings/)
shows.

## Multiplayer

Only the server needs Admin tools: the dedicated one, or the game you host.

## Problems

**A line in the command file does not run.** The line runs only after it ends
with a line break, and only while `enabled` is on. Lines already in the file
when the server starts never run.

**Something else goes wrong.** Open an issue in the
[mod's repository](https://github.com/enshwick/mod-admin-tools/issues). Attach
the files from the `logs/enshwick/` folder in your game folder.
