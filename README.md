# tmux_notes
Notes on how tmux works and usage

## tmux plugin manager (tpm)
> https://github.com/tmux-plugins/tpm

1. `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`
2. Add to the bottom of `~/.tmux.conf`
   ```console
    # List of plugins
    set -g @plugin 'tmux-plugins/tpm'
    set -g @plugin 'tmux-plugins/tmux-sensible'

    # Other examples:
    # set -g @plugin 'github_username/plugin_name'
    # set -g @plugin 'github_username/plugin_name#branch'
    # set -g @plugin 'git@github.com:user/plugin'
    # set -g @plugin 'git@bitbucket.com:user/plugin'

    #  Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
    run '~/.tmux/plugins/tpm/tpm'
   ```
3. Reload tmux `tmux source ~/.tmux.conf`

## tmux-logging plugin

1. Add to ~/.tmux.conf `set -g @plugin 'tmux-plugins/tmux-logging'`
2. Install `Ctrl+b I`
3. Running Saving complete history of pane  `Ctrl+b alt + shift + p`

## synchronize 'panes'

1. `Ctrl+b :` (enter command mode
2. `set-window-option synchronize-panes`
3. Issue the same command to disable

## enable mouse support

Enable disable mouse support

1. `Ctrl+b :`  (enter command mode)
2. `set -g mouse`

Add to ~/.tmux.conf

```
set -g mouse
```

*** WARNING: enabling mouse support causes weird stuff  to happen with copying and pasting if you are use to a terminal with right click paste. ***

## Copy and paste in a split screen (Ctrl+b + %)

https://news.ycombinator.com/item?id=7758368

1. Zoom in on the intended pane (`Ctrl+b z`)
2. Once zoomed in select text and copy
3. Zoom out of the pange (`Ctrl+b z`)
