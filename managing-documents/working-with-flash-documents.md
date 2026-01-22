# Working with Flash documents

## About Flash files

In Flash Pro, you can work with a variety of file types, each of which has a
separate purpose:

- **FLA files**, the primary files you work with in Flash Pro, contain the basic
  media, timeline, and script information for a Flash Pro document. _Media
  objects_ are the graphic, text, sound, and video objects that comprise the
  content of your Flash Pro document. The _Timeline_ is where you tell Flash Pro
  when specific media objects should appear on the Stage. You can add
  *ActionScript*® code to Flash Pro documents to more finely control their
  behavior and to make them respond to user interactions.

- **Uncompressed XFL** files are similar to FLA files. An XFL file, and the
  other associated files inside the same folder, are simply the uncompressed
  equivalent of a FLA file. This format makes it easier for groups of users to
  work on different elements of a flash project at the same time. For more
  information, see
  [Working with uncompressed XFL files](#working-with-uncompressed-xfl-files).

- **SWF files**, the compiled versions of FLA files, are the files you display
  in a web page. When you publish your FLA file, Flash Pro creates a SWF file.

  The Flash Pro SWF file format is an open standard that other applications
  support.

- **AS files** are ActionScript files—you can use these to keep some or all of
  your ActionScript code outside of your FLA files, which is helpful for code
  organization and for projects that have multiple people working on different
  parts of the Flash Pro content.

- **SWC files** contain the reusable Flash Pro components. Each SWC file
  contains a compiled movie clip, ActionScript code, and any other assets that
  the component requires.

- **ASC files** are files used to store ActionScript that will be executed on a
  computer running Flash Media Server. These files provide the ability to
  implement server-side logic that works in conjunction with ActionScript in a
  SWF file.

- **JSFL files** are JavaScript files that you can use to add new functionality
  to the Flash Pro authoring tool.

The following additional tutorials demonstrate working with Flash Pro. Some
videos may show Flash Pro CS3 or CS4, but are still applicable to Flash Pro CS5.

- Tutorial:
  [Creating your first Flash Professional CS5 document](https://web.archive.org/web/20120101020635mp_/http://www.adobe.com/devnet/flash/articles/flash_cs5_createfla.html)

## Working with other Adobe applications

Flash is designed to work with other Adobe® applications to enable a broad range
of creative workflows. You can import Illustrator® and Photoshop® files directly
into Flash. You can also create video from Flash and edit it in Adobe® Premiere®
Pro or After Effects®, or import video from either of those applications into
Flash. When publishing your SWF files, you can use Dreamweaver® to embed the
content in your web pages and launch Flash directly from within Dreamweaver to
edit the content.

## Opening XFL files

Beginning with Flash Professional CS5, XFL is the internal format of the FLA
files you create. When you save a file in Flash, the default format is FLA, but
the internal format of the file is XFL.

Other Adobe® applications such as After Effects® can export files in XFL format.
These files have the XFL file extension instead of the FLA extension. InDesign®
can export directly in FLA format, which internally is XFL. This allows you to
work on a project in After Effects or InDesign first and then continue working
with it in Flash.

You can open and work with XFL files in Flash in the same way you would open an
FLA file. When you open an XFL file in Flash Pro, you can then save the file as
a FLA file, or as an uncompressed XFL file.

To open an XFL file in Flash:

1.  In another Adobe® application, such as InDesign or After Effects, export
    your work as an XFL file.

    The application preserves all of the layers and objects of the original file
    in the XFL file.

2.  In Flash Pro, choose File \> Open and navigate to the XFL file. Click Open.

    The XFL file opens in Flash in the same way as an FLA file. All of the
    layers of the original file appear in the Timeline and the original objects
    appear in the Library panel.

    You can now work with the file normally.

3.  To save the file, choose File \> Save.

    Flash Pro prompts you to name the new FLA file in the Save As dialog box.

4.  Type a name and save the FLA file.

## Working with uncompressed XFL files

Beginning with Flash Professional CS5, you can choose to work with your Flash
files in uncompressed XFL format. This format allows you to see each of the
separate parts, or subfiles, that make up the Flash file. These parts include:

- An XML file that describes the Flash file as a whole.

- Separate XML files to describe each Library symbol.

- Additional XML files containing publish settings, mobile settings, and others.

- Folders containing external assets, such as bitmap files, used by the Flash
  file.

By working with uncompressed XFL format, you can allow each part of the Flash
file to be worked on separately by different people. You can also use a source
control system to manage the changes made to each subfile within your
uncompressed XFL file. Together, these capabilities allow for much easier
collaboration on larger projects with multiple designers and developers.

#### Using live update with XFL files

With live update of editable assets for Uncompressed XFL Documents, you can edit
any Library asset from an uncompressed XFL document while the document is open
in Flash. Your changes to the asset are reflected in Flash when you finish
editing the asset in another application.

To edit an asset from an uncompressed XFL document in another application:

1.  Save a Flash document in Uncompressed XFL format.

2.  In an appropriate editor, such as Photoshop, open the asset you want to edit
    from the LIBRARY folder of the Uncompressed XFL Document.

3.  Edit the asset and save your changes.

4.  Return to Flash Pro.

    The update to the asset is reflected in Flash immediately.

## Edit a SWF file from Dreamweaver in Flash

If you have both Flash and Dreamweaver installed, you can select a SWF file in a
Dreamweaver document and use Flash to edit it. Flash does not edit the SWF file
directly; it edits the source document (FLA file) and re‑exports the SWF file.

1.  In Dreamweaver, open the Property inspector (Window \> Properties).

2.  In the Dreamweaver document, do one of the following:
    - Click the SWF file placeholder to select it; then in the Property
      inspector click Edit.

    - Right-click (Windows) or Control-click (Macintosh) the placeholder for the
      SWF file, and select Edit With Flash from the context menu.

      Dreamweaver switches the focus to Flash, and Flash attempts to locate the
      Flash authoring file (FLA) for the selected SWF file. If Flash cannot
      locate the Flash authoring file, you are prompted to locate it.

      > **Note:** If the FLA file or SWF file is locked, check out the file in
      > Dreamweaver.

3.  In Flash, edit the FLA file. The Flash Document window indicates that you
    are modifying the file from within Dreamweaver.

4.  When you finish making edits, click Done.

    Flash updates the FLA file, re‑exports it as a SWF file, closes, and then
    returns the focus to the Dreamweaver document.

    > **Note:** To update the SWF file and keep Flash open, in Flash select
    > File \> Update for Dreamweaver.

5.  To view the updated file in the document, click Play in the Dreamweaver
    Property inspector or press F12 to preview your page in a browser window.

## Create mobile content with Adobe Device Central and Flash

1.  Start Flash.

2.  On the main Flash screen, select Create New \> Flash File (Mobile).

    Flash opens Adobe® Device Central and displays the New Document tab.

3.  In Device Central, select a Player version and ActionScript version.

    The Available Devices list on the left is updated. Devices that do not
    support the selected Player version and ActionScript version are dimmed.

4.  Select a content type.

    The Available Devices list on the left is updated and shows the devices that
    support the content type (as well as the Player version and ActionScript
    version) selected.

5.  In the Available Devices list, select a single target device or multiple
    devices (or select a set or individual device in the Device Sets list).

    Device Central lists proposed document sizes based on the device or devices
    you selected (if the devices have different display sizes). Depending on the
    design or content you are developing, you can create a separate mobile
    document for each display size or try to find one size appropriate for all
    devices. When choosing the second approach, you may want to use the smallest
    or largest suggested document size as a common denominator. You can even
    specify a custom size at the bottom of the tab.

6.  Click Create.

    Flash starts up and creates a document with preset publish settings from
    Device Central, including the correct size for the device (or group of
    devices) specified.

7.  Add content to the new Flash document.

8.  To test the document, select Control \> Test Movie \> Test.

    The new document is displayed in the Device Central Emulator tab. If one or
    more devices were selected in the Available Devices list in step 5, a new
    device set is created (named according to the FLA file) and listed in the
    Device Sets panel. The device shown in the Emulator tab is listed in the
    Device Sets panel with a special icon ![](../img/active_device.png). To test
    the new Flash document on another device, double-click the name of a
    different device in the Device Sets or Available Devices lists.

## Create a new document

You can create a new document or open a previously saved document in Flash Pro,
and you can open a new window as you work. You can set properties for new or
existing documents.

### Create a new document

1.  Select File \> New.
2.  On the General tab, select the type of Flash document you want to create.
3.  Do one of the following:
    - (CS5.5 only) Choose Height, Width, Frame Rate, and other settings on the
      right side of the dialog box.

    - Choose settings for the document. See
      [Set properties for a new or existing document](#set-properties-for-a-new-or-existing-document).

### Create a new document from a template

1.  Select File \> New.
2.  Click the Templates tab.
3.  Select a category from the Category list, select a document from the
    Category Items list, and click OK. You can select standard templates that
    come with Flash Pro or a template you have already saved.

### Open an existing document

1.  Select File \> Open.
2.  In the Open dialog box, navigate to the file or enter the path to the file
    in the Go To box.
3.  Click Open.

### View a document when multiple documents are open

When you open multiple documents, tabs at the top of the Document window
identify the open documents and let you easily navigate among them. Tabs appear
only when documents are maximized in the Document window.

![](../img/dingbat.png) Click the tab of the document you want to view.

By default, tabs appear in the order in which the documents were created. You
can drag the document tabs to change their order.

### Open a new window for the current document

![](../img/dingbat.png) Select Window \> Duplicate Window.

### Set properties for a new or existing document

1.  With the document open, select Modify \> Document.

    The Document Settings dialog box appears.

2.  To set the Dimensions of the Stage do one of the following:
    - To specify the Stage size in pixels, enter values in the Width and Height
      boxes. The minimum size is 1 x 1 pixels; the maximum is 2880 x 2880
      pixels.

    - To match the Stage size to the exact amount of space used by the contents
      of the Stage, select the Match Contents option.

    - To set the Stage size to the maximum available print area, select Match
      Printer. This area is determined by the paper size minus the current
      margin selected in the Margins area of the Page Setup dialog box (Windows)
      or the Print Margins dialog box (Macintosh).

    - To set the Stage size to the default size, 550 x 400 pixels, select Match
      Default.

3.  To adjust the position and orientation of 3D objects on the Stage to
    maintain their appearance relative to the edges of the Stage, select Adjust
    3D Perspective Angle to Preserve Current Stage Projection.

    This option is only available if you change the Stage size.

4.  (CS5.5 only) To automatically scale the contents of the stage relative to
    the change in Stage size, select Scale Content With Stage.

    This option is only available if you change the Stage size. You can choose
    whether to scale content in locked and hidden layers in the Preferences. For
    more information, see
    [Set General preferences](../workspace/set-preferences-in-flash.md#set-general-preferences).

5.  To specify the unit of measure for rulers displayed in the work area, select
    an option from the Ruler Units menu. (This setting also determines the units
    used in the Info panel.)

6.  To set the background color of your document, click the Background Color
    swatch and select a color from the palette.

7.  For Frame Rate, enter the number of animation frames to appear every second.

    For most computer-displayed animations, especially those playing from a
    website, 8 frames per second (fps) to 15 fps is sufficient. When you change
    the frame rate, the new frame rate becomes the default for new documents.

8.  (CS5.5 only) To automatically save the document at a specified time
    interval, select the Auto-Save option and specify a number of minutes
    between saves.

9.  Do one of the following:
    - To apply the new settings to the current document only, click OK.

    - To make the new settings the default properties for all new documents,
      click Make Default.

### Change document properties using the Property inspector

1.  Click in the work area outside the Stage to deselect all objects on the
    Stage. The document properties appear in the Property inspector. To open the
    Property inspector, choose (Window \> Properties).
2.  (CS5.5 only) In the Publish section, choose a Flash Player version and an
    ActionScript version for your document. To access additional Publish
    settings, click the Publish Settings button. For more information, see
    [Publish settings (CS5)](../publishing-and-exporting/publish-settings-cs5.md).
3.  In the Properties section, for FPS (frames per second), enter the number of
    animation frames to play each second.
4.  To change the Stage size, enter values for the width and height of the
    Stage.
5.  To select a background color for the Stage , click the color swatch next to
    the Stage property and select a color from the palette.
6.  To edit additional document properties, click the Edit button next to the
    Size properties. For more information on all document properties, see
    [Set properties for a new or existing document](#set-properties-for-a-new-or-existing-document).

### Add XMP metadata to a document

You can include Extensible Metadata Platform (XMP) data such as title, author,
description, copyright, and more in your FLA files. XMP is a metadata format
that certain other Adobe® applications can understand. The metadata is viewable
in Flash Pro and in Adobe® Bridge. For more information about XMP metadata, see
_Metadata and Keywords_ in Bridge Help.

Embedding metadata improves the ability of web-based search engines to return
meaningful search results for Flash Pro content. The search metadata is based on
the XMP (Extensible Metadata Platform) specifications and is stored in the FLA
file in a W3C-compliant format.

A file's metadata contains information about the contents, copyright status,
origin, and history of the file. In the File Info dialog box, you can view and
edit the metadata for the current file.

Depending on the selected file, the following types of metadata may appear:

Description  
Contains author, title, copyright, and other information.

IPTC  
Displays editable metadata. You can add captions to your files, as well as
copyright information. IPTC Core is a specification that was approved by the
IPTC (International Press Telecommunications Council) in October 2004. It
differs from the older IPTC (IIM, legacy) in that new properties were added,
some property names were changed, and some properties were deleted.

Camera Data (Exif)  
Displays information assigned by digital cameras, including the camera settings
used when the image was taken.

Video Data  
Displays metadata for video files, including pixel aspect ratio, scene, and
shot.

Audio Data  
Displays metadata for audio files, including artist, album, track number, and
genre.

Mobile SWF  
Lists information about SWF files, including title, author, description, and
copyright.

History  
Keeps a log of changes made to images with Photoshop.

> **Note:** The History Log preference must be turned on in Photoshop for the
> log to be saved with the file's metadata.

Version Cue  
Lists any Version Cue file-version information.

DICOM  
Displays information about images saved in the Digital Imaging and
Communications in Medicine (DICOM) format.

To add metadata:

1.  Choose File \> File Info.
2.  In the File Info dialog box that appears, enter the metadata that you want
    to include. You can add or remove metadata in the FLA file at any time.

## Save Flash documents

You can save a Flash Pro FLA document using its current name and location or
using a different name or location.

When a document contains unsaved changes, an asterisk (\*) appears after the
document name in the document title bar, the application title bar, and the
document tab. When you save the document, the asterisk is removed.

### Save a Flash document in the default FLA format

1.  Do one of the following:
    - To overwrite the current version on the disk, select File \> Save.

    - To save the document in a different location and/or with a different name,
      or to compress the document, select File \> Save As.

2.  If you selected Save As, or if the document has never been saved before,
    enter the filename and location.
3.  Click Save.

### Save a document in uncompressed XFL format

1.  Choose File \> Save As.
2.  From the Save as Type menu, choose Flash CS5 or CS5.5 Uncompressed Document
    (\*xfl).
3.  Choose a name and location for the file and click Save.

### Revert to the last saved version of a document

![](../img/dingbat.png) Select File \> Revert.

### Save a document as a template

1.  Select File \> Save As Template.

2.  In the Save As Template dialog box, enter a name for the template in the
    Name box.

3.  Select a category from the Category pop‑up menu, or enter a name to create a
    new category.

4.  Enter a description of the template in the Description box (up to 255
    characters), and click OK.

    The description appears when the template is selected in the New Document
    dialog box.

    To delete a saved template, navigate to one of the following folders and
    delete the template FLA file from the category folder that contains it.
    - Windows XP -
      `C:\Documents and Settings\<userName>\Local Settings\Application Data\Adobe\Flash CS5\<language>\Configuration\Templates\`

    - Windows Vista and 7 -
      `C:\Users\<userName>\AppData\Local\Adobe\Flash CS5\<language>\Configuration\Templates\`

    - Mac OS -
      `<HardDisk>/Users/<userName>/Library/Application Support/Adobe/Flash CS5/<language>/Configuration/Templates/`

### Save a document as a Flash CS4 document

1.  Select File \> Save As.
2.  Enter the filename and location.
3.  Select Flash CS4 Document from the Format pop‑up menu, and click Save.

    > **Important:** If an alert message indicates that content will be deleted
    > if you save in Flash CS4 format, click Save As Flash CS4 to continue. This
    > might happen if your document contains features that are available only in
    > Flash CS5. Flash Pro does not preserve these features when you save the
    > document in Flash CS4 format.

### Save documents when quitting Flash

1.  Select File \> Exit (Windows) or Flash \> Quit Flash (Macintosh).
2.  If you have documents open with unsaved changes, Flash Pro prompts you to
    save or discard the changes for each document.
    - Click Yes to save the changes and close the document.

    - Click No to close the document without saving the changes.

## Printing Flash documents

### Print from Flash documents

To preview and edit your documents, print frames from
Adobe® Flash® Professional CS5 documents, or specify frames to be printable from
Flash Player by a viewer.

When printing frames from a Flash Pro document, use the Print dialog box to
specify the range of scenes or frames to print and the number of copies. In
Windows, the Page Setup dialog box specifies paper size, orientation, and
various print options—including margin settings and whether all frames are to be
printed for each page. On the Macintosh, these options are divided between the
Page Setup and the Print Margins dialog boxes.

The Print and Page Setup dialog boxes are standard in either operating system,
and their appearance depends on the selected printer driver.

1.  Select File \> Page Setup (Windows) or File \> Print Margins (Macintosh).
2.  Set page margins. Select both Center options to print the frame in the
    center of the page.
3.  In the Frames menu, select whether to print all frames in the document or
    only the first frame of each scene.
4.  In the Layout menu, select from the following options:

    **Actual Size**  
    Prints the frame at full size. Enter a value for Scale to reduce or enlarge
    the printed frame.

    **Fit On One Page**  
    Reduces or enlarges each frame so it fills the print area of the page.

    **Storyboard**  
    Prints several thumbnails on one page. Select from Boxes, Grid, or Blank.
    Enter the number of thumbnails per page in the Frames box. Set the space
    between the thumbnails in the Frame Margin box, and select Label Frames to
    print the frame label as a thumbnail.

5.  To print frames, select File \> Print.

### Use frame labels to disable printing

To choose not to print any of the frames in the main Timeline, label a frame as
`!#p` to make the entire SWF file nonprintable. Labeling a frame as `!#p` dims
the Print command in the Flash Player context menu. You can also remove the
Flash Player context menu.

If you disable printing from Flash Player, the user can still use the browser
Print command to print frames. Because this command is a browser feature, you
cannot use Flash Pro to control or disable it.

#### Disable printing in the Flash Player context menu

1.  Open or make active the Flash Pro document (FLA file) to publish.

2.  Select the first keyframe in the main Timeline.

3.  Select Window \> Properties to view the Property inspector.

4.  In the Property inspector, for Frame Label enter `!#p` to specify the frame
    as non-printing.

    Specify only one `!#p` label to dim the Print command in the context menu.

    > **Note:** You can also select a blank frame (rather than a keyframe) and
    > label it `#p`.

#### Disable printing by removing the Flash Player context menu

1.  Open or make active the Flash Pro document (FLA file) to publish.
2.  Select File \> Publish Settings.
3.  Select the HTML tab and deselect Display Menu and click OK.

### Specify a print area when printing frames

1.  Open the Flash Pro document (FLA file) containing the frames you will set to
    print.

2.  Select a frame that you have not specified to print with a `#p` frame label
    that is on the same layer as a frame that is labeled with a `#p`.

    To organize your work, select the next frame after a frame labeled `#p`.

3.  Create a shape on the Stage the size of the desired print area. To use a
    frame's bounding box, select a frame with any object of the appropriate
    print area size.

4.  Select the frame in the Timeline that contains the shape to use for the
    bounding box.

5.  In the Property inspector (Window \> Properties), enter `#b` for Frame Label
    to specify the selected shape as the bounding box for the print area.

    Only one `#b` frame label per Timeline is allowed. This option is the same
    as selecting the Movie bounding box option with the Print action.

### Change the printed background color

You can print the background color set in the Document Properties dialog box.
Change the background color for only the frames to be printed by placing a
colored object on the lowest layer of the Timeline being printed.

1.  Place a filled shape that covers the Stage on the lowest layer of the
    Timeline that will print.

2.  Select the shape and select Modify \> Document. Select a color for the
    printing background.

    This action changes the entire document's background color, including that
    of movie clips and loaded SWF files.

3.  Do one of the following:
    - To print that color as the document's background, designate to print the
      frame in which you placed the shape.

    - To maintain a different background color for non-printing frames, repeat
      steps 2 and 3. Then place the shape on the lowest layer of the Timeline,
      in all the frames that are not designated to print.

### Print from the Flash Player context menu

Use the Print command in the Flash Player context menu to print frames from any
Flash Pro SWF file.

The context menu's Print command cannot print transparency or color effects and
cannot print frames from other movie clips; for more advanced printing
capabilities, use the `PrintJob` object or the `print()` function.

1.  Open the document.

    The command prints the frames labeled `#p` by using the Stage for the print
    area or the specified bounding box.

    If you haven't designated specific frames to print, all frames in the
    document main Timeline print.

2.  Select File \> Publish Preview \> Default or press F12 to view your Flash
    Pro content in a browser.

3.  Right-click (Windows) or Control‑click (Macintosh) in the Flash Pro content
    in the browser window to display the Flash Player context menu.

4.  Select Print from the Flash Player context menu to display the Print dialog
    box.

5.  In Windows, select the print range to select which frames to print.

6.  On the Macintosh, in the Print dialog box, select the pages to print.

7.  Select other print options, according to your printer's properties.

8.  Click OK (Windows) or Print (Macintosh).

> **Note:** Printing from the context menu does not interact with calls to the
> `PrintJob` object.

More Help topics

[About the Timeline](../workspace/the-timeline.md#about-the-timeline)

[Working with Illustrator and Flash](../using-imported-artwork/working-with-illustrator-ai-files-in-flash.md#working-with-illustrator-and-flash)

[Working with Photoshop and Flash](../using-imported-artwork/working-with-photoshop-psd-files-in-flash.md#working-with-photoshop-and-flash)

[Working with Adobe Premiere Pro and After Effects](../video/working-with-adobe-premiere-pro-and-after-effects.md)

[Set preferences in Flash](../workspace/set-preferences-in-flash.md)

[Publishing and Exporting](../publishing-and-exporting/index.md)

[Printing at runtime](../actionscript/printing-at-runtime.md)

[Publishing overview](../publishing-and-exporting/publishing-flash-documents.md#publishing-overview)
