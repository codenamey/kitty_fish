# Setting up fish & kitty to os x.
***
brew install fish

brew tap homebrew/cask-fonts

brew install --cask font-hack-nerd-font

brew install fzf

brew install fd

brew install fisher

change terminal to fish
cshs -s /opt/homebrew/bin/fish

##run following under
set -U fish_user_paths /opt/homebrew/bin/ $fish_user_paths

##needed to get it working

create file `.config/fish/functions/ssh.fish`

```
function ssh
    set -l SSH (which ssh)
    set -lx TERM xterm-256color
    set -lx COLORTERM 24bit
    eval SSH $argv
end
```

patch ~/.config/kitty/kitty.conf kitty_patchfile.patch

Sources:

    - https://sw.kovidgoyal.net/kitty/

    - https://fishshell.com
