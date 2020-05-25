# Hansl-Gretl-Language

Sublime support for Gretl's scripting language called *Hansl*.

Package's features are:
* Syntax-highlighting
* Auto-completion
* Snippets
* Gretl build-systems (Batch mode, CLI, REPL)

Gretl is an open-source statistics and econometrics software: http://gretl.sourceforge.net/

Hansl is a recursive acronym: it stands for "Hansl’s A Neat Scripting Language". For a primer on Hansl:
https://sourceforge.net/projects/gretl/files/manual/hansl-primer-a4.pdf/download


## I - Installation

This plug-in is available on [package control](https://packagecontrol.io/packages/Hansl-Gretl-Language). It's recommended to get it from there.

Call "Package Control" via the key-bind
- Win/Linux: ```ctrl+shift+p```
- Mac: ```cmd+shift+p```
, type "Package Control: Install Package" and search for "Hansl-Gretl-Language".

**Note:** If you don't see this plug-in in package control is likely because you have a too old version. The plug-in will only be visible with a build >= 3084.


### Syntax-highlighting

Build 3084 of Sublime introduced a new format for syntax definition files.
The documentation can be found [here](http://www.sublimetext.com/docs/3/syntax.html). This package makes use of this new syntax.

Once the package is installed, every file with an ```*.inp``` file type will automatically be recognized as a Gretl file using the Hansl syntax. You should experience syntax-highlighting immediately. Otherwise, go through the menu: `View > Syntax > Hansl`.

The new syntax will improve the way your Gretl/ Hansl code is coloured:
![alt text][sample]

[sample]: https://raw.githubusercontent.com/atecon/Hansl-Gretl-Language/master/hansl_screenshot.png "Screen-shot of Hansl syntax"

**Note:** There are still some edgy cases left for improvement.


### Auto-completion

This feature is automatically activated for every ```*.inp``` file. Start typing a gretl command, function name or name of an accessors and you will see some suggestions which can be accepted via the Tab key.


### Snippets

Snippets make you really productive! These are little templates which save typing. Simply open a gretl ```*.inp``` file, and start typing ```if```. You will see some suggestions which can be selected via the Tab key again. Explore and start writing your own snippets.

Watch for a tutorial on snippets here: https://youtu.be/MeOaWR2T6TU

### Gretl build-systems

Support for build-systems is a great feature of the Sublime editor. They allow you to execute a program. I've added different build-system for Gretl such that you can run your Gretl script via the "gretlcli" program --- Gretl's command line program *instead* of the GUI.

Three build-systems are configured (see ./build-systems/Gretl.sublime-build):
1) CLI: Execute a Gretl script in a terminal -- non-interactive.
2) Batch mode: Execute a Gretl script and quit.
3) REPL: Interactive mode opening a command line interface.

The REPL requires the additional installation of the *Terminus* package for sublime. For a video tutorial on *Terminus* see here: https://youtu.be/mV0ghkMwTQc

For a great video tutorial on how to make a build-system interactive with *Terminus* I also recommend: https://youtu.be/etIJMVIvVgg


## Changelog:
 May 2020:
 - Initial release
