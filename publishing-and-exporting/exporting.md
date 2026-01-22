# Exporting

## Exporting images and graphics

### FXG graphic interchange format

#### About FXG files

The FXG format is a graphic interchange file format for the Flash Platform. FXG
is based on a subset of MXML, the XML-based programming language used by the
Flex framework. The FXG format helps designers and developers collaborate more
efficiently by enabling them to exchange graphic content with high fidelity.
Designers can create graphics using Adobe design tools and export them into the
FXG format. You can then use the FXG file in tools such as Adobe Flash Builder
and Adobe Flash Catalyst to develop rich Internet experiences and applications.

You can work with the FXG file format in the following Adobe applications:

- Fireworks CS5 (export)

- Photoshop CS5 (export)

- Illustrator (export)

- Flash Professional CS5 (import and export)

- Flash Catalyst (import and export)

- Flash Builder 4 (import and export)

When creating an FXG file, vector graphics are stored directly within the file.
Elements for which there is no corresponding tag in FXG are exported as bitmap
graphics which are then referenced in the FXG file. These include bitmaps, some
filters, some blend modes, gradients, masks, and 3D. Some of these effects may
be able to be exported as FXG, but may not be able to imported by the
application that opens the FXG file.

When you export a file containing vector and bitmap images using FXG export, a
separate folder is created along with the FXG file. This folder has the name
\<filename.assets\> and contains the bitmap images associated with the FXG file.

