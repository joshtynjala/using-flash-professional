# Imported bitmaps and Flash

## Work with imported bitmaps

When you import a bitmap into Flash Pro, you can modify that bitmap and use it
in your Flash Pro document in a variety of ways.

If a Flash Pro document displays an imported bitmap at a size larger than the
original, the image may be distorted. To be sure that images are displayed
properly, preview imported bitmaps.

When you select a bitmap on the Stage, the Property inspector displays the
bitmap's symbol name and its pixel dimensions and position on the Stage. Using
the Property inspector, you can _swap_ an instance of a bitmap—that is, replace
the instance with an instance of another bitmap in the current document.

#### Display the Property inspector with bitmap properties

1.  Select an instance of a bitmap on the Stage.

2.  Select Window \> Properties.

#### Replace an instance of a bitmap with an instance of another bitmap

1.  Select a bitmap instance on the Stage.

2.  Select Window \> Properties, and click Swap.

3.  Select a bitmap to replace the one currently assigned to the instance.

## Set bitmap properties

You can apply anti-aliasing to an imported bitmap to smooth the edges in the
image. You can also select a compression option to reduce the bitmap file size
and format the file for display on the web.

1.  Select a bitmap in the Library panel and click the Properties button at the
    bottom of the Library panel.
2.  Select Allow Smoothing. Smoothing improves the quality of bitmap images when
    they are scaled.
3.  For Compression, select one of the following options:

    **Photo (JPEG)**  
    Compresses the image in JPEG format. To use the default compression quality
    specified for the imported image, select Use Document Default Quality. To
    specify a new quality compression setting, deselect Use Document Default
    Quality and enter a value between 1 and 100 in the Quality text field. (A
    higher setting preserves greater image integrity but yields a larger file
    size.)

    **Lossless (PNG/GIF)**  
    Compresses the image with lossless compression, in which no data is
    discarded from the image.

    > **Note:** Use Photo compression for images with complex color or tonal
    > variations, such as photographs or images with gradient fills. Use
    > lossless compression for images with simple shapes and relatively few
    > colors.

4.  To determine the results of the file compression, click Test. To determine
    if the selected compression setting is acceptable, compare the original file
    size to the compressed file size.
5.  Click OK.

> **Note:** JPEG Quality settings that you select in the Publish Settings dialog
> box do not specify a quality setting for imported JPEG files. Specify a
> quality setting for each imported JPEG file in the Bitmap Properties dialog
> box.

## Import a bitmap at runtime

