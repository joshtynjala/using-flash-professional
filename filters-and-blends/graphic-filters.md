# Graphic filters

## About filters

### Filter overview

Adobe® Flash® Professional CS5 filters (graphic effects) let you add interesting
visual effects to text, buttons, and movie clips. A feature unique to Flash Pro
is that you can animate the filters you apply using motion tweens.

Flash Pro blend modes let you create composite images. _Compositing_ is the
process of varying the transparency or color interaction of two or more
overlapping objects. Blending modes also add a dimension of control to the
opacity of objects and images. You can use Flash Pro blending modes to create
highlights or shadows that let details from an underlying image show through, or
to colorize a desaturated image.

#### Additional resources

Articles:

- [Graphic Effects Learning Guide for Flash CS4 Professional](https://web.archive.org/web/20120109064314mp_/http://www.adobe.com/devnet/flash/learning_guide/graphic_effects/)
  (Adobe.com)

### About animated filters

You animate filters in the Timeline. Objects on separate keyframes joined by a
tween have the parameters for corresponding filters tweened on intermediate
frames. If a filter does not have a matching filter (a filter of the same type)
at the opposite end of the tween, a matching filter is added automatically to
ensure that the effect occurs at the end of the animation sequence.

To prevent motion tweens from functioning incorrectly if a filter is missing at
one end of the tween, or if filters are applied in a different order at each
end, Flash Pro does the following:

- If you apply a motion tween to a movie clip with filters applied to it, when
  you insert a keyframe at the opposite end of the tween, the movie clip
  automatically has the same filters, with the same stacking order, on the last
  frame of the tween as it did at the beginning of the tween.

- If you place movie clips on two different frames with different filters
  applied to each, and you apply a motion tween between the frames, Flash Pro
  first processes the movie clip with the most filters. Flash Pro then compares
  the filters applied to the first movie clip against the filters that the
  second movie clip uses. If no matching filters are found in the second movie
  clip, Flash Pro generates a dummy filter with no parameters and the color of
  the existing filters.

- If a motion tween exists between two keyframes and you add a filter to the
  object in one keyframe, Flash Pro automatically adds a dummy filter to the
  movie clip when it reaches the keyframe at the other end of the tween.

- If a motion tween exists between two keyframes and you remove a filter from an
  object in one keyframe, Flash Pro automatically removes the matching filter
  from the movie clip when it reaches the keyframe at the other end of the
  tween.

- If you set filter parameters inconsistently between the beginning and end of a
  motion tween, Flash Pro applies the filter settings of the starting frame to
  the interpolated frames. Inconsistent settings occur when the following
  parameters are set differently between the beginning and end of the tween:
  knockout, inner shadow, inner glow, and type of gradient glow and gradient
  bevel.

  For example, if you create a motion tween using the drop shadow filter, and
  apply a drop shadow with a knockout on the first frame of the tween, and an
  inner shadow on the last frame of the tween, Flash Pro corrects the
  inconsistent use of the filter in the motion tween. In this case, Flash Pro
  applies the filter settings used on the first frame of the tween—a drop shadow
  with a knockout.

### About filters and Flash Player performance

The type, number, and quality of the filters you apply to objects can affect the
performance of SWF files as you play them. The more filters you apply to an
object, the greater the number of calculations Adobe® Flash® Player must process
to correctly display the visual effects you've created. Adobe® recommends that
you apply a limited number of filters to a given object.

Each filter includes controls that let you adjust the strength and quality of
the applied filter. Using lower settings improves performance on slower
computers. If you are creating content for playback on a wide range of
computers, or are unsure of the computing power available to your audience, set
the quality level to Low to maximize playback performance.

### About Pixel Bender filters

Adobe Pixel Bender™ is a programming language developed by Adobe that allows
users to create custom filters, effects, and blend modes for use in Flash and
After Effects. Pixel Bender is hardware independent and designed to run
efficiently on a variety of GPU and CPU architectures automatically.

Pixel Bender developers create filters by writing Pixel Bender code and saving
the code in a text file with the file extension pbj. Once written, a Pixel
Bender filter can be used by any Flash document. Use ActionScript® 3.0 to load
the filter and use its controls.

For more information about working with Pixel Bender in ActionScript, see
ActionScript 3.0 Developer's Guide.

## Working with filters

Each time you add a new filter to an object, it is added to the list of applied
filters for that object in the Property inspector. You can apply multiple
filters to an object, as well as remove filters that were previously applied.
You can apply filters only to text, button, and movie clip objects.

You can create a filter settings library that lets you easily apply the same
filter or sets of filters to an object. Flash Pro stores the filter presets you
create in the Filters section of the Property inspector in the Filters \>
Presets menu.

<p><i>Image Missing: se_filtermenu.png</i></p>

<caption>The Add Filter menu in the Property inspector</caption>

### Apply or remove a filter

1.  Select a text, button, or movie clip object to apply a filter to or remove a
    filter from.
2.  In the Filters section of the Property inspector, do one of the following:
    - To add a filter, click the Add Filter button ![](../img/add_filter.png),
      and select a filter. Experiment with the settings until you get the
      desired look.

    - To remove a filter, select the filter to remove in the list of applied
      filters, and click the Remove Filter button <i>Image Missing:
      remove_filter.png</i>. You can delete or rename any presets.

### Copy and paste a filter

1.  Select the object to copy a filter from, and select the Filters panel.
2.  Select the filter to copy, and click the Clipboard button <i>Image Missing:
    paste_filter.png</i> and choose Copy Selected from the pop-up menu. To copy
    all filters, choose Copy All.
3.  Select the object to apply the filter to, and click the Clipboard
    button <i>Image Missing: paste_filter.png</i> and choose Paste from the
    pop-up menu.

### Apply a preset filter to an object

1.  Select the object to apply a filter preset to, and select the Filter tab.
2.  Click the Add Filter button ![](../img/add_filter.png), and select Presets.
3.  Select the filter preset to apply from the list of available presets at the
    bottom of the preset menu.

> **Note:** When you apply a filter preset to an object, Flash Pro replaces any
> filters currently applied to the selected objects with the filters used in the
> preset.

### Enable or disable a filter applied to an object

![](../img/dingbat.png) Click the enable or disable icon next to the filter name
in the Filter list.

> **Note:** To toggle the enable state of the other filters in the list,
> Alt‑click (Windows) or Option-click (Macintosh) the enable icon in the Filter
> list. If you Alt‑click the disable icon, the selected filter is enabled, and
> all others filters in the list are disabled.

### Enable or disable all filters applied to an object

![](../img/dingbat.png) Click the Add Filter button ![](../img/add_filter.png),
and select Enable All or Disable All.

> **Note:** To enable or disable all of the filters in the list, Control-click
> the enable or disable icon in the Filter list.

### Create preset filter libraries

Save filter settings as preset libraries that you can easily apply to movie clip
and text objects. Share your filter presets with other users by providing them
with the filter configuration file. The filter configuration file is an XML file
that is saved in the Flash Pro Configuration folder in the following location:

- Windows XP: C:\Documents and Settings\\_username_\Local Settings\Application
  Data\Adobe\Flash CS5\\_language_\Configuration\Filters\\_filtername.xml_

- Windows Vista: C:\Users\\_username_\Local Settings\Application
  Data\Adobe\Flash CS5\\_language_\Configuration\Filters\\_filtername.xml_

- Macintosh: Macintosh HD/Users/_username_/Library/Application
  Support/Adobe/Flash CS5/_language_/Configuration/Filters/_filtername.xml_

#### Create a library of filters with preset settings

1.  Apply the filter or filters to the object.

2.  Click the Add Filter button ![](../img/add_filter.png), and add a new
    filter.

3.  Select the filter and click the Presets menu <i>Image Missing:
    filter_presets.png</i>, and choose Save As.

4.  Enter a name for the filter settings in the Save Preset As dialog box, and
    click OK.

#### Rename a filter preset

1.  Click the Add Filter button ![](../img/add_filter.png), and add a new
    filter.

2.  Select the filter and click the Presets menu <i>Image Missing:
    filter_presets.png</i>, and choose Rename.

3.  Double-click the preset name to modify.

4.  Enter a new preset name, and click Rename.

#### Delete a filter preset

1.  Click the Add Filter button ![](../img/add_filter.png), and add a new
    filter.

2.  Select the filter and click the Presets menu <i>Image Missing:
    filter_presets.png</i>, and choose Delete.

3.  Select the preset to remove, and click Delete.

## Applying filters

### Apply a drop shadow

The Drop Shadow filter simulates the look of an object casting a shadow onto a
surface.

<p><i>Image Missing: se_textDropShadow.png</i></p>

<caption>Text with the Drop Shadow filter applied</caption>

For a sample of a drop shadow with a classic tween, see the
[Flash Samples page](https://web.archive.org/web/20120102164641/http://www.adobe.com/devnet/flash/samples.html).
Download and decompress the Samples zip file and navigate to the
Graphics\AnimatedDropShadow directory.

1.  Select the object to apply a drop shadow to.
2.  In the Filters section of the Property inspector, click the Add Filter
    button ![](../img/add_filter.png), and select Drop Shadow.
3.  Edit the filter settings:
    - To set the width and height of the drop shadow, set the Blur X and Y
      values.

    - To set the darkness of the shadow, set the Strength value. The higher the
      numerical value, the darker the shadow.

    - Select the quality level for the drop shadow. High is approximate to that
      of a Gaussian blur. Low maximizes playback performance.

    - To set the angle of the shadow, enter a value.

    - To set the distance of the shadow from the object, set the Distance value.

    - Select Knockout to knock out (or visually hide) the source object and
      display only the drop shadow on the knockout image.

    - To apply the shadow within the boundaries of the object, select Inner
      shadow.

    - To hide the object and display only its shadow, select Hide Object. Hide
      Object lets you more easily create a realistic shadow.

    - To open the Color Picker and set the shadow color, click the Color
      control.

### Create a skewed drop shadow

<p><i>Image Missing: se_DropShadow_HideObject.png</i></p>

<caption>Skewing the Drop Shadow filter to create a more realistic looking shadow</caption>

1.  Select the object with the shadow you want to skew.
2.  Duplicate (select Edit \> Duplicate) the source object.
3.  Select the duplicated object, and skew it using the Free Transform tool
    (Modify \> Transform \> Rotate And Skew).
4.  Apply the Drop Shadow filter to the duplicated movie clip or text object.
    (It will already be applied if the object you duplicated already had a drop
    shadow.)
5.  In the Filters panel, select Hide Object to hide the duplicated object while
    leaving its shadow visible.
6.  Select Modify \> Arrange \> Send Backward to place the duplicated object and
    its shadow behind the original object that you duplicated.
7.  Adjust both the Drop Shadow filter settings and the angle of the skewed drop
    shadow until you achieve the desired look.

### Apply a blur

The Blur filter softens the edges and details of objects. Applying a blur to an
object can make it appear as if it is behind other objects, or make an object
appear to be in motion.

<p><i>Image Missing: se_textBlur.png</i></p>

<caption>Text with the Blur filter applied</caption>

1.  Select an object to apply a blur to, and select Filters.
2.  Click the Add Filter button ![](../img/add_filter.png), and select Blur.
3.  Edit the filter settings on the Filter tab:
    - To set the width and height of the blur, set the Blur X and Y values.

    - Select the quality level for the blur. High is approximate to that of a
      Gaussian blur. Low maximizes playback performance.

### Apply a glow

The Glow filter lets you apply a color around the edges of an object.

<p><i>Image missing: se_textGlowFilter.png</i></p>

<caption>Text with the Glow filter applied.</caption>

1.  Select an object to apply a glow to, and select Filters.
2.  Click the Add Filter button ![](../img/add_filter.png), and select Glow.
3.  Edit the filter settings in the Filter tab:
    - To set the width and height of the glow, set the Blur X and Y values.

    - To open the Color Picker and set the glow color, click the Color control.

    - To set the sharpness of the glow, set the Strength value.

    - To knock out (or visually hide) the source object and display only the
      glow on the knockout image, select Knockout.

      <p><i>Image Missing: se_textGlowKnockoutFilter.png</i></p>

      <caption>Using the Glow filter with the Knockout option</caption>

    - To apply the glow within the boundaries of the object, select Inner Glow.

    - Select the quality level for the glow. High is approximate to that of a
      Gaussian blur. Low maximizes playback performance.

### Apply a bevel

Applying a bevel applies a highlight to the object that makes it appear to be
curved up above the background surface.

<p><i>Image missing: se_textBevelFilter.png</i></p>

<caption>Text with a bevel applied</caption>

1.  Select an object to apply a bevel to, and select Filters.
2.  Click the Add Filter button ![](../img/add_filter.png), and select Bevel.
3.  Edit the filter settings in the Filter tab:
    - To set the type of bevel, select a bevel from the Type menu.

    - To set the width and height of the bevel, set the Blur X and Y values.

    - Select a shadow and highlight color for the bevel from the pop‑up color
      palette.

    - To set the opacity of the bevel without affecting its width, set the
      Strength value.

    - To change the angle of the shadow that the beveled edge casts, set the
      Angle value.

    - To define the width of the bevel, enter a value for Distance.

    - To knock out (or visually hide) the source object and display only the
      bevel on the knockout image, select Knockout.

### Apply a gradient glow

Applying a gradient glow produces a glow look with a gradient color across the
surface of the glow. The gradient glow requires one color at the beginning of
the gradient with an Alpha value of 0. You cannot move the position of this
color, but you can change the color.

<p><i>Image missing: se_textGradGlowFilter.png</i></p>

<caption>Text with a gradient glow applied</caption>

1.  Select an object to apply a gradient glow to.
2.  In the Filters section of the Property inspector, click the Add Filter
    button ![](../img/add_filter.png), and select Gradient Glow.
3.  Edit the filter settings on the Filter tab:
    - Select the type of glow to apply to the object from the Type pop‑up menu.

    - To set the width and height of the glow, set the Blur X and Y values.

    - To set the opacity of the glow without affecting its width, set the
      Strength value.

    - To change the angle of the shadow that the glow casts, set the Angle
      value.

    - To set the distance of the shadow from the object, set the Distance value.

    - To knock out (or visually hide) the source object and display only the
      gradient glow on the knockout image, select Knockout.

    - Specify a gradient color for the glow. A gradient contains two or more
      colors that fade or blend into one another. The color you select for the
      beginning of the gradient is referred to as the _alpha_ color.

      To change a color in the gradient, select one of the color pointers below
      the gradient definition bar and click the color space that appears
      directly below the gradient bar to display the Color Picker. Sliding these
      pointers adjusts the level and position of that color in the gradient.

      To add a pointer to the gradient, click on or below the gradient
      definition bar. To create a gradient with up to 15 color transitions, add
      up to 15 color pointers. To reposition a pointer on the gradient, drag the
      pointer along the gradient definition bar. To remove a pointer, drag it
      down and off the gradient definition bar.

    - Select the quality level for the gradient glow. High is approximate to
      that of a Gaussian blur. Low maximizes playback performance.

### Apply a gradient bevel

Applying a gradient bevel produces a raised look that makes an object appear to
be raised above the background, with a gradient color across the surface of the
bevel. The gradient bevel requires one color in the middle of the gradient with
an alpha value of 0.

1.  Select an object to apply a gradient bevel to.

2.  In the Filters section of the Property inspector, click the Add Filter
    button ![](../img/add_filter.png), and select Gradient Bevel.

3.  Edit the filter settings on the Filter tab:
    - Select the type of bevel to apply to the object from the Type pop‑up menu.

    - To set the width and height of the bevel, set the Blur X and Y values.

    - To affect the smoothness of the bevel without affecting its width, enter a
      value for Strength.

    - To set the angle of the light source, enter a value for Angle.

    - To knock out (or visually hide) the source object and display only the
      gradient bevel on the knockout image, select Knockout.

    - Specify a gradient color for the bevel. A gradient contains two or more
      colors that fade or blend into one another. The middle pointer controls
      the alpha color of the gradient. You can change the color of the alpha
      pointer, but you cannot reposition this color in the gradient.

      To change a color in the gradient, select one of the color pointers below
      the gradient definition bar, and click the color space that appears
      directly below the gradient bar to display the Color Picker. To adjust the
      level and position of that color in the gradient, slide these pointers.

      To add a pointer to the gradient, click on or below the gradient
      definition bar. To create a gradient with up to 15 color transitions, add
      up to 15 color pointers. To reposition a pointer on the gradient, drag the
      pointer along the gradient definition bar. To remove a pointer, drag it
      down and off the gradient definition bar.

### Apply the Adjust Color filter

The Adjust Color filter allows you to finely control the color attributes of the
selected object, including contrast, brightness, saturation, and hue.

1.  Select an object to adjust the color for.
2.  In the Filters section of the Property inspector, click the Add Filter
    button ![](../img/add_filter.png), and select Adjust Color.
3.  Enter values for the color attributes. The attributes and their
    corresponding values are as follows:

    **Contrast**  
    Adjusts the highlights, shadows, and midtones of an image.

    **Brightness**  
    Adjusts the brightness of an image.

    **Saturation**  
    Adjusts the intensity of a color.

    **Hue**  
    Adjusts the shade of a color.

4.  To reset all of the color adjustments to 0 and return the object to its
    original state, click Reset Filter.

More Help topics

[Change the color and transparency of an instance](../symbols-instances-and-library-assets/working-with-symbol-instances.md#change-the-color-and-transparency-of-an-instance)

![](../img/as3LinkIndicator.png)
[Working with Pixel Bender shaders](https://web.archive.org/web/20120109064314mp_/http://help.adobe.com/en_US/as3/dev/WS3E659D01-10C0-479d-8175-B40950BBC223.html)
