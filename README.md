# macOS-setup <!-- omit in toc -->

- [General information](#general-information)
  - [Before running this script for the first time](#before-running-this-script-for-the-first-time)
  - [Security & Homebrew packages](#security--homebrew-packages)
- [Install](#install)
- [Run](#run)
- [What gets installed?](#what-gets-installed)
  - [Command-line](#command-line)
  - [Applications](#applications)
  - [Fonts & themes](#fonts--themes)
- [Known issues](#known-issues)
  - [Homebrew](#homebrew)
  - [Mac App Store command-line interface & macOS Monterey](#mac-app-store-command-line-interface--macos-monterey)
- [Acknowledgements](#acknowledgements)

---

_macOS setup_ is a script for provisioning a machine running `macOS` with a focus on client-side development. 
<br/><small>(Also an excuse to dig into Bash/ZSH).</small>

It can be run multiple times on the same machine; installing, upgrading or skipping packages, as necessary.

**Warning:** Do not run this script unless you have a clear understanding of what it is doing to your computer.

---

# General information

## Before running this script for the first time

It is recommended that you:

- Sign-in to your _Apple iCloud_ account in the _App Store_ application
- Uninstall any previous applications that you want to control via command-line. For example, anything listed in `install/apps` and `install/casks`
- Ensure that the _Homebrew_ items for installation have checksum validation, cf. _[Security & Homebrew packages](#security--homebrew-packages)_ below

## Security & Homebrew packages

When installing anything via _Homebrew_'s `brew install` command, be sure it includes a checksum for package validation.

-   Review the [formula's](https://formulae.brew.sh/) JSON API file to confirm the presence of a property named `sha256`. It should contain a long string of alphanumeric characters
-   Any missing `sha256` or `sha256` with a value `"no_check"` should _NOT_ be installed via _Homebrew_; use a manual installation method (from an official source) instead

<small>_Homebrew_ will output a warning when installing a package without a checksum or a checksum of `"no_check"`.</small>

---

# Install

Download the script ZIP file from the latest release, or clone this Git repository:

```
git clone https://github.com/geniemouse/macos-setup.git && cd macos-setup
```

# Run

From the `macos-setup` directory, run command:

```bash
bash ./start
```

...or for optional file logging:

```bash
bash ./start 2>&1 | tee -a ~/macos-setup-run_$(date +%F).log
```

---

# What gets installed?

## Command-line

<details>
    <summary>Dependencies</summary>

-   [Xcode Developer Tools](https://developer.apple.com/xcode/) from Apple
-   [Homebrew](https://brew.sh/) macOS/Linux package manager
-   [NVM](https://github.com/nvm-sh/nvm) the [Node](https://nodejs.org/en/) version manager
    -   Allows use of different `node`/`npm` JavaScript build environments between projects
    -   Note: The Homebrew package is not supported by NVM team; using the official channel instead

</details>

<details>
    <summary>Package managers & build tools</summary>

-   [Eclipse Temurin](https://adoptium.net/) for switching between different Java JDK versions
-   [Git](https://git-scm.com/) for version control
-   [Maven](https://maven.apache.org/) for project building
-   [Wget](https://www.gnu.org/software/wget/) useful tool for getting internet files

</details>

<details>
    <summary>CLI tools & utilities</summary>

-   [git-standup](https://github.com/kamranahmedse/git-standup) to recall what you did yesterday
-   [ImageOptim-CLI](https://jamiemason.github.io/ImageOptim-CLI/) for batch optimising images
-   [mas](https://github.com/mas-cli/mas) to access Mac App Store
-   [Prettier](https://prettier.io/) for automated code formatting
-   [Vagrant](https://www.vagrantup.com) development environments & sandboxes

</details>

## Applications

<details>
    <summary>Browsers</summary>

-   [Brave](https://brave.com)
-   [Firefox](https://www.mozilla.org/en-US/firefox/new/)
-   [Firefox Developer](https://www.mozilla.org/en-US/firefox/developer/)
-   [Opera](https://www.opera.com)
-   [Tor Browser](https://www.torproject.org)
-   [Vivaldi](https://vivaldi.com)

</details>

<details>
    <summary>Design</summary>

-   [Affinity Designer](https://affinity.serif.com/en-us/designer/) vector graphics editor. Similar to Adobe Illustrator, without the subscription model
-   [Affinity Photo](https://affinity.serif.com/en-us/photo/) image editor. Similar to Adobe Photoshop, without the subscription model
-   [Skitch](https://evernote.com/products/skitch) annotated screenshots & sketches

</details>

<details>
    <summary>Development</summary>

-   [Dash](https://kapeli.com/dash) offline API docsets, manuals & code snippets
-   [ImageOptim](https://imageoptim.com/mac) image optimisation
-   [iTerm 2](https://iterm2.com) improved terminal
-   [Kaleidoscope](https://kaleidoscope.app) powerful diff tool
-   [Nova](https://nova.app) macOS native IDE
-   [Sublime Text](https://www.sublimetext.com) IDE for Linux, Mac & PC
-   [Postman](https://www.postman.com) API building platform for designing, prototyping & sharing APIs
-   [Visual Studio Code](https://code.visualstudio.com) IDE for Linux, Mac & PC
-   [xScope](https://xscopeapp.com) on-screen measuring tool

</details>

<details>
    <summary>Reading, writing & communication</summary>

-   [Bear](https://bear.app) Markdown notes for macOS
-   [iA Writer](https://ia.net/writer) minimalist text editor writing
-   [Keynote](https://www.apple.com/keynote/) Apple presentation software
-   [Magnet](https://magnet.crowdcafe.com) macOS window manager
-   [Numbers](https://www.apple.com/numbers/) Apple spreadsheet software
-   [Pages](https://www.apple.com/pages/) Apple word processing software
-   [Slack](https://slack.com) team/project communication
-   [Twitter/X](https://twitter.com/) (not so) social media channel

</details>

<details>
    <summary>Utilities & services</summary>

-   [Alfred](https://www.alfredapp.com) macOS helper for super-charged automation & shortcuts
-   [Encrypto](https://macpaw.com/encrypto) encrypting files & folders
-   [Microsoft Remote Desktop](https://www.microsoft.com/en-us/store/p/microsoft-remote-desktop/9wzdncrfj3ps)
-   [Reeder 5](https://www.reederapp.com) RSS reader
-   [Renamer](https://renamer.com) batch file renaming tool
-   [Spillo](https://bananafishsoftware.com/products/spillo/) macOS client for the [Pinboard](https://pinboard.in) bookmarking service
-   [The Unarchiver](https://macpaw.com/the-unarchiver) more powerful archive unpacking tool
-   [TunnelBear](https://www.tunnelbear.com) VPN service for privacy or testing geolocation code
-   [VLC](https://www.videolan.org) media player

</details>

## Fonts & themes

Fonts are installed by tapping [`homebrew/cask-fonts`](https://github.com/Homebrew/homebrew-cask-fonts) listing.

- [FiraCode](https://github.com/tonsky/FiraCode)
- [Hasklig](https://github.com/i-tu/Hasklig/)
- [JetBrains Mono](https://github.com/JetBrains/JetBrainsMono)

On the command-line, run the following to see more information about font recipes:

1. Currently installed font recipes: `brew list --cask | grep "font-*"`
2. Full list available to install: `brew search --cask "/font-/"`

---

# Known issues

## Homebrew

_Homebrew_ can't overwrite applications previously installed by other methods.

## Mac App Store command-line interface & macOS Monterey

The _Mac App Store_ command-line interface (`mas`) will fail to correctly recognise the _App Store_'s logged-in status on systems running _macOS Monterey_. This is a [known issue](https://github.com/mas-cli/mas/issues/417) to the project and is being worked on. In the meantime, _App Store_ purchases will have to be installed directly via the _App Store_ application.

---

# Acknowledgements

Inspiration, code and other things from the following people.

- [Mina Markham's Formation script](https://github.com/minamarkham/formation)
- [thoughbot's Laptop](https://github.com/thoughtbot/laptop/)
- Julia Evans for ["Bite Size Bash"](https://wizardzines.com/) and other zines

Go and checkout their fine work.