To add bitmaps to a document at runtime, use the ActionScript® 2.0 or the
ActionScript 3.0 `BitmapData` command. To do so, specify a linkage identifier
for the bitmap. For more information, see Assigning linkage to assets in the
library in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120104100159mp_/http://www.adobe.com/go/learn_cs5_learningas2_en)
or
[Exporting library symbols for ActionScript](https://web.archive.org/web/20120104100159mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b8ea63-7fee.html)
in the _ActionScript 3.0 Developer's Guide_.

1.  Select the bitmap in the Library panel.
2.  Do one of the following:
    - Select Linkage from the Panel menu in the upper-right corner of the panel.

    - Right-click (Windows) or Control-click (Macintosh) the bitmap name in the
      Library panel, and select Properties from the context menu.

      If the Linkage properties aren't visible in the Properties dialog box,
      click Advanced.

3.  For Linkage, select Export For ActionScript.
4.  Enter an identifier string in the text field, and click OK.

## Apply a bitmap as a fill

To apply a bitmap as a fill to a graphic object, use the Color panel. Applying a
bitmap as a fill tiles the bitmap to fill the object. The Gradient Transform
tool allows you to scale, rotate, or skew an image and its bitmap fill.

1.  To apply the fill to existing artwork, select a graphic object or objects on
    the Stage.

2.  Select Window \> Color.

3.  Select Bitmap from the pop-up menu in the upper right of the panel.

4.  To use a larger preview window to display more bitmaps in the current
    document, click the arrow in the lower-right corner to expand the Color
    panel.

5.  Click a bitmap to select it.

    The bitmap becomes the current fill color. If you selected artwork in step
    1, the bitmap is applied as a fill to the artwork.

## Edit a bitmap in an external editor

If you are editing a Fireworks PNG file imported as a flattened image, edit the
PNG source file for the bitmap, when available.

> **Note:** You cannot edit bitmaps from Fireworks PNG files imported as
> editable objects in an external image editor.

If you have Fireworks 3 or later or another image-editing application installed
on your system, you can start the application from Flash Pro to edit an imported
bitmap.

#### Edit a bitmap with Photoshop CS5 or later

> **Note:** If you are using Flash Pro CS5.5, you need to use Photoshop CS5.1 to
> access this feature.

1.  In the Library panel, right-click (Windows) or Control-click (Macintosh) the
    bitmap's icon and select Edit With Photoshop CS5.

2.  Perform the desired modifications to the file in Photoshop.

3.  In Photoshop, select File \> Save. (Do not change the file name or format.)

4.  Return to Flash Pro.

    The file is automatically updated in Flash Pro.

#### Edit a bitmap with Fireworks 3 or later

1.  In the Library panel, right-click (Windows) or Control-click (Macintosh) the
    bitmap's icon and select Edit With Fireworks 3.

2.  Specify whether to open the PNG source file or the bitmap file.

3.  Perform the desired modifications to the file in Fireworks.

4.  In Fireworks, select File \> Update.

5.  Return to Flash Pro.

    The file is automatically updated in Flash Pro.

#### Edit a bitmap with another image-editing application

1.  In the Library panel, right-click (Windows) or Control-click (Macintosh) the
    bitmap's icon, and select Edit With.

2.  Select an image-editing application to open the bitmap file, and click OK.

3.  Perform the desired modifications to the file in the image-editing
    application.

4.  Save the file in the image-editing application.

    The file is automatically updated in Flash Pro.

5.  Return to Flash Pro to continue editing the document.

## Break apart a bitmap and create a bitmap fill

Breaking apart a bitmap on the Stage separates the on-Stage image from its
library item and converts it from a bitmap instance to a shape. When you break
apart a bitmap, you can modify the bitmap with the Flash Pro drawing and
painting tools. Using the Lasso tool with the Magic Wand modifier, you can
select areas of the bitmap that contain the same or similar colors.

To paint with a broken-apart bitmap, select the bitmap with the Eyedropper tool
and apply the bitmap as a fill with the Paint Bucket tool or another drawing
tool.

#### Break a bitmap apart

1.  Select a bitmap in the current scene.

2.  Select Modify \> Break Apart.

#### Change the fill of areas of a broken-apart bitmap

1.  Select the Lasso tool, click the Magic Wand modifier, and set the following
    options:
    - For Threshold, enter a value between 1 and 200 to define how closely the
      color of adjacent pixels must match to be included in the selection. A
      higher number includes a broader range of colors. If you enter 0, only
      pixels of the exact same color as the first pixel you click are selected.

    - For Smoothing, select an option to define how much the edges of the
      selection are smoothed.

2.  To select an area, click the bitmap. To add to the selection, continue
    clicking.

3.  To fill the selected areas in the bitmap, select the fill to use from the
    Fill Color control.

4.  To apply the new fill, select the Paint Bucket tool and click anywhere in
    the selected area.

#### Convert a bitmap to a vector graphic

The Trace Bitmap command converts a bitmap into a vector graphic with editable,
discrete areas of color. You manipulate the image as a vector graphic, and you
can reduce the file size.

When you convert a bitmap to a vector graphic, the vector graphic is no longer
linked to the bitmap symbol in the Library panel.

> **Note:** If the imported bitmap contains complex shapes and many colors, the
> converted vector graphic might have a larger file size than the original
> bitmap. To find a balance between file size and image quality, try a variety
> of settings in the Trace Bitmap dialog box.

You can also break apart a bitmap to modify the image with Flash Pro drawing and
painting tools.

1.  Select a bitmap in the current scene.

2.  Select Modify \> Bitmap \> Trace Bitmap.

3.  Enter a Color Threshold value.

    When two pixels are compared, if the difference in the RGB color values is
    less than the color threshold, the two pixels are considered the same color.
    As you increase the threshold value, you decrease the number of colors.

4.  For Minimum Area, enter a value to set the number of surrounding pixels to
    consider when assigning a color to a pixel.

5.  For Curve Fit, select an option to determine how smoothly outlines are
    drawn.

6.  For Corner Threshold, select an option to determine whether sharp edges are
    retained or smoothed out.

    To create a vector graphic that looks most like the original bitmap, enter
    the following values:
    - Color Threshold: 10

    - Minimum Area: 1 pixel

    - Curve Fit: Pixels

    - Corner Threshold: Many Corners

#### Use the Eyedropper tool to apply a bitmap fill

1.  Select the Eyedropper tool and click the broken-apart bitmap on the Stage.
    The Eyedropper tool sets the bitmap to be the current fill and changes the
    active tool to the Paint Bucket.

2.  Do one of the following:
    - To apply the bitmap as a fill, click an existing graphic object with the
      Paint Bucket tool.

    - Select the Oval, Rectangle, or Pen tool, and draw a new object. The object
      is filled with the broken-apart bitmap.

      To scale, rotate, or skew the bitmap fill, use the Free Transform tool.

More Help topics

[Transform gradient and bitmap fills](../creating-and-editing-artwork/strokes-fills-and-gradients.md#transform-gradient-and-bitmap-fills)

[Adjust Stroke and Fill color](../creating-and-editing-artwork/strokes-fills-and-gradients.md#adjust-stroke-and-fill-color)
