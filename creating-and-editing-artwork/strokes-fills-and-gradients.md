# Strokes, fills, and gradients

## Create or edit a gradient fill

A gradient is a multicolor fill in which one color gradually changes into
another color. Flash Pro lets you apply up to 15 color transitions to a
gradient. Creating a gradient is a good way to create a smooth color gradation
across one or more objects. You can save a gradient as a swatch to make it easy
to apply the gradient to multiple objects. Flash Pro can create two types of
gradients:

_Linear gradients_ change color along a single axis (horizontal or vertical).

_Radial gradients_ change color in an outward direction starting from a central
focal point. You can adjust the direction of a gradient, its colors, the
location of the focal point, and many other properties of the gradient.

Adobe® Flash® Professional CS5 provides additional control over linear and
radial gradients for use with Flash Player. These controls, called overflow
modes, let you specify how colors are applied beyond the gradient.

For a sample of gradients, see the
[Flash Samples page](https://web.archive.org/web/20120102164641/http://www.adobe.com/devnet/flash/samples.html).
Download and decompress the Samples zip file and navigate to the
Graphics\AnimationAndGradients folder to access the sample.

1.  To apply a gradient fill to existing artwork, select an object or objects on
    the Stage.

2.  If the Color panel is not visible, select Window \> Color.

3.  To select a color display mode, select RGB (the default setting) or HSB from
    the panel menu.

4.  Select a gradient type from the Type menu:

    **Linear**  
    Creates a gradient that shades from the starting point to the end point in a
    straight line.

    **Radial**  
    Produces a gradient that blends outward in a circular path from a central
    focal point.

    > **Note:** When you select a linear or radial gradient, the Color panel
    > also includes two other options if you are publishing for Flash Player 8
    > or later. First, the Overflow menu is enabled below the Type menu. Use the
    > Overflow menu to control the colors applied past the limits of the
    > gradient. Second, the gradient definition bar appears, with pointers below
    > the bar indicating the colors in the gradient.

5.  (Optional) From the Overflow menu, select an overflow mode to apply to the
    gradient: Extend (the default mode), Reflect, or Repeat.

6.  (Optional) To create an SVG-compliant (Scalable Vector Graphics) linear or
    radial gradient, select the Linear RGB check box. This will allow the
    gradient to look smooth when scaled to different sizes after it is first
    applied.

7.  To change a color in the gradient, select one of the color pointers below
    the gradient definition bar (the triangle at the top of the selected color
    pointer will turn black). Then click in the color space pane that appears
    above the gradient bar. Drag the Brightness slider to adjust the lightness
    of the color.

8.  To add a pointer to the gradient, click on or below the gradient definition
    bar. Select a color for the new pointer, as described in the previous step.

    You can add up to 15 color pointers, letting you create a gradient with up
    to 15 color transitions.

9.  To reposition a pointer on the gradient, drag the pointer along the gradient
    definition bar. Drag a pointer down and off of the gradient definition bar
    to remove it.

10. To save the gradient, click the triangle in the upper-right corner of the
    Color panel, and select Add Swatch from the menu.

    The gradient is added to the Swatches panel for the current document.

11. To transform the gradient, such as to make a vertical gradient instead of a
    horizontal one, use the Gradient Transform tool. See
    [Transform gradient and bitmap fills](#transform-gradient-and-bitmap-fills)
    for more information.

## Adjust Stroke and Fill color

You can specify the stroke and fill color of graphic objects and shapes using
either the Stroke Color and Fill Color controls in the Tools panel, or the
Stroke Color and Fill Color controls in the Property inspector.

The Stroke Color and Fill Color section of the Tools panel contains controls for
activating the Stroke Color and Fill Color boxes, which in turn determine
whether the strokes or fills of selected objects are affected by color choices.
Also, the Colors section has controls for quickly resetting colors to the
default, setting the stroke and fill color settings to None, and swapping fill
and stroke colors.

In addition to letting you select a stroke and fill color for a graphic object
or shape, the Property inspector provides controls for specifying the stroke
width and style.

To use these controls to change the painting attributes of existing objects,
first select the objects on the Stage.

### Adjust stroke and fill color using the Tools panel

The Tools panel Stroke Color and Fill Color controls set the painting attributes
of new objects you create with the drawing and painting tools. To use these
controls to change the painting attributes of existing objects, first select the
objects on the Stage.

- Click the Stroke or Fill Color control, and select a color swatch.

- Click the System Color Picker button in the pop-up window, and select a color.

- Type a color's hexadecimal value in the box.

- To return to the default color settings (white fill and black stroke), click
  the Black And White button in the Tools panel.

- To remove any stroke or fill, click the No Color button.

  > **Note:** The No Color button appears only when you are creating an oval or
  > rectangle. You can create an object without a stroke or fill, but you cannot
  > use the No Color button with an existing object. Instead, select the
  > existing stroke or fill and delete it.

- To Swap colors between the fill and the stroke, click the Swap Colors button
  in the Tools panel.

### Apply a solid color fill using the Property inspector

1.  Select a closed object or objects on the Stage.
2.  Select Window \> Properties.
3.  To select a color, click the Fill Color control and do one of the following:
    - Select a color swatch from the palette.

    - Type a color's hexadecimal value in the box.

### Select a stroke color, style, and weight using the Property inspector

To change the stroke color, style, and weight for a selected object, use the
Stroke Color control in the Property inspector. For stroke style, choose from
styles that are preloaded with Flash Pro, or create a custom style. To select a
solid color fill, use the Fill Color control in the Property inspector.

1.  Select an object or objects on the Stage (for symbols, first double-click to
    enter symbol‑editing mode).

2.  Select Window \> Properties.

3.  To select a stroke style, click the Style menu and select an option. To
    create a custom style, click Custom in the Property inspector, select
    options in the Stroke Style dialog box, and click OK.

    > **Note:** Selecting a stroke style other than Solid can increase file
    > size.

4.  To select a stroke weight, set the Stroke slider or enter a value in the
    text box.

5.  To enable stroke hinting, select the Stroke Hinting check box. Stroke
    hinting adjusts line and curve anchors on full pixels, preventing blurry
    vertical or horizontal lines.

6.  To set the style for a path end, select a Cap option:

    **None**  
    Is flush with the path's end.

    **Round**  
    Adds a round cap that extends beyond the path end by half the stroke width.

    **Square**  
    Adds a square cap that extends beyond the path by half the stroke width.

7.  (Optional) If you are drawing lines using the Pencil or Brush tools with the
    drawing mode set to Smooth, use the Smoothing slider to specify the degree
    to which Flash Pro smooths the lines you draw.

    By default, the Smoothing value is set to 50, but you can specify a value
    from 0 to 100. The greater the smoothing value, the smoother the resulting
    line.

    > **Note:** When the drawing mode is set to Straighten or Ink, the Smoothing
    > slider is disabled.

8.  To define how two path segments meet, select a Join option. To change the
    corners in an open or closed path, select a path and select another join
    option.

    <p><i>Image Missing: dr_mtr_rnd_bvl_joins.png</i></p>

    <caption>Miter, round, and bevel joins.</caption>

9.  To avoid beveling a Miter join, enter a Miter limit.

    Line lengths exceeding this value are squared instead of pointed. For
    example, a Miter limit of 2 for a 3-point stroke means that when the length
    of the point is twice the stroke weight, Flash Pro removes the limit point.

    <p><i>Image Missing: dr_miter_bevel_joins.png</i></p>

    <caption>Applying a Miter limit.</caption>

### Adjust the strokes of multiple lines or shapes

To change the stroke color, width, and style of one or more lines or shape
outlines, use the Ink Bottle tool. You can apply only solid colors, not
gradients or bitmaps, to lines or shape outlines.

Using the Ink Bottle tool, rather than selecting individual lines, makes it
easier to change the stroke attributes of multiple objects at one time.

1.  Select the Ink Bottle tool from the Tools panel.
2.  Select a stroke color.
3.  Select a stroke style and stroke width from the Property inspector.
4.  To apply the stroke modifications, click an object on the Stage.

### Copy strokes and fills

Use the Eyedropper tool to copy fill and stroke attributes from one object and
immediately apply them to another object. The Eyedropper tool also lets you
sample the image in a bitmap to use as a fill.

1.  To apply the attributes of a stroke or filled area to another stroke or
    filled area, select the Eyedropper tool and click the stroke or filled area
    whose attributes you want to apply.

    When you click a stroke, the tool automatically changes to the Ink Bottle
    tool. When you click a filled area, the tool automatically changes to the
    Paint Bucket tool with the Lock Fill modifier turned on.

2.  Click another stroke or filled area to apply the new attributes.

## Modifying painted areas

The Paint Bucket tool fills enclosed areas with color. This tool lets you do the
following:

- Fill empty areas, and change the color of already painted areas.

- Paint with solid colors, gradients, and bitmap fills.

- Use the Paint Bucket tool to fill areas that are not entirely enclosed.

- Have Flash Pro close gaps in shape outlines as you use the Paint Bucket tool.

1.  Select the Paint Bucket tool from the Tools panel.
2.  Select a fill color and style.
3.  Click the Gap Size modifier that appears at the bottom of the Tools panel
    and select a gap size option:
    - Don't Close Gaps to close gaps manually before filling the shape. Closing
      gaps manually can be faster for complex drawings.

    - A Close option to have Flash Pro fill a shape that has gaps.

      > **Note:** If gaps are too large, you might have to close them manually.

4.  Click the shape or enclosed area to fill.

## Transform gradient and bitmap fills

You can transform a gradient or bitmap fill by adjusting the size, direction, or
center of the fill.

1.  Select the Gradient Transform tool <i>Image Missing:
    fill_transform_tool.png</i> from the Tools panel. If you do not see the
    Gradient Transform tool in the Tools panel, click and hold on the Free
    Transform tool and then select the Gradient Transform tool from the menu
    that appears.
2.  Click an area filled with a gradient or bitmap fill. A bounding box with
    editing handles appears. When the pointer is over any one of these handles,
    it changes to indicate the function of the handle.

    **Center point**  
    The rollover icon for the center point handle is a four-way arrow.

    **Focal point**  
    The focal point handle appears only when you select a radial gradient. The
    rollover icon for the focal point handle is an inverted triangle.

    **Size**  
    The rollover icon for the size handle (middle handle icon on the edge of the
    bounding box) is a circle with an arrow inside of it.

    **Rotation**  
    Adjusts the rotation of the gradient. The rollover icon for the rotation
    handle (the bottom handle icon on the edge of the bounding box) is four
    arrows in the shape of a circle.

    **Width**  
    Adjusts the width of the gradient. The rollover icon for the width handle
    (the square handle) is a double-ended arrow.

    <p><i>Image Missing: dr_fillTransform.png</i></p>

    Radial gradient controls

    A.  
    Center point

    B.  
    Width

    C.  
    Rotation

    D.  
    Size

    E.  
    Focal point.

    Press Shift to constrain the direction of a linear gradient fill to
    multiples of 45°.

3.  Reshape the gradient or fill in any of the following ways:
    - To reposition the center point of the gradient or bitmap fill, drag the
      center point.

      <p><i>Image missing: dr_04bmp_move.png</i></p>

      <caption>Four-way rollover icon on center point of color graphic.</caption>

    - To change the width of the gradient or bitmap fill, drag the square handle
      on the side of the bounding box. (This option resizes only the fill, not
      the object containing the fill.)

      <p><i>Image missing: dr_04bmp_width.png</i></p>

      <caption>Double-ended arrow indicates rollover icon to adjust gradient width.</caption>

    - To change the height of the gradient or bitmap fill, drag the square
      handle at the bottom of the bounding box.

      <p><i>Image missing: dr_04bmp_height.png</i></p>

      <caption>Double-ended arrow indicates rollover icon to adjust gradient height.</caption>

    - To rotate the gradient or bitmap fill, drag the circular rotation handle
      at the corner. You can also drag the lowest handle on the bounding circle
      of a circular gradient or fill.

      <p><i>Image missing: dr_04bmp_rotate.png</i></p>

      <caption>Drag circular rotation handle at the corner to rotate gradient or bitmap fill.</caption>

    - To scale a linear gradient or a fill, drag the square handle at the center
      of the bounding box.

      <p><i>Image missing: dr_04scale_linear.png</i></p>

      <caption>Square handle at center of bounding box.</caption>

    - To change the focal point of a circular gradient, drag the middle circular
      handle on the bounding circle.

      <p><i>Image missing: dr_04scale_radial.png</i></p>

      <caption>Middle circular handle on bounding circle.</caption>

    - To skew or slant a fill within a shape, drag one of the circular handles
      on the top or right side of the bounding box.

      <p><i>Image missing: dr_04bmp_skew.png</i></p>

      <caption>Circular handles on the top or right side of the bounding box.</caption>

    - To tile a bitmap inside a shape, scale the fill.

      <p><i>Image missing: dr_04bmp_tile.png</i></p>

      <caption>Handles for scaling fill.</caption>

      > **Note:** To see all the handles when working with large fills or fills
      > close to the edge of the Stage, select View \> Pasteboard.

## Lock a gradient or bitmap to fill the Stage

You can lock a gradient or bitmap fill to make it appear that the fill extends
over the entire Stage and that the objects painted with the fill are masks
revealing the underlying gradient or bitmap.

When you select the Lock Fill modifier with the Brush or Paint Bucket tool and
paint with the tool, the bitmap or gradient fill extends across the objects you
paint on the Stage.

<p><i>Image Missing: dr_04Lock_Fill_example.png</i></p>

Using the Lock Fill modifier creates the appearance of a single gradient or
bitmap fill being applied to separate objects on the Stage.

### Use a locked gradient fill

1.  Select the Brush or Paint Bucket tool and select a gradient or bitmap as a
    fill.
2.  Select Linear or Radial from the Type menu in the Color panel.
3.  Click the Lock Fill modifier <i>Image Missing: lockGradient.png</i>.
4.  First paint the areas where you want to place the center of the fill, and
    then move to other areas.

### Use a locked bitmap fill

1.  Select the bitmap to use.
2.  Select Bitmap from the Type menu in the Color panel.
3.  Select the Brush or Paint Bucket tool.
4.  Click the Lock Fill modifier <i>Image Missing: lockGradient.png</i>.
5.  First paint the areas where you want to place the center of the fill, and
    then move to other areas.

More Help topics

[Break apart groups and objects](./arranging-objects.md#break-apart-groups-and-objects)

[Work with imported bitmaps](../using-imported-artwork/imported-bitmaps-and-flash.md#work-with-imported-bitmaps)
