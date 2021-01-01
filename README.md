# macos-setup <!-- omit in toc -->

- [Install](#install)
- [Run](#run)
- [What gets installed?](#what-gets-installed)
  - [Dependencies](#dependencies)
  - [Package managers & build tools](#package-managers--build-tools)
  - [CLI tools & utilities](#cli-tools--utilities)
  - [Applications](#applications)
- [Security & Homebrew packages](#security--homebrew-packages)

---

_macOS setup_ is a script for provisioning a machine running `macOS` with a focus on client-side development. 
<br/><small>(Also an excuse to dig into Bash/ZSH).</small>

It can be run multiple times on the same machine; installing, upgrading or skipping packages, as necessary.

**Warning:** Do not run this script unless you have a clear understanding of what it is doing to your computer.

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
bash ./start 2>&1 | tee -a ~/macos-setup-run_$(date +%F-%H%M).log
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

@todo.

---

## Security & Homebrew packages

When installing anything via _Homebrew_'s `brew install` command, be sure it includes a checksum for package validation.

-   Review the [formula's](https://formulae.brew.sh/) JSON API file to confirm the presence of a property named `sha256`. It should contain a long string of alphanumeric characters
-   Any missing `sha256` or `sha256` with a value `"no_check"` should _NOT_ be installed via _Homebrew_; use a manual installation method (from an official source) instead

<small>_Homebrew_ will output a warning when installing a package without a checksum or a checksum of `"no_check"`.</small>
