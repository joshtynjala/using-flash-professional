# Best practices - Tips for creating content for mobile devices

## Creating Flash content for use on mobile devices

To create Flash content for mobile devices, follow some basic principles. For
example, Flash developers often avoid extremely complex artwork and excessive
tweening or transparency.

Flash Lite developers face additional challenges because performance on mobile
devices varies greatly. If content must be published to many different devices,
developers sometimes have to author for the lowest common denominator.

Optimizing mobile content requires making trade‑offs. For example, one technique
may make the content look better, while another results in better performance.
As you evaluate these trade‑offs, you will be going back and forth repeatedly
between testing in the emulator and testing on the target device. You must see
your content on the actual device to evaluate the trueness of colors, text
readability, physical interactions, UI responsiveness, and other aspects of the
real mobile experience.

For more tips and techniques for creating content for mobile phones and devices,
see
[www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).

## Flash Lite guidelines for animation in mobile devices

When creating animated content for a mobile devices, keep device CPU limitations
in mind. Following these guidelines can help preventFlash Lite content from
running slowly:

- When creating a new Flash Lite file, check that the document is set up
  correctly. Although Flash files scale smoothly, performance can suffer if the
  file is not running at its native Stage size and has to scale in the player.
  Try to set the document Stage size to match the resolution of the target
  device. Also set the Flash Player to the correct version of Flash Lite and
  select an appropriate device profile in Device Central.

- Flash Lite can render vector graphics at low, medium, and high quality. The
  higher the rendering quality, the more smoothly and accurately Flash Lite
  renders vector graphics and the greater the demand on the device's CPU. To
  provide complex animation, experiment with changing the player's quality
  setting and then thoroughly test the SWF file. To control the rendering
  quality of a SWF file, use the `_quality` property or the `SetQuality`
  command. Valid values for the `_quality` property are `LOW`, `MEDIUM`, and
  `HIGH`.

- Limit the number of simultaneous tweens. Reduce the number of tweens, or
  sequence the animation so that one begins when another ends.

- Use transparency (alpha) effects on symbols sparingly because they are CPU
  intensive. In particular, avoid tweening symbols with alpha levels that are
  not fully opaque (less than 100%).

- Avoid CPU-intensive visual effects, such as large masks, extensive motion,
  alpha blending, extensive gradients, and complex vectors.

- Experiment with combinations of tweens, keyframe animations, and
  ActionScript-driven movement to produce the most efficient results.

- Rendering vector ovals and circles is much more memory intensive than
  rendering quadrangles. Using round and oval strokes also greatly increases CPU
  use.

- Test animations frequently on actual target devices.

- When Flash draws an animated region, it defines a rectangular bounding box
  around the area. Optimize the drawing by making that rectangle as small as
  possible. Avoid overlapping tweens, because Flash interprets the merged area
  as a single rectangle, resulting in a larger total region. Use Flash's Show
  Redraw Region feature to optimize the animation.

- Avoid using `_alpha = 0` and `_visible = false` to hide on‑screen movie clips.
  If you simply turn a movie clip's visibility off or change its alpha to zero,
  it is still included in line-rendering calculations, which can affect
  performance.

- Similarly, do not try to hide a movie clip by obscuring it behind another
  piece of artwork. It will still be included in the player's calculations.
  Instead, move movie clips completely off the Stage or remove them by calling
  `removeMovieClip`. For more tips and techniques for creating content for
  mobile phones and devices, see
  [www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).

## Flash Lite bitmap and vector graphics in mobile devices

Flash Lite can render both vector and bitmap graphics. Each type of graphic has
its advantages and disadvantages. The decision to use vector rather than bitmap
graphics is not always clear and often depends on several factors.

Vector graphics are compactly represented in SWF files as mathematical equations
and rendered at run time by the Flash Lite player. In contrast, bitmap graphics
are represented as arrays of picture elements (pixels), which require more bytes
of data. Therefore, using vector graphics in a file can help reduce file size
and memory usage.

Vector graphics also maintain their smooth shapes when scaled in size. Bitmap
images can appear boxy, or pixelated, when scaled.

Compared to bitmaps, vector graphics require more processing power to render,
especially vector graphics that have many complex shapes and fills.
Consequently, heavy use of vector shapes can sometimes reduce overall file
performance. Because bitmap graphics do not require as much processing time to
render as vector graphics, they are better choice for some files, for example, a
complex road map meant to be animated and scrolled on a mobile phone.

Keep these considerations in mind:

