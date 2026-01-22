# Color

Color models describe the colors we see and work with in digital graphics. Each
color model, such as RGB, HSB, or CMYK, represents a different method for
describing and classifying color. Color models use numeric values to represent
the visible spectrum of color. A color space is a variant of a color model and
has a specific gamut (range) of colors. For example, within the RGB color model
are a number of color spaces: Adobe® RGB, sRGB, and Apple® RGB. While each of
these color spaces defines color using the same three axes (R, G, and B), their
gamuts are different.

When you work with the colors in a graphic, you are actually adjusting numerical
values in the file. It's easy to think of a number as a color, but these
numerical values are not absolute colors in themselves—they only have a color
meaning within the color space of the device that is producing the color.

Because each device has its own color space, it can reproduce colors only in its
gamut. When an image moves from one device to another, image colors may change
because each device interprets the RGB or HSB values according to its own color
space. For example, it is impossible for all the colors viewed on a monitor to
be identically matched in a print from a desktop printer. A printer operates in
a CMYK color space and a monitor operates in an RGB color space. Their gamuts
are different. Some colors produced by inks cannot be displayed on a monitor,
and some colors that can be displayed on a monitor cannot be reproduced using
inks on paper.

When creating colors for use in Flash documents, keep in mind that even though
it is impossible to perfectly match all colors on different devices, you can
achieve good results by considering the graphic display capabilities of the
devices in use by your target audience.

Adobe® Flash® Professional CS5 lets you apply, create, and modify colors using
the RGB or HSB color models. Using the default palette or a palette you create,
you can choose colors to apply to the stroke or fill of an object you are about
to create, or an object already on the Stage.

When applying a stroke color to a shape, you can do any of the following:

- Apply a solid color, gradient, or bitmap to a shape's fill. To apply a bitmap
  fill to a shape, you must import a bitmap into the current file. Select any
  solid color, gradient, and the style and weight of the stroke.

- Create an outlined shape with no fill by using No Color as a fill.

- Create a filled shape with no outline by using No Color as an outline.

- Apply a solid color fill to text.

With the Color panel, you can create and edit solid colors and gradient fills in
RGB and HSB modes.

To access the system color picker, select the Color Picker icon
![](../img/color_picker_nobackground.png) from the Stroke Color or Fill Color
control in the Color panel, the Tools panel or Shape Property inspector.

## The Color panel

The Color panel lets you modify the color palette of a FLA and change the color
of strokes and fills, including the following:

- Import, export, delete, and otherwise modify the color palette for a FLA file
  by using the Swatches panel.

- Select colors in hexadecimal mode.

- Create multicolor gradients.

- Use gradients to produce a wide range of effects, such as giving an illusion
  of depth to a two-dimensional object. The Color panel contains the following
  controls:

Stroke Color  
Changes the color of the stroke, or the border, of a graphic object.

Fill Color  
Changes the color of the fill. The fill is the area of color that fills up the
shape.

Color Type menu  
Changes the fill style:

None  
Removes the fill.

Solid Color  
Provides a solid, single fill color.

Linear Gradient  
Produces a gradient that blends on a linear path.

Radial Gradient  
Produces a gradient that blends outward in a circular path from a central focal
point.

Bitmap Fill  
Tiles the selected fill area with a bitmap image that you can select. When you
choose Bitmap, a dialog box lets you select a bitmap image on your local
computer, and add it to the library. You can apply this bitmap as a fill; the
appearance is similar to a mosaic tile pattern with the image repeated within
the shape.

HSB  
Lets you change the Hue, Saturation, and Brightness of the colors in a fill.

RGB  
Lets you change the density of the red, green, and blue (RGB) colors in a fill.

Alpha  
Sets the opacity for a solid fill, or the currently selected slider for a
gradient fill. An alpha value of 0% creates an invisible (or transparent) fill;
an alpha value of 100% creates an opaque fill.

Current Color Swatch  
Displays the currently selected color. If you select a gradient fill type
(Linear or Radial) from the fill Type menu, the Current Color Swatch displays
the color transitions within the gradient you create.

System Color Picker  
Lets you select a color visually. Click System Color Picker and drag the
cross-hair pointer until you find the color you want.

Hexadecimal value  
Displays the current color's hexadecimal value. To change the color using the
hexadecimal value, type in a new value. Hexadecimal color values (also called
hex values) are 6‑digit alphanumeric combinations that represent a color.

Flow  
Lets you control colors applied past the limits of a linear or radial gradient.

Extend Color  
(Default) Applies the colors you specify past the end of the gradient.

Reflect Color  
Causes the gradient colors to fill the shape using a reflective mirroring
effect. The gradients you specify are repeated in a pattern from the beginning
of the gradient to the end, and then repeated in the opposite sequence from the
end of the gradient to the beginning, and then back to the beginning of the
gradient to the end until the selected shape is filled.

