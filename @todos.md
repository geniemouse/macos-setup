# macOS set-up @todo items

1. Fix XCode commandline already installed branch (Software update in System Settings message); throws error & exits!
2. Add SSH key generation step
    - Add key copy command to `.zshrc` alias list
3. Add directories:
    - Repos
    - VirtualMachines
4. See if installation of brews & casks can detect presence of checksum?
5. Update/fix Apple Mac Store routines
    - Installing branch getting skipped; `mas upgrade APP_ID` works when manually entered
    - Add `mas outdated` command on secondary run to see if anything previously installed is no longer available in Apple App Store
6. Add [Bun](https://bun.sh/) JavaScript runtime to try as faster/more complete project toolkit replacement for `npm`?
    - Install command `curl -fsSL https://bun.sh/install | bash`
7. _VirtualBox_ requires allowing Oracle America as a trusted developer in `macOS` security settings
    - Detect VirtualBox in casks file, ask to skip? Would give script a chance to complete before trying
8. Sort out traps