- Avoid using outlines on vector shapes. Outlines have an inner and outer edge
  (fills have only one) and are twice the work to render.

- Corners are simpler to render than curves. When possible, use flat edges,
  especially with very small vector shapes.

- Optimization is especially helpful with small vector shapes such as icons.
  Complex icons may lose their details upon rendering, and the work of rendering
  the details is wasted.

- As a general rule, use bitmaps for small, complex images (such as icons) and
  vector graphics for larger and simpler ones.

- Import bitmap graphics at the correct size; don't import large graphics and
  scale them down in Flash, because this wastes file size and run‑time memory.

- The Flash Lite player does not support bitmap smoothing. If a bitmap is scaled
  or rotated, it will have a chunky appearance. If it is necessary to scale or
  rotate a graphic, consider using a vector graphic instead.

- Text is essentially just a very complex vector shape. Of course, text is often
  critical, so it can rarely be avoided entirely. When text is needed, avoid
  animating it or placing it over an animation. Consider using text as a bitmap.
  For multiline dynamic and input text, the line break of the text string is not
  cached. Flash breaks lines at run time and recalculates the breaks every time
  the text field needs to be redrawn. Static text fields are not problematic,
  because the line breaking is precalculated at compile time. For dynamic
  content, using dynamic text fields is unavoidable, but when possible, consider
  using static text fields instead.

- Minimize the use of transparency in PNG files; Flash must calculate redraws
  even for the transparent portions of the bitmap. For example, with a
  transparent PNG file that represents a foreground element, don't export the
  transparent PNG at the full size of the screen. Instead, export it at the
  actual size of the foreground element.

- Try to group bitmap layers together and vector layers together. Flash needs to
  implement different renderers for bitmap and vector content, and switching
  between renderers takes time.

For more tips and techniques for creating content for mobile phones and devices,
see
[www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).

## Set compression of Flash Lite bitmaps for mobile devices

When using bitmaps, you can set image-compression options (on a per-image basis
or globally for all bitmap images) that reduce SWF file size.

For more tips and tricks about using Adobe Device Central with other Adobe
products, see
[www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).

### Set compression options for an individual bitmap file

1.  Start Flash and create a document.

2.  Select a bitmap in the Library window.

3.  Right-click (Windows) or Control-click (Macintosh) the bitmap icon in the
    Library window, and select Properties from the context menu to open the
    Bitmap Properties dialog box.

4.  In the Compression pop‑up menu, select one of the following options:

    - Select the Photo (JPEG) option for images with complex color or tonal
      variations, such as photographs or images with gradient fills. This option
      produces a JPEG file. Select the Use Imported JPEG Data check box to use
      the default compression quality specified for the imported image. To
      specify a new quality compression setting, deselect Use Imported JPEG Data
      and enter a value between 1 and 100 in the Quality text box. A higher
      setting produces an image of higher image, but also a larger file, so
      adjust the value accordingly.

    - Select the Lossless (PNG/GIF) option for images with simple shapes and a
      few colors. This option compresses the image using lossless compression,
      which discards no data.

5.  Click Test to determine the results of the file compression.

    Compare the original file size to the compressed file size to decide whether
    the selected compression setting is acceptable.

### Set compression for all bitmap images

1.  Select File \> Publish Settings, and then click the Flash tab to display
    compression options.
2.  Adjust the JPEG quality slider, or enter a value. A higher JPEG quality
    value produces an image of higher image quality but a larger SWF file. A
    lower image quality produces a smaller SWF file. Try different settings to
    determine the best trade‑off between size and quality.

## Optimizing Flash Lite frames for mobile devices

- Most devices that support Flash Liteplay back content at about 15 to 20 frames
  per second (fps). The frame rate can be as low as 6 fps. During development,
  set the document frame rate to approximate the playback speed of the target
  device. This shows how the content will run on a device with limited
  performance. Before publishing a final SWF file, set the document frame rate
  to at least 20 fps or higher to avoid limiting performance in case the device
  supports a higher frame rate.

- When using `gotoAndPlay`, remember that every frame between the current frame
  and the requested frame needs to be initialized before Flash plays the
  requested frame. If many of these frames contain different content, it could
  be more efficient to use different movie clips rather than using the Timeline.

- Although preloading all content by putting it at the beginning of the file
  makes sense on the desktop, preloading on a mobile device can delay file
  startup. Space content throughout the file so that movie clips are initialized
  as they are used.

For more tips and techniques for creating content for mobile phones and devices,
see
[www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).

## Optimizing ActionScript for Flash Lite content on mobile devices

