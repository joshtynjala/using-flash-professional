# Optimizing graphics and animation

Before you create optimized and streamlined animations or graphics, outline and
plan your project. Make a target for the file size and length of the animation,
and test throughout the development process. Follow these guidelines to optimize
graphics and animation:

- Avoid using gradients, because they require many colors and calculations to be
  processed, which is more difficult for a computer processor to render.

- For the same reason, keep the amount of alpha or transparency you use in a SWF
  file to a minimum.

  Animating objects that include transparency is processor-intensive and should
  be kept to a minimum. Animating transparent graphics over bitmaps is a
  particularly processor-intensive kind of animation, and must be kept to a
  minimum or avoided completely.

  > **Note:** The best bitmap format to import into Flash Pro is PNG, which is
  > the native file format of Macromedia Fireworks from Adobe. PNG files have
  > RGB and alpha information for each pixel. If you import a Fireworks PNG file
  > into Flash Pro, you retain some ability to edit the graphic objects in the
  > FLA file.

- Optimize bitmaps without overcompressing them. A 72‑dpi resolution is optimal
  for the web. Compressing a bitmap image reduces file size, but compressing it
  too much compromises the quality of the graphic. Check that the settings for
  JPEG quality in the Publish Settings dialog box do not overcompress the image.
  Representing an image as a vector graphic is preferable in most cases. Using
  vector images reduces file size, because the images are made from calculations
  instead of many pixels. Limit the number of colors in your image while still
  retaining quality.

  > **Note:** Avoid scaling bitmaps larger than their original dimensions,
  > because it reduces the quality of the image and is processor intensive.

- Set the `_visible` property to `false` instead of changing the `_alpha` level
  to 0 or 1 in a SWF file. Calculating the `_alpha` level for an instance on the
  Stage is processor intensive. If you disable the instance's visibility, it
  saves CPU cycles and memory, which can give your SWF files smoother
  animations. Instead of unloading and possibly reloading assets, set the
  `_visible` property to `false`, which is less processor-intensive.

- Reduce the number of lines and points you use in a SWF file. Use the Optimize
  Curves dialog box (Modify \> Shape \> Optimize) to reduce the number of
  vectors in a drawing. Select the Use Multiple Passes option for more
  optimization. Optimizing a graphic reduces file size, but compressing it too
  much compromises its quality. However, optimizing curves reduces your file
  size and improves SWF file performance. Third-party options are available for
  specialized optimization of curves and points that yield different results. To
  get the best results, try different ways of producing animated content, and
  test each of the options.

A higher frame rate (measured in frames per second, or _fps_) produces smooth
animation in a SWF file but it can be processor-intensive, particularly on older
computers. Test your animations at different frame rates to find the lowest
frame rate possible.

For a sample of scripted animation, see the Flash Samples web page at
[www.adobe.com/go/learn_fl_samples](https://web.archive.org/web/20111105041642mp_/http://www.adobe.com/go/learn_fl_samples).
Download and decompress the Samples zip file and navigate to the
ActionScript2.0/Animation folder to access the sample.

More Help topics

[Animation frame rate and performance](../optimizing-fla-files-for-swf-output/animation-frame-rate-and-performance.md)

[Video conventions](../video-conventions.md)
