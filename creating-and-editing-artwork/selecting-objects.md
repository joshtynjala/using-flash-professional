# Selecting objects

To modify an object, select it first. Select objects with the Pointer,
Subselection, and Lasso tools. You can group individual objects to manipulate
them as a single object. Modifying lines and shapes can alter other lines and
shapes on the same layer. When you select objects or strokes, Flash highlights
them with a marquee.

You can choose to select only an object's strokes or only its fills. You can
hide selection highlighting to edit objects without viewing highlighting.

When you select an object, the Property inspector displays the following:

- The object's stroke and fill, its pixel dimensions, and the _x_ and _y_
  coordinates of the object's transformation point

- A mixed selection, if you select multiple items. The pixel dimensions and x
  and y coordinates of the selected set of items.

You can use a shape's Property inspector to change that object's stroke and
fill.

To prevent a group or symbol from being selected and accidentally changed, lock
the group or symbol.

## Select objects with the Selection tool

The Selection tool ![](../img/selection.png) lets you select entire objects by
clicking an object or dragging to enclose the object within a rectangular
selection marquee.

> **Note:** To select the Selection tool, you can also press the V key. To
> temporarily switch to the Selection tool when another tool is active, hold
> down the Control key (Windows) or Command key (Macintosh).

To disable the Shift-selecting option, deselect the option in Flash General
Preferences. See
[Set preferences in Flash](../workspace/set-preferences-in-flash.md). Instances,
groups, and type blocks must be completely enclosed to be selected.

- To select a stroke, fill, group, instance, or text block, click the object.
- To select connected lines, double-click one of the lines.
- To select a filled shape and its stroked outline, double-click the fill.
- To select objects within a rectangular area, drag a marquee around the object
  or objects to select.
- To add to a selection, hold down the Shift key while making additional
  selections.
- To select everything on every layer of a scene, select Edit \> Select All, or
  press Control+A (Windows) or Command+A (Macintosh). Select All doesn't select
  objects on locked or hidden layers, or layers not on the current Timeline.
- To deselect everything on every layer, select Edit \> Deselect All, or press
  Control+Shift+A (Windows) or Command+Shift+A (Macintosh).
- To select everything on one layer between keyframes, click a frame in the
  Timeline.
- To lock or unlock a group or symbol, select the group or symbol, and then
  select Modify \> Arrange \> Lock. Select Modify \> Arrange \> Unlock All to
  unlock all locked groups and symbols.

## Draw a freehand selection area

1.  Drag the Lasso tool ![](../img/lasso.png) around the area.

2.  End the loop approximately where you started, or let Flash automatically
    close the loop with a straight line.

## Draw a straight-edged selection area

1.  Select the Lasso tool's Polygon Mode modifier ![](../img/lassoPolygon.png)
    in the options area of the Tools panel.

2.  Click to set the starting point.
3.  Position the pointer where you want the first line to end, and click.
    Continue setting end points for additional line segments.
4.  To close the selection area, double-click.

## Draw a selection area with both freehand and straight-line edges

When you use the Lasso tool and its Polygon Mode modifier, you can switch
between the freehand and straight-edged selection modes.

1.  Deselect the Polygon Mode modifier of the Lasso tool.
2.  To draw a freehand segment, drag the Lasso tool on the Stage.
3.  To draw straight-edged segments, hold down the Alt key (Windows) or Option
    key (Macintosh) and click to set start and end points for each new line
    segment.
4.  To close the selection area, do one of the following:
    - Release the mouse button; Flash Pro will close the selection area for you.

    - Double-click on the starting end of the selection area line.

## Hide selection highlighting

Hiding highlighting while you are selecting and editing objects lets you see how
artwork appears in its final state.

![](../img/dingbat.png) Select View \> Hide Edges.

Select the command again to show selection highlighting.

## Set custom bounding box colors for selected objects

You can set different colors to be used for the bounding box rectangles that
appear around different kinds of selected objects on the Stage.

1.  Select Edit \> Preferences (Windows) or Flash \> Preferences (Macintosh).
2.  Click the General category.
3.  In the Highlight Color section, select a color for each type of object and
    click OK.

## Set preferences for selecting

The Pointer, Subselection, and Lasso tools select objects by clicking on them.
The Pointer and Subselection tools select objects by dragging a rectangular
selection marquee around the object. The Lasso tool selects objects by dragging
a free-form selection marquee around the object. When an object is selected, a
rectangular box appears around the object.

1.  Select Edit \> Preferences (Windows) or Flash \> Preferences (Macintosh).
2.  In the General category of the Preferences dialog box, do one of the
    following:
    - To select only objects and points that are completely enclosed by the
      selection marquee, deselect Contact-Sensitive Selection and Lasso tools.
      Points that lie within the selection area will still be selected.

    - To select objects or groups that are only partially enclosed by the
      selection marquee, select Contact-Sensitive Selection and Lasso tools.

More Help topics

[Creating and Editing Artwork](./index.md#creating-and-editing-artwork)

[Color](./color.md)

[Group objects](./arranging-objects.md#group-objects)

[About symbols](../symbols-instances-and-library-assets/working-with-symbols.md#about-symbols)
