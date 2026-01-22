# Applying blend modes

## About blend modes

Blend modes let you create composite images. _Compositing_ is the process of
varying the transparency or color interaction of two or more overlapping
objects. Blending lets you create unique effects by blending the colors in
overlapping movie clips.

A blending mode contains the following elements:

Blend color  
The color applied to the blend mode.

Opacity  
The degree of transparency applied to the blend mode.

Base color  
The color of pixels underneath the blend color.

Result color  
The result of the blend's effect on the base color.

Blend modes depend on both the color of the object you're applying the blend to
and the underlying color. Adobe® recommends that you experiment with the
different blend modes to achieve the desired effect.

Normal  
Applies color normally, with no interaction with the base colors.

Layer  
Lets you stack movie clips on top of each other without affecting their color.

Darken  
Replaces only the areas that are lighter than the blend color. Areas darker than
the blend color don't change.

Multiply  
Multiplies the base color by the blend color, resulting in darker colors.

Lighten  
Replaces only pixels that are darker than the blend color. Areas lighter than
the blend color don't change.

Screen  
Multiplies the inverse of the blend color by the base color, resulting in a
bleaching effect.

Overlay  
Multiplies or screens the colors, depending on the base colors.

Hard Light  
Multiplies or screens the colors, depending on the blend mode color. The effect
is similar to shining a spotlight on the object.

Difference  
Subtracts either the blend color from the base color or the base color from the
blend color, depending on which has the greater brightness value. The effect is
similar to a color negative.

Add  
Commonly used to create an animated lightening dissolve effect between two
images.

Subtract  
Commonly used to create an animated darkening dissolve effect between two
images.

Invert  
Inverts the base color.

Alpha  
Applies an alpha mask.

Erase  
Removes all base color pixels, including those in the background image.

> **Note:** Erase and Alpha blend modes require that a Layer blend mode be
> applied to the parent movie clip. You cannot change the background clip to
> Erase and apply it because the object would appear invisible.

## Blend mode examples

The following examples illustrate how different blend modes affect the
appearance of an image. The resulting effect of a blend mode might be
considerably different, depending on the color of the underlying image and the
type of blend mode you apply.

|                                                              |                                                            |                                                    |
| ------------------------------------------------------------ | ---------------------------------------------------------- | -------------------------------------------------- |
| <img src="../img/se_blend_original.jpg" /><br>Original image | <img src="../img/se_blend_layer.jpg" /><br>Layer           | <img src="../img/se_blend_darken.jpg" /><br>Darken |
| <img src="../img/se_blend_multiply.jpg" /><br>Multiply       | <img src="../img/se_blend_lighten.jpg" /><br>Lighten       | <img src="../img/se_blend_screen.jpg" /><br>Screen |
| <img src="../img/se_blend_overlay.jpg" /><br>Overlay         | <img src="../img/se_blend_hardlight.jpg" /><br>Hard Light  | <img src="../img/se_blend_add.jpg" /><br>Add       |
| <img src="../img/se_blend_subtract.jpg" /><br>Subtract       | <img src="../img/se_blend_difference.jpg" /><br>Difference | <img src="../img/se_blend_invert.jpg" /><br>Invert |

## Apply a blend mode

To apply blends to selected movie clips, use the Property inspector.

> **Note:** You cannot apply different blend modes to different graphic symbols
> because multiple graphic symbols are merged as a single shape when you publish
> the SWF file.

1.  Select the movie clip instance (on the Stage) to apply a blend mode to.

2.  To adjust the color and transparency of the movie clip instance, use the
    Color pop‑up menu in the Properties panel.

3.  Select a blend mode for movie clips from the Blend pop‑up menu in the
    Properties panel. The blend mode is applied to the selected movie clip
    instance.

4.  Verify that the blend mode you selected is appropriate to the effect you're
    trying to achieve.

    Experiment with both the color and transparency settings of the movie clip
    and the different blend modes to achieve the desired effect.

## Additional resources

The following resources provide additional detailed information about working
with blends in Flash Pro:

- [Graphic Effects Learning Guide for Flash CS4 Professional](https://web.archive.org/web/20111110202424mp_/http://www.adobe.com/devnet/flash/learning_guide/graphic_effects/)
  (Adobe.com)

More Help topics

[Change the color and transparency of an instance](../symbols-instances-and-library-assets/working-with-symbol-instances.md#change-the-color-and-transparency-of-an-instance)
