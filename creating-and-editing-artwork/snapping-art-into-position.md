# Snapping art into position

To automatically align graphic elements with one another, use _snapping_. Flash
Pro provides three ways for you to align objects on the Stage:

- Object snapping snaps objects directly to other objects along their edges.

- Pixel snapping snaps objects directly to individual pixels or lines of pixels
  on the Stage.

- Snap alignment snaps objects to a specified _snap tolerance_, a preset
  boundary between objects and other objects or between objects and the edge of
  the Stage.

  > **Note:** You can also snap to the grid or to guides.

## Turn object snapping on or off

To turn on object snapping, use the Snap To Objects modifier for the Selection
tool, or the Snap To Objects command in the View menu.

If the Snap To Objects modifier for the Selection tool is on, a small black ring
appears under the pointer when you drag an element. The small ring changes to a
larger ring when the object is within snapping distance of another object.

![](../img/dingbat.png) Select View \> Snapping \> Snap To Objects. A check mark
appears next to the command when it is on.

When you move or reshape an object, the position of the Selection tool on the
object provides the reference point for the snap ring. For example, if you move
a filled shape by dragging near its center, the center point snaps to other
objects. This is particularly useful for snapping shapes to motion paths for
animating.

> **Note:** For better control of object placement when snapping, begin dragging
> from a corner or center point.

## Adjust object snapping tolerances

1.  Select Edit \> Preferences (Windows) or Flash \> Preferences (Macintosh),
    and click Drawing.
2.  Under Drawing Settings, adjust the Connect Lines setting.

## Use pixel snapping

To turn on pixel snapping, use the Snap To Pixels command in the View menu. If
Snap To Pixels is on, a pixel grid appears when the view magnification is set to
400% or higher. The pixel grid represents the individual pixels that appear in
your Flash Pro application. When you create or move an object, it is constrained
to the pixel grid. If you create a shape whose edges fall between pixel
boundaries—for example, if you use a stroke with a fractional width, such as 3.5
pixels—Snap To Pixels snaps to pixel boundaries, not to the edge of the shape.

- To turn pixel snapping on or off, select View \> Snapping \> Snap To Pixels.
  If the magnification is set to 400% or higher, a pixel grid is displayed. A
  check mark appears next to the command when it is on.

- To turn pixel snapping on or off temporarily, press the C key. When you
  release the C key, pixel snapping returns to the state you selected with
  View \> Snapping \> Snap To Pixels.

- To temporarily hide the pixel grid, press the X key. When you release the X
  key, the pixel grid reappears.

## Select settings for Snap Alignment

When you select Snap Alignment settings, set the snap tolerance between
horizontal or vertical edges of objects, and between objects' edges and the
Stage border. You can also turn on snap alignment between the horizontal and the
vertical centers of objects. All Snap Alignment settings are measured in pixels.

1.  Select View \> Snapping \> Edit Snapping.
2.  In the Edit Snapping dialog box, select the types of objects to want to snap
    to.
3.  Click the Advanced button and select any of the following:

    - To set the snap tolerance between objects and the Stage border, enter a
      value for Movie Border.

    - To set the snap tolerance between the horizontal or vertical edges of
      objects, enter a value for Horizontal, Vertical, or both.

    - To turn on Horizontal or Vertical Center Alignment, select Horizontal or
      Vertical Center Alignment or both.

## Turn on Snap Alignment

When Snap Alignment is turned on, dotted lines appear on the Stage when you drag
an object to the specified snap tolerance. For example, if you set Horizontal
snap tolerance to 18 pixels (the default setting), a dotted line appears along
the edge of the object you are dragging when the object is exactly 18 pixels
from another object. If you turn on Horizontal Center Alignment, a dotted line
appears along the horizontal center vertices of two objects when you precisely
align the vertices.

![](../img/dingbat.png) Select View \> Snapping \> Snap Align. A check mark
appears next to the command when it is on.

## Create a guide layer

For help in aligning objects when drawing, create guide layers and align objects
on other layers to the objects you create on the guide layers. Guide layers are
not exported and do not appear in a published SWF file. Any layer can be a guide
layer. Guide layers are indicated by a guide icon to the left of the layer name.

![](../img/dingbat.png) Select the layer and Right-click (Windows) or
Control-click (Macintosh) and select Guide from the context menu. To change the
layer back to a normal layer, select Guide again.

More Help topics

[About the main toolbar and edit bar](../workspace/using-the-stage-and-tools-panel.md#about-the-main-toolbar-and-edit-bar)

[Drawing preferences](./drawing-in-flash/drawing-preferences.md)
