# macOS set-up @todo items

1.Add SSH key generation step
    - Add key copy command to `.zshrc` alias list
1. Add directories:
    - Repos
    - VirtualMachines
1. See if installation of brews & casks can detect presence of checksum?
1. Update/fix Apple Mac Store routines
    - Installing branch getting skipped; `mas upgrade APP_ID` works when manually entered
    - Add `mas outdated` command on secondary run to see if anything previously installed is no longer available in Apple App Store
1. Add [Bun](https://bun.sh/) JavaScript runtime to try as faster/more complete project toolkit replacement for `npm`?
    - Install command `curl -fsSL https://bun.sh/install | bash`
1. _VirtualBox_ requires allowing Oracle America as a trusted developer in `macOS` security settings
    - Detect VirtualBox in casks file, ask to skip? Would give script a chance to complete before trying
1. Sort out traps
