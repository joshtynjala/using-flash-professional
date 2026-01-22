# Optimize Flash documents

As your document file size increases, so does its download time and playback
speed. You can take several steps to prepare your document for optimal playback.
As part of the publishing process, Flash Pro automatically performs some
optimization on documents. Before exporting a document, you can optimize it
further by using various strategies to reduce the file size. You can also
compress a SWF file as you publish it. As you make changes, test your document
by running it on a variety of computers, operating systems, and Internet
connections.

## Optimize documents

- Use symbols, animated or otherwise, for every element that appears more than
  once.

- Use tweened animations whenever possible when creating animation sequences.
  Tweened animations use less file space than a series of keyframes.

- Use movie clips instead of graphic symbols for animation sequences.

- Limit the area of change in each keyframe; make the action take place in as
  small an area as possible.

- Avoid animating bitmap elements; use bitmap images as background or static
  elements.

- Use mp3, the smallest sound format, whenever possible.

## Optimize elements and lines

- Group elements.

- Use layers to separate elements that change during the animation from elements
  that do not.

- Use Modify \> Shape \> Optimize to minimize the number of separate lines that
  are used to describe shapes.

- Limit the number of special line types, such as dashed, dotted, ragged, and so
  on. Solid lines require less memory. Lines created with the Pencil tool
  require less memory than brush strokes.

## Optimize text and fonts

- Limit the number of fonts and font styles. Use embedded fonts sparingly
  because they increase file size.

- For Embed Fonts options, select only the characters needed instead of
  including the entire font.

## Optimize colors

- Use the Color menu in the Symbol Property inspector to create many instances
  of a single symbol in different colors.

- Use the Color panel (Window \> Color) to match the color palette of the
  document to a browser-specific palette.

- Use gradients sparingly. Filling an area with gradient color requires about 50
  bytes more than filling it with solid color.

- Use alpha transparency sparingly because it can slow playback.
