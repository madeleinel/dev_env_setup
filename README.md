# Dev environment setup

## Setup
- [ ] Install Atom - https://atom.io/
- [ ] Install iTerm2 - https://www.iterm2.com/
- [ ] Hush login message - `touch ~/.hushlogin`
- [ ] Install Homebrew - https://brew.sh/
- [ ] Install ZSH - `brew install zsh`
- [ ] Change shell - `chsh -s /usr/local/bin/zsh`
- [ ] Install Oh-my-zsh - `curl -L http://install.ohmyz.sh | sh`

### Add Atom shell command
This is to enable running the command `atom <file_name>` in the terminal.  
In Atom, go to `Menu` and click `Install Shell Commands`.

## Customisation
- [ ] Configure the terminal setup in `~/.zshrc`
    - [ ] Set terminal theme (showing current branch etc) - `ZSH_THEME="agnoster"` - Details at https://github.com/agnoster/agnoster-zsh-theme
    - [ ] Set default user so it’s not displayed in the terminal window - `DEFAULT_USER="madeleinelinder"`
- [ ] Configure the terminal setup in `~/.oh-my-zsh/themes/agnoster.zsh-theme`
    - [ ] Set it to only display the last two steps of the directory path - set `prompt_dir()` to `prompt_segment blue black '%2~'`
- [ ] Install Powerline font - list of fonts at https://github.com/powerline/fonts 
```
# clone the fonts repo
$ git clone https://github.com/powerline/fonts.git --depth=1
# run the installation script
$ cd fonts
$ ./install.sh
# tidy up the directory
$ cd ..
$ rm -rf fonts
```
- [ ] Change settings in iTerm Preferences > Profiles
  - [ ] Set the font: Text > Change font > `12pt Roboto Mono for Powerline`
  - [ ] Change colour scheme: Colors > Colour Presets > `Pastel Dark Background` && change ANSI blacks to `100% Black`
  - [ ] Set the home directory: General > Working directory > Change to `/Users/madeleinelinder/code`
- [ ] Set up syntax highlighting
  - [ ] To install: `cd ~/.oh-my-zsh && git clone git://github.com/zsh-users/zsh-syntax-highlighting.git`
  - [ ] To enable: Add `source ~/.oh-my-zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh` to `~.zshrc` and then restart the terminal and run command `source ~/.zshrc`
