# Bitmap caching and SWF file performance

Bitmap caching helps you enhance the performance of nonchanging movie clips in
your applications. When you set the `MovieClip.cacheAsBitmap` or
`Button.cacheAsBitmap` property to `true`, Flash Player caches an internal
bitmap representation of the movie clip or button instance. This can improve
performance for movie clips that contain complex vector content. All of the
vector data for a movie clip that has a cached bitmap is drawn to the bitmap,
instead of to the main Stage.

> **Note:** The bitmap is copied to the main Stage as unstretched, unrotated
> pixels snapped to the nearest pixel boundaries. Pixels are mapped one-to-one
> with the parent object. If the bounds of the bitmap change, the bitmap is
> re‑created instead of being stretched.

For detailed information on caching button or movie clip instances see the
following topics:

- About caching and scrolling movie clips with ActionScript in
  [Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)

- Caching a movie clip in
  [Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)

  Use the `cacheAsBitmap` property with movie clips with mostly static content
  and that do not scale and rotate frequently. With such movie clips, using the
  `cacheAsBitmap` property can lead to performance improvements when the movie
  clip is translated (when its `x` and `y` position is changed).

  Enabling caching for a movie clip creates a _surface_, which has several
  advantages, such as helping complex vector animations to render fast. In some
  situations, enabling caching does not improve performance, or even decrease
  it.

  Overall performance of cached data depends on how complex the vector data of
  your instances are, how much of the data you change, and whether or not you
  set the opaqueBackground property. If you are changing small regions, the
  difference between using a surface and using vector data might be negligible.
  Test both scenarios with your work before you deploy the application.

#### When to use bitmap caching

The following are typical scenarios in which you might see significant benefits
when you enable bitmap caching by optimizing vector graphics.

Complex background image  
An application that contains a detailed and complex background image of vector
data. To improve performance, select the content, store it in a movie clip, and
set the opaqueBackground property to true. The background is rendered as a
bitmap and can be redrawn quickly, so that your animation plays faster.

Scrolling text field  
An application that displays a large amount of text in a scrolling text field.
Place the text field in a movie clip that you set as scrollable with scrolling
bounds (the scrollRect property), enabling fast pixel scrolling for the
specified instance. When a user scrolls the movie clip instance, the scrolled
pixels shift up and generate the newly exposed region instead of regenerating
the entire text field.

Windowing system  
An application with a complex system of overlapping windows. Each window can be
open or closed (for example, web browser windows). If you mark each window as a
surface (set the cacheAsBitmap property to true), each window is isolated and
cached. Users can drag the windows so that they overlap each other, and each
window doesn't need to regenerate the vector content.

#### When to avoid using bitmap caching

Misusing bitmap caching can negatively affect your SWF file. When you develop a
FLA file that uses surfaces, remember the following guidelines:

- Do not overuse surfaces (movie clips with caching enabled). Each surface uses
  more memory than a regular movie clip; only enable surfaces to improve
  rendering performance.

- A cached bitmap can use significantly more memory than a regular movie clip
  instance. For example, if the movie clip on the Stage is 250 pixels by 250
  pixels, when cached it might use 250 KB instead of 1 KB when it's a regular
  (uncached) movie clip instance.

- Avoid zooming in on cached surfaces. If you overuse bitmap caching, a large
  amount of memory is consumed (see previous bullet), especially if you zoom in
  on the content.

- Use surfaces for movie clip instances that are largely static (nonanimating).
  You can drag or move the instance, but the contents of the instance should not
  animate or change a lot. For example, if you rotate or transform an instance,
  the instance changes between the surface and vector data, which is difficult
  to process and negatively affects your SWF file.

- If you mix surfaces with vector data, it increases the amount of processing
  that Flash Player (and sometimes the computer) needs to do. Group surfaces
  together; for example, when you create windowing applications.
