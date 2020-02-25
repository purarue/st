## st - simple terminal

My fork of [st](https://st.suckless.org/)

Patches listed in [patches](./patches):

* visualbell
* scrollback
* externalpipe
* vertcenter
* font2
* externalpipe history (uses last 2000 lines instead of just whats on screen)

### Dependencies

* [roboto-mono](https://www.archlinux.org/packages/community/any/ttf-roboto-mono/) as the base font.
* [libx11](https://www.archlinux.org/packages/extra/x86_64/libx11/)
* For emoji support; requires [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) till thats merged into upstream libxft. I use [Noto Color Emoji](https://www.archlinux.org/packages/extra/any/noto-fonts-emoji/) as the `font2` fallback, but since the xft bug is fixed, most emoji fonts should work.
* [`st-copylast(cmd|output)`](https://github.com/seanbreckenridge/dotfiles/tree/master/.scripts/system). For `Alt+O`, `Alt+P`, externalpipe calls shell scripts which parse the output. Those have to be somewhere on your `$PATH`.

#### Custom Keybindings:

Key | Does
--- | ---
`Mouse Scroll` | Scrolls
`Ctrl + Shift + Plus` | Zoom In
`Ctrl + Shift + Minus` | Zoom Out
`Ctrl + Shift + 0` | Reset Zoom
`Alt + PageUp`/`Ctrl + Shift + Up` | Scrolls a screen up
`Alt + PageDown`/`Ctrl + Shift + Down` | Scrolls a screen down
`Alt + Up` | Scrolls screen up 1 line
`Alt + Down` | Scrolls screen down 1 line
`Alt + U` | Grabs any links from the current terminal, prompts user to select one and opens it in the browser
`Alt + Y` | Same as above, but copies the link to your clipboard
`Alt + O` | Finds commands that have been run in the current terminal, prompts user to select one, and copies the command and output to your clipboard
`Alt + P` | Same as above, but only copies the command and not the output

#### Install

clone, `make`, then `sudo make clean install`

#### Sync changes from upstream:

```
git remote add upstream https://git.suckless.org/st
git fetch upstream
git checkout master
git rebase upstream/master
```
