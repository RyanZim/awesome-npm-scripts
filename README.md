# Awesome npm scripts

> Everything awesome related to npm scripts and using npm as a build tool.

*You might also like [awesome-npm](https://github.com/sindresorhus/awesome-npm).*

## Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Articles](#articles)
- [Task Runners](#task-runners)
- [File Watchers](#file-watchers)
- [Cross-platform Utilities](#cross-platform-utilities)
  - [Utility Packs](#utility-packs)
- [Other Utilities](#other-utilities)
- [Cross-platform Shell Reference](#cross-platform-shell-reference)
- [`npm run` Reference](#npm-run-reference)
- [Contributing](#contributing)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Articles

- [Why we should stop using Grunt & Gulp](https://www.keithcirkel.co.uk/why-we-should-stop-using-grunt/) - by Keith Cirkel.
- [How to Use npm as a Build Tool](https://www.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/) - A sequel to [Why we should stop using Grunt & Gulp](https://www.keithcirkel.co.uk/why-we-should-stop-using-grunt/).
- [Why I Left Gulp and Grunt for npm Scripts](https://medium.freecodecamp.com/why-i-left-gulp-and-grunt-for-npm-scripts-3d6853dd22b8) -  by Cory House.

## Task Runners

Tools for running multiple commands or npm scripts in parallel or sequentially.

- [script-runner](https://github.com/paulpflug/script-runner) - Simple task runner with a terse syntax.
- [npm-run-all](https://github.com/mysticatea/npm-run-all) - Fully featured task runner.

## File Watchers

- [onchange](https://github.com/Qard/onchange) - `onchange <glob> -- <command>`.
- [watch](https://github.com/mikeal/watch) - `watch <command> <directory>`.

## Cross-platform Utilities

- [rimraf](https://github.com/isaacs/rimraf) - Cross-platform `rm -rf`.
- [mkdirp](https://github.com/substack/node-mkdirp) - Cross-platform `mkdir -p`.
- [copyfiles](https://github.com/calvinmetcalf/copyfiles) - Cross-platform file copying.
- [echo-cli](https://github.com/iamakulov/echo-cli) - Cross-platform `echo` with JS escape sequence support.

### Utility Packs

- [shx](https://github.com/shelljs/shx) - Supports `pwd`, `ls`, `rm`, `echo`, `touch`, `cp`, and `mkdir`.

## Other Utilities

- [hashmark](https://github.com/keithamus/hashmark) -  Take contents of a file and output as new file with a hash in the name.


## Cross-platform Shell Reference

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
- You can pass arguments to your scripts by passing `--` to `npm run`, followed by the arguments. Example: Given the script `"mocha": "mocha"`, you can run `npm run mocha -- --reporter xunit`. This effectivly runs `mocha --reporter xunit`.
- Running `npm test` is the same as running `npm run test`. The same applies to `npm start` and `npm stop`.

## Contributing

See [CONTRIBUTING.md](https://github.com/RyanZim/awesome-npm-scripts/blob/master/CONTRIBUTING.md).

## License

[![CC0](http://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
