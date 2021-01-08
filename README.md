# macOS-setup <!-- omit in toc -->

- [General information](#general-information)
  - [Before running this script for the first time](#before-running-this-script-for-the-first-time)
  - [VirtualBox installation](#virtualbox-installation)
  - [Security & Homebrew packages](#security--homebrew-packages)
- [Install](#install)
- [Run](#run)
- [What gets installed?](#what-gets-installed)
  - [Dependencies](#dependencies)
  - [Package managers & build tools](#package-managers--build-tools)
  - [CLI tools & utilities](#cli-tools--utilities)
  - [Applications](#applications)
  - [Fonts & themes](#fonts--themes)

---

_macOS setup_ is a script for provisioning a machine running `macOS` with a focus on client-side development. 
<br/><small>(Also an excuse to dig into Bash/ZSH).</small>

It can be run multiple times on the same machine; installing, upgrading or skipping packages, as necessary.

**Warning:** Do not run this script unless you have a clear understanding of what it is doing to your computer.

## General information

### Before running this script for the first time

It is recommended that you:

- Sign-in to your  _Apple iCloud_ account in the _App Store_ application
- Uninstall any previous applications that you want Homebrew to control instead (i.e. items listed in `install/casks`); _Homebrew_ can't overwrite applications installed by other methods
- Ensure that the _Homebrew_ items for installation have checksum validation, cf. _[Security & Homebrew packages](#security--homebrew-packages)_ below

### VirtualBox installation

If installing _[VirtualBox](https://www.virtualbox.org/)_ for the first time, the set-up script may fail until _Oracle_ is added as a trusted developer to the `macOS` Security & Privacy settings (_General_ tab).

After allowing _Oracle_ as a trusted developer, running the set-up script should complete the process.

### Security & Homebrew packages

When installing anything via _Homebrew_'s `brew install` command, be sure it includes a checksum for package validation.

-   Review the [formula's](https://formulae.brew.sh/) JSON API file to confirm the presence of a property named `sha256`. It should contain a long string of alphanumeric characters
-   Any missing `sha256` or `sha256` with a value `"no_check"` should _NOT_ be installed via _Homebrew_; use a manual installation method (from an official source) instead

<small>_Homebrew_ will output a warning when installing a package without a checksum or a checksum of `"no_check"`.</small>

---

## Install

Download the script files.

```
git clone https://github.com/geniemouse/macos-setup.git && cd macos-setup
```

## Run

From the `macos-setup` directory, run command:

```bash
bash ./start
```

...or for optional file logging:

```bash
bash ./start 2>&1 | tee -a ~/macos-setup-run_$(date +%F).log
```

---

## What gets installed?

### Dependencies

-   [Xcode Developer Tools](https://developer.apple.com/xcode/) from Apple
-   [Homebrew](https://brew.sh/) macOS/Linux package manager

### Package managers & build tools

-   [AdoptOpenJDK](https://adoptopenjdk.net/) for switching between different Java JDK versions
-   [Git](https://git-scm.com/) for version control
-   [Maven](https://maven.apache.org/) for project building
-   [Node](https://nodejs.org/en/) for `npm` & JavaScript-based project building
-   [Wget](https://www.gnu.org/software/wget/) useful tool for getting internet files

### CLI tools & utilities

-   [git-standup](https://github.com/kamranahmedse/git-standup) to recall what you did yesterday
-   [ImageOptim-CLI](https://jamiemason.github.io/ImageOptim-CLI/) for batch optimising images
-   [mas](https://github.com/mas-cli/mas) to access Mac App Store
-   [Prettier](https://prettier.io/) for automated code formatting
-   ...and more @todo ...

### Applications

// @todo.

### Fonts & themes

// @todo.
