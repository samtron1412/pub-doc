[TOC]

# Overview

# Usage

- Description of a package: `brew desc <pkg>`
- Install: `brew install <pkg>`
- Uninstall: `brew uninstall <pkg>`
- Update: `brew update`
- List outdated packages: `brew outdated`
- Upgrade: `brew upgrade`
- List all packages: `brew list`
- Search a package: `brew search <text>`
- Cleaning up
    + Showing old version of packages: `brew cleanup -n`
    + Cleaning up all old versions: `brew cleanup`
    + Cleaning up old versions of a package: `brew cleanup <pkg>`
- Dependencies
    + Showing dependencies of a package: `brew deps <pkg>`
    + Showing dependencies as tree for a package: `brew deps --tree pkg`
    + Showing dependencies as tree for all installed packages:
        * `brew deps --tree --installed`
    + Showing list of dependencies for all installed packages:
        * `brew deps --installed`
- Showing packages that are not dependencies of another installed
  packaged: `brew leaves`
- Tap
    + List all installed taps: `brew tap`
    + Tap a package repository: `brew tap <user/repo>`
- Info
    + Summary info for packages/formulae: `brew info`
    + Summary info for taps: `brew tap-info`
- Cask: install macOS applications distributed as binaries
    + commands: info, install, uninstall, list, outdated, upgrade
    + after the name of a cask, if it has "auto_updates": it means that
      the package has a mechanism to update itself, so brew cask does
      not upgrade the package
- Remove a package with its dependencies:
    + `brew tap beeftornado/rmtree`
    + `brew rmtree <pkg>`
- Bundle
    + Install
        * `brew bundle`: looking for `Brewfile` in the current directory
          and install all the formulae in the file
        * `brew bundle --file <path/to/a/different/Brewfile>`
    + Dump
        * `brew bundle dump`: create a `Brewfile` from all existing
          Homebrew packages at the current directory
        * `brew bundle dump --force`: overwrite an existing Brewfile
        * `brew bundle dump [--force] --describe`: output a description
          comment above each line
    + Cleanup
        * `brew bundle cleanup`: listing all packages that are not
          listed in the Brewfile
        * `brew bundle cleanup --force`: uninstall them
    + Check: `brew bundle check [--verbose]`
    + List
        * `brew bundle list --all [--casks, --taps, --mas, --brews]`
        * default `--brews`
- mas: Mac App Store
    + `mas list`
    + `mas search Xcode [--price]`
    + `mas install <app_id>`: application identifier
    + `mas outdated`
    + `mas upgrade` or `mas upgrade <app_id>`
    + `mas signin --dialog mas@example.com`: sign in
    + `mas account`: account info
    + `mas info <app_id>`
    + `mas uninstall <app_id> [--dry-run]`
    + `mas version`
- Different versions of a package
    + `brew tap homebrew/cask-versions`