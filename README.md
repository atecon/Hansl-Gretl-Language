# Hansl-gretl-Language
Sublime support for gretl's scripting language called *Hansl*. The package's features are:

* Syntax-highlighting

* Completions

* Snippets

* gretl build-systems (Batch mode, CLI, REPL)

gretl is an open-source statistics and econometrics software: http://gretl.sourceforge.net/

Hansl is a recursive acronym: it stands for "Hansl’s A Neat Scripting Language". For a primer on Hansl:
https://sourceforge.net/projects/gretl/files/manual/hansl-primer-a4.pdf/download


## I - Installation
This plug-in is available on [package control](https://packagecontrol.io/packages/Hansl-gretl-Language). It's recommended to get it from there.

Steps for installation:

1) Call "Package Control" via the key-bind
	- Win/Linux: ```ctrl+shift+p```
	- Mac: ```cmd+shift+p```

2) Type "Package Control: Install Package" and search for "Hansl-gretl-Language".

**Note:** If you don't see this plug-in in package control is likely because you have a too old version of Sublime installed. The plug-in will only be visible with a build >= 3084.


### Syntax-highlighting
Build 3084 of Sublime introduced a new format for syntax definition files.
The documentation can be found [here](http://www.sublimetext.com/docs/3/syntax.html). This package makes use of this new syntax.

Once the package is installed, every file with an ```*.inp``` file type will automatically be recognized as a gretl file using the Hansl syntax. You should experience syntax-highlighting immediately. Otherwise, go through the menu: `View > Syntax > Hansl`.

The new syntax will improve the way your gretl/Hansl code is coloured:
![alt text][sample]

![Auto-indentation](<figures/hansl_screenshot.png>)

**Note:** There are still some edgy cases left for improvement.


### Completions
This feature is automatically activated for every ```*.inp``` file. Start typing a gretl command, function name or name of an accessors and you will see  suggestions which can be accepted via the Tab key or Enter.


### Completion of accessors
The package treats gretl's built-in accessors as 'variables' (scope). Since Sublime 4, one can add annotations to variables.

Here an example:
![Completion of an accessor](<figures/completion_accessor.gif>)

### Completion of commands
The package treats gretl's built-in commands as 'namespace' (scope). Since Sublime 4, one can add annotations to commands, too.

Here an example:
![Completion of an accessor](<figures/completion_command.gif>)

This is how it works for command blocks:
![Completion of an accessor](<figures/completion_command_block.gif>)

### Completion of data types
Gretl data types are treated as 'type' (scope). Since Sublime 4, one can add annotations here, too.

Here an example:
![Completion of an accessor](<figures/completion_dtype.gif>)

### Completion of keywords
Gretl data types are treated as 'keyword' (scope). Since Sublime 4, one can add annotations here, too.

Here an example:
![Completion of an accessor](<figures/completion_keyword.gif>)


### Indentation
Since version 0.3.0 auto-indentation is supported for gretl scripts.

Here an example of an if-else block.

![Auto-indentation](<figures/indent_ifelse.gif>)

However, indentation of nested blocks are not fully supported, yet.


### Snippets
Snippets make you really productive! These are little templates which save typing. Simply open a gretl ```*.inp``` file, and start typing ```if```. You will see some suggestions which can be selected via the Tab key again. Explore and start writing your own snippets.

This is how snippets work:

![Snippet for creating a function block](<figures/snippet_function.gif>)


For an overview of available snippets you can do the either:
1. `Ctrl+Shift+P -> Snippet` will list the available snippets.
2. See [here](https://github.com/atecon/Hansl-Gretl-Language/tree/master/Snippets) for all defined snippets (which you can use for your own templates).


Watch for a tutorial on snippets here: https://youtu.be/MeOaWR2T6TU


### gretl build-systems
Support for build-systems is a great feature of the Sublime editor. They allow you to execute a program. I've added different build-system for gretl such that you can run your gretl script via the "gretlcli" program --- gretl's command line program *instead* of the GUI.

Three build-systems are configured (see ./build-systems/gretl.sublime-build):

1) "CLI": Execute a gretl script in a terminal -- non-interactive.

2) "Batch mode": Execute a gretl script and quit.

3) "REPL": Interactive mode opening a command line interface.

The REPL requires the additional installation of the *Terminus* package for sublime. For a video tutorial on *Terminus* see here: https://youtu.be/mV0ghkMwTQc

For a great video tutorial on how to make a build-system interactive with *Terminus* I also recommend: https://youtu.be/etIJMVIvVgg


## Changelog:
v0.3.0 (June 2021):
    - Finish completions for all gretl commands
    - Add support for auto-indentation
v0.2.5 (June 2021):
    - Add further completions for commands
v0.2.4 (June 2021):
    - Add further completions for commands
v0.2.3 (June 2021):
    - Add much better support for completions for commands including type annotations, annotations and pre-configured options
v0.2.2 (June 2021):
    - Add new snippets defining a bundle
    - Minor improvements
v0.2.1 (May 2021):
    - Added new snippets for loops
    - Improve existing snippets (all backward compatible)
v0.2.0 (November 2020):
    - Added new additional snippets
v0.1.0 (May 2020):
    - Initial release
