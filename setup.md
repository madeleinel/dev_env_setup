# Dev environment setup

## Setup
- [ ] Install Atom - https://atom.io/
- [ ] Install iTerm2 - https://www.iterm2.com/
- [ ] Hush login message - `touch ~/.hushlogin`
- [ ] Install Homebrew - https://brew.sh/
- [ ] Install ZSH - `brew install zsh`
- [ ] Change shell - `chsh -s /usr/local/bin/zsh`
- [ ] Install Oh-my-zsh - `curl -L http://install.ohmyz.sh | sh`

## Customisation
- [ ] Configure the terminal setup in `~/.zshrc`
    - [ ] Set terminal theme (showing current branch etc) - `ZSH_THEME="agnoster”` - Details at https://github.com/agnoster/agnoster-zsh-theme
    - [ ] Set default user so it’s not displayed in the terminal window - `DEFAULT_USER="madeleinelinder”`
- [ ] Configure the terminal setup in `~/.oh-my-zsh/themes/agnoster.zsh-theme`
    - [ ] Set it to only display the last two steps of the directory path - set `prompt_dir()` to `prompt_segment blue black '%2~’`
        - [ ] At this point, need to install a Powerline (see screenshot of current display)

- [ ] Install syntax highlighting - `cd ~/.oh-my-zsh && git clone git://github.com/zsh-users/zsh-syntax-highlighting.git`
- [ ] Enable syntax highlighting - Add `source ~/.oh-my-zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh` to `~.zshrc` and then restart the terminal and run command `source ~/.zshrc`
- [ ] Install Powerline font - list of fonts at https://github.com/powerline/fonts 
```
# clone the fonts repo
$ git clone https://github.com/powerline/fonts.git --depth=1
# install
$ cd fonts
$ ./install.sh
# clean-up a bit
$ cd ..
$ rm -rf fonts
```
- [ ] Set font in iTerm - Preferences>Profiles>Text>Change font > `12pt Roboto Mono for Powerline`
- [ ] Set home directory in iTerm - Preferences>Profiles>General>Working directory > Change to `/Users/madeleinelinder/Documents/Code`
- [ ] Change colour scheme - Preferences>Profiles>Colors>Colour Presets > `Pastel Dark Background` && change ANSI blacks to `100% Black`

## Further tools / software
- [ ] Install Xcode - Through App Store
- [ ] Install Node & npm - `brew install node`
- [ ] Install postgres - `brew install postgresql` and `brew services start postgresql`
- [ ] Install docker & docker-compose - download through https://docs.docker.com/docker-for-mac/install/#download-docker-for-mac - install

- [ ] Set up Atom syntax highlighters
    - [ ] JS
    - [ ] React
    - [ ] HTML/CSS
    - [ ] Python
