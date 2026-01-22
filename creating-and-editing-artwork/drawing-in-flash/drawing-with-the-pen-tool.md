# Drawing with the Pen tool

To draw precise paths as straight lines or smooth, flowing curves, use the Pen
tool. When you draw with the Pen tool, click to create points on straight line
segments and drag to create points on curved line segments. Adjust straight and
curved line segments by adjusting points on the line.

## Pen tool drawing states

The Pen tool provides feedback about its current drawing state by displaying
different pointers. The various drawing states are indicated by the following
pointers:

Initial Anchor Point pointer <i>Image Missing: penx.png</i>  
The first pointer you see when you select the Pen tool. Indicates that the next
mouse click on the Stage will create an initial anchor point, which is the
beginning of a new path (all new paths begin with an initial anchor point). Any
existing drawing paths are terminated.

Sequential Anchor Point pointer <i>Image Missing: penplain.png</i>  
Indicates that the next mouse click will create an anchor point with a line
connecting it to the previous anchor point. This pointer is displayed during the
creation of all user-defined anchor points except the initial anchor point of a
path.

Add Anchor Point pointer <i>Image Missing: penplus.png</i>  
Indicates that the next mouse click will add an anchor point to an existing
path. To add an anchor point, the path must be selected, and the Pen tool must
not be over an existing anchor point. The existing path is redrawn based on the
additional anchor point. Only one anchor point can be added at a time.

Delete Anchor Point pointer <i>Image Missing: penminus.png</i>  
Indicates that the next mouse click on an existing path will remove an anchor
point. To remove an anchor point, the path must be selected with the Selection
tool, and the pointer must be over an existing anchor point. The existing path
is redrawn based on the removal of the anchor point. Only one anchor point can
be removed at a time.

Continue Path pointer  <i>Image Missing: penslash.png</i>  
Extends a new path from an existing anchor point. For this pointer to be
activated, the mouse must be over an existing anchor point on a path. This
pointer is only available when you are not currently drawing a path. The anchor
point does not have to be one of the terminal anchor points of a path; any
anchor point can be the location of a continued path.

Close Path pointer <i>Image Missing: penclose.png</i>  
Closes the path you're drawing on the starting point of the path. You can only
close a path that you are currently drawing, and the existing anchor point must
be the starting anchor point of the same path. The resulting path does not have
any specified fill color settings applied to the enclosed shape; apply fill
color separately.

Join Paths pointer <i>Image Missing: penclose2.png</i>  
Similar to the Close Path Tool except that the mouse must not be over the
initial anchor point of the same path. The pointer must be over either of the
terminal points of a unique path. The segment may or may not be selected.

> **Note:** Joining paths may or may not result in a closed shape. Retract
> Bezier Handle pointer <i>Image Missing: penconvrt.png</i>  
> Appears when the mouse is over an anchor point whose Bezier handles are
> displayed. Clicking the mouse retracts the Bezier handles and causes the
> curved path across the anchor point to revert to straight segments.

Convert Anchor Point pointer <i>Image Missing: convdrpt.png</i>  
Converts a corner point without direction lines to a corner point with
independent direction lines. To enable the Convert Anchor Point pointer, use the
Shift + C modifier keys to toggle the Pen tool.

## Draw straight lines with the Pen tool

The simplest path you can draw with the Pen tool is a straight line, made by
clicking the Pen tool to create two anchor points. Continue to click to create a
path made of straight line segments connected by corner points.

1.  Select the Pen tool <i>Image Missing: pen.png</i>.
2.  Position the Pen tool where the straight segment is to begin, and click to
    define the first anchor point. If direction lines appear, you accidentally
    dragged the Pen tool; choose Edit \> Undo and click again.

    > **Note:** The first segment you draw is not visible until you click a
    > second anchor point (unless you've specified Show Pen Preview in the
    > Drawing category of the Preferences dialog box).

3.  Click again where you want the segment to end (Shift-click to constrain the
    angle of the segment to a multiple of 45°).
4.  Continue clicking to set anchor points for additional straight segments.

    <p><i>Image Missing: dr_01.png</i></p>

    <caption>Clicking Pen tool creates straight segments.</caption>

5.  To complete the path as an open or closed shape, do one of the following:
    - To complete an open path, double-click the last point, click the Pen tool
      in the Tools panel, or Control-click (Windows) or Command-click
      (Macintosh) anywhere away from the path.

    - To close the path, position the Pen tool over the first (hollow) anchor
      point. A small circle appears next to the Pen <i>Image Missing:
      penclose.png</i> tool pointer when it is positioned correctly. Click or
      drag to close the path.

    - To complete the shape as is, select Edit \> Deselect All, or select a
      different tool in the Tools panel.

