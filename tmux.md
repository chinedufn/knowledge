# Tmux

## Handy plugins

Install the [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm).

Then set up our `~.tmux.conf`

```
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-continuum'
set -g @plugin 'tmux-plugins/tmux-sidebar'
set -g @plugin 'tmux-plugins/tmux-pain-control'

# Fix copy paste in vim
set -g default-shell $SHELL
set -g default-command "reattach-to-user-namespace -l ${SHELL}"

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com/user/plugin'
# set -g @plugin 'git@bitbucket.com/user/plugin'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'

## NAVIGATION: ############################

# Switch panes
# Usage: "ALT+arrow keys" (without prefix key)
# from https://gist.github.com/spicycode
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R

# Switch windows
# usage: "SHIFT+arrow" (without prefix key)
bind -n S-Left  previous-window
bind -n S-Right next-window
```
