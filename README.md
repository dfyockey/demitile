# semitile
Point &amp; Press Tiling for Xfce

## Overview

Semitile enables tiling control by pointing the mouse at a particular
screen area and pressing a single keyboard shortcut
to tile the active window based on the mouse pointer position.

## Setup

1. Place the `semitile` file in the directory of your choice.
2. Select a key or key combination to use as the tiling key.
3. Set a keyboard shortcut for the selected key(s) to launch `semitile`.

_**Notes**_

* If the directory containing `semitile` isn't on your PATH, you'll need
to provide the keyboard shortcut with the full path to `semitile`.
* A good choice for a tiling key would be a key that you don't use.
Depending on the user, such keys found on ordinary keyboards might include
Menu, Scroll Lock, Pause, or one of the Windows or Super keys.
* Users with a 4+ button mouse should be able to use an extra mouse button
as the tiling key.

## Description & Use

### Basic Tiling

Semitile divides the screen working area (i.e. the area excluding never-hidden panels)
into a grid of equal-size areas as shown in the following table.

    -----------------------------------------------------------------------------------------------
    |  Tile to Upper-Left Quarter  |      Tile to Upper Half      |  Tile to Upper-Right Quarter  |
    -----------------------------------------------------------------------------------------------
    |      Tile to Left Half       |      Position at Center      |      Tile to Right Half       |
    -----------------------------------------------------------------------------------------------
    |  Tile to Lower-Left Quarter  |      Tile to Lower Half      |  Tile to Lower-Right Quarter  |
    -----------------------------------------------------------------------------------------------

To tile the active window to a particular location, point the mouse
to a screen area press the tiling key.
The window should immediately tile to the indicated size and position
indicated in the table. When the mouse pointer is located in the center
area, the window is centered in the working area but not resized.

_**Note**_

* For practical reasons, windows that are not "Normal" according to xwininfo
are excluded from tiling. These include the desktop window, desktop panels,
and other unusual windows (e.g. skinned
VLC windows, Conky windows with `own_window_type` other than normal, etc.).
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
