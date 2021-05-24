# semitile
Point &amp; Key Tiling for Xfce

## Overview

Semitile enables tiling control by pointing the mouse at a particular
screen area and pressing a single tiling key or key combination
to tile the active window based on the mouse pointer position.

## Setup

1. Place the `semitile` file in the directory of your choice.
2. Select a key or key combination to use as the tiling key.
3. Set a keyboard shortcut for the selected key(s) to launch `semitile`.

_**Notes**_

* If the directory containing `semitile` isn't on your PATH, you'll need
to provide the keyboard shortcut with the full path to `semitile`.
* A good choice for a tiling key would be a key that you rarely use. Such
keys found on ordinary keyboards might include Menu, Scroll Lock, Pause,
or one of the Windows or Super keys. A key combination may be used if
necessary or desired.

## Description & Use

### Basic Tiling

Semitile defines screen areas to control tiling by dividing the
screen into a 3x3 grid of equal-size areas, as follows,
where tiling areas are portions of
the screen working area (i.e. the area excluding never-hidden panels):

    -----------------------------------------------------------------------------------------------
    |  Tile to Upper-Left Quarter  |      Tile to Upper Half      |  Tile to Upper-Right Quarter  |
    -----------------------------------------------------------------------------------------------
    |      Tile to Left Half       |      Position at Center      |      Tile to Right Half       |
    -----------------------------------------------------------------------------------------------
    |  Tile to Lower-Left Quarter  |      Tile to Lower Half      |  Tile to Lower-Right Quarter  |
    -----------------------------------------------------------------------------------------------

To tile the active window to a particular location, point the mouse at
the corresponding area of the screen indicated in the grid above and
press the tiling key. Where the active window is a
normal window, it should immediately tile to the indicated size and position.
Where the mouse pointer in the center area, the active window is
centered in the working area without resizing.

For practical reasons, some windows are excluded from tiling. Such windows include the
desktop window and desktop panels, as well windows not "Normal" according to xwininfo
(e.g. skinned VLC windows, Conky windows with `own_window_type` other than normal, etc.).
Attempts to tile such windows will have no effect.

### Additional Tiling

#### Centered Reading Tile

A window may also be tiled to screen center at half working area width and
full working area height to facilitate extended reading.
To tile a window in this manner,
position the mouse in the "Position at Center" area indicated in Basic Tiling
above and then press the tiling key twice in succession.
The first key press centers the window without resizing,
while the second resizes it to the dimensions indicated.

_**Note**_

* The second successive key press will be effective any time after the
first until a tiling operation is performed on another window
(i.e. there is no "double-press" time limit). Nevertheless,
this tiling is conveniently viewed as a point & double-press operation.