## Draw curves with the Pen tool

To create a curve, add an anchor point where a curve changes direction and drag
the direction lines that shape the curve. The length and slope of the direction
lines determine the shape of the curve.

Curves are easier to edit and your system can display and print them faster if
you draw them using as few anchor points as possible. Using too many points can
also introduce unwanted bumps in a curve. Instead, draw widely spaced anchor
points, and practice shaping curves by adjusting the length and angles of the
direction lines.

1.  Select the Pen tool <i>Image Missing: pen.png</i>.

2.  Position the Pen tool where the curve is to begin, and hold down the mouse
    button.

    The first anchor point appears, and the Pen tool pointer changes to an
    arrowhead. (In Photoshop, the pointer changes only after you've started
    dragging.)

3.  Drag to set the slope of the curve segment you're creating, and then release
    the mouse button.

    In general, extend the direction line about one third of the distance to the
    next anchor point you plan to draw. (You can adjust one or both sides of the
    direction line later.)

    Hold down the Shift key to constrain the tool to multiples of 45°.

    <p><i>Image Missing: dr_13.png</i></p>

    <caption>Drawing the first point in a curve</caption>

    A.  
    Positioning Pen tool

    B.  
    Starting to drag (mouse button pressed)

    C.  
    Dragging to extend direction lines.

4.  Position the Pen tool where the curve segment is to end, and do one of the
    following:
    - To create a C-shaped curve, drag in a direction opposite to the previous
      direction line and release the mouse button.

      <p><i>Image Missing: dr_14.png</i></p>

      <caption>Drawing the second point in a curve</caption>

      A.  
      Starting to drag second smooth point

      B.  
      Dragging away from previous direction line, creating a C curve

      C.  
      Result after releasing mouse button.

    - To create an S-shaped curve, drag in the same direction as the previous
      direction line and release the mouse button.

      <p><i>Image Missing: dr_15.png</i></p>

      <caption>Drawing an S curve</caption>

      A.  
      Starting to drag new smooth point

      B.  
      Dragging in the same direction as previous direction line, creating an S
      curve

      C.  
      Result after releasing mouse button.

5.  To create a series of smooth curves, continue dragging the Pen tool from
    different locations. Place anchor points at the beginning and end of each
    curve, not at the tip of the curve.

    > ![](../../img/tip_help.png) To break out the direction lines of an anchor
    > point, Alt-drag (Windows) or Option-drag (Macintosh) direction lines.

6.  To complete the path, do one of the following:
    - To close the path, position the Pen tool over the first (hollow) anchor
      point. A small circle appears next to the Pen tool pointer <i>Image
      Missing: penclose.png</i> when it is positioned correctly. Click or drag
      to close the path.

    - To leave the path open, Ctrl-click (Windows) or Command-click (Macintosh)
      anywhere away from all objects, select a different tool, or choose Edit \>
      Deselect All.

## Add or delete anchor points

Adding anchor points can give you more control over a path or it can extend an
open path. However, it's a good idea not to add more points than necessary. A
path with fewer points is easier to edit, display, and print. To reduce the
complexity of a path, delete unnecessary points.

The toolbox contains three tools for adding or deleting points: the Pen
tool <i>Image Missing: pen.png</i>, the Add Anchor Point tool <i>Image Missing:
P_AnchorAdd_Lg_N.png</i>, and the Delete Anchor Point tool <i>Image Missing:
P_AnchorDel_Lg_N.png</i>.

By default, the Pen tool changes to the Add Anchor Point tool as you position it
over a selected path, or to the Delete Anchor Point tool as you position it over
an anchor point.

> **Note:** Don't use the Delete, Backspace, and Clear keys or the Edit \> Cut
> or Edit \> Clear commands to delete anchor points; these keys and commands
> delete the point and the line segments that connect to that point.

1.  Select the path to modify.
2.  Click and hold the mouse button on the Pen tool <i>Image Missing:
    pen.png</i>, then select the Pen tool <i>Image Missing: pen.png</i>, Add
    Anchor Point tool <i>Image Missing: P_AnchorAdd_Lg_N.png</i>, or the Delete
    Anchor Point tool <i>Image Missing: P_AnchorDel_Lg_N.png</i>.
3.  To add an anchor point, position the pointer over a path segment, and click.
    To delete an anchor point, position the pointer over an anchor point, and
    click.

## Adjust anchor points on paths

When you draw a curve with the Pen tool, you create smooth points—anchor points
on a continuous, curved path. When you draw a straight line segment or a
straight line connected to a curved segment, you create corner points—anchor
points on a straight path or at the juncture of a straight and a curved path.

