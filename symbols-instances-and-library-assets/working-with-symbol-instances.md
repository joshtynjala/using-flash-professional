# Working with symbol instances

## Create instances

After you create a symbol, you can create instances of that symbol throughout
your document, including inside other symbols. When you modify the symbol, Flash
Pro updates all instances of the symbol.

You can give names to instances from the Property inspector. Use the instance
name to refer to an instance in ActionScript. To control instances with
ActionScript®, give each instance within a single timeline a unique name. For
more information, see Handling events in
[Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)
or
[Handling events](https://web.archive.org/web/20111231232956mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b90204-7fca.html)
in the _ActionScript 3.0 Developer's Guide_.

To specify color effects, assign actions, set the graphic display mode, or
change the behavior of new instances, use the Property inspector. The behavior
of the instance is the same as the symbol behavior, unless you specify
otherwise. Any changes you make affect only the instance and not the symbol.

#### Create an instance of a symbol

1.  Select a layer in the Timeline. Flash Pro can place instances only in
    keyframes, always on the current layer. If you don't select a keyframe,
    Flash Pro adds the instance to the first keyframe to the left of the current
    frame.

    > **Note:** A keyframe is a frame in which you define a change in the
    > animation. For more information, see
    > [Insert frames in the Timeline](../timelines-and-animation/frames-and-keyframes.md#insert-frames-in-the-timeline).

2.  Select Window \> Library.

3.  Drag the symbol from the library to the Stage.

4.  If you created an instance of a graphic symbol, to add the number of frames
    that will contain the graphic symbol, select Insert \> Timeline \> Frame.

#### Apply a custom name to an instance

1.  Select the instance on the Stage.

2.  Select Window \> Properties, and enter a name in the Instance Name box.

## Editing instance properties

Each symbol instance has its own properties that are separate from the symbol.
You can change the tint, transparency, and brightness of an instance; redefine
how the instance behaves (for example, change a graphic to a movie clip); and
specify how an animation plays inside a graphic instance. You can also skew,
rotate, or scale an instance without affecting the symbol.

In addition, you can name a movie clip or button instance so that you can use
ActionScript to change its properties. For more information, see Classes in
[Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)
or
[Objects and classes](https://web.archive.org/web/20111231232956mp_/http://help.adobe.com/en_US/as3/learn/WS5b3ccc516d4fbf351e63e3d118a9b90204-7f9f.html)
in _Learning ActionScript 3.0_. To edit instance properties, you use the
Property inspector (Windows \> Properties).

The properties of an instance are saved with it. If you edit a symbol or relink
an instance to a different symbol, any instance properties you've changed still
apply to the instance.

## Set the visibilty of an instance (CS5.5 only)

You can make a symbol instance on the Stage invisible by turning off the Visible
property. Using the Visible property provides faster rendering performance than
setting the symbol's Alpha property to 0.

The Visible property requires a Player setting of Flash Player 10.2 or later and
is only compatible with movie clip, button, and component instances.

1.  Select the instance on the Stage.

2.  In the Display section of the Properties panel, deselect the Visible
    property.

## Change the color and transparency of an instance

Each instance of a symbol can have its own color effect. To set color and
transparency options for instances, use the Property inspector. Settings in the
Property inspector also affect bitmaps placed in symbols.

When you change the color and transparency for an instance in a specific frame,
Flash Pro makes the change as soon as it displays that frame. To make gradual
color changes, apply a motion tween. When tweening color, you enter different
effect settings in starting and ending keyframes of an instance, and then tween
the settings to make the instance's colors shift over time.

> **Note:** If you apply a color effect to a movie clip symbol that has multiple
> frames, Flash Pro applies the effect to every frame in the movie clip symbol.

1.  Select the instance on the Stage, and select Window \> Properties.
2.  In the Property inspector, select one of the following options from the
    Style menu in the Color Effect section:

    **Brightness**  
    Adjusts the relative lightness or darkness of the image, measured on a scale
    from black (–100%) to white (100%). To adjust brightness, click the triangle
    and drag the slider or enter a value in the box.

    **Tint**  
    Colors the instance with the same hue. To set the tint percentage from
    transparent (0%) to completely saturated (100%), use the Tint slider in the
    Property inspector. To adjust tint, click the triangle and drag the slider
    or enter a value in the box. To select a color, enter red, green, and blue
    values in the respective boxes, or click the Color control and select a
    color from the Color Picker.

    **Alpha**  
    Adjusts the transparency of the instance, from transparent (0%) to
    completely saturated (100%). To adjust the alpha value, click the triangle
    and drag the slider or enter a value in the box.

    **Advanced**  
    Separately adjusts the red, green, blue, and transparency values of an
    instance. This is most useful to create and animate subtle color effects on
    objects such as bitmaps. The controls on the left let you reduce the color
    or transparency values by a specified percentage. The controls on the right
    let you reduce or increase the color or transparency values by a constant
    value.

    The current red, green, blue, and alpha values are multiplied by the
    percentage values, and then added to the constant values in the right
    column, producing the new color values. For example, if the current red
    value is 100, setting the left slider to 50% and the right slider to 100%
    produces a new red value of 150 (\[100 x .5\] + 100 = 150).

    > **Note:** The Advanced settings in the Effect panel implement the function
    > (a \* y+ b)= x where a is the percentage specified in the left set of
    > boxes, y is the color of the original bitmap, b is the value specified in
    > the right set of boxes, and x is the resulting effect (between 0 and 255
    > for RGB, and 0 and 100 for alpha transparency).

    You can also change the color of an instance using the ActionScript
    ColorTransform object. For detailed information on the Color object, see
    ColorTransform in _ActionScript 2.0 Language Reference_ or _ActionScript 3.0
    Language and Components Reference_.

## Swap one instance for another

To display a different instance on the Stage and preserve all the original
instance properties, such as color effects or button actions, assign a different
symbol to an instance.

For example, suppose you're creating a cartoon with a rat symbol for your
character, but decide to change the character to a cat. You could replace the
rat symbol with the cat symbol and have the updated character appear in roughly
the same location in all your frames.

#### Assign a different symbol to an instance

1.  Select the instance on the Stage, and select Window \> Properties.

2.  Click the Swap button in the Property inspector.

3.  Select a symbol to replace the symbol currently assigned to the instance. To
    duplicate a selected symbol, click Duplicate Symbol and click OK.

    Duplicating lets you base a new symbol on an existing one in the library and
    minimizes copying if you're making several symbols that differ slightly.

#### Replace all instances of a symbol

![](../img/dingbat.png) Drag a symbol with the same name as the symbol you are
replacing from one Library panel into the Library panel of the FLA file you are
editing and click Replace. If you have folders in the library, the new symbol
must be dragged into the same folder as the symbol you are replacing.

## Change an instance's type

To redefine an instance's behavior in a Flash Pro application, change its type.
For example, if a graphic instance contains animation that you want to play
independently of the main Timeline, redefine the graphic instance as a movie
clip instance.

1.  Select the instance on the Stage, and select Window \> Properties.
2.  Select Graphic, Button, or Movie Clip from the menu in the Property
    inspector.

## Set looping for a graphic instance

To determine how animation sequences inside a graphic instance play in your
Flash Pro application, set options in the Property inspector.

An animated graphic symbol is tied to the Timeline of the document in which the
symbol is placed. In contrast, a movie clip symbol has its own independent
Timeline. Animated graphic symbols, because they use the same Timeline as the
main document, display their animation in document-editing mode. Movie clip
symbols appear as static objects on the Stage and do not appear as animations in
the Flash Pro editing environment.

1.  Select a graphic instance on the Stage, and select Window \> Properties.
2.  Select an animation option from the Options menu in the Looping section of
    the Property inspector:

    **Loop**  
    Loops all the animation sequences contained in the current instance for as
    many frames as the instance occupies.

    **Play Once**  
    Plays the animation sequence beginning from the frame you specify to the end
    of the animation and then stops.

    **Single Frame**  
    Displays one frame of the animation sequence. Specify which frame to
    display.

3.  To specify the first frame of the graphic symbol to display when looping,
    enter a frame number in the First text box. The Single Frame option also
    uses the frame number you specify here.

## Break apart a symbol instance

To break the link between an instance and a symbol and make the instance into a
collection of ungrouped shapes and lines, you _break apart_ the instance. This
feature is useful for changing the instance substantially without affecting any
other instance. For example, you must break apart an instance before applying a
[shape tween](https://web.archive.org/web/20111231232956mp_/http://www.adobe.com/devnet/flash/articles/concept_shape_tween.html)
to it.

Changes to the source symbol for an instance do not affect an instance after it
has been broken apart.

1.  Select the instance on the Stage.
2.  Select Modify \> Break Apart. This action breaks the instance into its
    component graphic elements.
3.  To modify these elements, use the painting and drawing tools.

## Get information about instances on the Stage

The Property inspector and Info panel display the following information about
instances selected on the Stage:

- In the Property inspector, view the instance's behavior and settings—for all
  instance types, color effect settings, location, and size; for graphics, the
  loop mode and first frame that contains the graphic; for buttons, the instance
  name (if assigned) and tracking option; for movie clips, the instance name (if
  assigned). For location, the Property inspector displays the _x_ and _y_
  coordinates of either the symbol's registration point or the symbol's
  upper-left corner, depending on which option is selected in the Info panel.

- In the Info panel, view the instance's size and location; the location of its
  registration point; its red (R), green (G), blue (B), and alpha (A) values (if
  the instance has a solid fill); and the location of the pointer. The Info
  panel also displays the _x_ and _y_ coordinates of either the symbol's
  registration point or the symbol's upper-left corner, depending on which
  option is selected. To display the coordinates of the registration point,
  click the center square in the Coordinate grid in the Info panel. To display
  the coordinates of the upper-left corner, click the upper-left square in the
  Coordinate grid.

- In the Movie Explorer, view the contents of the current document, including
  instances and symbols.

  View any actions assigned to a button or movie clip in the Actions panel.

#### Get information about an instance

1.  Select the instance on the Stage.

2.  Display the Property inspector (Window \> Properties) or panel to use:
    - To display the Info panel, select Window \> Info.

    - To display the Movie Explorer, select Window \> Movie Explorer.

    - To display the Actions panel, select Window \> Actions.

#### View the symbol definition for the selected symbol in the Movie Explorer

1.  Click the Show Buttons, Movie Clips, and Graphics button at the top of the
    Movie Explorer.

2.  Right-click (Windows) or Control-click (Macintosh), and select Show Symbol
    Instances and Go To Symbol Definition; or select these options from the menu
    in the upper-right corner of the Movie Explorer.

#### Jump to the scene containing instances of a selected symbol

1.  Display the symbol definitions.

2.  Right-click (Windows) or Control-click (Macintosh), and select Show Movie
    Elements and Go To Symbol Definition; or select these options from the menu
    in the upper-right corner of the Movie Explorer.

More Help topics

[Add classic tween animation to an instance, a group, or text](../timelines-and-animation/working-with-classic-tween-animation.md#add-classic-tween-animation-to-an-instance-a-group-or-text)

[Creating buttons](../symbols-instances-and-library-assets/creating-buttons.md)
