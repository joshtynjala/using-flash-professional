# Working with Fireworks files in Flash

## About imported Fireworks PNG files

You can import Adobe® Fireworks PNG files into Flash Pro as flattened images or
as editable objects. When you import a PNG file as a flattened image, the entire
file (including any vector artwork) is rasterized, or converted to a bitmap
image. When you import a PNG file as editable objects, vector artwork in the
file is preserved in vector format. Choose to preserve placed bitmaps, text,
filters (called effects in Fireworks), and guides in the PNG file when you
import it as editable objects.

## About imported filters and blends from Fireworks PNG files

When you import Fireworks® PNG files, you can retain many of the filters and
blending modes applied to objects in Fireworks and continue to modify those
filters and blends using Flash Pro.

Flash Pro only supports modifiable filters and blends for objects imported as
text and movie clips. If an effect or blend mode is not supported, Flash Pro
rasterizes or ignores it when it is imported. To import a Fireworks PNG file
that contains filters or blends that Flash Pro does not support, rasterize the
file during the import process. After this operation, you cannot edit the file.

#### Fireworks effects supported in Flash

Flash Pro imports the following Fireworks effects as modifiable filters: |
Fireworks effect | Flash Pro filter | | ----------------------- |
------------------------------------------------------ | | Drop shadow | Drop
shadow | | Solid shadow | Drop shadow | | Inner shadow | Drop shadow (with Inner
shadow automatically selected) | | Blur | Blur (where blurX = blurY=1) | | Blur
more | Blur (where blurX = blurY=1) | | Gaussian blur | Blur | | Adjust color
brightness | Adjust color | | Adjust color contrast | Adjust color |

#### Fireworks blend modes supported in Flash

Flash Pro imports the following Fireworks blend modes as modifiable blends: |
Fireworks blending mode | Flash Pro blending mode | | ----------------------- |
----------------------- | | Normal | Normal | | Darken | Darken | | Multiply |
Multiply | | Lighten | Lighten | | Screen | Screen | | Overlay | Overlay | |
Hard light | Hard light | | Additive | Add | | Difference | Difference | |
Invert | Invert | | Alpha | Alpha | | Erase | Erase | Flash Pro ignores all
other blending modes imported from Fireworks. The blending modes that Flash Pro
does not support are Average, Negation, Exclusion, Soft Light, Subtractive,
Fuzzy Light, Color Dodge, and Color Burn.

## Importing text from Fireworks into Flash

When you import text from Fireworks into Flash Pro 8 or later, the text is
imported with the default anti-alias setting of the current document.

If you import the PNG file as a flattened image, you can start Fireworks from
Flash Pro and edit the original PNG file (with vector data).

When you import multiple PNG files in a batch, you select import settings one
time. Flash Pro uses the same settings for all files in the batch.

> **Note:** To edit bitmap images in Flash Pro, convert the bitmap images to
> vector artwork or break apart the bitmap images.

1.  Select File \> Import \> Import To Stage or Import To Library.
2.  Select PNG Image from the Files Of Type (Windows) or Show (Macintosh) pop-up
    menu.
3.  Navigate to a Fireworks PNG image and select it.
4.  Click Open.
5.  Select one of the following for Location:

    **Import All Page(s) into New Scene(s)**  
    Imports all pages in the PNG file as scenes within a movie clip, with all of
    their frames and layers intact inside the movie clip symbol. A new layer is
    created that uses the name of the Fireworks PNG file name. The first frame
    (page) of the PNG document is placed on a keyframe that starts at the last
    keyframe; all other frames (pages) follow.

    **Import One Page into Current Layer**  
    Imports the selected page (identified in the Page Name pop-up menu) of the
    PNG file into the current Flash Pro document in a single new layer as a
    movie clip. The contents of the selected page are imported as a movie clip,
    with all of their original layer and frame structure intact. If the page
    movie clip has frames inside it, each frame is a movie clip in itself.

    **Page Name**  
    Specifies the Fireworks page you want to import into the current scene.

6.  Select one of the following for File Structure:

    **Import As Movie Clip And Retain Layers**  
    Imports the PNG file as a movie clip, with all of its frames and layers
    intact inside the movie clip symbol.

    **Import Page(s) as New Layer(s)**  
    Imports the PNG file into the current Flash Pro document in a single new
    layer at the top of the stacking order. The Fireworks layers are flattened
    into the single layer. The Fireworks frames are contained in the new layer.

7.  For Objects, select one of the following:

    **Rasterize If Necessary To Maintain Appearance**  
    Preserves Fireworks fills, strokes, and effects in Flash Pro.

    **Keep All Paths Editable**  
    Keeps all objects as editable vector paths. Some Fireworks fills, strokes,
    and effects are lost on import.

8.  For Text, select one of the following:

    **Rasterize If Necessary To Maintain Appearance**  
    Preserves Fireworks fills, strokes, and effects in text imported into Flash
    Pro.

    **Keep All Paths Editable**  
    Keeps all text editable. Some Fireworks fills, strokes, and effects are lost
    on import.

9.  To flatten the PNG file into a single bitmap image, select Import As A
    Single Flattened Bitmap. When this option is selected, all other options are
    dimmed.
10. Click OK.

More Help topics

[Edit a bitmap in an external editor](./imported-bitmaps-and-flash.md#edit-a-bitmap-in-an-external-editor)

[Break apart a bitmap and create a bitmap fill](./imported-bitmaps-and-flash.md#break-apart-a-bitmap-and-create-a-bitmap-fill)
