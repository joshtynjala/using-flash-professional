# Draw simple lines and shapes

## Draw straight lines with the Line Segment tool

To draw one straight line segment at a time, use the Line tool.

1.  Select the Line tool <i>Image Missing: P_Line_Lg_N.png</i>.
2.  Select Window \> Properties and select stroke attributes.

    > **Note:** You cannot set fill attributes for the Line tool.

3.  Click the Object Drawing button <i>Image Missing: objectDrawButton.png</i>
    in the Options section of the Tools panel to select either Merge or Object
    Drawing mode. When the Object Drawing button is depressed, the Line tool is
    in Object Drawing mode.
4.  Position the pointer where the line is to begin, and drag to where the line
    is to end. To constrain the angle of the line to multiples of 45°,
    Shift-drag.

## Draw rectangles and ovals

The Oval and Rectangle tools let you create these basic geometric shapes, and
apply strokes, fills, and specify rounded corners. In addition to the Merge and
Object drawing modes, the Oval and Rectangle tools also provide the Primitive
Object drawing mode.

When you create rectangles or ovals using the Rectangle Primitive or Oval
Primitive tools, Flash draws the shapes as separate objects not unlike the
shapes you create using Object Drawing mode. The primitive shape tools let you
specify the corner radius of rectangles, and the start and end angle and the
inner radius of ovals using controls in the Property inspector. After you create
a primitive shape, alter the radius and dimensions by selecting the shape on the
Stage and adjusting the controls in the Property inspector.

> **Note:** When either of the Primitive Object drawing tools is selected, the
> Property inspector retains the values of the last primitive object that you
> edited. For example, if you modify a rectangle and then draw a second
> rectangle.

### Draw rectangle primitives

1.  To select the Rectangle Primitive tool, click and hold the mouse button on
    the Rectangle tool <i>Image Missing: rectagle.png</i>, and select the
    Rectangle Primitive tool <i>Image Missing: rectangle_primitive.png</i> from
    the pop-up menu.

2.  To create a rectangle primitive, drag with the Rectangle Primitive tool on
    the Stage.

    > **Note:** To change the corner radius while dragging with the Rectangle
    > primitive tool, press the Up Arrow key or Down Arrow key. When the corners
    > achieve the desired roundness, release the key.

3.  With the rectangle primitive selected, you can use the controls in the
    Property inspector to further modify the shape or specify fill and stroke
    colors.

    <p><i>Image Missing: dr_PrimRecPI.png</i></p>

    <caption>Properties for a rectangle primitive.</caption>

    Theses Property inspector controls are specific to the Rectangle Primitive
    tool:

    **Rectangle Corner Radius Controls** Let you specify the corner radiuses for
    the rectangle. You can enter a numeric value for the inner radius in each
    text box. Entering a negative value creates an inverse radius. You can also
    deselect the constrain corner radius icon, and adjust each corner radius
    individually.

    **Reset** Resets all of the Rectangle Primitive tool controls, and restores
    the rectangle primitive shape drawn on the Stage to its initial size and
    shape.

4.  To specify a different corner radius for each corner, deselect the Lock icon
    in the Rectangle Options area of the Property inspector. When locked, the
    radius controls are restrained so that each corner uses the same radius.

5.  To reset the corner radii, click the Reset button in the Property inspector.

### Draw oval primitives

1.  Click and hold the mouse button on the Rectangle tool <i>Image Missing:
    rectagle.png</i>, and select the Oval Primitive tool <i>Image Missing:
    oval_primitive.png</i>.

2.  To create an oval primitive, drag the Primitive Oval tool on the Stage. To
    constrain the shape to a circle, Shift-drag.

