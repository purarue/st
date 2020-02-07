## st - simple terminal

My fork of [st](https://st.suckless.org/)

Patches listed in [patches](./patches):

* visualbell
* scrollback
* externalpipe
* vertcenter
* font2

### Dependencies

* [roboto-mono](https://www.archlinux.org/packages/community/any/ttf-roboto-mono/) as the base font.
* [libx11](https://www.archlinux.org/packages/extra/x86_64/libx11/)
* For emoji support; requires [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) till thats merged into upstream libxft. I use [Noto Color Emoji](https://www.archlinux.org/packages/extra/any/noto-fonts-emoji/) as the `font2` fallback, but since the xft bug is fixed, most emoji fonts should work.

#### Custom Keybindings:

Key | Does
--- | ---
`Shift + Mouse Scroll` | Scrolls
`Ctrl + Shift + Plus` | Zoom In
`Ctrl + Shift + Minus` | Zoom Out
`Ctrl + Shift + 0` | Reset Zoom
`Alt + PageUp` | Scrolls a screen up
`Alt + PageDown` | Scrolls a screen down
`Alt + Up` | Scrolls screen up 1 line
`Alt + Down` | Scrolls screen down 1 line
`Alt + U` | Grabs any links on screen currently, prompts user to select one and opens it in the browser
`Alt + Y` | Same as above, but copies the link to your clipboard

#### Install

clone, `make`, then `sudo make clean install`

#### Sync changes from upstream:

```
git remote add upstream https://git.suckless.org/st
git fetch upstream
git checkout master
git rebase upstream/master
```
