# Placing artwork into Flash

## About importing artwork into Flash

Adobe® Flash® Professional CS5 can use artwork created in other applications.
You can import vector graphics and bitmaps in a variety of file formats. If you
have QuickTime® 4 or later installed on your system, you can import additional
vector or bitmap file formats. You can import Adobe® FreeHand® files (version MX
and earlier) and Adobe® Fireworks® PNG files directly into Flash Pro, preserving
attributes from those formats.

Graphic files that you import into Flash Pro must be at least 2 pixels x
2 pixels in size.

To load JPEG files into a Flash Pro SWF file during runtime, use the `loadMovie`
action or method. For detailed information, see loadMovie (MovieClip.loadMovie
method) in
[_ActionScript 2.0 Language Reference_](https://web.archive.org/web/20120101020625mp_/http://www.adobe.com/go/learn_cs5_as2lr_en)
or
[Working with movie clips](https://web.archive.org/web/20120101020625mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b90204-7e1d.html)
in the _ActionScript 3.0 Developer's Guide_.

Flash Pro imports vector graphics, bitmaps, and sequences of images as follows:

- When you import Adobe® Illustrator® and Adobe® Photoshop® files into Flash
  Pro, you can specify import options that let you preserve most of your
  artwork's visual data, and the ability to maintain the editability of certain
  visual attributes with the Flash Pro authoring environment.

- When you import vector images into Flash Pro from FreeHand, select options for
  preserving FreeHand layers, pages, and text blocks.

- When you import PNG images from Fireworks, import files as editable objects to
  modify in Flash Pro, or as flattened files to edit and update in Fireworks.

- Select options for preserving images, text, and guides.

  > **Note:** If you import a PNG file from Fireworks by cutting and pasting,
  > the file is converted to a bitmap.

- Vector images from SWF and Windows® Metafile Format (WMF) files that you
  import directly into a Flash Pro document (instead of into a library) are
  imported as a group in the current layer.

- Bitmaps (scanned photographs, BMP files) that you import directly into a Flash
  Pro document are imported as single objects in the current layer. Flash Pro
  preserves the transparency settings of imported bitmaps. Because importing a
  bitmap can increase the file size of a SWF file, consider compressing imported
  bitmaps.

  > **Note:** Bitmap transparency might not be preserved when bitmaps are
  > imported by dragging and dropping from an application or desktop to Flash
  > Pro. To preserve transparency, use the File \> Import To Stage or Import To
  > Library command for importing.

- Any sequence of images (for example, a PICT or BMP sequence) that you import
  directly into a Flash Pro document is imported as successive keyframes of the
  current layer.

## Supported file formats for import

> **Note:** For a complete list of every file format supported by Flash for
> import, export, or edit, see the
> [Supported File Formats](https://web.archive.org/web/20120101020625mp_/http://kb2.adobe.com/cps/402/kb402701.html)
> TechNote.

**Graphics formats**

Flash Pro can import different vector or bitmap file formats depending on
whether QuickTime 4 or later is installed on your system. Using Flash Pro with
QuickTime 4 installed is especially useful for collaborative projects in which
authors work on both Windows and Macintosh platforms. QuickTime 4 extends
support for certain file formats (including PICT, QuickTime Movie, and others)
to both platforms.

You can import the following vector or bitmap file formats into Flash Pro 8 or
later, regardless of whether QuickTime 4 is installed: | File type | Extension |
Windows | Macintosh | | ----------------------------------------- | --------- |
------- | --------- | | Adobe Illustrator (version 10 or earlier) | .ai | • | •
| | Adobe Photoshop | .psd | • | • | | AutoCAD® DXF | .dxf | • | • | | Bitmap |
.bmp | • | • | | Enhanced Windows Metafile | .emf | • |   | | FutureSplash
Player | .spl | • | • | | GIF and animated GIF | .gif | • | • | | JPEG | .jpg |
• | • | | PNG | .png | • | • | | Flash Player 6/7 | .swf | • | • | | Windows
Metafile | .wmf | • | • | | Adobe XML Graphic file | .fxg | • | • | You can
import the following bitmap file formats into Flash Pro only if QuickTime 4 or
later is installed: | File type | Extension | Windows | Macintosh | |
--------------- | --------- | ------- | --------- | | QuickTime Image | .qtif |
• | • | | TIFF | .tif | • | • | **Sound formats**

Flash can import the following audio formats: | File type | Extension | Windows
| Macintosh | | ----------------------------- | --------- | ------- | ---------
| | Adobe Soundbooth | .asnd | • | • | | Wave | .wav | • |   | | Audio
Interchange File Format | .aiff |   | • | | MP3 | .mp3 | • | • | Flash can
import the following audio formats only if QuickTime 4 or later is installed: |
File type | Extension | Windows | Macintosh | | ----------------------------- |
--------- | ------- | --------- | | Audio Interchange File Format | .aiff | • |
• | | Sound Designer II | .sd2 |   | • | | Sound-only QuickTime movies | .mov,
.qt | • | • | | Sun AU | .au | • | • | | System 7 sounds | .snd |   | • | | Wave
| .wav | • | • | **Video formats**

Flash can import the following video formats: | File type | Extension | Windows
| Macintosh | | ----------------------------- |
------------------------------------------------------ | ------- | --------- | |
Video for Adobe Flash | .flv, .f4v | • | • | | QuickTime Movie | .mov, .qt | • |
• | | Video for Windows | .avi | • | • | | MPEG | .mpg, .m1v, .m2p, .m2t, .m2ts,
.mts, .tod, .mpe, .mpeg | • | • | | MPEG-4 | .mp4, .m4v, .avc | • | • | |
Digital Video | .dv, .dvi | • | • | | 3GPP/3GPP2 for Mobile Devices | .3gp,
.3gpp, .3gp2, .3gpp2, .3p2 | • | • |

## Import artwork in Flash

Flash Pro lets you import artwork in various file formats either directly to the
Stage, or to the library.

### Import a file into Flash

1.  Do one of the following:
    - To import a file directly into the current Flash Pro document, select
      File \> Import \> Import To Stage.

    - To import a file into the library for the current Flash Pro document,
      select File \> Import \> Import To Library. (To use a library item in a
      document, drag it onto the Stage. )

2.  Select a file format from the Files Of Type (Windows) or Show (Macintosh)
    pop-up menu.
3.  Navigate to the desired file and select it. If an imported file has multiple
    layers, Flash Pro might create new layers (depending on the import file
    type). Any new layers appear in the Timeline.
4.  Click Open.
5.  If the name of the file you are importing ends with a number and additional
    sequentially numbered files are in the same folder, do one of the following:
    - To import all the sequential files, click Yes.

    - To import only the specified file, click No.

      The following are examples of filenames that can be used as a sequence:
      - Frame001.gif, Frame002.gif, Frame003.gif

      - Bird 1, Bird 2, Bird 3

      - Walk-001.ai, Walk-002.ai, Walk-003.ai

### Paste a bitmap from another application directly into the current Flash document

1.  Copy the image in the other application.
2.  In Flash Pro, select Edit \> Paste In Center.

## Importing FXG files

The FXG format allows Flash to exchange graphics with other Adobe applications
such as Adobe Illustrator, Fireworks, and Photoshop with all of the complex
graphic information preserved. Flash allows you to import FXG files (2.0 version
only) as well as save selections of objects on the Stage or the entire Stage in
FXG format. For more information about FXG files, see
[About FXG files](../publishing-and-exporting/exporting.md#about-fxg-files).

- To import an FXG file, choose File \> Import \> Import to Stage or Import to
  Library and select the FXG file you want to open.

## About AutoCAD DXF files

Flash Pro supports the AutoCAD® DXF format in AutoCAD 10.

DXF files do not support the standard system fonts. Flash Pro tries to map fonts
appropriately, but the results can be unpredictable, particularly for text
alignment.

Because the DXF format does not support solid fills, filled areas are exported
as outlines only. For this reason, the DXF format is most appropriate for line
drawings, such as floor plans and maps.

You can import two-dimensional DXF files into Flash Pro. Flash Pro does not
support three-dimensional DXF files.

Although Flash Pro doesn't support scaling in a DXF file, all imported DXF files
produce 12-inch x 12-inch files that you can scale using Modify \> Transform \>
Scale. Also, Flash Pro supports only ASCII DXF files. If your DXF files are
binary, convert them to ASCII before importing them into Flash Pro.

## Loading artwork with ActionScript

With ActionScript, you can load external image files or assets from the Library
at runtime.

For information about working with images and assets in ActionScript, see the
following article:

- [Loading images and Library assets in Flash with ActionScript 3](https://web.archive.org/web/20120101020625mp_/http://www.adobe.com/devnet/flash/quickstart/loading_images_library_as3/)
  (Adobe.com)

More Help topics

[Imported bitmaps and Flash](./imported-bitmaps-and-flash.md)

[Video](../video/index.md)

[Sound](../sound/index.md)

[Set bitmap properties](./imported-bitmaps-and-flash.md#set-bitmap-properties)

[Symbols, instances, and library assets](../symbols-instances-and-library-assets/index.md)
