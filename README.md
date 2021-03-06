SublimeLinter-contrib-pug-lint
================================

[![Build Status](https://travis-ci.org/benedfit/SublimeLinter-contrib-pug-lint.svg?branch=master)](https://travis-ci.org/benedfit/SublimeLinter-contrib-pug-lint)

This linter plugin for [SublimeLinter][docs] provides an interface to [pug-lint](https://github.com/pugjs/pug-lint). It will be used with files that have the “pug” syntax.

## Installation
SublimeLinter 3 must be installed in order to use this plugin. If SublimeLinter 3 is not installed, please follow the instructions [here][installation].

### Linter installation
Before using this plugin, you must ensure that `pug-lint` is installed on your system. To install `pug-lint`, do the following:

1. Install [Node.js](http://nodejs.org) (and [npm](https://github.com/joyent/node/wiki/Installing-Node.js-via-package-manager) on Linux).

1. Install `pug-lint` by typing the following in a terminal:
   ```
   npm install -g pug-lint
   ```

**Note:** This plugin requires `pug-lint` 2.1.1 or later.

### Linter configuration
In order for `pug-lint` to be executed by SublimeLinter, you must ensure that its path is available to SublimeLinter. Before going any further, please read and follow the steps in [“Finding a linter executable”](http://sublimelinter.readthedocs.org/en/latest/troubleshooting.html#finding-a-linter-executable) through “Validating your PATH” in the documentation.

Once you have installed and configured `pug-lint`, you can proceed to install the SublimeLinter-contrib-pug-lint plugin if it is not yet installed.

### Plugin installation
Please use [Package Control][pc] to install the linter plugin. This will ensure that the plugin will be updated when new versions are available. If you want to install from source so you can modify the source code, you probably know what you are doing so we won’t cover that here.

To install via Package Control, do the following:

1. Within Sublime Text, bring up the [Command Palette][cmd] and type `install`. Among the commands you should see `Package Control: Install Package`. If that command is not highlighted, use the keyboard or mouse to select it. There will be a pause of a few seconds while Package Control fetches the list of available plugins.

1. When the plugin list appears, type `pug-lint`. Among the entries you should see `SublimeLinter-contrib-pug-lint`. If that entry is not highlighted, use the keyboard or mouse to select it.

## Settings
For general information on how SublimeLinter works with settings, please see [Settings][settings]. For information on generic linter settings, please see [Linter Settings][linter-settings].

You can configure pug-lint options in the way you would from the command line, with `.pug-lintrc` files. For more information, see the [pug-lint docs](https://github.com/pugjs/pug-lint#configuration-file). The linter plugin does this by searching for a `.pug-lintrc` file in your stylus file’s current directory tree. If you are an OSX / Linux user, you can also set a global `.pug-lintrc` in your User (`~`) directory.

You may provide a custom config file by setting the linter’s `"args"` setting to `["--config", "/path/to/file"]`. On Windows, be sure to double the backslashes in the path, for example `["--config", "C:\\Users\\Name\\pug-lint.conf"]`.

The path to the `.pug-lintrc` file is cached, meaning if you create a new .pug-lintrc that should have precedence over the previous one (meaning it is closer to the .pug file) you need to clear the cache for the linter to use the new `.pug-lintrc` You can clear the cache by going to: Tools > SublimeLinter > Clear Caches.

## Contributing
If you would like to contribute enhancements or fixes, please do the following:

1. Fork the plugin repository.
1. Hack on a separate topic branch created from the latest `master`.
1. Commit and push the topic branch.
1. Make a pull request.
1. Be patient.  ;-)

Please note that modifications should follow these coding guidelines:

- Indent is 4 spaces.
- Code should pass flake8 and pep257 linters.
- Vertical whitespace helps readability, don’t be afraid to use it.
- Please use descriptive variable names, no abbreviations unless they are very well known.

Thank you for helping out!

[docs]: http://sublimelinter.readthedocs.org
[installation]: http://sublimelinter.readthedocs.org/en/latest/installation.html
[locating-executables]: http://sublimelinter.readthedocs.org/en/latest/usage.html#how-linter-executables-are-located
[pc]: https://sublime.wbond.net/installation
[cmd]: http://docs.sublimetext.info/en/sublime-text-3/extensibility/command_palette.html
[settings]: http://sublimelinter.readthedocs.org/en/latest/settings.html
[linter-settings]: http://sublimelinter.readthedocs.org/en/latest/linter_settings.html
[inline-settings]: http://sublimelinter.readthedocs.org/en/latest/settings.html#inline-settings