3.  With the oval primitive selected on the Stage, you can use the controls
    found in the Property inspector to further modify the shape or specify fill
    and stroke colors.

    <p><i>Image Missing: dr_PrimOvalPI.png</i></p>

    <caption>Properties for an oval primitive.</caption>

    These Property inspector controls are specific to the Oval Primitive tool:

    **Start Angle**/**End Angle** The angle of the start point and end point of
    the oval. Using these controls, you can easily modify the shape of ovals and
    circles into pie slices, half circles, and other creative shapes.

    **Inner Radius** An inner radius (or oval) within the oval. You can either
    enter a numeric value for the inner radius in the box or click the slider
    and interactively adjust the size of the inner radius. You can enter values
    from 0 to 99 representing the percentage of fill that is removed.

    **Close Path** Determines whether the path (or paths, if you are specifying
    an inner radius) of the oval is closed. If you specify an open path, no fill
    is applied to the resulting shape, only the stroke is drawn. Close Path is
    selected by default.

    **Reset** Resets all of the Oval Primitive tool controls and restores the
    oval primitive shape drawn on the Stage to its initial size and shape.

### Draw ovals and rectangles

The Oval and Rectangle tools create these basic geometric shapes.

1.  To select the Rectangle tool <i>Image Missing: rectagle.png</i> or Oval
    tool <i>Image Missing: ellipse.png</i>, click and hold the mouse button on
    the Rectangle tool and drag.

2.  To create a rectangle or oval, drag the Rectangle or Oval tool on the Stage.

3.  For the Rectangle tool, specify rounded corners by clicking the Round
    Rectangle modifier and entering a corner radius value. A value of zero (0)
    creates square corners.

4.  Drag on the Stage. If you are using the Rectangle tool, press the Up Arrow
    and Down Arrow keys while dragging to adjust the radius of rounded corners.

    For the Oval and Rectangle tools, Shift-drag to constrain the shapes to
    circles and squares.

5.  To specify a specific size of oval or rectangle, select the Oval or
    Rectangle tool and press the Alt key (Windows) or Option key (Macintosh).
    Then click the Stage to display the Oval And Rectangle Settings dialog box.
    - For ovals, specify the width and height in pixels and whether to draw the
      oval from the center.

    - For rectangles, specify the width and height in pixels, the radius of the
      rounded corners, and whether to draw the rectangle from the center.

## Draw polygons and stars

1.  Select the PolyStar tool <i>Image Missing: polystar.png</i> by clicking and
    holding the mouse button on the Rectangle tool and selecting from the pop-up
    menu that appears.
2.  Select Window \> Properties and select fill and stroke attributes.
3.  Click Options and do the following:
    - For Style, select Polygon or Star.

    - For Number Of Sides, enter a number from 3 through 32.

    - For Star Point Size, enter a number from 0 through 1 to specify the depth
      of the star points. A number closer to 0 creates deeper points (like
      needles). If you are drawing a polygon, leave this setting unchanged. (It
      does not affect the polygon shape.)

4.  Click OK.
5.  Drag on the Stage.

## Draw with the Pencil tool

To draw lines and shapes, use the Pencil tool, in much the same way that you use
a real pencil to draw. To apply smoothing or straightening to the lines and
shapes as you draw, select a drawing mode for the Pencil tool.

1.  Select the Pencil tool <i>Image Missing: P_Draw_Lg_N.png</i>.
2.  Select Window \> Properties and select a stroke color, line weight, and
    style.
3.  Select a drawing mode under Options in the Tools panel:
    - To draw straight lines and convert approximations of triangles, ovals,
      circles, rectangles, and squares into these common geometric shapes,
      select Straighten <i>Image Missing: pencil_straighten.png</i>.

    - To draw smooth curved lines, select Smooth <i>Image Missing:
      pencil_smooth.png</i>.

    - To draw freehand lines with no modification applied, select Ink <i>Image
      Missing: pencil_ink.png</i>.

      <p><i>Image Missing: dr_03pencil_mode.png</i></p>

      <caption>Lines drawn with Straighten, Smooth, and Ink mode, respectively.</caption>

4.  To draw with the Pencil tool, Shift-drag to constrain lines to vertical or
    horizontal directions, click the Stage, and drag.

## Paint with the Brush tool

The Brush tool <i>Image Missing: P_Brush_Lg_N.png</i> draws brush-like strokes.
It creates special effects, including calligraphic effects. Select a brush size
and shape using the Brush tool modifiers.

Brush size for new strokes remains constant even when you change the
magnification level for the Stage, so the same brush size appears larger when
the Stage magnification is lower. For example, suppose you set the Stage
magnification to 100% and paint with the Brush tool using the smallest brush
size. Then, you change the magnification to 50% and paint again using the
smallest brush size. The new stroke that you paint appears 50% thicker than the
earlier stroke. (Changing the magnification of the Stage does not change the
size of existing brush strokes.)

Use an imported bitmap as a fill when painting with the Brush tool. See
[Break apart groups and objects](../arranging-objects.md#break-apart-groups-and-objects).

If you have a Wacom pressure-sensitive tablet connected to your computer, vary
the width and angle of the brush stroke by using the Brush tool Pressure and
Tilt modifiers, and varying pressure on the stylus.

The Pressure modifier varies the width of brush strokes when you vary the
pressure on the stylus. The Tilt modifier varies the angle of brush strokes when
you vary the angle of the stylus on the tablet. The Tilt modifier measures the
angle between the top (eraser) end of the stylus and the top (north) edge of the
tablet. For example, if you hold the pen vertically against the tablet, the Tilt
is 90. The Pressure and Tilt modifiers are both fully supported for the eraser
function of the stylus.

<p><i>Image Missing: dr_pressure_stroke.png</i></p>

<caption>A variable-width brush stroke drawn with a stylus.</caption>

1.  Select the Brush tool <i>Image Missing: P_Brush_Lg_N.png</i>.
2.  Select Window \> Properties and select a fill color.
3.  Click the Brush Mode modifier and select a painting mode:

    **Paint Normal**  
    Paints over lines and fills on the same layer.

    **Paint Fills**  
    Paints fills and empty areas, leaving lines unaffected.

    **Paint Behind**  
    Paints in blank areas of the Stage on the same layer, leaving lines and
    fills unaffected.

    **Paint Selection**  
    Applies a new fill to the selection when you select a fill in the Fill Color
    control or the Fill box of the Property inspector, the same as selecting a
    filled area and applying a new fill.

    **Paint Inside**  
    Paints the fill in which you start a brush stroke and never paints lines. If
    you start painting in an empty area, the fill doesn't affect any existing
    filled areas.

4.  Select a brush size and brush shape from the Brush tool modifiers.
5.  If a Wacom pressure-sensitive tablet is attached to your computer, select
    the Pressure modifier, the Tilt modifier, or both, to modify brush strokes.
    - Select the Pressure modifier to vary the width of your brush strokes by
      varying the pressure on your stylus.

    - To vary the angle of your brush strokes by varying the angle of the stylus
      on the Wacom pressure-sensitive tablet, select the Tilt modifier.

6.  Drag on the Stage. To constrain brush strokes to horizontal and vertical
    directions, Shift-drag.

More Help topics

[Adjust Stroke and Fill color](../strokes-fills-and-gradients.md#adjust-stroke-and-fill-color)

[Drawing modes and graphic objects](./drawing-modes-and-graphic-objects.md)
