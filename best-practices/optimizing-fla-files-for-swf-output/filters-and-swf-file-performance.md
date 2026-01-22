# Filters and SWF file performance

If you use too many filters in an application, you can use large amounts of
memory and cause Flash Player performance to suffer. Because a movie clip with
filters attached has two bitmaps that are both 32‑bit, these bitmaps can cause
your application to use a significant amount of memory if you use many bitmaps.
The computer's operating system might generate an out-of-memory error. On a
modern computer, out-of-memory errors should be rare, unless you are using
filter effects extensively in an application (for example, you have thousands of
bitmaps on the Stage).

However, if you do encounter an out-of-memory error, the following occurs:

- The filters array is ignored.

- The movie clip is drawn using the regular vector renderer.

- No bitmaps are cached for the movie clip.

  After an out-of-memory error occurs, a movie clip never attempts to use a
  filters array or a bitmap cache. Another factor that affects player
  performance is the value that you use for the quality parameter for each
  filter that you apply. Higher values require more CPU and memory for the
  effect to render, whereas setting the quality parameter to a lower value
  requires fewer computer resources. Avoid using an excessive number of filters,
  and use a lower quality setting when possible.

  > **Important:** If a 100 pixel by 100 pixel object is zoomed in once, it uses
  > four times the memory since the content's dimensions are now 200 pixels by
  > 200 pixels. If you zoom another two times, the shape is drawn as an 800
  > pixel by 800 pixel object which uses 64 times the memory as the original 100
  > pixel by 100 pixel object. Whenever you use filters in a SWF file, disable
  > the zoom menu options from the SWF file's context menu.

  You can encounter errors if you use invalid parameter types. Some filter
  parameters also have a particular valid range. If you set a value that's
  outside of the valid range, the value changes to a valid value that's within
  the range. For example, quality should be a value from 1 to 3 for a standard
  operation, and can only be set to 0 to 15. Anything higher than 15 is set
  to 15.

  Some constructors have restrictions on the length of arrays required as input
  parameters. If a convolution filter or color matrix filter is created with an
  invalid array (not the right size), the constructor fails and the filter is
  not created successfully. If the filter object is then used as an entry on a
  movie clip's filters array, it is ignored.

  > ![](../img/tip_help.png) When using a blur filter, using values for blurX
  > and blurY that are powers of 2 (such as 2, 4, 8, 16, and 32) can be computed
  > faster and give a 20% to 30% performance improvement.
