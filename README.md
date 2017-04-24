# Awesome npm scripts [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

[<img src="npm-logo.png" align="right" width="150">](https://www.npmjs.com/)

> Everything awesome related to npm scripts and using npm as a build tool.

You might also like [awesome-npm](https://github.com/sindresorhus/awesome-npm).

**Notice: I'm currently too busy to actively expand this list; therefore, I've decided to make this an [OPEN Open Source Project](http://openopensource.org). Individuals making significant and valuable contributions are given commit-access to the project to contribute as they see fit.**

## Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Articles](#articles)
- [Videos/Talks](#videostalks)
- [Task Runners](#task-runners)
- [File Watchers](#file-watchers)
- [Dev Servers](#dev-servers)
- [Cross-platform Utilities](#cross-platform-utilities)
  - [Utility Packs](#utility-packs)
- [Other Utilities](#other-utilities)
- [Miscellaneous](#miscellaneous)
- [Cross-platform Shell Reference](#cross-platform-shell-reference)
- [`npm run` Reference](#npm-run-reference)
- [Contributing](#contributing)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Articles

- [Why we should stop using Grunt & Gulp](https://www.keithcirkel.co.uk/why-we-should-stop-using-grunt/) - by Keith Cirkel.
- [How to Use npm as a Build Tool](https://www.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/) - A sequel to [Why we should stop using Grunt & Gulp](https://www.keithcirkel.co.uk/why-we-should-stop-using-grunt/).
- [Why I Left Gulp and Grunt for npm Scripts](https://medium.freecodecamp.com/why-i-left-gulp-and-grunt-for-npm-scripts-3d6853dd22b8) -  by Cory House.

## Videos/Talks

- [Advanced front-end automation with npm scripts](https://www.youtube.com/watch?v=0RYETb9YVrk) - by Kate Hudson
- [How to create a build system with npm scripts](http://www.penta-code.com/how-to-create-a-build-system-with-npm-scripts/) - Video tutorial series on setting up a front-end build system.

## Task Runners

Tools for running multiple commands or npm scripts in parallel or sequentially.

- [script-runner](https://github.com/paulpflug/script-runner) - Simple task runner with a terse syntax.
- [npm-run-all](https://github.com/mysticatea/npm-run-all) - Fully featured task runner.
- [redrun](https://github.com/coderaiser/redrun) - Expand scripts from package.json to improve execution speed.

## File Watchers

- [onchange](https://github.com/Qard/onchange) - `onchange <glob> -- <command>`.
- [watch](https://github.com/mikeal/watch) - `watch <command> <directory>`.

## Dev Servers

- [http-server](https://github.com/indexzero/http-server) - A simple zero-configuration command-line http server.
- [live-server](https://github.com/tapio/live-server) - Simple development http server with live reload capability.

## Cross-platform Utilities

- [rimraf](https://github.com/isaacs/rimraf) - Cross-platform `rm -rf`.
- [del-cli](https://github.com/sindresorhus/del-cli) - Safer file and folder deletion.
- [mkdirp](https://github.com/substack/node-mkdirp) - Cross-platform `mkdir -p`.
- [cpy-cli](https://github.com/sindresorhus/cpy-cli) - Cross-platform file/directory copying/renaming.
- [copyfiles](https://github.com/calvinmetcalf/copyfiles) - Cross-platform file copying.
- [sync-files](https://github.com/byteclubfr/node-sync-files) - Cross-platform `rsync`-like directory syncing with watch mode.
- [echo-cli](https://github.com/iamakulov/echo-cli) - Cross-platform `echo` with JS escape sequence support.
- [clear-cli](https://github.com/sindresorhus/clear-cli) - Clear the terminal cross-platform.
- [cross-env](https://github.com/kentcdodds/cross-env) - Set environment variables for scripts, unix-style.
- [cross-os](https://github.com/milewski/cross-os) - Run platform-specific npm scripts.
- [ntee](https://github.com/stefanmaric/ntee) - Cross-platform Unix `tee`; read from standard input and write to standard output and files.
- [catw](https://github.com/substack/catw) - Cross-platform `cat`, with optional watch mode.

### Utility Packs

- [shx](https://github.com/shelljs/shx) - Supports `pwd`, `ls`, `rm`, `echo`, `touch`, `cp`, and `mkdir`.

## Other Utilities

- [hashmark](https://github.com/keithamus/hashmark) -  Take contents of a file and output as new file with a hash in the name.
- [gzip-size-cli](https://github.com/sindresorhus/gzip-size-cli) - Get the gzipped size of a file or stdin.
- [opn-cli](https://github.com/sindresorhus/opn-cli) - Open websites, files, executables, etc. with the user's preferred application.
- [headr](https://github.com/heldr/headr) - Add header / banner info to a file.
- [Bower files CLI](https://github.com/thompsonemerson/bower-files-cli) - Getting all main bower files using CLI

## Miscellaneous

- [screwy](https://github.com/samueleaton/screwy) - The npm scripts GUI.
- [Forrest](https://github.com/stefanjudis/forrest) - An npm scripts desktop client.
- [run-npm](https://github.com/timoxley/npm-run) - Run locally-installed node module executables. Useful for debugging npm scripts.
- [npm-quick-run](https://github.com/bahmutov/npm-quick-run) - Quickly run npm scripts by prefix without typing the full name.
- [edit-script](https://github.com/RyanZim/edit-script) - Edit npm scripts from the command line without worrying about JSON escaping.

## Cross-platform Shell Reference

A quick reference of the shell operators & commands that work the same on Unix and Windows.

- `&&` runs commands in sequence. If a command fails, the script exits.
- `|` pipes the stdout of one command into the stdin of the next. (`do-something | something else`)
- `>` writes the stdout of a command to a file. (`do-something > file`)
- `<` sends the contents of a file to a command's stdin. (`command < file`)
- `cd <dir>` changes the current working directory to `<dir>`. Note that `cd` alone prints the current working directory on windows, but changes the working directory to `~` on \*nix.

## `npm run` Reference

You can use `npm run-script` or `npm run`; they both do the same thing, but `npm run` is shorter.

- Run just `npm run` to print a list of scripts.
- Running `npm run script` (where `script` is the name of your script) will run `prescript`, `script`, and `postscript`; in that order.
  - You can't nest `pre` and `post` hooks (i.e. `preprescript` won't work).
- You can pass arguments to your scripts by passing `--` to `npm run`, followed by the arguments. Example: Given the script `"mocha": "mocha"`, you can run `npm run mocha -- --reporter xunit`. This effectively runs `mocha --reporter xunit`.
- Running `npm test` is the same as running `npm run test`. The same applies to `npm start` and `npm stop`.
- You can run `npm run <script> -s` to silence the default npm output (useful for calling a script within another script).

## Contributing

See [CONTRIBUTING.md](https://github.com/RyanZim/awesome-npm-scripts/blob/master/CONTRIBUTING.md).

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
