# Dev environment setup

## Setup
- [ ] [Install Atom](https://atom.io/)
- [ ] [Install iTerm2](https://www.iterm2.com/)
- [ ] Hush login message - `touch ~/.hushlogin`
- [ ] [Install Homebrew](https://brew.sh/)
- [ ] Install ZSH - `brew install zsh`
- [ ] Change shell - `chsh -s /usr/local/bin/zsh` OR `chsh -s /bin/zsh` - run `atom /etc/shells` to check which path is included in the list of acceptable shells. If neither are included, add it to the bottom of that list.
- [ ] Install Oh-my-zsh - `curl -L http://install.ohmyz.sh | sh`

#### Add CLIs and short commands
- [ ] Enable the command `atom <file_name>` in the terminal: In Atom, go to `Menu` and click `Install Shell Commands`
- [ ] Add the Heroku CLI: `brew tap heroku/brew && brew install heroku` - [More info](https://devcenter.heroku.com/articles/heroku-cli#download-and-install)

## Customisation
- [ ] Configure the terminal setup in `~/.zshrc`
    - [ ] Set terminal theme (showing current branch etc) - `ZSH_THEME="agnoster"` - [More info](https://github.com/agnoster/agnoster-zsh-theme)
    - [ ] Set default user so it’s not displayed in the terminal window - `DEFAULT_USER="madeleinelinder"`
- [ ] Configure the terminal setup in `~/.oh-my-zsh/themes/agnoster.zsh-theme`
    - [ ] Set it to only display the last two steps of the directory path - set `prompt_dir()` to `prompt_segment blue black '%2~'`
- [ ] Install Powerline font - [list of available fonts](https://github.com/powerline/fonts)
```
# Clone the font repo
$ git clone https://github.com/powerline/fonts.git --depth=1
# Run the installation script
$ cd fonts
$ ./install.sh
# Tidy up the directory
$ cd ..
$ rm -rf fonts
```
- [ ] Change settings in iTerm Preferences > Profiles
  - [ ] Set the font: Text > Change font > `12pt Roboto Mono for Powerline`
  - [ ] Change colour scheme: Colors > Colour Presets > `Pastel Dark Background` && change ANSI blacks to `100% Black`
  - [ ] Set the home directory: General > Working directory > Change to `/Users/madeleinelinder/code`
- [ ] Set up syntax highlighting
  - [ ] To install: `cd ~/.oh-my-zsh && git clone git://github.com/zsh-users/zsh-syntax-highlighting.git`
  - [ ] To enable: Add `source ~/.oh-my-zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh` to the end of `~.zshrc` and then restart the terminal and run command `source ~/.zshrc`

## Authentication
Connect the terminal to your GitHub account [using SSH keys](https://help.github.com/en/articles/connecting-to-github-with-ssh).

- [ ] Check if there are existing public SSH keys: `ls -al ~/.ssh`
  Public keys are one of following file format: `id_dsa.pub`, `id_ecdsa.pub`, `id_ed25519.pub`, `id_rsa.pub`
- [ ] [Generate a new SSH key and add it to the ssh-agent](https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- [ ] [Add the SSH key to your GitHub account](https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account)
- [ ] Check that it's working by running eg `git pull origin master` in one of the repos

## Git config
Update the content in the git config file to ensure that GitHub commits are being assigned to the right user.

- [ ] Update the name - `git config --global user.name "<Full Name>"`
- [ ] Update the email address - `git config --global user.email "<email_address>"`

# Heroku config
Set Heroku CLI credentials to enable connecting to the Heroku account through the terminal.

- [ ] `heroku login` > Press any key to open the browser > Return to the terminal > Should see message `Logged in as <email_address>`
- [ ] Run `cat ~/.netrc` to confirm that the login credentials have been added to that file