Because of the processing speed and memory limitations on most mobile devices,
follow these guidelines when developing ActionScript for Flash Lite content used
on mobile devices:

- Keep the file and its code as simple as possible. Remove unused movie clips,
  delete unnecessary frame and code loops, and avoid too many frames or
  extraneous frames.

- Using `FOR` loops can be expensive because of the overhead incurred while the
  condition is checked with each iteration. When the costs of the iteration and
  the loop overhead are comparable, execute multiple operations individually
  instead of using a loop. The code may be longer, but performance will improve.

- Stop frame-based looping as soon as it is no longer needed.

- When possible, avoid string and array processing because it can be
  CPU-intensive.

- Always try to access properties directly rather than using ActionScript getter
  and setter methods, which have more overhead than other method calls.

- Manage events wisely. Keep event listener arrays compact by using conditions
  to check whether a listener exists (is not `null`) before calling it. Clear
  any active intervals by calling `clearInterval`, and remove any active
  listeners by calling `removeListener` before removing content using
  `unloadapplication` or `removeapplicationClip`. Flash does not re-collect SWF
  data memory (for example, from intervals and listeners) if any ActionScript
  functions are still referring to the SWF data when a movie clip is unloaded.

- When variables are no longer needed, delete them or set them to `null`, which
  marks them for garbage collection. Deleting variables helps optimize memory
  use during run time, because unneeded assets are removed from the SWF file. It
  is better to delete variables than to set them to `null`.

- Explicitly remove listeners from objects by calling `removeListener` before
  garbage collection.

- If a function is being called dynamically and passing a fixed set of
  parameters, use `call` instead of `apply`.

- Make namespaces (such as paths) more compact to reduce startup time. Every
  level in the package is compiled to an `IF` statement and causes a new
  `Object`call, so having fewer levels in the path saves time. For example, a
  path with the levels `com.xxx.yyy.aaa.bbb.ccc.funtionName` causes an object to
  be instantiated for `com.xxx.yyy.aaa.bbb.ccc`. Some Flash developers use
  preprocessor software to reduce the path to a unique identifier, such as
  `58923409876.functionName`, before compiling the SWF code.

- If a file consists of multiple SWF files that use the same ActionScript
  classes, exclude those classes from select SWF files during compilation. This
  can help reduce file download time and run‑time memory requirements.

- Avoid using `Object.watch` and `Object.unwatch`, because every change to an
  object property requires the player to determine whether a change notification
  must be sent.

- If ActionScript code that executes on a keyframe in the timeline requires more
  than 1 second to complete, consider splitting up that code to execute over
  multiple keyframes.

- Remove `trace` statements from the code when publishing the SWF file. To do
  this, select the Omit Trace Actions check box on the Flash tab in the Publish
  Settings dialog box.

- Inheritance increases the number of method calls and uses more memory: a class
  that includes all the functionality it needs is more efficient at run time
  than a class that inherits some of its functionality from a superclass.
  Therefore, you may need to make a design trade‑off between extensibility of
  classes and efficiency of code.

- When one SWF file loads another SWF file that contains a custom ActionScript
  class (for example, `foo.bar.CustomClass`) and then unloads the SWF file, the
  class definition remains in memory. To save memory, explicitly delete any
  custom classes in unloaded SWF files. Use the `delete` statement and specify
  the fully qualified class name, such as: `delete foo.bar.CustomClass.`

- Limit the use of global variables, because they are not marked for garbage
  collection if the movie clip that defined them is removed.

- Avoid using the standard user interface components (available in the
  Components panel in Flash). These components are designed to run on desktop
  computers and are not optimized to run on mobile devices.

- Whenever possible, avoid deeply nested functions.

- Avoid referencing nonexistent variables, objects, or functions. Compared to
  the desktop version of Flash Player, Flash Lite 2 looks up references to
  nonexistent variables slowly, which can significantly affect performance.

- Avoid defining functions using anonymous syntax. For example,
  `myObj.eventName = function{ ...}`. Explicitly defined functions are more
  efficient, such as `function myFunc { ...}; my Obj.eventName = myFunc;`.

- Minimize the use of Math functions and floating-point numbers. Calculating
  these values slows performance. If you must use the Math routines, consider
  precalculating the values and storing them in an array of variables.
  Retrieving the values from a data table is much faster than having Flash
  calculate them at run time. For more tips and techniques for creating content
  for mobile phones and devices, see
  [www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).

## Managing Flash Lite file memory for mobile devices

