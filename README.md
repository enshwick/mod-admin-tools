# Admin tools

This mod is retired. The Enshwick loader does its work itself: on a
dedicated server, lines typed into the server's console window or added to
`mod-data/enshwick/commands.txt` run on the server's console. `enshwick help`
lists the tools, among them `world`, `entity`, `placed`, `mods`, `reload`,
`kick`, `ban` and `unban`. The
[console chapter](https://github.com/enshwick/enshwick/blob/main/book/src/chat.md#the-command-file)
describes them.

The loader never loads this mod and names its file in the log as replaced,
so it can be deleted from the `mods` folder. A command file left in
`mod-data/enshwick.admin-tools/` is still read.