For more information about the FXG file format, see the
[FXG 2.0 Specification](https://web.archive.org/web/20120114054857/http://opensource.adobe.com/wiki/display/flexsdk/FXG+2.0+Specification).

#### FXG export constraints

Flash allows single or multiple selection of any objects on the stage for export
to FXG. Object and layer names are preserved when exporting to FXG format.

The following items are constrained when saving to an FXG file:

- Scale-9 grids: exported, but readable only by Adobe Illustrator.

- Sound and video: not exported.

- Components: not exported.

- Tweens and animation with multiple frames: not exported, but a selected frame
  will be exported as a static object.

- Embedded fonts: not exported.

- Button symbols: Flash exports only the Up state of buttons.

- 3D properties: not exported.

- Inverse Kinematics (IK) properties: not exported.

- Text attributes: some attributes may not be exported.

#### Export Flash content in FXG format

In Flash, you can export content in FXG format in two ways:

- To export objects on the Stage as FXG, select the objects and choose Export \>
  Export Selection. Then select FXG format from the File Type menu.

- To save the entire Stage as FXG, choose Export \> Export Image and select
  Adobe FXG from the File Type menu.

### JPEG Sequence and JPEG Image

These options match the JPEG Publish Settings options with one exception: Match
Screen matches the exported image to the size of the Flash Pro content as it
appears on your screen. Match Movie matches the JPEG image to the Flash Pro
content and maintains the aspect ratio of the original image.

### PNG Sequence and PNG Image

The PNG export settings options are similar to the PNG Publish Settings options
(which you can apply as well), with the following exceptions:

Dimensions  
Sets the size of the exported bitmap image to the number of pixels you enter in
the Width and Height fields.

Resolution  
Enter a resolution in dpi. To use the screen resolution and maintain the aspect
ratio of your original image, select Match Screen.

Colors  
The same as the Bit Depth option in the PNG Publish Settings tab and sets the
number of bits per pixel to use in creating the image. For a 256‑color image,
select 8‑bit; for thousands of colors, select 24‑bpc; for thousands of colors
with transparency (32 bpc) select 24‑bpc with Alpha. The higher the bit depth,
the larger the file.

Include  
Select to export the minimum image area or specify the full document size.

Filter  
Options match those in the PNG Publish Settings tab.

### Animated GIF, GIF Sequence, and GIF Image

The settings are the same as those on the GIF tab in the Publish Settings dialog
box, with the following exceptions:

Resolution  
Set in dots per inch (dpi). To use the screen resolution, enter a resolution or
click Match Screen.

Include  
Export the minimum image area or the full document size.

Colors  
Set the number of colors that can be used to create the exported image. The
color choices are: black and white, 4, 6, 16, 32, 64, 128, or 256 colors; or
Standard Color (the standard 216-color, web-safe palette).

Animation  
Available for the Animated GIF export format only. Enter the number of
repetitions, where 0 repeats endlessly.

### Bitmap (BMP) image

Create bitmap images for use in other applications. The Export Bitmap dialog box
has the following options:

Dimensions  
Sets the size of the exported bitmap image in pixels. The size you specify
always has the same aspect ratio as your original image.

Resolution  
Sets the resolution of the exported bitmap image in dots per inch (dpi) and
automatically calculates width and height based on the size of your drawing. To
set the resolution to match your monitor, select Match Screen.

Color Depth  
Specifies the bit depth of the image. Some Windows applications do not support
the newer 32‑bit per channel (bpc) depth for bitmap images; if you have problems
using a 32‑bpc format, use the 24‑bpc format.

Smooth  
Applies anti-aliasing to the exported bitmap. Anti-aliasing produces a
higher-quality bitmap image, but it can create a halo of gray pixels around an
image placed on a colored background. Deselect if a halo appears.

### Flash document (SWF)

To place the Flash Pro content in another application, such as Dreamweaver,
export the entire document as a SWF file. Flash Pro exports the SWF file using
the current settings from the Flash tab of the Publish Settings for the FLA
file.

## Exporting video and sound

### About Video for Adobe Flash Player (FLV)

With Flash Pro, you can import or export video with encoded audio. Flash can
import FLV video and export FLV or QuickTime (MOV). Use video with
communications applications, such as video conferencing or files that contain
screen-share encoded data exported from Adobe's Flash Media Server.

When you export video clips from Flash in FLV format with streaming audio, the
Streaming Sound dialog box settings compress the audio.

Files in the FLV format are compressed with the Sorensen codec.

### Export a copy of an FLV file from the Library

1.  Right-click the FLV video clip in the Library panel.
2.  Choose Properties from the context menu.
3.  In the Video Properties dialog box, click Export.
4.  Enter a name for the exported file. Select a location to save it to, click
    Save, and click OK.

### About QuickTime

Flash Pro provides two methods of exporting Flash Pro documents as QuickTime:
QuickTime export  
Exports a QuickTime file that can be distributed as streaming video, on a DVD,
or used in a video editing application such as Adobe® Premiere Pro®. QuickTime
export is intended for users who want to distribute Flash Pro content, such as
animation, in the QuickTime video format.

Be aware that the performance of the computer used to export QuickTime video may
affect the quality of the video. If Flash is unable to export each frame, it
will drop frames, resulting in poor video quality. If you encounter dropped
frames, try using a faster computer with more memory or reduce the frames per
second of the Flash document.

Publish as QuickTime  
Creates an application with a Flash Pro track in the same QuickTime format
installed on your computer. This lets you combine the interactive features of
Flash Pro with the multimedia and video features of QuickTime in a single
QuickTime 4 movie, which anyone with QuickTime 4 or later can view. If you
import a video clip (in any format) into a document as an embedded file, you can
publish the document as a QuickTime movie. If you import a video clip in
QuickTime format into a document as a linked file, you can also publish the
document as a QuickTime movie.

Exports all layers in the Flash Pro document as a single Flash Pro track, unless
the document contains an imported QuickTime movie. The imported QuickTime movie
remains in QuickTime format in the exported application.

### Export QuickTime

1.  Select File \> Export \> Export Movie.
2.  Specify settings for the QuickTime movie to export. By default, QuickTime
    export creates a movie file using the same dimensions as the source Flash
    document and exports the Flash document in its entirety. The Export
    QuickTime Video dialog box contains the following options:

    **Dimensions**  
    The width and height in pixels for the frames of the QuickTime movie. You
    can specify only the width or the height; the other dimension is
    automatically set to maintain the aspect ratio of your original document. To
    set both the width and the height independently of each other, deselect
    Maintain Aspect Ratio.

    > **Note:** If the dimensions of the video are particularly large (for
    > example, 740 x 480 pixels), you may need to change the frame rate of the
    > movie to avoid dropping frames.

    > **Note:** The Dimensions option you set in the QuickTime Export Settings
    > dialog is for the width and height of the FLA file exported as video. The
    > dimensions you set in the QuickTime Settings dialog specify the size of
    > the exported QuickTime movie. If you do not change the size in the later
    > dialog, it remains as "current" so you do not need to change it.

    **Ignore stage color**  
    Creates an alpha channel using the stage color. The alpha channel is encoded
    as a transparent track, letting you overlay the exported QuickTime movie on
    top of other content to alter the background color or scene.

    To create a QuickTime video with an alpha channel, you must select a video
    Compression Type that supports 32-bit encoding with an alpha channel. Codecs
    that support this are Animation, PNG, Planar RGB, JPEG 2000, TIFF, or TGA.
    You must also select Million of Color+ from the Compressor/Depth setting. To
    set the compression type and color depth, click the Settings button in the
    Video category of the Movie Settings dialog box.

    When last frame is reached Exports the entire Flash document as a movie
    file.

    After time has elapsed The duration of the Flash document to export in
    hours:minutes:seconds:milliseconds.

    **QuickTime Settings**  
    Opens the advanced QuickTime settings dialog box. The Advanced settings let
    you specify custom QuickTime settings. In general, use the default QuickTime
    settings, as they provide optimal playback performance for most
    applications. To modify the QuickTime settings, see the documentation
    provided with Apple QuickTime Pro for information on the available video
    parameters.

3.  Click export.

### Windows AVI (Windows)

Exports a document as a Windows video but discards any interactivity. Good for
opening a Flash Pro animation in a video-editing application. Because AVI is a
bitmap-based format, documents that contain long or high-resolution animations
can quickly become very large.

The Export Windows AVI dialog box has the following options:

Dimensions  
Specifies a width and height, in pixels, for the frames of an AVI movie. Specify
only the width or the height; the other dimension is automatically set to
maintain the aspect ratio of your original document. To set both the width and
the height, deselect Maintain Aspect Ratio.

Video Format  
Selects a color depth. Some applications do not yet support the Windows 32‑bpc
image format. If this format presents problems, use the older 24‑bpc format.

Compress Video  
Select standard AVI compression options.

Smooth  
Applies anti-aliasing to the exported AVI movie. Anti-aliasing produces a
higher-quality bitmap image, but it can cause a halo of gray pixels to appear
around images when placed over a colored background. Deselect if a halo appears.

Sound Format  
Set the sample rate and size of the sound track, and whether to export in mono
or stereo. The smaller the sample rate and size, the smaller the exported file,
with a possible trade-off in sound quality.

### WAV audio (Windows)

Exports only the sound file of the current document to a single WAV file. You
can specify the sound format of the new file.

To determine the sampling frequency, bit rate, and stereo or mono setting of the
exported sound, select Sound Format. To exclude events sounds from the exported
file, select Ignore Event Sounds.

More Help topics

[Specify publish settings for JPEG files (CS5)](./publish-settings-cs5.md#specify-publish-settings-for-jpeg-files-cs5)

[Specify publish settings for PNG files (CS5)](./publish-settings-cs5.md#specify-publish-settings-for-png-files-cs5)

[Specify publish settings for Flash Player detection (CS5)](./publish-settings-cs5.md#specify-publish-settings-for-flash-player-detection-cs5)

[Publishing Flash documents](./publishing-flash-documents.md)

[Import Adobe Illustrator files](../using-imported-artwork/working-with-illustrator-ai-files-in-flash.md#import-adobe-illustrator-files)

[Specify publish settings for SWF files (CS5)](./publish-settings-cs5.md#specify-publish-settings-for-swf-files-cs5)

[Video formats and Flash](../video/create-video-files-for-use-in-flash.md#video-formats-and-flash)

[About compressing sounds for export](../sound/exporting-sounds.md#about-compressing-sounds-for-export)
