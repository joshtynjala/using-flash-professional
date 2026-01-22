# Arranging objects

## Stack objects

In a layer, Flash stacks objects in the order in which they are created, placing
the most recently created object at the top of the stack. The stacking order of
objects determines how they appear when they overlap. You can change the
stacking order of objects at any time.

Drawn lines and shapes always appear below groups and symbols on the stack. To
move them up the stack, you must group them or make them into symbols.

Layers also affect the stacking order. Everything on Layer 2 appears in front of
everything on Layer 1, and so on. To change the order of layers, drag the layer
name in the Timeline to a new position.

1.  Select the object.
2.  Do one of the following:
    - Select Modify \> Arrange \> Bring To Front Or Send To Back to move the
      object or group to the top or bottom of the stacking order.

    - Select Modify \> Arrange \> Bring Forward Or Send Backward to move the
      object or group forward or backward one position in the stacking order.

    If more than one group is selected, the groups move in front of or behind
    all unselected groups, while maintaining their order relative to each other.

## Align objects

The Align panel lets you align selected objects along the horizontal or vertical
axis. You can align objects vertically along the right edge, center, or left
edge of the selected objects, or horizontally along the top edge, center, or
bottom edge of the selected objects.

1.  Select the objects to align.
2.  Select Window \> Align.
3.  To apply alignment modifications relative to Stage dimensions, in the Align
    panel, select To Stage.
4.  To modify the selected object(s), select the alignment buttons.

## Group objects

To manipulate elements as a single object, group them. For example, after
creating a drawing, you might group the elements of the drawing so that you can
easily select and move the drawing as a whole.

When you select a group, the Property inspector displays the _x_ and _y_
coordinates of the group and its pixel dimensions.

You can edit groups without ungrouping them. You can also select an individual
object in a group for editing without ungrouping the objects.

![](../img/dingbat.png) Select the objects to group. You can select shapes,
other groups, symbols, text, and so on.

- To group objects, select Modify \> Group, or press Control+G (Windows) or
  Command+G (Macintosh).

- To ungroup objects, select Modify \> Ungroup, or press Control+Shift+G
  (Windows) or Command+Shift+G (Macintosh).

## Edit a group or an object within a group

1.  Select the group, and then select Edit \> Edit Selected, or double-click the
    group with the Selection tool.

    Everything on the page that is not part of the group is dimmed, indicating
    that elements outside the group are inaccessible.

2.  Edit any element within the group.

3.  Select Edit \> Edit All, or double-click a blank spot on the Stage with the
    Selection tool.

    Flash restores the group to its status as a single entity, and you can work
    with other elements on the Stage.

## Break apart groups and objects

To separate groups, instances, and bitmaps into ungrouped, editable elements,
you break them apart, which significantly reduces the file size of imported
graphics.

Although you can select Edit \> Undo immediately after breaking apart a group or
object, breaking apart is not entirely reversible. It affects objects as
follows:

- Severs a symbol instance's link to its master symbol

- Discards all but the current frame in an animated symbol

- Converts a bitmap to a fill

- Places each character into a separate text block when applied to text blocks

- Converts characters to outlines when applied to a single text character.

  Do not confuse the Break Apart command with the Ungroup command. The Ungroup
  command separates grouped objects, returning grouped elements to the state
  they were in before grouping. It does not break apart bitmaps, instances, or
  type, or convert type to outlines.

1.  Select the group, bitmap, or symbol to break apart.
2.  Select Modify \> Break Apart.

> **Note:** Breaking apart animated symbols, or groups in an interpolated
> animation is not recommended and might have unpredictable results. Breaking
> apart complex symbols and large blocks of text can take a long time. You might
> need to increase the application's memory allocation to properly break apart
> complex objects.

More Help topics

[Create and organize layers](../timelines-and-animation/timeline-layers.md#create-and-organize-layers)
