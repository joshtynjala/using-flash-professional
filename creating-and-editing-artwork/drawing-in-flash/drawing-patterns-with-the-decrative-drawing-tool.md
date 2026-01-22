# Drawing patterns with the Decorative drawing tool

The Decorative drawing tool lets you create complex, geometric shapes and
patterns. The Decorative drawing tools use algorithmic calculations—known as
_procedural drawing_.

**Tutorials**

- Jonathan Duran has provided an in-depth article entitled Using the Deco tool
  and Spray Brush for creating complex, geometric patterns in Flash at
  [ Deco tool and Spray Brush for creating complex, geometric patterns in Flash](https://web.archive.org/web/20111108230903mp_/http://www.adobe.com/devnet/flash/articles/deco_intro.html).

## Apply the Symmetry Brush effect

Use the Symmetry Brush effect to arrange symbols symmetrically around a central
point. When you draw the symbols on the Stage, a set of handles appears. Use the
handles to control the symmetry by increasing the number of symbols, adding
symmetries, or editing and modifying the effect.

Use the Symmetry Brush effect to create circular user interface elements (such
as an analog clock face or dial gauge) and swirl patterns. The default symbol
for the Symmetry Brush effect is a black rectangle shape with no stroke that is
25 x 25 pixels.

1.  Select the Deco Drawing tool, and select Symmetry Brush from the Drawing
    Effect menu in the Property inspector.

2.  In the Deco Drawing tool Property inspector, select a fill color to use for
    the default rectangle shape. Or, click Edit to select a custom symbol from
    the library.

    You can use any movie clip or graphic symbol in the library with the
    Symmetry Brush effect. These symbol-based particles give you a great deal of
    creative control over artwork you create.

3.  The Symmetry Brush advanced options appear in the Property inspector when
    you select Symmetry Brush from the Drawing Effect pop-up menu in the
    Property inspector.

    **Rotate Around**  
    Rotates the shapes in the symmetry around a fixed point that you designate.
    The default reference point is the center point of the symmetry. To rotate
    the object around its center point, drag in a circular motion.

    **Reflect Across Line**  
    Flips the shapes an equal distance apart across an invisible line that you
    specify.

    **Reflect Around Point**  
    Places two shapes an equal distance apart around a fixed point that you
    specify.

    **Grid Translation**  
    Creates a grid using the shapes in the Symmetry effect you are drawing. Each
    click of the Deco Drawing tool on the Stage creates a grid of shapes. Adjust
    the height and width of the shapes using the x and y coordinates defined by
    the Symmetry Brush handles.

    **Test Collisions**  
    Prevents shapes in the Symmetry effect you are drawing from colliding with
    one another, regardless of how you increase the number of instances within
    the Symmetry effect. Deselect this option to overlap the shapes in the
    Symmetry effect.

4.  Click the Stage where you want the Symmetry Brush artwork to appear.

5.  Use the Symmetry Brush handles to adjust the size of the symmetry and the
    number of symbol instances.

## Apply the Grid Fill effect

The Grid Fill effect lets you fill the Stage, a symbol, or closed region with a
symbol from the library. After the Grid Fill is drawn to the Stage, if the
filled symbol is moved or resized, the Grid Fill will move or resize
accordingly.

Use the Grid Fill effect to create a checkerboard, a tiled background, or area
or shape with a custom pattern. The default symbol for the Symmetry effect is a
black rectangle shape with no stroke that is 25 x 25 pixels.

1.  Select the Deco Drawing tool, and select Grid Fill from the Drawing Effect
    menu in the Property inspector.

2.  In the Property inspector, select a fill color for the default rectangle
    shape. Or click Edit to select a custom symbol from the library.

    You can use up to 4 movie clip or graphic symbols in the library with the
    Grid Fill effect. The symbols alternate as Flash fills the grid.

3.  Choose a Layout for the grid fill. There are 3 options for Layout.

    **Tile Pattern**  
    The symbols are arranged in a simple grid pattern.

    **Brick Pattern**  
    The symbols are arranged in a horizontally offset grid pattern.

    **Floor Pattern**  
    The symbols are arranged in a horizontally and vertically offset grid
    pattern.

4.  To allow the fill to overlap the edge of the containing symbol, shape, or
    the Stage, select the Paint Over Edge option.

5.  To allow the symbols to be distributed randomly within the grid, select the
    Random Order option.

6.  You can specify the horizontal and vertical spacing and the scale of the
    fill shape. Once the Grid Fill effect is applied, you cannot change the
    advanced options in the Property inspector afterwards to alter the fill
    pattern.

    **Horizontal spacing**  
    Specifies the horizontal distance in pixels between symbols used in the Grid
    Fill.

    **Vertical spacing**  
    Specifies the vertical distance in pixels between symbols used in the Grid
    Fill.

    **Pattern scale**  
    Enlarges or shrinks the symbols horizontally (along the x axis), and
    vertically (along the y axis).

7.  Click the Stage or within the shape or symbol where you want the Grid Fill
    pattern to appear.

## Apply the Vine Fill effect

The Vine Fill effect lets you fill the Stage, a symbol, or closed region with a
vine pattern. You can substitute your own artwork for the leaves and flowers by
selecting symbols from the library. The resulting pattern is contained in a
movie clip that itself contains the symbols that make up the pattern.

1.  Select the Deco Drawing tool, and select Vine Fill from the Drawing Effect
    menu in the Property inspector.

2.  In the Deco Drawing tool Property inspector, select a fill color for the
    default flower and leaf shapes. Or, click Edit to select a custom symbol
    from the library to replace one or both of the default flower and leaf
    symbols.

    You can use any movie clip or graphic symbol in the library to replace the
    default flower and leaf symbols with the Vine Fill effect.

3.  You can specify the horizontal and vertical spacing and the scale of the
    fill shape. After you apply the Vine Fill effect, you cannot change the
    advanced options in the Property inspector afterward to alter the fill
    pattern.

    **Branch angle**  
    Specifies the angle of the branch pattern.

    **Branch color**  
    Specifies the color to use for the branch.

    **Pattern scale**  
    Scaling an object enlarges or reduces it both horizontally (along the x
    axis), and vertically (along the y axis).

    **Segment length**  
    Specifies the length of the segments between leaf and flower nodes.

    **Animate pattern**  
    Specifies that each iteration of the effect is drawn to a new frame in the
    timeline. This option creates a frame-by-frame animated sequence of the
    flower pattern as it's drawn.

    **Frame step**  
    Specifies how many frames to span per second of the effect being drawn.

4.  Click the Stage or within the shape or symbol where you want the Grid Fill
    pattern to appear.

## Apply the Particle System effect

Using the Particle System effect, you can create particle animations such as
fire, smoke, water, bubbles, and other effects.

To use the particle system effect:

1.  Select the Deco tool in the Tools panel.

2.  Set the properties for the effect in the Properties panel.

3.  Click the Stage in the location where you want to the effect to appear.

    Flash creates a frame-by-frame animation of the particle effect according to
    the properties you set. The particles generated on Stage are contained in a
    group in each frame of the animation.

The Particle System effect has the following properties:

Particle 1  
This is the first of 2 symbols you can assign to be used as particles. If you do
not specify a symbol, a small black square is used. By choosing graphics wisely,
you can generate very interesting and realistic effects.

Particle 2  
This is the second symbol that you can assign as a particle.

Total Length  
The duration of the animation in frames, starting from the current frame.

Particle Generation  
The number of frames in which particles are generated. If the number of frames
is less than the Total Length property, the tool stops making new particles in
the remaining frames, but the particles already generated continue to animate.

Rate per Frame  
The number of particles generated per frame.

Life Span  
The number of frames that an individual particle is visible on the Stage.

Initial Speed  
The speed of movement of each particle at the beginning of its life span. The
unit of speed is pixels per frame.

Initial Size  
The scaling of each particle at the beginning of its life span.

Min Initial Direction  
The minimum of the range of possible directions of movement of each particle at
the beginning of its life span. The measurement is in degrees. Zero is upward;
90 is to thr right; 180 is downward, 270 is to the left, and 360 is also upward.
Negative numbers are allowed.

Max Initial Direction  
The maximum of the range of possible directions of movement of each particle at
the beginning of its life span. The measurement is in degrees. Zero is upward;
90 is to thr right; 180 is downward, 270 is to the left, and 360 is also upward.
Negative numbers are allowed.

Gravity  
When this number is positive, the particles change direction to downward and
their speed increases, as if they are falling. If Gravity is negative, the
particles change direction to upward.

Rotation Rate  
The degrees of rotation to apply to each particle per frame.

## Apply the 3D Brush effect

The 3D Brush effect allows you to paint multiple instances of a symbol on the
Stage, with 3D perspective. Flash creates 3D perspective by scaling the symbols
down near the top of the Stage (the background), and up near the bottom of the
Stage (the forground). Symbols drawn closer to the bottom of the Stage are drawn
on top of symbols nearer the top of the Stage, regardless the order in which
they are drawn.

You can include from 1 to 4 symbols in the painting pattern. Each symbol
instance that appears on the Stage is in its own group. You can paint directly
on the Stage, or inside a shape or symbol. If the first click of the 3D brush
occurs inside a shape, the 3D brush is active only within the shape.

To use the 3D Brush effect:

1.  Click the Deco tool in the Tools panel.

2.  Select the 3D Brush effect from the Drawing effect menu in the Property
    inspector.

3.  Select from 1 to 4 symbols that you want to include in the painting pattern.

4.  Set the other properties for the effect in the Property inspector. Be sure
    the Perspective property is selected to create a 3D effect.

5.  Drag on the Stage to begin painting. Move the cursor toward the top of the
    Stage to paint smaller instances. Move the cursor toward the bottom of the
    Stage to paint larger instances.

The 3D Brush effect has the following properties:

Max objects  
The maximum number of objects to paint.

Spray area  
The maximum distance from the cursor that instances are painted.

Perspective  
This toggles the 3D effect. To paint instances of a consistent size, deselect
this option.

Distance scale  
This property determines the amount of the 3D perspective effect. Increase the
value to increase the scaling caused by moving the cursor up or down.

Random scale range  
This property allows the scaling to be randomly determined for each instance.
Increase the value to increase the range of scale values that can be applied to
each instance.

Random rotation range  
This property allows the rotation to be randomly determined for each instance.
Increase the value to increase the maximum possible rotation for each instance.

## Apply the Building Brush effect

The Building Brush effect allows you to draw buildings on the Stage. The
appearance of the buildings depends on values you choose for the building
properties.

To draw a building on the Stage:

1.  Click the Deco tool in the Tools panel.

2.  In the Property inspector, choose Building Brush from the Drawing Effect
    menu.

3.  Set the properties of the Building Brush effect.

4.  Starting where you want the bottom of the building, drag the cursor upwards
    vertically to the height you want for your finished building.

The Building Brush effect has the following properties:

Building type  
The style of building to create.

Building size  
The width of the building. Larger values create wider buildings.

## Apply the Decorated Brush effect

The Decorated brush effect allows you to draw decorative lines, such as dotted
lines, wavy lines, and others. Experiment with the effect to discover which
setting work for your intended designs.

To use the Decorated Brush effect:

1.  Click the Deco tool in the Tools panel.

2.  Set the properties for the effect in the Property inspector.

3.  Drag the cursor on the Stage.

    The Decorated Brush effect creates a styled line that follows the path of
    the cursor.

The Decorated Brush effect has the following properties:

Line style  
The style of line to draw. Experiment with all 20 choices to see the various
effects.

Pattern color  
The color of the line.

Pattern size  
The size of the selected pattern.

Pattern width  
The width of the selected pattern.

## Apply the Fire Animation effect

The Fire Animation effect creates stylized frame-by-frame fire animation.

To use the Fire Animation effect:

1.  Click the Deco tool in the Tools panel.

2.  Choose Fire Animation from the Drawing Effect menu in the Property
    inspector.

3.  Set the properties for the Fire Animation effect.

4.  Drag on the Stage to create the animation.

    Flash adds frames to the timeline while you hold the mouse button.

In most situations, it is best to place your fire animation inside its own
symbol, such as a movie clip symbol.

The Fire Animation effect has the following properties:

Fire size  
The width and height of the flames. Higher values create larger flames.

Fire speed  
The speed of the animation. Larger values create faster flames.

Fire duration  
The number of frames created in the timeline during the animation.

End animation  
Select this option to create an animation of the fire burning out instead of
burning continuously. Flash adds additional frames after the specified Fire
duration to accommodate the burning-out effect. If you want to loop the finished
animation to create a continuous burning effect, do not select this option.

Flame color  
The color of the tips of the flames.

Flame core color  
The color of the base of the flames.

Fire spark  
The number of individual flames at the base of the fire.

## Apply the Flame Brush effect

The Flame Brush effect allows you to draw flames on the Stage in the current
frame of the timeline

To use the Flame Brush effect:

1.  Click the Deco tool in the Tools panel.

2.  Choose Flame Brush from the Drawing Effect menu in the Property inspector.

3.  Set the properties for the Flame Brush effect.

4.  Drag on the Stage to draw flames.

The Flame Brush effect has the following properties:

Flame size  
The width and height of the flames. Higher values create larger flames.

Flame color  
The color of the center of the flames. As you draw, the flames change from the
selected color to black.

## Apply the Flower Brush effect

The Flower Brush effect allows you to draw stylized flowers in the current frame
of the timeline.

To use the Flower Brush effect:

1.  Click the Deco tool in the Tools panel.

2.  Choose Flower Brush from the Drawing Effect menu in the Property inspector.

3.  Select a flower from the Flower Type menu.

4.  Set the properties for the Flower Brush effect.

5.  Drag on the Stage to draw flowers.

The Flower Brush effect has the following properties:

Flower color  
The color of the flowers.

Flower size  
The width and height of the flowers. Higher values create larger flowers.

Leaf color  
The color of the leaves.

Leaf size  
The width and height of the leaves. Higher values create larger leaves.

Fruit color  
The color of the fruit.

Branch  
Select this option to draw branches in addition to the flowers and leaves.

Branch color  
The color of the branches.

## Apply the Lightning Brush effect

The Lightning Brush effect lets you create lightning bolts. You can also create
animated lighting.

To use the Lightning Brush effect:

1.  Click the Deco tool in the Tools panel.

2.  Select the Lightning Brush effect from the Drawing Effect menu in the
    Property inspector.

3.  Set the Properties for the Lightning Brush effect.

4.  Drag on the Stage. Flash draws lightning toward the direction you move the
    mouse.

The Lightning Brush effect has the following properties:

Lightning color  
The color of the lightning.

Lightning scale  
The length of the lightning.

Animation  
This option allows you to create frame-by-frame animation of the lightning.
Flash adds frames to the current layer in the Timeline while the lightning is
being drawn.

Beam width  
the thickness of the lightning at its root.

Complexity  
The number of times each branch divides. Higher values create longer lightning
with more branches.

## Apply the Smoke Animation effect

The Smoke Animation effect creates stylized frame-by-frame smoke animation.

To use the Smoke Animation effect:

1.  Click the Deco tool in the Tools panel.

2.  Choose Smoke Animation from the Drawing Effect menu in the Property
    inspector.

3.  Set the properties for the Smoke Animation effect.

4.  Drag on the Stage to create the animation.

    Flash adds frames to the timeline while you hold the mouse button.

In most situations, it is best to place your smoke animation inside its own
symbol, such as a movie clip symbol.

The Smoke Animation effect has the following properties:

Smoke size  
The width and height of the smoke. Higher values create larger flames.

Smoke speed  
The speed of the animation. Larger values create faster smoke.

Smoke duration  
The number of frames created in the timeline during the animation.

End animation  
Select this option to create an animation of the smoke burning out instead of
smoking continuously. Flash adds additional frames after the specified Smoke
duration to accommodate the burning-out effect. If you want to loop the finished
animation to create a continuous smoking effect, do not select this option.

Smoke color  
The color of the smoke.

Background color  
The background color of the smoke. The smoke changes to this color as it
dissipates.

## Apply the Tree Brush effect

The Tree Brush effect allows you to quickly create tree artwork.

To use the Tree Brush effect:

1.  Click the Deco tool in the Tools panel.

2.  In the Property inspector, select the Tree Brush effect from the Drawing
    Effect menu.

3.  Set the properties for the Tree Brush effect.

4.  Drag on the Stage to create a tree.

    Create large branches by dragging. Create smaller branches by keeping the
    cursor in one place.

Flash creates branches that are contained in groups on the Stage.

The Tree Brush effect has the following properties:

Tree style  
The kind of tree to create. Each tree style is based on an actual tree species.

Tree Scale  
The size of the tree. Values must be between 75-100. Higher values create larger
trees.

Branch color  
The color of the tree stems.

Leaf Color  
The color of the leaves.

Flower/Fruit color  
The color of the flowers and fruit.
