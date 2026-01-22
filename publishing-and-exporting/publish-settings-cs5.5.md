# Publish settings (CS5.5)

## Specify publish settings for Flash (.swf) files (CS5.5)

> **Note:** CS5.5 only - You can also specify the Publish settings for Player
> version and ActionScript version in the Property inspector. Deselect all items
> on Stage to display the Document properties in the Property inspector.

1.  Select File \> Publish Settings, and select a Player version from the Player
    pop-up menu. Not all Adobe® Flash® Professional CS5 features work in
    published SWF files that target Flash Player versions earlier than Flash
    Player 10. To specify Flash Player detection, click the HTML Wrapper
    category in the left column and select Detect Flash Version and enter Flash
    Player version to detect.

    **_Note:_** In Flash Pro CS5.5, the Flash Player 10.2 setting creates a SWF
    file using version 11 of the SWF format. The Flash Player 10 & 10.1 setting
    creates a SWF file using version 10 of the format.

2.  Select the ActionScript® version from the Script pop‑up menu. If you select
    ActionScript 2.0 or 3.0 and you've created classes, click the ActionScript
    Settings button to set the relative classpath to class files that differ
    from the default directory path set in Preferences.

3.  To control bitmap compression, click the Flash category in the left column
    and adjust the JPEG Quality value. Lower image quality produces smaller
    files; higher image quality produces larger files. Try different settings to
    determine the best trade-off between size and quality; 100 provides the
    highest quality and least compression.

    To make highly compressed JPEG images look smoother, select Enable JPEG
    Deblocking. This option reduces typical artifacts resulting from JPEG
    compression, such as the common appearance of 8x8-pixel blocking of the
    image. Some JPEG images may lose a small amount of detail when this option
    is selected.

4.  To set the sample rate and compression for all streaming sounds or event
    sounds in the SWF file, click the values next to Audio Stream or Audio Event
    and select options as needed.

    > **Note:** A streaming sound plays as soon as enough data for the first few
    > frames downloads; it is synchronized to the Timeline. An event sound does
    > not play until it downloads completely, and it continues to play until
    > explicitly stopped.

5.  To override settings for individual sounds specified in the Sound section of
    the Property inspector, select Override Sound Settings. To create a smaller,
    low-fidelity version of a SWF file, select this option.

    > **Note:** If the Select Override Sound Settings option is deselected,
    > Flash Pro scans all streaming sounds in the document (including sounds in
    > imported video) and publishes all stream sounds at the highest individual
    > setting. This can increase file size if one or more stream sounds has a
    > high export setting.

6.  To export sounds suitable for mobile devices, instead of the original
    library sound, select Export Device Sounds. Click OK.

