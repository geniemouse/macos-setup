# macOS set-up @todo items

1. Remove brew casks that don't have checksum validation:
    - _Google Chrome_
    - _Tresorit_
2. Remove `canary` - no cask available
3. Investigate `sass` installation or remove it
4. Add an information file for manual installs (include link, open in browser):
    - [_Google Chrome_](https://www.google.com/chrome/)
    - [_Modern IE_](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/)
    - [_Tresorit_](https://tresorit.com/download)
5. _VirtualBox_ requires allowing Oracle America as a trusted developer in macOS security settings. Warn about this
6. _AdoptOpenJDK_:
    - Add function to `brew tap` before installing the JDK versions
    ```shell
    brew tap AdoptOpenJDK/openjdk
    brew install --cask adoptopenjdk14
    ```
7. Add SSH key generation step
    - Add key copy command to `.zshrc` alias list
8. Add function to create initial global `.gitconfig` file, if it doesn't exist
    - Use prompt to get name & email details, rather than store these in code repository
9. As `mvn` is installed, add an `.m2` directory with initial `settings.xml` file
10. Add developer fonts
11. Add directories:
    - Repos
    - VirtualMachines
12. Update `ReadMe.md`:
    - Recommend signing-in to _Apple iCloud_ before running script
    - Include warnings about not installing Homebrew packages without checksums
    - How to review Homebrew formulae & casks for checksums (via their JSON file)
    - Explain about previously installed apps & Homebrew installation