Flash Lite regularly clears from memory any objects and variables that a file no
longer references. This is known as garbage collection. Flash Lite runs its
garbage-collection process once every 60 seconds, or whenever usage of file
memory increases suddenly by 20% or more.

Although you cannot control how and when Flash Lite performs garbage collection,
you can still free unneeded memory deliberately. For timeline or global
variables, use the `delete` statement to free the memory that ActionScript
objects use. For local variables—for example, a variable defined within a
function definition—you can't use the `delete` statement to free an object's
memory, but you can set to `null` the variable that references the object. This
frees the memory that the object uses, provided there are no other references to
that object.

The following two code examples show how to free memory that objects use by
deleting the variable that references those objects. The examples are identical,
except that the first example creates a timeline variable and the second creates
a global variable.

    // First case: variable attached to a movie or
    // movie clip timeline
    //
    // Create the Date object.
    var mcDateObject = new Date();
    // Returns the current date as a string.
    trace(mcDateObject);
    // Delete the object.
    delete mcDateObject;
    // Returns undefined.
    trace(mcDateObject);
    //
    // Second case: global variable attached to a movie or
    // movie clip timeline
    //
    // Create the Date object.
    _global.gDateObject = new Date();
    // Returns the current date as a string.
    trace(_global.gDateObject);
    // Delete the object.
    delete _global.gDateObject;
    // Returns undefined.
    trace(_global.gDateObject);

As mentioned previously, you can't use the `delete` statement to free memory
that a local function variable uses. Instead, set the variable reference to
`null`, which has the same effect as using `delete`.

    function func()
    {
        // Create the Date object.
        var funcDateObject = new Date();
        // Returns the current date as a string.
        trace(funcDateObject);
        // Delete has no effect.
        delete funcDateObject;
        // Still returns the current date.
        trace(funcDateObject);
        // Set the object reference to null.
        funcDateObject = null;
        // Returns null.
        trace(funcDateObject);
    }
    // Call func() function.
    func();

For more tips and techniques for creating content for mobile phones and devices,
see
[www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).

## Loading data for mobile devices in Flash Lite

When developing files for mobile devices, minimize the amount of data you
attempt to load at one time. If you are loading external data into a Flash Lite
file (for example, using `XML.load`), the device's operating system may generate
a "memory failure" error if insufficient memory is allocated for the incoming
data. This situation can occur even if the total amount of remaining memory is
sufficient.

For example, suppose a file attempts to load an XML file that's 100 KB, but the
device's operating system has allocated only 30 KB to handle that incoming data
stream. In this case, Flash Litedisplays an error message to the user,
indicating that not enough memory is available.

To load large amounts of data, group the data in smaller pieces—for example, in
several XML files—and make several data-loading calls for each piece. The size
of each piece of data, and therefore the number of data-loading calls you need
to make, varies by device and file. To determine an appropriate balance between
the number of data requests and the likelihood of a memory failure, test files
on a variety of target devices.

For optimum performance, avoid loading and parsing XML files if possible.
Instead, store data in simple name/value pairs and load the data from a text
file using `loadVars` or from precompiled SWF files.

For more tips and techniques for creating content for mobile phones and devices,
see
[www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).

## Exclude classes from compilation for Flash Lite

To reduce the size of a SWF file, consider excluding classes from compilation
but retaining the ability to access and use them for type checking. For example,
try this if you are developing a file that uses multiple SWF files or shared
libraries, especially those that access many of the same classes. Excluding
classes helps avoid duplicating classes in those files.

1.  Create a new XML file.

2.  Name the XML file FLA_filename_exclude.xml, where FLA_filename is the name
    of the FLA file without the .fla extension. For example, if the FLA file is
    sellStocks.fla, the XML filename must be sellStocks_exclude.xml.

3.  Save the file in the same directory as the FLA file.

4.  Place the following tags in the XML file:

        <excludeAssets>
            <asset name="className1" />
            <asset name="className2" />
        </excludeAssets>

    The values specified for the name attributes in the `<asset>` tags are the
    names of classes that should be excluded from the SWF file. Add as many as
    required for the file. For example, the following XML file excludes the
    `mx.core.UIObject` and `mx.screens.Slide` classes from the SWF file:

        <excludeAssets>
            <asset name="mx.core.UIObject" />
            <asset name="mx.screens.Slide" />
        </excludeAssets>

    For more tips and techniques for creating content for mobile phones and
    devices, see
    [www.adobe.com/go/learn_cs_mobilewiki_en](https://web.archive.org/web/20120102084434mp_/http://www.adobe.com/go/learn_cs_mobilewiki_en).
