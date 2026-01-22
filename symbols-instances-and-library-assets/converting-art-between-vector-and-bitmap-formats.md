# Converting art between vector and bitmap formats (CS5.5 only)

## Advantages of vectors and bitmap formats

For definitions of vector and bitmap art, see
[Vector and bitmap graphics](../creating-and-editing-artwork/drawing-in-flash/about-drawing.md#vector-and-bitmap-graphics).

Vector artwork has these advantages:

- Smaller file sizes

- Scalable with no loss of fidelity

Bitmap artwork has these advantages:

- Faster rendering performance

- Requires less CPU speed

- More appropriate for mobile devices with slower processors

## Render an instance as a bitmap on the Stage

The Export as Bitmap option allows you to render instances of movie clip and
button symbols as bitmaps on the Stage during authoring. Flash also uses these
bitmaps when publishing a SWF file. Playback performance is faster than the
Cache as Bitmap option because it prevents Flash Player from having to do the
conversion at runtime. This results in better rendering on lower-performance
devices.

Once you select the Export as Bitmap option, you can still double-click the
instance to edit its symbol. The edits are then reflected in the bitmaps on the
Stage.

You can use the Export as Bitmap option on movie clips containing shapes, text,
and 3D objects.

1.  Select the movie clip or button instance on the Stage.

2.  In the Display section of the Property inspector, choose Export as Bitmap
    from the Render menu.

3.  Choose an option from the Background menu (below the Render menu).
    - Transparent

    - Opaque - allows you to specify a background color for the bitmap.

> **Note:** When instances of movie clips are rendered as bitmaps on the Stage,
> only the first frame of the movie clip is rasterized. Flash preserves all the
> properties of the movie clip instance on its first frame, including any
> ActionScript in frame 1. Also, Export as Bitmap is disabled for tweened
> symbols.

## Create a bitmap from a stage selection

You can create a bitmap and add it to the library by using the Convert to Bitmap
command.

1.  Select one or more objects on the Stage.

2.  Choose Modify \> Convert to Bitmap.

Flash converts the selection to a bitmap, adds the bitmap to the library, and
replaces the selection on the stage with an instance of the bitmap.

The bitmap resolution is 24 bit with an alpha channel. The default format is
PNG. You can change the format to JPEG in the properties of the bitmap in the
Library panel.

You cannot edit the bitmap in Flash Pro, but you can edit it in Photoshop or
another image editor and then reimport it into Flash Pro.