7.  To set Advanced settings, select any of the following options:

    **Compress Movie**  
    (Default) Compresses the SWF file to reduce file size and download time.
    Most beneficial when a file is text- or ActionScript-intensive. A compressed
    file plays only in Flash Player 6 or later.

    **Include Hidden Layers**  
    (Default) Exports all hidden layers in the Flash document. Deselecting
    Export Hidden Layers prevents all layers (including layers nested inside
    movie clips) marked as hidden from being exported in the resulting SWF. This
    lets you easily test different versions of Flash documents by making layers
    invisible.

    **Include XMP metadata**  
    (Default) Exports all metadata entered in the File Info dialog box. Click
    the Modify XMP Metadata button to open the dialog box. You can also open the
    File Info dialog box by choosing File \> File Info. The metadata is viewable
    when the SWF file is selected in Adobe® Bridge.

    **Generate Size Report**  
    Generates a report listing the amount of data in the final Flash Pro content
    by file.

    **Omit Trace Statements**  
    Causes Flash Pro to ignore ActionScript `trace` statements in the current
    SWF file. When you select this option, information from `trace` statements
    does not appear in the Output panel. For more information, see
    [Output panel overview](../actionscript/debugging-actionscript-1.0-and-2.0.md#output-panel-overview).

    **Permit Debugging**  
    Activates the Debugger and allows remote debugging of a Flash Pro SWF file.
    Lets you use password protection with your SWF file.

    **Protect From Import**  
    Prevents others from importing a SWF file and converting it back into a FLA
    document. Lets you use password protection with your Flash Pro SWF file.

8.  If you are using ActionScript 2.0, and selected either Permit Debugging or
    Protect From Import, enter a password in the Password text field. If you add
    a password, other users must enter the password before they can debug or
    import the SWF file. To remove the password, clear the Password text field
    and re-publish. For more information on the Debugger, see
    [Debugging ActionScript 1.0 and 2.0](../actionscript/debugging-actionscript-1.0-and-2.0.md).
    If you are using ActionScript 3.0, see
    [Debugging ActionScript 3.0](../actionscript/debugging-actionscript-3.0.md).

9.  To set a maximum time that scripts can take to execute in the SWF file,
    enter a value for the Script Time Limit. Flash Player cancels execution of
    any scripts that exceed the limit.

10. Select the Flash Pro security model to use from the Local Playback Security
    pop‑up menu. Specify whether to grant your published SWF file local or
    network security access.

    **Local Access Only**  
    Lets the published SWF file interact with files and resources on the local
    system but not on the network.

    **Access Network Only**  
    Lets the published SWF file interact with files and resources on the network
    but not on the local system

11. To enable the SWF file to use hardware acceleration, select one of the
    following options from the Hardware Acceleration menu:

    **Level 1 - Direct**  
    Direct mode improves playback performance by allowing Flash Player to draw
    directly on the screen instead of letting the browser do the drawing.

    **Level 2 - GPU**  
    In GPU mode, Flash Player utilizes the available computing power of the
    graphics card to perform video playback and compositing of layered graphics.
    This provides another level of performance benefit depending on the user's
    graphics hardware. Use this option when you expect that your audience will
    have high-end graphics cards.

    If the playback system does not have sufficient hardware to enable
    acceleration, Flash Player reverts to normal drawing mode automatically. For
    best performance on web pages containing multiple SWF files, enable hardware
    acceleration for only one of the SWF files. Hardware acceleration is not
    used in Test Movie mode.

    When you publish your SWF file, the HTML file that embeds it contains a
    `wmode` HTML parameter. Choosing Level 1 or Level 2 hardware acceleration
    sets the `wmode` HTML parameter to `"direct"` or `"gpu"` respectively.
    Turning on hardware acceleration overrides the Window Mode setting you may
    have chosen in the HTML tab of the Publish Settings dialog box, because it
    is also stored in the `wmode` parameter in the HTML file.

## Specify publish settings for SWC files and projectors (CS5.5)

A
[SWC](https://web.archive.org/web/20120102230756mp_/http://www.adobe.com/devnet/flash/articles/concept_swc.html)
file is used for distributing components. The SWC file contains a compiled clip,
the component's ActionScript class file, and other files that describe the
component.

Projectors are Flash files that contain both the published SWF and Flash Player.
Projectors can play like an ordinary application, without the need for a web
browser, the Flash Player plugin, or Adobe AIR.

- To publish a SWC file, select SWC from the left column of the Publish Settings
  dialog and click Publish.

- To publish a Windows Projector, select Win Projector from the left column and
  click Publish.

- To publish a Macintosh Projector, select Mac Projector from the left column
  and click Publish.

To save the SWC file or projector with a different file name that the original
FLA file, enter a name for the Output File.

## Specify publish settings for HTML wrapper files (CS5.5)

Playing Flash Pro content in a web browser requires an HTML document that
activates the SWF file and specifies browser settings. The Publish command
automatically generates this document from parameters in an HTML template
document.

The template document can be any text file that contains the appropriate
template variables—including a plain HTML file, a file that includes code for
special interpreters such as ColdFusion® or Active Server Pages (ASP), or a
template included with Flash Pro.

To manually enter HTML parameters for Flash Pro or customize a built‑in
template, use an HTML editor.

HTML parameters determine where the content appears in the window, the
background color, the size of the SWF file, and so on, and set attributes for
the `object` and `embed` tags. Change these and other settings in the HTML panel
of the Publish Settings dialog box. Changing these settings overrides options
you've set in the SWF file.

### Specify the settings

1.  Select File \> Publish Settings and click the HTML Wrapper category from the
    left column of the dialog box.
2.  Use the default filename, which matches the name of your document, or enter
    a unique name, including the .html extension.
3.  To select an installed template to use, choose one from the Template pop‑up
    menu. To show a description of the selected template, click Info. The
    default selection is the Flash Only template.
4.  If you selected any HTML template other than Image Map, and you set the
    Flash Player version to 4 or later, select Flash Version Detection. For more
    information, see
    [Specify publish settings for Flash Player detection (CS5.5)](#specify-publish-settings-for-flash-player-detection-cs55).

    > **Note:** Flash Version Detection configures your document to detect the
    > version of Flash Player that the user has and sends the user to an
    > alternative HTML page if the user does not have the targeted player. The
    > alternative HTML page contains a link to download the latest version of
    > Flash Player.

5.  Select a Size option to set the values of the `width` and `height`
    attributes in the HTML `object` and `embed` tags:

    **Match Movie**  
    (Default) Uses the size of the SWF file.

    **Pixels**  
    Uses the Width and Height you specify. Enter the number of pixels for the
    width and height.

    **Percent**  
    The SWF file occupies the percentage of the browser window that you specify.
    Enter the percentages for width and height that you want to use.

6.  To control the SWF file's playback and features, select Playback options:

    **Paused At Start**  
    Pauses the SWF file until a user clicks a button or selects Play from the
    shortcut menu. (Default) The option is deselected and the content begins to
    play as soon as it is loaded (the `PLAY` parameter is set to `true)`.

    **Loop**  
    Repeats the content when it reaches the last frame. Deselect this option to
    stop the content when it reaches the last frame. (Default) The `LOOP`
    parameter is on.

    **Display Menu**  
    Shows a shortcut menu when users right-click (Windows) or Control-click
    (Macintosh) the SWF file. To show only About Flash in the shortcut menu,
    deselect this option. By default, this option is selected (the `MENU`
    parameter is set to `true).`

    **Device Font**  
    (Windows only) Substitutes anti-aliased (smooth-edged) system fonts for
    fonts not installed on the user's system. Using device fonts increases the
    legibility of type at small sizes and can decrease the SWF file's size. This
    option affects only SWF files that contain static text (text that you create
    when authoring a SWF file and that does not change when the content appears)
    set to display with device fonts.

7.  To determine the trade-off between processing time and appearance, as
    described in the following list, select Quality options. These options set
    the `QUALITY` parameter's value in the `object` and `embed` tags.

    **Low**  
    Favors playback speed over appearance and does not use anti-aliasing.

    **Auto Low**  
    Emphasizes speed at first but improves appearance whenever possible.
    Playback begins with anti-aliasing turned off. If Flash Player detects that
    the processor can handle it, anti-aliasing is automatically turned on.

    **Auto High**  
    Emphasizes playback speed and appearance equally at first but sacrifices
    appearance for playback speed if necessary. Playback begins with
    anti-aliasing turned on. If the actual frame rate drops below the specified
    frame rate, anti-aliasing is turned off to improve playback speed. To
    emulate the View \> Antialias setting, use this setting.

    **Medium**  
    Applies some anti-aliasing but does not smooth bitmaps. Medium produces a
    better quality than the Low setting but lower quality than the High setting.

    **High**  
    (Default) Favors appearance over playback speed and always uses
    anti-aliasing. If the SWF file does not contain animation, bitmaps are
    smoothed; if the SWF file contains animation, bitmaps are not smoothed.

    **Best**  
    Provides the best display quality and does not consider playback speed. All
    output is anti-aliased and bitmaps are always smoothed.

8.  Select a Window Mode option, which controls the HTML `wmode` attribute in
    the `object` and `embed` tags. The window mode modifies the relationship of
    the content bounding box or virtual window with content in the HTML page as
    described in the following list:

    **Window**  
    (Default) Does not embed any window-related attributes in the `object` and
    `embed` tags. The background of the content is opaque and uses the HTML
    background color. The HTML code cannot render above or below the Flash Pro
    content.

    **Opaque Windowless**  
    Sets the background of the Flash Pro content to opaque, obscuring anything
    under the content. Lets HTML content appear above or on top of content.

    **Transparent Windowless**  
    Sets the background of the Flash Pro content to transparent, allowing the
    HTML content to appear above and below the content. For browsers that
    support windowless modes, see
    [Parameters and attributes for object and embed tags](#parameters-and-attributes-for-object-and-embed-tags).

    If you turn on Hardware Acceleration in the Flash tab of the Publish
    Settings dialog box, the Window Mode you select is ignored and defaults to
    Window.

    For a demonstration of setting the Window Mode, see the TechNote titled
    [How to make a Flash movie with a transparent background](https://web.archive.org/web/20120102230756mp_/http://kb2.adobe.com/cps/142/tn_14201.html).

    > **Note:** In some instances, complex rendering in Transparent Windowless
    > mode can result in slower animation when the HTML images are also complex.

9.  To show error messages if tag settings conflict—for example, if a template
    has code referring to an alternative image that was not specified—select
    Show Warning Message.
10. To place the content within specified boundaries if you've changed the
    document's original width and height, select a Scale option. The Scale
    option sets the `SCALE` parameter in the HTML `object` and `embed` tags.

    **Default (Show All)**  
    Shows the entire document in the specified area without distortion while
    maintaining the original aspect ratio of the SWF files. Borders can appear
    on two sides of the application.

    **No Border**  
    Scales the document to fill the specified area and keeps the SWF file's
    original aspect ratio without distortion, cropping the SWF file if needed.

    **Exact Fit**  
    Shows the entire document in the specified area without preserving the
    original aspect ratio, which can cause distortion.

    **No Scale**  
    Prevents the document from scaling when the Flash Player window is resized.

11. To position the SWF file window in the browser window, select one of the
    following HTML Alignment options:

    **Default**  
    Centers the content in the browser window and crops edges if the browser
    window is smaller than the application.

    **Left, Right, or Top**  
    Align SWF files along the corresponding edge of the browser window and crop
    the remaining three sides as needed.

12. To set how the content is placed within the application window and how it is
    cropped, select the Flash Horizontal Alignment and Flash Vertical Alignment
    options. These options set the `SALIGN` parameter of the HTML `object` and
    `embed` tags.

### Parameters and attributes for object and embed tags

The following tag attributes and parameters describe the HTML code that the
Publish command creates. Refer to this list as you write custom HTML to show
Flash Pro content. Unless noted, all items apply to both the `object` and
`embed` tags. Optional entries are noted. Internet Explorer recognizes
parameters used with the `object` tag; Netscape recognizes the `embed` tag.
Attributes are used with both the `object` and `embed` tags. When you customize
a template, you can substitute a template variable (identified in the Value
section for each parameter in the following list) for the value.

> **Note:** The attributes and parameters listed in this section are shown in
> lowercase to comply with the XHTML standard. devicefont attribute/parameter  
> (Optional) Specifies whether static text objects are rendered in device fonts,
> even if the Device Font option is not selected. This attribute applies when
> the necessary fonts are available from the operating system.

Value: `true | false`

Template variable: `$DE`

src attribute  
Specifies the name of the SWF file to be loaded. Applies to the `embed` tag
only.

Value: `movieName.swf`

Template variable:` $MO`

movie parameter  
Specifies the name of the SWF file to be loaded. Applies to the `object` tag
only.

Value: `movieName.swf`

Template variable:` $MO`

classid attribute  
Identifies the ActiveX control for the browser. The value must be entered
exactly as shown. Applies to the `object` tag only.

Value: `clsid:d27cdb6e-ae6d-11cf-96b8-444553540000`

width attribute  
Specifies the width of the application either in pixels or as a percentage of
the browser window.

Value: `n` or ` n``% `

Template variable: `$WI`

height attribute  
Specifies the height of the application either in pixels or as a percentage of
the browser window.

> **Note:** Because Flash Pro applications are scalable, quality doesn't degrade
> at different sizes if the aspect ratio is maintained. (For example, the
> following sizes all have a 4:3 aspect ratio: 640 x 480 pixels, 320 x 240
> pixels, and 240 x 180 pixels.) Value: `n` or ` n``% `

Template variable: `$HE`

codebase attribute  
Identifies the location of the Flash Player ActiveX control so that the browser
can automatically download it if it is not already installed. The value must be
entered exactly as shown. Applies to the `object` tag only.

Value:
`http://fpdownload.adobe.com/pub/shockwave/cabs/flash/swflash.cab#version=7,0,0,0`

pluginspage attribute  
Identifies the location of the Flash Player plug‑in so that the user can
download it if it is not already installed. The value must be entered exactly as
shown. Applies to the `embed` tag only.

Value:
`http://www.adobe.com/shockwave/download/index.cgi?P1_Prod_Version=ShockwaveFlash`

swliveconnect attribute  
(Optional) Specifies whether the browser should start Java™ when loading Flash
Player for the first time. The default value is `false` if this attribute is
omitted. If you use JavaScript and Flash Pro on the same page, Java must be
running for the `fscommand()` function to work. However, if you use JavaScript
only for browser detection or another purpose unrelated to `fscommand()`
actions, you can prevent Java from starting by setting `SWLIVECONNECT` to
`false`. To force Java to start when you are not using JavaScript, explicitly
set the `SWLIVECONNECT` attribute to `true`. Starting Java substantially
increases the startup time for a SWF file; set this tag to `true` only when
necessary. Applies to the `embed` tag only.

Use the `fscommand()` action to start Java from a stand-alone projector file.

Value: `true | false`

play attribute/parameter  
(Optional) Specifies whether the application begins playing immediately on
loading in the web browser. If your Flash Pro application is interactive, let
the user initiate play by clicking a button or performing another task. In this
case, set the `play` attribute to `false` to prevent the application from
starting automatically. The default value is `true` if this attribute is
omitted.

Value: `true | false`

Template variable:` $PL`

loop attribute/parameter  
(Optional) Specifies whether the content repeats indefinitely or stops when it
reaches the last frame. The default value is `true` if this attribute is
omitted.

Value: `true | false`

Template variable:` $LO`

quality attribute/parameter  
(Optional) Specifies the level of anti-aliasing to be used. Because
anti-aliasing requires a faster processor to smooth each frame of the SWF file
before it is rendered on the viewer's screen, select one of the following values
based on whether your priority is speed or appearance:

Low  
Favors playback speed over appearance and never uses anti-aliasing.

Autolow  
Emphasizes speed at first but improves appearance whenever possible. Playback
begins with anti-aliasing turned off. If Flash Player detects that the processor
can handle it, anti-aliasing is turned on. Note: SWF files authored using
ActionScript 3.0 do not recognize the `autolow` value.

Autohigh  
Initially emphasizes playback speed and appearance equally, but sacrifices
appearance for playback speed if necessary. Playback begins with anti-aliasing
turned on. If the frame rate drops below the specified frame rate, anti-aliasing
is turned off to improve playback speed. Use this setting to emulate the
Antialias command (View \> Preview Mode \> Antialias).

Medium  
Applies some anti-aliasing and does not smooth bitmaps. It produces a better
quality than the Low setting but a lower quality than the High setting.

High  
Favors appearance over playback speed and always applies anti-aliasing. If the
SWF file does not contain animation, bitmaps are smoothed; if the SWF file has
animation, bitmaps are not smoothed.

Best  
Provides the best display quality and does not consider playback speed. All
output is anti‑aliased, and all bitmaps are smoothed.

The default value for `quality` is `high` if this attribute is omitted.

Value: `low | medium | high | autolow | autohigh | best`

Template variable:` $QU`

bgcolor attribute/parameter  
(Optional) Specifies the background color of the application. Use this attribute
to override the background color setting that the SWF file specifies. This
attribute does not affect the background color of the HTML page.

Value: `#RRGGBB` (hexadecimal RGB value)

Template variable:` $BG`

scale attribute/parameter  
(Optional) Defines how the application is placed in the browser window when
`width` and `height` values are percentages.

Showall (Default)  
Makes the entire content visible in the specified area without distortion while
maintaining the original aspect ratio of the application. Borders can appear on
two sides of the application.

Noborder  
Scales the content to fill the specified area, without distortion but possibly
with some cropping, while maintaining the original aspect ratio of the
application.

Exactfit  
Makes the entire content visible in the specified area without trying to
preserve the original aspect ratio. Distortion can occur.

The default value is `showall` if this attribute is omitted (and `width` and
`height` values are percentages).

Value: `showall | noborder | exactfit`

Template variable:` $SC`

align attribute  
Specifies the `align` value for the `object`, `embed`, and `img` tags and
determines how the SWF file is positioned within the browser window.

Default  
Centers the application in the browser window and crops edges if the browser
window is smaller than the application.

L, R, and T  
Align the application along the left, right, or top edge, respectively, of the
browser window and crop the remaining three sides as needed.

Value: `Default | L | R | T`

Template variable:` $HA`

salign parameter  
(Optional) Specifies where a scaled SWF file is positioned in the area that the
`width` and `height` settings define.

L, R, and T  
Align the application along the left, right, or top edge, respectively, of the
browser window and crop the remaining three sides as needed.

TL and TR  
Align the application to the top-left and top-right corner, respectively, of the
browser window and crop the bottom and remaining right or left side as needed.

If this attribute is omitted, the content is centered in the browser window.

Value: `L | R | T | B | TL | TR`

Template variable:` $SA`

base attribute  
(Optional) Specifies the base directory or URL used to resolve all relative path
statements in the SWF file. This attribute is helpful when you keep SWF files in
a different folder from your other files.

Value: base directory or URL

menu attribute or parameter  
(Optional) Specifies what type of menu appears when the viewer right-clicks
(Windows) or Command-clicks (Macintosh) the application area in the browser.

true  
shows the full menu, which gives the user several options to enhance or control
playback.

false  
shows a menu that contains only the About Adobe Flash Player 6 option and the
Settings option.

The default value is `true` if this attribute is omitted`.`

Value: `true | false`

Template variable: `$ME`

wmode attribute or parameter  
(Optional) Lets you use the transparent Flash Pro content, absolute positioning,
and layering capabilities available in Internet Explorer 4.0. For a list of
browsers this attribute/parameter supports, see
[Publishing Flash documents](./publishing-flash-documents.md). The `wmode`
paramater is also used for hardware acceleration in Flash Player 9 and later.

Window  
Plays the application in its own rectangular window on a web page. Window
indicates that the Flash Pro application has no interaction with HTML layers and
is always the top-most item.

Opaque  
Makes the application hide everything behind it on the page.

Transparent  
Makes the background of the HTML page show through all the transparent portions
of the application and can slow animation performance.

Opaque windowless and Transparent windowless  
Both interact with HTML layers, letting layers above the SWF file block out the
application. Transparent allows transparency so that HTML layers below the SWF
file can be seen through the background of the SWF file; opaque does not.

Direct  
Level 1 - Direct mode hardware acceleration is turned on. The other window mode
settings apply only when hardware acceleration is turned off.

GPU  
Level 2 - GPU mode hardware acceleration is turned on. The other window mode
settings apply only when hardware acceleration is turned off.

For more information about hardware acceleration, see
[Specify publish settings for SWF files (CS5)](./publish-settings-cs5.5.md#specify-publish-settings-for-flash-swf-files-cs55).

The default value is `Window` if this attribute is omitted. Applies to `object`
only.

Value: `Window | Opaque | Transparent | Direct | GPU`

Template variable:` $WM`

allowscriptaccess attribute or parameter  
Use `allowscriptaccess` to let your Flash Pro application communicate with the
HTML page hosting it. The `fscommand()` and `getURL()` operations can cause
JavaScript to use the permissions of the HTML page, which can be different from
the permissions of your Flash Pro application. This has important implications
for cross-domain security.

always  
Permits scripting operations at all times.

never  
Forbids all scripting operations.

samedomain  
Permits scripting operations only if the Flash Pro application is from the same
domain as the HTML page.

The default value that all HTML publish templates use is `samedomain`.

Value: `always | never | samedomain`

SeamlessTabbing parameter  
(Optional) Lets you set the ActiveX control to perform seamless tabbing, so that
the user can tab out of a Flash Pro application. This parameter works only in
Windows with the Flash Player ActiveX control, version 7 and higher.

true  
(or omitted) Sets the ActiveX control to perform seamless tabbing: After users
tab through the Flash Pro application, the next tab keypress moves the focus out
of the Flash Pro application and into the surrounding HTML content or to the
browser status bar if nothing can have focus in the HTML following the Flash Pro
application.

false  
Sets the ActiveX control to behave as it did in version 6 and earlier: After
users tab through the Flash Pro application, the next tab keypress wraps the
focus around to the beginning of the Flash Pro application. In this mode, you
cannot use the tab key to advance the focus past the Flash Pro application.

Value: `true | false`

### Examples using object and embed tags

For `object`, four settings (`height`, `width`, `classid`, and `codebase`) are
attributes that appear in the `object` tag; all others are parameters that
appear in separate, named `param` tags, as shown in the following example:

    <object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="100"
    height="100" codebase="http://fpdownload.adobe.com/pub/shockwave/cabs/flash/swflash.cab#version=9,0,0,0">
    <param name="movie" value="moviename.swf">
    <param name="play" value="true">
    <param name="loop" value="true">
    <param name="quality" value="high">
    </object>

For the `embed` tag, all settings (such as `height`, `width`, `quality`, and
`loop`) are attributes that appear between the angle brackets of the opening
`embed` tag, as shown in the following example:

    <embed src="moviename.swf" width="100" height="100" play="true"
    loop="true" quality="high"
    pluginspage="http://www.adobe.com/shockwave/download/index.cgi?P1_Prod_Version=ShockwaveFlash">
    </embed>

To use both tags, position the `embed` tag before the closing `object` tag, as
shown in the following example:

    <object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="100"
    height="100" codebase="http://fpdownload.adobe.com/pub/shockwave/cabs/flash/swflash.cab#version=9,0,0,0">
    <param name="movie" value="moviename.swf">
    <param name="play" value="true">
    <param name="loop" value="true">
    <param name="quality" value="high">
    <embed src="moviename.swf" width="100" height="100" play="true"
    loop="true" quality="high"
    pluginspage="http://www.adobe.com/shockwave/download/index.cgi?P1_Prod_Version=ShockwaveFlash">
    </embed>
    </object>

> **Note:** If you use the `object` and `embed` tags, use identical values for
> each attribute or parameter to ensure consistent playback across browsers. The
> `swflash.cab#version=9,0,0,0` parameter is optional; only omit this parameter
> if you don't want to check for the version number.

### Browsers that support windowless modes

For detailed information about web browser support for the WMODE attribute, see
the
[table in TechNote 12701: Flash OBJECT Tag Attributes](https://web.archive.org/web/20120102230756mp_/http://kb2.adobe.com/cps/127/tn_12701.html#main_Browser_support_for_Window_Mode__wmode__values_).

## Specify publish settings for Flash Player detection (CS5.5)

Flash Version Detection configures your document to detect the version of Flash
Player that the user has and sends the user to an alternative HTML page if the
user does not have the targeted player. The alternative HTML page contains a
link to download the latest version of Flash Player

Flash Player detection is available only for publish settings set to Flash
Player 4 or later, and for SWF files embedded in the Flash Only or Flash HTTPS
templates.

> **Note:** Flash Player 5 and later are installed on 98% of Internet-connected
> computers, making Flash Player detection a reasonable method to ensure that
> end users have the correct version of Flash Pro installed to view your
> content. The following HTML templates do not support Flash Player detection
> because the JavaScript in these templates conflicts with the JavaScript used
> to detect the Flash Player:

- Flash Pro for PocketPC 2003

- Flash Pro with AICC Tracking

- Flash Pro with FSCommand

- Flash Pro with Named Anchors

- Flash Pro with SCORM Tracking

> **Note:** Image Map HTML template does not support Player detection because
> they do not embed the Flash Player.

1.  Select File \> Publish Settings, and click the HTML Wrapper category in the
    left column.

2.  Select one of the Flash Only templates or the Flash HTTPS template from the
    Template pop‑up menu. These templates support the single-page HTML detection
    kit. Any of these templates enable the Detect Flash Version check box and
    the version number text fields.

3.  Select the Detect Flash Version check box. Your SWF file is embedded in a
    web page that includes Flash Player detection code. If the detection code
    finds an acceptable version of Flash Player installed on the end user's
    computer, the SWF file plays as designed.

4.  (Optional) To specify precise revisions of Flash Player, use the Major
    Revision and Minor Revision text fields. For example, specify Flash Player
    version 10.1.2 if it provides a feature specific to displaying your SWF
    file.

    When you publish your SWF file, Flash Pro creates a single HTML page in
    which to embed the SWF file and the Flash Player detection code. If an end
    user does not have the version of Flash Pro you've specified to view the SWF
    file, an HTML page appears with a link to download the latest version of
    Flash Player.

## Specify publish settings for GIF files (CS5.5)

Use GIF files to export drawings and simple animations from Flash Pro for use in
web pages. Standard GIF files are compressed bitmaps.

An animated GIF file (sometimes referred to as a GIF89a) offers a simple way to
export short animation sequences. Flash Pro optimizes an animated GIF file,
storing only frame-to-frame changes.

Flash Pro exports the first frame in the SWF file as a GIF file, unless you mark
a different keyframe for export by entering the `#Static` frame label in the
Property inspector. Flash Pro exports all the frames in the current SWF file to
an animated GIF file unless you specify a range of frames for export by entering
the `#First` and `#Last` frame labels in the appropriate keyframes.

Flash Pro can generate an image map for a GIF file to maintain URL links for
buttons in the original document. Use the Property inspector to place the frame
label \#Map in the keyframe in which to create the image map. If you don't
create a frame label, Flash Pro creates an image map using the buttons in the
last frame of the SWF file. Create an image map only if the `$IM`template
variable is present in the template you select.

1.  Select File \> Publish Settings, and click GIF Image in the left column of
    the dialog box.
2.  For the GIF filename, use the default filename or enter a new filename with
    the .gif extension.
3.  Select options for the GIF file:

    **Size**  
    Select Match Movie to make the GIF the same size as the SWF file and
    maintain the aspect ratio of your original image or enter values for width
    and height in pixels for the exported bitmap image.

    **Playback**  
    Determines whether Flash Pro creates a still (Static) image or an animated
    GIF (Animation). If you select Animation, select Loop Continuously or enter
    the number of repetitions.

4.  To specify additional appearance settings for the exported GIF file, expand
    the Colors section and select one of the following options:

    **Optimize Colors**  
    Removes any unused colors from a GIF file's color table. This option reduces
    the file size without affecting image quality, but slightly increases the
    memory requirements. This option has no effect on an adaptive palette. (An
    adaptive palette analyzes the colors in the image and creates a unique color
    table for the selected GIF file.)

    **Interlace**  
    Incrementally shows the exported GIF file in a browser as it downloads. Lets
    the user see basic graphic content before the file completely downloads and
    can download the file faster over a slow network connection. Do not
    interlace an animated GIF image.

    **Smooth**  
    Applies anti-aliasing to an exported bitmap to produce a higher-quality
    bitmap image and improve text display quality. However, smoothing might
    cause a halo of gray pixels to appear around an anti-aliased image placed on
    a colored background, and it increases the GIF file size. Export an image
    without smoothing if a halo appears or if you're placing a GIF transparency
    on a multicolored background.

    **Dither Solids**  
    Applies dithering to solid colors as well as gradients.

    **Remove Gradients**  
    (Default is off) Converts all gradient fills in the SWF file to solid colors
    using the first color in the gradient. Gradients increase the size of a GIF
    file and are often poor quality. To prevent unexpected results, select the
    first color of your gradients carefully if you use this option.

5.  To determine the transparency of the application's background and the way
    alpha settings are converted to GIF, select one of the following Transparent
    options:

    **Opaque**  
    Makes the background a solid color.

    **Transparent**  
    Makes the background transparent.

    **Alpha**  
    Sets partial transparency. Enter a Threshold value between 0 and 255. A
    lower value results in greater transparency. A value of 128 corresponds to
    50% transparency.

6.  To specify how pixels of available colors are combined to simulate colors
    not available in the current palette, select a Dither option. Dithering can
    improve color quality, but it increases the file size.

    **None**  
    Turns off dithering and replaces colors not in the basic color table with
    the solid color from the table that most closely approximates the specified
    color. Turning dithering off can result in smaller files but unsatisfactory
    colors.

    **Ordered**  
    Provides good-quality dithering with the smallest increase in file size.

    **Diffusion**  
    Provides the best-quality dithering but increases file size and processing
    time. Works only with the web 216-color palette selected.

7.  To define the image's color palette, select one of the following Palette
    types:

    **Web 216**  
    Uses the standard 216‑color, web‑safe palette to create the GIF image, for
    good image quality and the fastest processing on the server.

    **Adaptive**  
    Analyzes the colors in the image and creates a unique color table for the
    selected GIF file. Best for systems displaying thousands or millions of
    colors; it creates the most accurate color for the image but increases file
    size. To reduce the size of a GIF file with an adaptive palette, use the Max
    Colors option to decrease the number of colors in the palette. To set the
    number of colors used in the GIF image, enter a value for Max Colors. A
    smaller number of colors can produce a smaller file but can degrade the
    colors in the image

    **Web Snap Adaptive**  
    Is the same as the Adaptive palette option except it converts similar colors
    to the web 216-color palette. The resulting color palette is optimized for
    the image, but when possible Flash Pro uses colors from the web 216-color
    palette. This produces better colors for the image when the web 216-color
    palette is active on a 256‑color system. To set the number of colors used in
    the GIF image, enter a value for Max Colors. A smaller number of colors can
    produce a smaller file but can degrade the colors in the image

    **Custom**  
    Specifies a palette that you optimized for the selected image. The custom
    palette is processed at the same speed as the web 216-color palette. To use
    this option, know how to create and use custom palettes. To select a custom
    palette, click the Palette folder icon (the folder icon that appears at the
    end of the Palette text field), and select a palette file. Flash Pro
    supports palettes saved in the ACT format that some graphics applications
    export.

## Specify publish settings for JPEG files (CS5.5)

The JPEG format lets you publish a FLA file as a highly compressed, 24‑bit
bitmap. Generally, GIF format is better for exporting line art, and JPEG format
is better for images with continuous tones, such as photographs, gradients, or
embedded bitmaps.

Flash Pro exports the first frame in the SWF file as a JPEG, unless you mark a
different keyframe for export by entering the `#Static` frame label in the
Timeline.

1.  Select File \> Publish Settings, and select JPEG Image in the left column.
2.  For the JPEG filename, either use the default filename, or enter a new
    filename with the .jpg extension.
3.  Select options for the JPEG file:

    **Size**  
    Select Match Movie to make the JPEG image the same size as the Stage and
    maintain the aspect ratio of your original image, or enter values for width
    and height in pixels for the exported bitmap image.

    **Quality**  
    Drag the slider or enter a value to control the amount of JPEG file
    compression. The lower the image quality, the smaller the file size, and the
    reverse. To determine the best compromise between size and quality, try
    different settings.

    > **Note:** To change the object's compression setting, use the Bitmap
    > Properties dialog box to set the bitmap export quality per object. The
    > default compression option in the Bitmap Properties dialog box applies the
    > Publish Settings JPEG Quality option.

    **Progressive**  
    Show Progressive JPEG images incrementally in a web browser, which makes
    images appear faster when loading with a slow network connection. Similar to
    interlacing in GIF and PNG images.

4.  Click OK.

## Specify publish settings for PNG files (CS5.5)

PNG is the only cross-platform bitmap format that supports transparency (an
alpha channel). It is also the native file format for Adobe® Fireworks®.

Flash Pro exports the first frame in the SWF file as a PNG file, unless you mark
a different keyframe for export by entering the `#Static frame` label in the
Timeline.

1.  Select File \> Publish Settings, and select PNG Image in the left column.
2.  For the PNG filename, either use the default filename, or enter a new
    filename with the .png extension.
3.  For Size, select Match Movie to make the PNG image the same size as the SWF
    file and maintain the aspect ratio of your original image, or enter values
    for Width and Height in pixels for the exported bitmap.
4.  For Bit Depth, set the number of bits per pixel and colors to use in
    creating the image. The higher the bit depth, the larger the file. 8-bit  
    per channel (bpc) for a 256-color image

    24-bit  
    for thousands of colors

    24 bit with Alpha  
    for thousands of colors with transparency (32 bpc)

5.  To specify appearance settings for the exported PNG, select from the
    following options:

    **Optimize Colors**  
    Removes any unused colors from a PNG file's color table, reducing the file
    size by 1000 to 1500 bytes without affecting image quality but increasing
    the memory requirements slightly. Has no effect on an adaptive palette.

    **Interlace**  
    Incrementally shows the exported PNG in a browser as it downloads. Lets the
    user see basic graphic content before the file completely downloads and
    might download the file faster over a slow network connection. Do not
    interlace an animated PNG file.

    **Smooth**  
    Applies anti-aliasing to an exported bitmap to produce a higher-quality
    bitmap image and improve text display quality. However, smoothing might
    cause a halo of gray pixels to appear around an anti-aliased image placed on
    a colored background, and it increases the PNG file size. Export an image
    without smoothing if a halo appears or if you're placing a PNG transparency
    on a multicolored background.

    **Dither Solids**  
    Applies dithering to solid colors and gradients.

    **Remove Gradients**  
    (Default is off) Converts all gradient fills in the application to solid
    colors using the first color in the gradient. Gradients increase the size of
    a PNG and are often poor quality. To prevent unexpected results, select the
    first color of your gradients carefully if you use this option.

6.  If you selected 8‑bpc for Bit Depth, select a Dither option to specify how
    pixels of available colors are mixed to simulate colors not available in the
    current palette. Dithering can improve color quality, but it increases file
    size. Select from the following options:

    **None**  
    Turns off dithering and replaces colors not in the basic color table with
    the solid color from the table that most closely approximates the specified
    color. Turning dithering off can produce smaller files but unsatisfactory
    colors.

    **Ordered**  
    Provides good-quality dithering with the smallest increase in file size.

    **Diffusion**  
    Provides the best-quality dithering but increases file size and processing
    time. It also works only with the Web 216-color palette selected.

7.  If you selected 8‑bpc for Bit Depth, select one of the following Palette
    Types to define the color palette for the PNG image:

    **Web 216**  
    Uses the standard 216‑color, web-safe palette to create the PNG image, for
    good image quality and the fastest processing on the server.

    **Adaptive**  
    Analyzes the colors in the image and creates a unique color table for the
    selected PNG file. Best for systems showing thousands or millions of colors;
    it creates the most accurate color for the image but results in a file size
    larger than a PNG created with the web-safe 216-color palette.

    **Web Snap Adaptive**  
    Is the same as the Adaptive palette option except that it converts colors
    similar to the web-safe 216-color palette. The resulting color palette is
    optimized for the image, but when possible, Flash Pro uses colors from the
    web-safe 216-color palette. This produces better colors for the image when
    the web-safe 216-color palette is active on a 256‑color system. To reduce
    the size of a PNG file with an adaptive palette, use the Max Colors option
    to decrease the number of palette colors.

    **Custom**  
    Specifies a palette that you optimized for the selected image. The custom
    palette is processed at the same speed as the web-safe 216-color palette. To
    use this option, know how to create and use custom palettes. To select a
    custom palette, click the Palette folder icon (the folder icon that appears
    at the end of the Palette text field), and select a palette file. Flash Pro
    supports palettes saved in the ACT format that leading graphics applications
    export.

8.  If you selected the Adaptive or Web Snap Adaptive palette, enter a value for
    Max Colors to set the number of colors used in the PNG image. A smaller
    number of colors can produce a smaller file but might degrade the colors in
    the image.
9.  To select a line-by-line filtering method to make the PNG file more
    compressible and experiment with the different options for a particular
    image, select one of the following Filter Options:

    **None**  
    Turns off filtering.

    **Sub**  
    Transmits the difference between each byte and the value of the
    corresponding byte of the previous pixel.

    **Up**  
    Transmits the difference between each byte and the value of the
    corresponding byte of the pixel immediately above.

    **Average**  
    Uses the average of the two neighboring pixels (left and above) to predict
    the value of a pixel.

    **Path**  
    Computes a simple linear function of the three neighboring pixels (left,
    above, upper left), and selects the neighboring pixel closest to the
    computed value as a predictor of the color.

    **Adaptive**  
    Analyzes the colors in the image and creates a unique color table for the
    selected PNG file. Best for systems showing thousands or millions of colors;
    it creates the most accurate color for the image but results in a file size
    larger than a PNG created with the web 216-color palette. Reduce the size of
    a PNG created with an adaptive palette by decreasing the number of colors in
    the palette.

## Preview the publishing format and settings (CS5.5)

The Publish Preview command exports the file and opens the preview in the
default browser. If you preview a QuickTime video, Publish Preview starts the
QuickTime video Player. If you preview a projector, Flash Pro starts the
projector.

![](../img/dingbat.png) Select File \> Publish Preview, and select the file
format to preview.

Using the current Publish Settings values, Flash Pro creates a file of the
specified type in the same location as the FLA file. This file remains in this
location until you overwrite or delete it.

## Using publish profiles (CS5.5)

Publish profiles let you:

- Save a publish settings configuration, export it, and import the publish
  profile to other documents or for others to use.

- Import publish profiles to use in your document.

- Create profiles to publish in several media formats.

- Create a publish profile for in-house use that differs from the way you'd
  publish the files for a client.

- Create a standard publish profile for your company to ensure files are
  published uniformly.

Publish profiles are saved at the document rather than application level.

### Create a publish profile

1.  In the Publish Settings dialog box, click the Profile Options menu and
    choose Create Profile.
2.  Name the publish profile, and click OK.
3.  Specify the publish settings for your document, and click OK.

### Duplicate, modify, or delete a publish profile

![](../img/dingbat.png) From the Profile pop‑up menu in the Publish Settings
dialog box (File \> Publish Settings), select the publish profile to use:

- To create a duplicate profile, click the Profile Options menu and choose
  Duplicate Profile. Enter the profile name in the Duplicate Name text field,
  and click OK.

- To modify a publish profile, select it from the Profile menu, specify the new
  publish settings for your document, and click OK.

- To delete a publish profile, click the Profile Options menu and choose Delete
  Profile. Then click OK.

### Export a publish profile

1.  From the Profile pop‑up menu in the Publish Settings dialog (File \> Publish
    Settings), select the publish profile to export.
2.  Click the Profile Options menu and choose Export Profile. Export the publish
    profile as an XML file for import into other documents.
3.  Either accept the default location in which to save the publish profile or
    browse to a new location, and click Save.

### Import a publish profile

Other users can create and export publish profiles, which you can import and
select as a publish settings option.

1.  In the Publish Settings dialog box (File \> Publish Settings), click the
    Profile Options menu and choose Import Profile.
2.  Browse to the publish profile XML file, and click Open.

More Help topics

[Using publish profiles (CS5)](./publish-settings-cs5.md#using-publish-profiles-cs5)

[Sound](../sound/index.md)

[Using sounds in Flash Lite](../sound/using-sounds-in-flash.md#using-sounds-in-flash-lite)

[Publishing overview](./publishing-flash-documents.md#publishing-overview)

[Configure a server for Flash Player](./publishing-flash-documents.md#configure-a-server-for-flash-player)

[HTML publishing templates](./html-publishing-templates.md)

[Create an image map to substitute for a SWF file](./html-publishing-templates.md#create-an-image-map-to-substitute-for-a-swf-file)

[Import and export color palettes](../creating-and-editing-artwork/color.md#import-and-export-color-palettes)

[Set bitmap properties](../using-imported-artwork/imported-bitmaps-and-flash.md#set-bitmap-properties)
