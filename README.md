## st - simple terminal

My fork of [st](https://st.suckless.org/)

Patches listed in [patches](./patches):

* visualbell
* scrollback
* externalpipe
* vertcenter
* font2

Uses [roboto-mono](https://www.archlinux.org/packages/community/any/ttf-roboto-mono/) as the base font.

Added emoji support; requires [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) till thats merged into upstream libxft. I use [Noto Color Emoji](https://www.archlinux.org/packages/extra/any/noto-fonts-emoji/) as the `font2` fallback, but since the xft bug is fixed, most things should work.

#### Custom Keybindings:

Key | Does
--- | ---
`Shift + Mouse Scroll` | Scrolls
`Ctrl + Shift + Plus` | Zoom In
`Ctrl + Shift + Minus` | Zoom Out
`Ctrl + Shift + 0` | Reset Zoom
`Shift + PageUp` | Scrolls a screen up
`Shift + PageDown` | Scrolls a screen down
`Ctrl + Shift + K`/`Ctrl + Shift + Up` | Scrolls screen up 1 line
`Ctrl + Shift + J`/`Ctrl + Shift + Down` | Scrolls screen down 1 line

