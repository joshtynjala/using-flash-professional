# Working with classic text

## About classic text

Classic text is the name for the older text engine in Flash Professional. The
classic text engine is still available in Flash Professional CS5 and later.
Classic text may be preferable for certain types of content, such as for mobile
devices, where SWF file size must be kept to a minimum. However, in some cases,
such as those requiring fine control over text layout, you will want to use the
new TLF text. For information about TLF text, see
[Working with Text Layout Framework (TLF) text](./working-with-text-layout-framework-tlf-text.md).

You specify whether an individual text object on the Stage uses the Classic or
TLF text engine by selecting the text object and then choosing the desired text
engine in the Text Property inspector.

> **Note:** You can change the text engine used by a text object at any time.
> For infomration about converting Classic text to TLF text, see
> [Converting between Classic and TLF text](./working-with-text-layout-framework-tlf-text.md#converting-between-classic-and-tlf-text).
> You can include classic text in your Flash Pro applications in a variety of
> ways. You can create text fields containing _static_ text, which you create
> when you author the document. You can also create _dynamic_ text fields, which
> display updating text, such as stock quotes or news headlines, and _input_
> text fields, which allow users to enter text for forms or surveys.

Flash Pro provides many ways to work with text. For example, you can orient text
horizontally or vertically; set attributes such as font, size, style, color, and
line spacing; check spelling; transform text by rotating, skewing, or flipping;
link text; make text selectable; animate text; control font substitution; and
use a font as part of a shared library. Flash Pro documents can use Type 1
PostScript® fonts, TrueType®, and bitmap fonts (Macintosh only).

You can preserve rich text formatting in text fields, using HTML tags and
attributes. When you use HTML text for the content of a dynamic or input text
field, the text can flow around an image, such as a SWF or JPEG file or a movie
clip. See Using HTML-formatted text in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120102171708mp_/http://www.adobe.com/go/learn_cs5_learningas2_en).

Like movie clip instances, text field instances are ActionScript® objects that
have properties and methods. By giving a text field an instance name, you can
manipulate it with ActionScript. However, you cannot write ActionScript code
inside a text instance, because text instances don't have Timelines.

You can use ActionScript to format input and dynamic text, and to create
scrolling text fields. ActionScript has events for dynamic and input text fields
that you can capture and use to trigger scripts. For information on using
ActionScript to control text, see Working with Text and Strings in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120102171708mp_/http://www.adobe.com/go/learn_cs5_learningas2_en).

## About classic text fields

You can create three types of classic text fields: static, dynamic, and input.

- Static text fields display text that doesn't change characters dynamically.

- Dynamic text fields display dynamically updating text, such as stock quotes or
  weather reports.

- Input text fields allow users to enter text in forms or surveys.

  You can create horizontal text (with a left-to-right flow) or static vertical
  text (with either a right-to-left or left-to-right flow). Note that the use of
  horizontal [bidirectional](https://en.wikipedia.org/wiki/BiDi) languages
  (Hebrew, Arabic etc.) in classic text fields is not supported. TLF fields
  should be used instead.

  When creating static text, you can place text on a single line that expands as
  you type, or in a fixed-width field (for horizontal text) or fixed-height
  field (for vertical text) that expands and wraps words automatically. When
  creating dynamic or input text, you can place text on a single line, or create
  a text field with a fixed width and height.

  All classic text fields support Unicode.

  Flash Pro displays a handle on the corner of each text field to identify the
  type of text field:

- For static horizontal text that extends, a round handle appears at the
  upper-right corner of the text field.

    <p><i>Image missing: tx_text_static_extend.png</i></p>

    <caption>A round handle at the upper-right corner of the text field.</caption>

- For static horizontal text that has a fixed width, a square handle appears at
  the upper-right corner of the text field.

      <p><i>Image missing: tx_text_static_defined.png</i></p>

      <caption>A square handle appears at the upper-right corner of the text field.</caption>

- For static vertical text that has right-to-left flow and extends, a round
  handle appears at the lower-left corner of the text field.

      <p><i>Image missing: tx_text_static_extend_vert_rl.png</i></p>

      <caption>A round handle appears at the lower-left corner of the text field.</caption>

- For static vertical text that has right-to-left flow and a fixed height, a
  square handle appears at the lower-left corner of the text field.

      <p><i>Image missing: tx_text_static_fixed_vert_rl.png</i></p>

      <caption>A square handle appears at the lower-left corner of the text field.</caption>

- For static vertical text that has left-to-right flow and extends, a round
  handle appears at the lower-right corner of the text field.

      <p><i>Image missing: tx_text_static_extend_vert_lr.png</i></p>

      <caption>A round handle appears at the lower-right corner of the text field.</caption>

- For static vertical text that has left-to-right flow and a fixed height, a
  square handle appears at the lower-right corner of the text field.

      <p><i>Image missing: tx_text_static_fixed_vert_lr.png</i></p>

      <caption>A square handle appears at the lower-right corner of the text field.</caption>

- For dynamic or input text fields that extend, a round handle appears at the
  lower-right corner of the text field.

      <p><i>Image missing: tx_text_dynamic_extend.png</i></p>

      <caption>A round handle appears at the lower-right corner of the text field.</caption>

- For dynamic or input text that has a defined height and width, a square handle
  appears at the lower-right corner of the text field.

      <p><i>Image missing: tx_text_dynamic_fixed.png</i></p>

      <caption>A square handle appears at the lower-right corner of the text field.</caption>

- For dynamic scrollable classic text fields, the round or square handle becomes
  solid black instead of hollow.

      <p><i>Image missing: tx_text_dynamic_scrollable.png</i></p>

      <caption>The round or square handle becomes solid black instead of hollow.</caption>

  Shift-double-click the handle of dynamic and input text fields to create text
  fields that don't expand when you enter text on the Stage. This allows you to
  create a text field of a fixed size and fill it with more text than it can
  display to create scrolling text.

  After you use the Text tool to create a text field, use the Property inspector
  to specify the type of text field, and to set values that control how the text
  field and its contents appear in the SWF file.

## Create and edit text fields

Text is horizontal by default. However, static text can also be aligned
vertically.

You can use most common word-processing techniques to edit text in Flash Pro.
Use the Cut, Copy, and Paste commands to move text in a Flash Pro file as well
as between Flash Pro and other applications.

### Add text to the Stage

1.  Select the Text tool <i>Image Missing: type.png</i>.
2.  Select Classic Text from the Text Engine menu at the top of the Text
    Property inspector.
3.  In the Property inspector (Window \> Properties), select a text type from
    the pop‑up menu to specify the type of text field:

    **Dynamic Text**  
    Creates a field that displays dynamically updating text.

    **Input Text**  
    Creates a field in which users can enter text.

    **Static Text**  
    Creates a field that cannot update dynamically.

4.  For static text only: In the Text Property inspector, select a direction for
    text orientation and flow from the Orientation Of Text menu. (Horizontal is
    the default setting.)
5.  On the Stage, do one of the following:
    - To create a text field that displays text in a single line, click where
      you want the text to start.

    - To create a text field with a fixed width (for horizontal text) or fixed
      height (for vertical text), position the pointer where you want the text
      to start and drag to the desired width or height.

    > **Note:** If you create a text field that extends past the edge of the
    > Stage as you type, the text isn't lost. To make the handle accessible
    > again, add line breaks, move the text field, or select View \> Pasteboard.

6.  Select text attributes in the Property inspector.

### Change the size of a text field

![](../img/dingbat.png) Drag the text field's resize handle.

When text is selected, a blue bounding box lets you resize the text field by
dragging one of its handles. Static text fields have four handles that let you
resize the text field horizontally. Dynamic text fields have eight handles that
let you resize the text field vertically, horizontally, or diagonally.

### Switch a text field between fixed-width (or fixed-height) and extending

![](../img/dingbat.png) Double-click a resize handle.

### Select characters in a text field

1.  Select the Text tool <i>Image Missing: type.png</i>.
2.  Do one of the following:
    - Drag to select characters.

    - Double-click to select a word.

    - Click to specify the beginning of the selection, and Shift-click to
      specify the end of the selection.

    - Press Control+A (Windows) or Command+A (Macintosh) to select all the text
      in the field.

### Select text fields

![](../img/dingbat.png) Using the Selection tool ![](../img/selection.png),
click a text field. Shift-click to select multiple text fields.

### Set dynamic and input text options

1.  Click in an existing dynamic text field.

2.  In the Property inspector, make sure Dynamic or Input is displayed in the
    pop‑up menu.

3.  Enter an instance name for the text field.

4.  Specify the height, width, and location of text.

5.  Select the font and style.

6.  In the Paragraph section of the Property inspector, specify one of the
    following options from the Behavior menu:

    **Single line**  
    Displays the text as one line.

    **Multiline**  
    Displays the text in multiple lines.

    **Multiline No Wrap**  
    Displays text in multiple lines that break only if the last character is a
    breaking character, such as Enter (Windows) or Return (Macintosh).

7.  To enable users to select dynamic text, click Selectable <i>Image Missing:
    text-selctbl.png</i>. Deselect this option to prevent users from selecting
    dynamic text.

8.  To preserve rich text formatting (such as fonts and hyperlinks) with the
    appropriate HTML tags, click Render Text As HTML <i>Image Missing:
    render_text_HTML.png</i>.

9.  To display a black border and white background for the text field, click
    Show Border Around Text <i>Image Missing: show_border.png</i>.

10. (Optional) In the Var box, enter the variable name for the text field. (Use
    this option only when authoring for Macromedia Flash Player 5 from Adobe or
    earlier.)

    Beginning with Macromedia Flash MX (version 6), you assign the text field an
    instance name using the Property inspector. Although you can use the
    variable name method with dynamic text fields for backwards compatibility to
    Macromedia Flash 5 and earlier versions, Adobe doesn't recommend this,
    because you can't control other text field properties, or apply style sheet
    settings.

11. (Optional) Click Embed to open the Font Embedding dialog box. for more
    information, see
    [Embed fonts for consistent text appearance](./embed-fonts-for-consistent-text-appearance.md).

### Set preferences for vertical text

1.  Select Edit \> Preferences (Windows) or Flash \> Preferences (Macintosh) and
    click the Text category in the Preferences dialog box.
2.  Under Vertical Text, set any of these options:

    **Default Text Orientation**  
    Automatically gives new text fields vertical orientation.

    **Right to Left Text Flow**  
    Makes lines of vertical text fill the page from right to left.

    **No Kerning**  
    Prevents kerning from being applied to vertical text. (Kerning remains
    enabled for horizontal text.)

## Setting classic text attributes

### About classic text attributes

> **Note:** To use Cascading Style Sheets (CSS), use ActionScript to apply a
> stylesheet. For more information, see
> [Applying cascading style sheets](https://web.archive.org/web/20120102171708mp_/http://help.adobe.com/en_US/as3/dev/WS8d7bb3e8da6fb92f-20050207122bd5f80cb-7ff3zephyr_serranozephyr.html)
> in the ActionScript 3.0 Developer's Guide. You can set the font and paragraph
> attributes of text. Font attributes include font family, point size, style,
> color, letter spacing, autokerning, and character position. Paragraph
> attributes include alignment, margins, indents, and line spacing.

For static text, font outlines are exported in a published SWF file. For
horizontal static text, you can use device fonts instead of exporting font
outlines.

For dynamic or input text, Flash Pro stores the names of the fonts, and Flash
Player locates identical or similar fonts on the user's system. You can also
embed font outlines in dynamic or input text fields. Embedding font outlines can
increase file size, but it ensures that users have the correct font information.

When creating new text, Flash Pro uses the text attributes that are currently
set in the Property inspector. When you select existing text, use the Property
inspector to change font or paragraph attributes, and to direct Flash Pro to use
device fonts rather than embedding font outline information.

### Set a font, point size, style, and color

1.  Using the Selection tool ![](../img/selection.png), select one or more text
    fields on the Stage.

2.  In the Property inspector (Window \> Properties), select a font from the
    Family pop‑up menu, or enter a font name.

    > **Note:** The \_sans, \_serif, \_typewriter, and device fonts can be used
    > only with static horizontal text.

3.  Enter a value for the font size.

    Font size is set in points, regardless of the current ruler units.

4.  To apply bold or italic style, select the style from the Style menu.

    If the selected font does not include a bold or italic style, the style does
    not appear in the menu. You can select the Faux Bold or Faux Italic styles
    from the Text menu (Text \> Style \> Faux Bold or Faux Italic). Faux Bold
    and Faux Italic styles are added to the Regular style by the operating
    system. The faux styles may not look as good as fonts that include a true
    bold or italic style.

5.  Select a font rendering method from the Anti-Aliasing pop‑up menu (directly
    below the Color control) to optimize text.

6.  To select a fill color for text, click the Color control and do one of the
    following:
    - Select a color from the Color menu.

    - Type a color's hexadecimal value in the box in the upper-left corner.

    - Click Color Picker <i>Image Missing: color_picker.png</i> and select a
      color from the system color picker. (When setting the text color, use only
      solid colors, not gradients. To apply a gradient to text, break the text
      apart and convert the text to its component lines and fills.)

### Set letter spacing, kerning, and character position

Letter spacing inserts a uniform amount of space between characters. Use letter
spacing to adjust the spacing of selected characters or entire blocks of text.

Kerning controls the spacing between pairs of characters. Many fonts have
built-in kerning information. For example, _A_ and _V_ are often closer together
than _A_ and _D_. Flash Pro provides horizontal tracking and kerning (for
horizontal text) and vertical tracking and kerning (for vertical text).

For vertical text, you can disable kerning by default in Flash Preferences. If
you do this and leave the kerning option selected in the Property inspector,
kerning is applied to horizontal text only.

1.  Using the Text tool <i>Image Missing: type.png</i>, select one or more
    sentences, phrases, or text fields on the Stage.
2.  In the Property inspector (Window \> Properties), set the following options:
    - To specify letter spacing (tracking and kerning), enter a value in the
      Letter Spacing field.

    - To use a font's built-in kerning information, select Auto-Kern.

    - To specify superscript or subscript character position, click the Toggle
      Superscript or Toggle Subscript button. The default position is Normal.
      Normal places text on the baseline, Superscript places text above the
      baseline (horizontal text) or to the right of the baseline (vertical
      text), and Subscript places text below the baseline (horizontal text) or
      to the left of the baseline (vertical text).

### Set alignment, margins, indents, and line spacing

Alignment determines the position of each line of text in a paragraph relative
to edges of the text field. Horizontal text is aligned relative to the left and
right edges of the text field, and vertical text is aligned relative to the top
and bottom edges of the text field. Text can be aligned to one edge of the text
field, centered in the text field, or aligned to both edges of the text field
(full justification).

Margins determine the amount of space between the border of a text field and its
text. Indents determine the distance between the margin of a paragraph and the
beginning of the first line.

Line spacing determines the distance between adjacent lines in a paragraph. For
vertical text, line spacing adjusts the space between vertical columns.

#### Work with horizontal text

1.  Using the Text tool <i>Image Missing: type.png</i>, select one or more text
    fields on the Stage.
2.  In the Property inspector (Window \> Properties), set the following options:
    - To set alignment, click Left, Center, Right, or Full Justification.

    - To set the left or right margin, enter values in the Margins text fields
      in the Paragraph section of the Property inspector.

    - To specify indents, enter a value in the Indentation text field in the
      Paragraph section of the Property inspector.

    - To specify line spacing, enter a value in the Line Spacing text field in
      the Paragraph section of the Property inspector.

#### Work with vertical text

1.  Using the Text tool <i>Image Missing: type.png</i>, select one or more text
    fields on the Stage.
2.  In the Property inspector (Window \> Properties), set the following options:
    - To set alignment, click Top, Center, Bottom, or Full Justification.

    - To set the top or bottom margin, enter values in the Margins fields in the
      Paragraph section of the Property inspector.

    - To specify indents, enter a value in the Indentation text field in the
      Paragraph section of the Property inspector.

    - To specify line spacing, enter a value in the Line Spacing text field in
      the Paragraph section of the Property inspector.

### Classic text anti-aliasing

Anti-aliasing lets you smooth the edges of onscreen text. The anti-aliasing
options are particularly effective for rendering smaller font sizes. When
anti-aliasing is enabled, all text in the current selection is affected.
Anti-aliasing operates with text of all point sizes in the same way.

Anti-aliasing is supported for static, dynamic, and input text if the user has
Flash® Player 7 or later. It is supported only for static text if the user has
an earlier version of Flash Player.

When using small text in a Flash Pro document, keep in mind the following
guidelines:

- Sans serif text, such as Helvetica or Arial, appears clearer at small sizes
  than serif text.

- Some type styles, such as bold and italic, can make text less legible at small
  sizes.

- In some cases, text appears somewhat smaller than text of the same point size
  in other applications.

The Flash Pro text rendering engine provides clear, high-quality text rendering
in Flash Pro (FLA) documents and published SWF files. The Anti-alias for
Readability setting makes text more legible, particularly at small font sizes.
Custom anti-aliasing lets you specify the thickness and sharpness of fonts used
in individual text fields.

High quality anti-aliasing is automatically enabled whenever you publish to
Flash Player 8 or later and Anti-Alias For Readability or Custom Anti-Alias is
selected. Anti-Alias For Readability may cause a slight delay when you load
Flash Pro SWF files, especially if you are using four or five different
character sets in the first frame of a Flash Pro document. High-quality
anti-aliasing may also increase Flash Player's memory usage. Using four or five
fonts, for example, can increase memory usage by approximately 4 MB.

When the publish setting of your file is Adobe® Flash® Player 8 or later, and
Anti-Alias For Readability or Custom Anti-Alias is your chosen anti-aliasing
option, high-quality anti-aliasing applies to the following:

- Untransformed text that is scaled or rotated

  > **Note:** Although the text can be scaled or rotated, it must remain flat
  > (that is, untransformed). For example, if you skew the fonts or otherwise
  > manipulate the font shapes, Anti-Alias for Readability is automatically
  > disabled.

- All font families (including bold, italic, and so on)

- Display sizes of up to 255 points

- Exporting to most non-Flash Pro file formats (GIF or JPEG)

High-quality anti-aliasing is disabled under the following conditions:

- Flash Player 7 or earlier is the selected version of Flash Player.

- An anti-aliasing option other than Anti-Alias for Readability or Custom
  Anti-Alias is selected.

- Text is skewed or flipped.

- The FLA file is exported to a PNG file.

### Work with text anti-aliasing

Flash Pro provides improved font rasterization that lets you specify the
anti-aliasing properties for fonts. The improved anti-aliasing capabilities are
available only for SWF files published for Flash Player 8 or later. If you are
publishing files for earlier versions of Flash Player, you can only use the
Anti-Alias For Animation feature.

> **Note:** Anti-aliasing requires that the fonts used by a text field are
> embedded. If you do not embed the fonts, then the text field may appear blank
> for classic text. If changing the Anti-Alias setting to Use Device Fonts
> causes the text to appear incorrectly, then you need to embed the fonts. Flash
> automatically embeds the fonts for text that already exists in a text field
> created on the Stage. However, if you plan to allow the text to change at
> runtime, you should embed the fonts manually. For instructions, see
> [Embed fonts for consistent text appearance](./embed-fonts-for-consistent-text-appearance.md).

#### Choose an anti-aliasing option for selected text

![](../img/dingbat.png) In the Property inspector, choose one of the following
options from the Anti-Aliasing pop‑up menu:

Use Device Fonts  
Specifies that the SWF file use the fonts installed on the local computer to
display the fonts. Typically, device fonts are legible at most font sizes.
Although this option doesn't increase the size of the SWF file, it forces you to
rely on the fonts installed on the user's computer for font display. When using
device fonts, choose only commonly installed font families.

You cannot use device fonts with rotated or vertical classic text. If you want
to use rotated or vertical classic text, select another anti-alias mode and
embed the fonts used by the text field.

Bitmap Text (No Anti-Alias)  
Turns off anti-aliasing and provides no text smoothing. The text is displayed
using sharp edges, and the resulting SWF file size is increased because the font
outlines are embedded in the file. Bitmap text is sharp at the exported size,
but scales poorly.

Anti-Alias For Animation  
Creates a smoother animation by ignoring alignment and kerning information. This
option creates a larger SWF file because font outlines are embedded. For
legibility, use 10-point or larger type when specifying this option.

Anti-Alias For Readability  
Uses the Flash text rendering engine to improve the legibility of fonts,
particularly at small sizes. This option creates a larger SWF file because font
outlines are embedded. To use this option, you must publish to Flash Player 8 or
later. (Do not use this option if you intend to animate text; instead, use
Anti-Alias For Animation.)

Custom Anti-Alias  
Lets you modify the font's properties. Use Sharpness to specify the smoothness
of the transition between the text edges and the background. Use Thickness to
specify how thick the font anti-aliasing transition appears. (Larger values
cause the characters to look thicker.) Specifying Custom Anti-Alias creates a
larger SWF file because font outlines are embedded. To use this option, you must
publish to Flash Player 8 or later.

#### Upgrade content for Flash 8 or later anti-aliasing

1.  Open a FLA file created for use with Flash Player 7 or earlier.
2.  In the Publish Settings dialog box (File \> Publish Settings), select Flash
    Player 8 or Flash Player 9 from the Version pop‑up menu.
3.  Select the text field to apply the Anti-Alias For Readability or Custom
    Anti-Alias option to.
4.  In the Property inspector, select Anti-Alias For Readability or Custom
    Anti-Alias from the Font Rendering Method pop‑up menu.

### Make classic text selectable

Static horizontal text or dynamic text can be selectable by users viewing your
Flash Pro application. (Input text is selectable by default.) After selecting
text, the user can copy, cut, and then paste the text into a separate document.

1.  Using the Text tool <i>Image Missing: type.png</i>, select the horizontal
    text that you want to make selectable.
2.  In the Property inspector (Window \> Properties), select Static Text or
    Dynamic Text.
3.  Click Selectable <i>Image Missing: text-selctbl.png</i>.

## Transforming text

You can create text effects by transforming text fields. For example, you can
rotate, skew, flip, and scale text fields. (When you scale a text field as an
object, the Property inspector does not reflect increases or decreases in point
size.) The text in a transformed text field can still be edited, although severe
transformations may make it difficult to read.

You can also animate text by using Timeline effects. For example, you can make
text bounce, fade in or out, or explode.

## Break Classic text apart

You can break apart Classic text to place each character in a separate text
field. Then you can quickly distribute the text fields to separate layers and
animate each field. However, you cannot break apart text in scrollable classic
text fields.

You can also convert the text to its component lines and fills to reshape,
erase, and otherwise manipulate it as a graphic. As with any other shape, you
can individually group these converted characters, or change them to symbols and
animate them. After you convert text to graphic lines and fills, you can no
longer edit the text.

> **Note:** The Break Apart command for Classic text applies only to outline
> fonts such as TrueType fonts. Bitmap fonts disappear from the screen when you
> break them apart. PostScript fonts can be broken apart only on Macintosh
> systems.

1.  Using the Selection tool ![](../img/selection.png), click a text field.

2.  Select Modify \> Break Apart.

    Each character in the selected text is placed in a separate text field. The
    text remains in the same position on the Stage.

3.  Select Modify \> Break Apart again to convert the characters to shapes on
    the Stage.

## Create a text hyperlink

1.  Select text or a text field:
    - Use the Text tool <i>Image Missing: type.png</i> to select text in a text
      field.

    - To link all the text in a text field, use the Selection
      tool ![](../img/selection.png) to select a text field.

2.  In the Link text field in the Options section of the Property inspector
    (Window \> Properties), enter the URL to which you want to link the text
    field.

> **Note:** To create a link to an e-mail address, use the mailto: URL. For
> example, enter `mailto:adamsmith@example.com`.

## Create scrolling classic text

There are several ways to create scrolling text in Flash Pro:

- Make dynamic or input text fields scrollable by using menu commands or the
  text field handle. This does not add a scrollbar to the text field, but
  instead allows the user to scroll the text with the arrow keys (for text
  fields also set to Selectable) or the mouse wheel. The user must first click
  the text field to give it focus.

- Add an ActionScript 3.0 UIScrollbar component to a text field to make it
  scroll. For more information, see "Use the UIScrollBar component" in
  [_Using ActionScript 3.0 Components_](https://web.archive.org/web/20120102171708mp_/http://help.adobe.com/en_US/ActionScript/3.0_UsingComponentsAS3/).

- In ActionScript 3.0, use the `scrollH` and `scrollV` properties of the
  `TextField` class.

- Add an ActionScript 2.0 ScrollBar component to a text field to make it scroll.
  For more information, see "UIScrollBar Component" in the
  [_ActionScript 2.0 Components Language Reference_](https://web.archive.org/web/20120102171708mp_/http://www.adobe.com/go/learn_cs5_as2complangref_en).

- In ActionScript 2.0, use the TextField object's `scroll` and `maxscroll`
  properties to control vertical scrolling and the `hscroll` and `maxhscroll`
  properties to control horizontal scrolling in a text field. See Example:
  Creating scrolling text in
  [_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120102171708mp_/http://www.adobe.com/go/learn_cs5_learningas2_en).

### Make dynamic text scrollable

![](../img/dingbat.png) Do one of the following:

- Shift-double-click the lower-right handle on the dynamic text field. The
  handle will turn from an unfilled square (non-scrollable) to a filled square
  (scrollable).

- Using the Selection tool ![](../img/selection.png), select the dynamic text
  field and then select Text \> Scrollable.

- Select the dynamic text field with the Selection tool. Right-click (Windows)
  or Control-click (Macintosh) the dynamic text field and select Scrollable from
  the context menu.

## Masking device font text

You can use a movie clip to mask device font text in another movie clip. (You
cannot mask device fonts by using a mask layer on the Stage.) For this movie
clip mask to function, the user must have Flash Player 6 (6.0.40.0) or later.

When you use a movie clip to mask device font text, Flash Pro uses the
rectangular bounding box of the mask as the masking shape. That is, if you
create a nonrectangular movie clip mask for device font text in the Flash Pro
authoring environment, the mask that appears in the SWF file takes the shape of
the rectangular bounding box of the mask, not the shape of the mask itself.

For more information on using a movie clip as a mask, see Using movie clips as
masks in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20120102171708mp_/http://www.adobe.com/go/learn_cs5_learningas2_en).

For a sample of device font masking, see the Flash Samples web page at
[www.adobe.com/go/learn_fl_samples](https://web.archive.org/web/20120102171708mp_/http://www.adobe.com/go/learn_fl_samples).
Download and decompress the Samples zip file and navigate to the
Masking\DeviceFontMasking folder to access the sample.

## Unicode text encoding in SWF applications

Flash Player 7 and later support Unicode text encoding for SWF files in Flash
Player format. This support greatly enhances your ability to use multilanguage
text in your SWF files, such as two languages within a single text field. Any
user with Flash Player 7 or later can view multilanguage text in a Flash Player
7 or later application, regardless of the language used by the operating system
running the player.

More Help topics

[Transforming objects](../creating-and-editing-artwork/transforming-and-combining-graphic-objects.md#transforming-objects)

[Transforming and combining graphic objects](../creating-and-editing-artwork/transforming-and-combining-graphic-objects.md)

[Distributing objects to layers for tweened animation](../timelines-and-animation/animation-basics.md#distributing-objects-to-layers-for-tweened-animation)

[Timelines and Animation](../timelines-and-animation/index.md)

[Creating multilanguage text](./multilanguage-text.md#creating-multilanguage-text)