Repeat Color  
Repeats the gradient from the beginning of the gradient to the end until the
selected shape is filled.

> **Note:** Overflow modes are supported only in Adobe Flash Player 8 and later.

Linear RGB  
Creates a SVG-compliant (Scalable Vector Graphics) linear or radial gradient.

## Color palettes

Each Flash Pro file contains its own color palette, stored in the Flash Pro
document. Flash Pro displays a file's palette as swatches in the Fill Color and
Stroke Color controls and in the Swatches panel. The default color palette is
the web-safe palette of 216 colors. To add colors to the current color palette,
use the Color panel.

You can import and export both solid and gradient color palettes between Flash
Pro files, as well as between Flash Pro and other applications.

### The default palette and the web-safe palette

Save the current palette as the default palette, replace the current palette
with the default palette defined for the file, or load the web-safe palette to
replace the current palette.

- To load or save the default palette, in the Swatches panel, select one of the
  following commands from the menu in the upper-right corner:

  **Load Default Colors**  
  Replaces the current palette with the default palette.

  **Save As Default**  
  Saves the current color palette as the default palette. The new default
  palette is used when you create new files.

- To load the web-safe 216-color palette, in the Swatches panel, select Web 216
  from the menu in the upper-right corner

### Sort color by hue in the palette

To make it easier to locate a color, sort colors in the palette by hue.

![](../img/dingbat.png) In the Swatches panel, select Sort by Color from the
menu in the upper-right corner.

### Import and export color palettes

To import and export both RGB colors and gradients between Flash Pro files, use
Flash Pro Color Set files (CLR files). Import and export RGB color palettes by
using Color Table files (ACT files). You can also import color palettes, but not
gradients, from GIF files. You cannot import or export gradients from ACT files.

#### Import a color palette

1.  In the Swatches panel, select one of the following commands from the menu in
    the upper-right corner:

    - To append the imported colors to the current palette, select Add Colors.

    - To replace the current palette with the imported colors, select Replace
      Colors.

2.  Navigate to the desired file, select it, and click OK.

#### Export a color palette

1.  In the Swatches panel, select Save Colors from the menu in the upper-right
    corner and enter a name for the color palette.
2.  For Save As Type (Windows) or Format (Macintosh), select Flash Color Set or
    Color Table. Click Save.

## Create or edit a solid color

You can create any color using the Color panel. If an object is selected on the
Stage, the color modifications you make in the Color panel are applied to the
selection. You can select colors in RGB or HSB, or you can expand the panel to
use hexadecimal mode. You can also specify an alpha value to define the degree
of transparency for a color. In addition, you can select a color from the
existing color palette.

You can expand the Color panel to display a larger color space in place of the
color bar, a split color swatch showing the current and previous colors, and a
Brightness slider to modify color brightness in all color modes.

1.  To apply the color to existing artwork, select an object or objects on the
    Stage, and select Window \> Color.

2.  Click the Stroke or Fill icon to specify which attribute to modify.

    > **Note:** Click the icon, not the Color control, or the Color Picker
    > opens.

3.  If you selected the Fill icon in step 3, verify that Solid is selected in
    the Type menu.

4.  If an object is selected on the Stage, the color modifications you make in
    the Color panel are applied to the selection. Do one of the following:

    - To select a color, click in the color space in the Color panel. To adjust
      the brightness of the color, drag the Brightness slider.

      > **Note:** To create colors other than black or white, make sure the
      > Brightness slider is not set to either extreme.

    - Enter values in the color value boxes: Red, Green, and Blue values for RGB
      display; Hue, Saturation, and Brightness values for HSB display; or
      hexadecimal values for hexadecimal display. Enter an Alpha value to
      specify the degree of transparency, from 0 for complete transparency to
      100 for complete opacity.

    - To return to the default color settings, black and white (black stroke and
      white fill), click the Black and White button
      ![](../img/black_and_white.png)

    - To swap colors between the fill and the stroke, click the Swap Colors
      button ![](../img/swap_colors.png)

    - To apply no color to the fill or stroke, click the No Color
      ![](../img/no_color.png)

      > **Note:** You cannot apply a stroke or fill of No Color to an existing
      > object. Instead, select the existing stroke or fill, and delete it.

    - Click the Stroke or Fill Color control, and select a color.

5.  To add the new color to the color swatch list for the current document,
    select Add Swatch from the menu in the upper-right corner.

## Duplicate, delete, and clear colors

Duplicate colors in the palette, delete individual colors, or clear all colors
from the palette.

- To duplicate or delete a color, select Window \> Swatches, click the color to
  duplicate or delete, and select Duplicate Swatch or Delete Swatch from the
  panel menu. When duplicating a swatch, the paint bucket appears. Click in the
  empty area of the Swatches panel with the paint bucket to make a duplicate of
  the selected color.

- To clear all colors from the color palette, in the Swatches panel, select
  Clear Colors from the panel menu. All colors except black and white are
  removed from the palette.
