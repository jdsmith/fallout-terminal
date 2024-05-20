# Fallout Terminal

Fallout terminal is a collection of scripts that I've gathered and customized from other bash Fallout projects. It includes a fun startup sequence for your terminal, a fallout themed "quit" sequence, and the password hacking game. I also included the iterm and powerline 10k profiles I use for my terminal.

# REQUIREMENTS

You must have the following for the scripts to work:

* Linux based or MacOS operating system
* The following packages installed:
    * pv
    * sox

The following is required to use the included profiles:

* iTerm 2.0
* ohmyzsh running the p10k theme

# PROFILE SETUP
Add the following to your .profile, .zshrc, or .bashrc file. Include the startup script at the top so that zsh or bash doesn't complain about execution output.

```
export FO3_TERM_BASE_DIR=<path_to_repo>
# this runs the startup sequence when the terminal opens
bash $FO3_TERM_BASE_DIR/boot_terminal.sh

...
The rest of your profile goes here
...

# some shortcut aliases I use
alias quit="bash $FO3_TERM_BASE_DIR/quit_terminal.sh && exit"
alias "zax.login"="bash $FO3_TERM_BASE_DIR/password_game.sh"
```