## st - simple terminal

My fork of [st](https://st.suckless.org/)

Patches listed in [patches](./patches):

* visualbell
* scrollback
* externalpipe
* vertcenter
* font2

Added emoji support; requires [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) till thats merged into upstream libxft. I use Noto Color Emoji as the `font2` fallback, but most since the xft bug is fixed, most things should work.

#### Custom Keybindings:

Key | Does
--- | ---
`Shift + Mouse Scroll` | Scrolls
`Ctrl + Shift + Plus` | Zoom In
`Ctrl + Shift + Minus` | Zoom Out
`Ctrl + Shift + 0` | Reset Zoom
`Shift + PageUp` | Scrolls a screen up
`Shift + PageDown` | Scrolls a screen down
`Shift + K`/`Shift + Up` | Scrolls screen up 1 line
`Shift + J`/`Shift + Down` | Scrolls screen down 1 line

