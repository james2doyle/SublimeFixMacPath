MacShell
==============

> Originally forked from [tedmiston/SublimeFixMacPath](https://github.com/tedmiston/SublimeFixMacPath)

_This fork includes support for [fish shell](http://fishshell.com/)_

On OS X, Sublime Text has its `PATH` set by `launchctl`, not by your shell<sup>1</sup>. Commands like `make` run by Sublime Text are then unable to find non-system binaries, including those installed by homebrew and MacPorts.

MacShell is a simple plugin for Sublime Text 2 and 3 which sets Sublime Text's `PATH` to that reported by your shell. Now, if you add homebrew's `/usr/local/bin` directory to your `PATH` in `.bash_profile` (or whatever other way you set your shell's `PATH`) Sublime Text will inherit that `PATH`.

<sup>1: This isn't true if you launch Sublime Text from within your shell (e.g., with the `subl` command.)</sup>

Install
-------

MacShell is for Sublime Text 2 and 3 running on Mac OS X. (Other platforms don't suffer from the problem this plugin fixes, to my knowledge, so it isn't needed.)

The easiest way to get this is to use [Package Control](http://wbond.net/sublime_packages/package_control) and search for "MacShell".

To manually install MacShell, run

    git clone https://github.com/james2doyle/MacShell.git ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/MacShell

for Sublime Text 2, or

    git clone https://github.com/james2doyle/MacShell.git ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/MacShell

for Sublime Text 3.


Options
-----------

You can optionally set the following option to your user preferences:

* `"additional_path_items": []`

An array of strings of locations you wish to add to Sublime Text's PATH, in addition to those pulled from your shell.

For example, to add `~/Desktop` and `~/bin` to the shell's PATH in Sublime Text, you would use `"additional_path_items": ["~/Desktop", "~/bin"]`.
