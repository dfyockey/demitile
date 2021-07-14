# demitile
Point &amp; Keypress Tiling for Xfce

## Description

Demitile enables active window tiling to different locations using a single
tiling key. Tiling location is determined by mouse pointer position, and
tile size is controlled by repeated tiling key presses. A detailed article
on this tiling control technique, including a demonstration video,
is available at http://dfyockey.github.io/demitile/article.html.

### Coarse Tiling

The screen workarea (i.e. the area excluding never-hidden panels) is
viewed by Demitile as a grid of equal-size areas, as shown in the
following table. These areas are used to determine large-scale tiling
location.

    -----------------------------------------------------------------------------------------------
    |  Tile to Upper-Left Quarter  |      Tile to Upper Half      |  Tile to Upper-Right Quarter  |
    -----------------------------------------------------------------------------------------------
    |      Tile to Left Half       |        Tile to Center        |      Tile to Right Half       |
    -----------------------------------------------------------------------------------------------
    |  Tile to Lower-Left Quarter  |      Tile to Lower Half      |  Tile to Lower-Right Quarter  |
    -----------------------------------------------------------------------------------------------

To tile the active window to a particular location,
the mouse is pointed to the corresponding area, after which the tiling key
is pressed.
The window should immediately tile to the size and position
indicated in the table.

When the mouse pointer is located in the center
area, the window centered while being sized to full height and
half-screen-workarea width.

For practical reasons, windows that are not "Normal" according to the
`xwininfo` utility
are excluded from tiling. These include the desktop window, desktop panels,
and other unusual windows (e.g. skinned
VLC windows, Conky windows with `own_window_type` other than normal, etc.).
Attempts to tile such windows will have no effect.

### Fine Tiling

After a window has been coarsely tiled, fine tile selection
can be performed by repeated presses of the tiling key. In so doing, a
tile's size can be toggled between a number of widths.

Repeated presses of the tiling key toggle window width between the
following workarea fractions:

#### Left/Right Quarter or Half Tiles

* Quarter,
* Three-quarters, and
* Half

#### Upper/Lower Half Tiles

* Half (centered horizontally), and
* Full (i.e. maximum width)

**_Notes:_**

* Unlike mouse double-clicking, successive key presses are
effective any time after the first key press until either

	1. a tiling operation is performed on another window, or
	
	2. the mouse pointer is positioned in a different screen area when
	the tiling key is pressed.

* Fine Tiling does not apply to a center tiled window; attempts will
have no effect.

## Setup

1. Place the `demitile` file in the directory of your choice.

2. Select a key or key combination to use as the tiling key.

	* Suggestions for a tiling key include the Menu key or one of the
Windows or Super keys. However, any available key or key combination
can be used as the tiling key.

3. Set a keyboard shortcut for the selected tiling key(s) to launch `demitile`.

	* If the directory containing `demitile` isn't on your PATH, the
keyboard shortcut will need the full path to `demitile`.

4. (Optional) If checked, uncheck
`Automatically tile windows when moving toward the screen edge` on the
Accessibility Tab in Window Manager Tweaks.

	* Recommended to avoid confusion due to differences
between drag-tiled and demitiled window behavior after tiling.
If moved after tiling, drag-tiled windows return to their pre-tiled size
while demitiled windows retain their tiled size. Also, a drag-tiled window
requires a spurious demitile window operation before it will toggle in width.

5. (Optional) If checked, uncheck `Show shadows under regular windows`
on the Compositor Tab in Window Manager Tweaks.

	* Provides sharper visual definition of tiled window edges.
