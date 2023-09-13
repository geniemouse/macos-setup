# macOS set-up @todo items

1. Test for NVM install doesn't work, so install attempt runs each time
    - Update NVM git repo url to latest version
    - Remove if NVM statement, as not working. NVM's own checks seem sufficient
    - Wrap NPM install in if-statement instead?
1. Add SSH key generation step
    - Add key copy command to `.zshrc` alias list
1. Add directories:
    - Repos
    - VirtualMachines
1. See if installation of brews & casks can detect presence of checksum?
1. Add [Bun](https://bun.sh/) JavaScript runtime to try as faster/more complete project toolkit replacement for `npm`?
    - Install command `curl -fsSL https://bun.sh/install | bash`
1. _VirtualBox_ requires allowing Oracle America as a trusted developer in `macOS` security settings
    - Detect VirtualBox in casks file, ask to skip? Would give script a chance to complete before trying
1. Sort out traps
