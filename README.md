# semitile
Point &amp; Press Tiling for Xfce

## Description

Semitile enables active window tiling to different locations using a single
tiling key, with tiling location being determined by mouse pointer position.
Tile sizing is controlled by repeated tiling key presses.

### Basic Tiling

The screen working area (i.e. the area excluding never-hidden panels) is
viewed by Semitile as a grid of equal-size areas, as shown in the
following table.

    -----------------------------------------------------------------------------------------------
    |  Tile to Upper-Left Quarter  |      Tile to Upper Half      |  Tile to Upper-Right Quarter  |
    -----------------------------------------------------------------------------------------------
    |      Tile to Left Half       |      Position at Center      |      Tile to Right Half       |
    -----------------------------------------------------------------------------------------------
    |  Tile to Lower-Left Quarter  |      Tile to Lower Half      |  Tile to Lower-Right Quarter  |
    -----------------------------------------------------------------------------------------------

To tile the active window to a particular location,
the mouse is pointed to the corresponding area, afterwhich the tiling key
is pressed.
The window should immediately tile to the size and position
indicated in the table. When the mouse pointer is located in the center
area, the window is centered in the working area but not resized.

For practical reasons, windows that are not "Normal" according to the
`xwininfo` utility
are excluded from tiling. These include the desktop window, desktop panels,
and other unusual windows (e.g. skinned
VLC windows, Conky windows with `own_window_type` other than normal, etc.).
Attempts to tile such windows will have no effect.

### Tile Sizing

After a window has been tiled, its width can be toggled between a number
of sizes by repeated presses of the tiling key. A center-positioned
window's height is also affected.

Unlike with mouse double-clicking, successive key presses will be
effective any time after the first key press until either 1) a tiling
operation is performed on another window, or 2) the mouse pointer is
positioned in a different screen area when the tiling key is pressed.
That is, there is no time limit analogous to the mouse's double-click time.

#### Center Tile

After a window has been positioned at center as indicated in Basic Tiling,
subsequent presses of the tiling key set the window height to its maximum
and toggle the window width between the following sizes:

* Half-screen width (intended to facilitate reading of lengthy documents), and
* Three-quarter-screen width.

#### Left/Right Tiles

After a window has been tiled to the left or right as indicated in
Basic Tiling, subsequent presses of the tiling key toggle the tiled
window width between the following sizes:

* Quarter-screen width,
* Three-quarter-screen width, and
* Half-screen width.

#### Upper/Lower Tiles

After a window is tiled to the upper or lower half as indicated in
Basic Tiling, subsequent presses of the tiling key toggle the tiled
window width between the following sizes:

* Half-screen width (centered horizontally), and
* Maximum width.

## Setup

1. Place the `semitile` file in the directory of your choice.
2. Select a key or key combination to use as the tiling key.
3. Set a keyboard shortcut for the selected key(s) to launch `semitile`.

_**Notes**_

* If the directory containing `semitile` isn't on your PATH, the
keyboard shortcut will need the full path to `semitile`.
* Suggestions for a tiling key include the Menu key or one of the
Windows or Super keys. However, any available key or key combination
can be used as the tiling key.
* Users with a 4+ button mouse may be able to use an extra mouse button
as the tiling key.