By default, selected smooth points appear as hollow circles, and selected corner
points appear as hollow squares.

<p><i>Image Missing: dr_22.png</i></p>

<caption>Dragging a direction point out of a corner point to create a smooth point.</caption>

### Move or add anchor points

- To move an anchor point, drag the point with the Subselection
  tool ![](../../img/diretsl.png).

- To nudge an anchor point or points, select the point or points with the
  Subselection tool and use the arrow keys to move the point or points.
  Shift-click to select multiple points.

- To add an anchor point, click a line segment with the Pen tool. A plus (+)
  sign appears next to the Pen tool <i>Image Missing: penplus.png</i> if an
  anchor point can be added to the selected line segment. If the line segment is
  not yet selected, click it with the Pen tool to select it, and then add an
  anchor point.

### Delete anchor points

Deleting unneeded anchor points on a curved path optimizes the curve and reduces
the resulting SWF file size.

- To delete a corner point, click the point once with the Pen tool. A minus (-)
  sign appears next to the Pen tool if an anchor point can be deleted from the
  selected line segment. If the line segment is not yet selected, click it with
  the Pen tool to select it, and then delete the anchor point.

- To delete a smooth point, click the point once with the Pen tool. A minus (-)
  sign appears next to the Pen tool if an anchor point can be deleted from the
  selected line segment. If the line segment is not yet selected, click it with
  the Pen tool to select it, and then delete the corner point. (Click once to
  convert the point to a corner point, and once more to delete the point.)

### Convert segments between straight and curved

To convert segments in a line from straight segments to curve segments, convert
corner points to smooth points. You can also do the reverse.

- To convert a corner point to a smooth point, use the Subselection tool to
  select the point, then Alt‑drag (Windows) or Option-drag (Macintosh) the point
  to place the tangent handles.

- To convert a smooth point to a corner point, click the point with the Pen
  tool. The carat ^ marker next to the pointer <i>Image Missing:
  penconvrt.png</i> indicates when it is over the smooth point.

## Adjust segments

To change the angle or length of the segment or adjust curved segments to change
the slope or direction of the curve, adjust straight segments. When you move a
tangent handle on a smooth point, the curves on both sides of the point adjust.
When you move a tangent handle on a corner point, only the curve on the same
side of the point as the tangent handle adjusts.

- To adjust a straight segment, select the Subselection
  tool ![](../../img/diretsl.png), and select a straight segment. Use the
  Subselection tool to drag an anchor point on the segment to a new position.

- To adjust a curve segment, select the Subselection tool and drag the segment.

  > **Note:** When you click the path, Flash Pro shows the anchor points.
  > Adjusting a segment with the Subselection tool can add points to the path.

- To adjust points or tangent handles on a curve, select the Subselection tool,
  and select an anchor point on a curved segment.

- To adjust the shape of the curve on either side of the anchor point, drag the
  anchor point, or drag the tangent handle. To constrain the curve to multiples
  of 45º, Shift-drag. To drag tangent handles individually, Alt‑drag (Windows)
  or Option-drag (Macintosh).

<p><i>Image Missing: dr_16.png</i></p>

<caption>Drag the anchor point, or drag the direction point.</caption>

## Pen tool preferences

Specify preferences for the appearance of the Pen tool pointer, for previewing
line segments as you draw, and for the appearance of selected anchor points.
Selected line segments and anchor points use the outline color of the layer on
which the lines and points appear.

1.  Select the Pen tool <i>Image Missing: pen.png</i>, then select Edit \>
    Preferences (Windows) or Flash \> Preferences (Macintosh).
2.  In the Category list, select Drawing.
3.  Set the following options for the Pen tool:

    **Show Pen Preview**  
    Previews line segments as you draw. A preview of the line segment appears as
    you move the pointer around the Stage, before you click to create the end
    point of the segment. If this option is not selected, a line segment does
    not appear until you create the end point.

    **Show Solid Points**  
    Displays selected anchor points as hollow and deselected anchor points as
    solid. If this option is not chosen, selected anchor points are solid, and
    deselected anchor points are hollow.

    **Show Precise Cursors**  
    Specifies that the Pen tool pointer appears as a cross-hair pointer rather
    than the default Pen tool icon, for more precise placement of lines. To
    display the default Pen tool icon with the Pen tool, deselect the option.

    > **Note:** To switch between the cross-hair pointer and the default Pen
    > tool icon, press Caps Lock.

4.  Click OK.

More Help topics

[Reshape lines and shapes](../reshape-lines-and-shapes.md)

[Adjust Stroke and Fill color](../strokes-fills-and-gradients.md#adjust-stroke-and-fill-color)
