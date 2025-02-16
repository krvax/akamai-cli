# 1.5.2 (July 28, 2022)

## Enhancements

* New help option without arguments.

## Fixes

* Fix `akamai update` command failures when the directory `~/.akamai-cli/src/cli-xyz` is in a git detached state.
* Show the correct version for CLI modules which version is set via ldflags.
* Fix execution of Python submodules on Windows ([GH#159](https://github.com/akamai/cli/issues/159)).
* Fine print update warnings for homebrew installations.
* Fix failing unit tests on Windows.

# 1.5.1 (June 8, 2022)

## Fixes

* `update` command does not work for some packages, ie. `cli-terraform`.

# 1.5.0 (May 26, 2022)

## Enhancements

* Support for new Apple M1(Darwin ARM64) build ([GH#127](https://github.com/akamai/cli/issues/127)). NOTE: not all CLI packages currently support Apple M1.

# 1.4.2 (May 11, 2022)

## Fixes

* Handle recent Python versions ([GH#148](https://github.com/akamai/cli/issues/148)).
* Handle `yes` command input ([GH#136](https://github.com/akamai/cli/issues/136)).
* Purge directories on unit test error.

# 1.4.1 (March 24, 2022)

## Fixes

* Refactor CLI error to debug statement when virtual environment deactivation fails.
* Refactor CLI documentation by dropping usage examples of cli-property (decommissioned).

# 1.4.0 (March 14, 2022)

## Enhancements

* [IMPORTANT] Refactor Python support, making use of virtual environments to isolate dependencies for each Python package.
  * Refer to README.md for new system dependencies.

# 1.3.1 (December 8, 2021)

## Enhancements

* Improved message for updating CLI version

# 1.3.0 (October 6, 2021)

## Fixes

* Remove old binary in PowerShell terminal ([#125](https://github.com/akamai/cli/issues/125)).
* Document CLI exit codes.
* Review exit code when trying to install an already installed command ([#83](https://github.com/akamai/cli/issues/83)).

## Enhancements
* Update list of installable CLI commands.
* Document `--version` flag ([#94](https://github.com/akamai/cli/issues/94)).
* Add alias with package prefix to all installed commands to work around possible command name collisions ([#60](https://github.com/akamai/cli/issues/60)).
* Make .edgerc location configurable ([#81](https://github.com/akamai/cli/issues/81))

# 1.2.1 (April 28, 2021)

## Fixes
* Fixed `PROXY` flag not working correctly in go 1.16
* Fixed old executable not being removed after upgrading on windows

## Enhancements
* `upgrade` command can now be executed with auto upgrades disabled
* Improved error messages on several commands
* Added upgrade command error message for homebrew installation 

# 1.2.0 (March 16, 2021)

## Fixes
* Synced logs with terminal output in most commands.
* Fixed module update issue ([#113](https://github.com/akamai/cli/issues/113)).
* Fix panic when attempting to write on an empty writer ([#116](https://github.com/akamai/cli/issues/116))

## Enhancements
* Code improvements: unit test coverage improvement and project structure refactoring.
* Glide build tool was dropped in favor of go modules.
* Dockerfile has been moved to [akamai-docker](https://github.com/akamai/akamai-docker/) repository.
* Logging: all `TRACE` log messages are now written in `DEBUG` level. Besides, all commands are traced in logs with `START`, `FINISH` or eventually `ERROR`.
* Logging: new `AKAMAI_CLI_LOG_PATH` environment variable to redirect logs to a file.
