# Working with symbols

## About symbols

A \_symbol \_is a graphic, button, or movie clip that you create once in the
Flash Pro authoring environment or by using the Button (AS 2.0), SimpleButton
(AS 3.0), and MovieClip classes. You can then reuse the symbol throughout your
document or in other documents.

A symbol can include artwork that you import from another application. Any
symbol that you create automatically becomes part of the library for the current
document.

An _instance_ is a copy of a symbol located on the Stage or nested inside
another symbol. An instance can be different from its parent symbol in color,
size, and function. Editing the symbol updates all of its instances, but
applying effects to an instance of a symbol updates only that instance.

Using symbols in your documents dramatically reduces file size; saving several
instances of a symbol requires less storage space than saving multiple copies of
the contents of the symbol. For example, you can reduce the file size of your
documents by converting static graphics, such as background images, into symbols
and then reusing them. Using symbols can also speed SWF file playback, because a
symbol needs to be downloaded to Flash® Player only once.

Share symbols among documents as shared library assets during authoring or at
runtime. For runtime shared assets, you can link assets in a source document to
any number of destination documents, without importing the assets into the
destination document. For assets shared during authoring, you can update or
replace a symbol with any other symbol available on your local network.

If you import library assets with the same name as assets already in the
library, you can resolve naming conflicts without accidentally overwriting
existing assets.

Additional introductory instruction about symbols is available from these
resources:

- Flash Professional Design Center article:
  [Using Flash for the first time – Part 1: Building a banner](https://web.archive.org/web/20120104100145mp_/http://www.adobe.com/designcenter/flash/articles/flacs3it_firstflash_pt1.html)

#### Types of symbols

Each symbol has a unique Timeline and Stage, complete with layers. You can add
frames, keyframes, and layers to a symbol Timeline, just as you can to the main
Timeline. When you create a symbol you choose the symbol type.

- Use graphic symbols ![](../img/GraphicSymbol.png) for static images and to
  create reusable pieces of animation that are tied to the main Timeline.
  Graphic symbols operate in sync with the main Timeline. Interactive controls
  and sounds won't work in a graphic symbol's animation sequence. Graphic
  symbols add less to the FLA file size than buttons or movie clips because they
  have no timeline.

- Use button symbols ![](../img/Button.png) to create interactive buttons that
  respond to mouse clicks, rollovers, or other actions. You define the graphics
  associated with various button states, and then assign actions to a button
  instance. For more information, see Handling events in
  [Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)
  or
  [Handling events](https://web.archive.org/web/20120104100145mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b90204-7fca.html)
  in the _ActionScript 3.0 Developer's Guide_.

- Use movie clip symbols ![](../img/MovieClip.png) to create reusable pieces of
  animation. Movie clips have their own multiframe Timeline that is independent
  from the main Timeline—think of them as nested inside a main Timeline that can
  contain interactive controls, sounds, and even other movie clip instances. You
  can also place movie clip instances inside the Timeline of a button symbol to
  create animated buttons. In addition, movie clips are scriptable with
  ActionScript®.

- Use font symbols to export a font and use it in other Flash Pro documents.

  Flash Pro provides built‑in _components_, movie clips with defined parameters,
  that you can use to add user interface elements, such as buttons, checkboxes,
  or scroll bars, to your documents. For more information, see About Components
  in _Using ActionScript 2.0 Components_, or
  [About ActionScript 3.0 Components](https://web.archive.org/web/20120104100145mp_/http://help.adobe.com/en_US/as3/components/WS5b3ccc516d4fbf351e63e3d118a9c64d27-7ff4.html)
  in _Using ActionScript 3.0 Components_.

  > **Note:** To preview animation in component instances and scaling of
  > 9-slice-scaled movie clips in the Flash Pro authoring environment, select
  > Control \> Enable Live Preview.

## Create symbols

You can create a symbol from selected objects on the Stage, create an empty
symbol and make or import the content in symbol-editing mode, and create font
symbols in Flash Pro. Symbols can contain all the functionality that Flash Pro
can create, including animation.

Using symbols that contain animation lets you create Flash Pro applications with
a lot of movement while minimizing file size. Consider creating animation in a
symbol that has a repetitive or cyclic action—the up‑and‑down motion of a bird's
wings, for example.

To add symbols to your document, use shared library assets during authoring or
at runtime.

### Convert selected elements to a symbol

1.  Select an element or several elements on the Stage. Do one of the following:
    - Select Modify \> Convert To Symbol.

    - Drag the selection to the Library panel.

    - Right-click (Windows) or Control-click (Macintosh) and select Convert To
      Symbol from the context menu.

2.  In the Convert To Symbol dialog box, type the name of the symbol and select
    the behavior.

3.  Click in the registration grid to position the registration point for the
    symbol.

4.  Click OK.

    Flash Pro adds the symbol to the library. The selection on the Stage becomes
    an instance of the symbol. Once you have created a symbol, you can edit it
    in symbol edit mode by choosing Edit \> Edit Symbols, or you can edit it in
    the context of the Stage by choosing Edit \> Edit In Place. You can also
    change the registration point of a symbol.

### Create an empty symbol

1.  Do one of the following:
    - Select Insert \> New Symbol.

    - Click the New Symbol button at the lower left of the Library panel.

    - Select New Symbol from the Library Panel menu in the upper-right corner of
      the Library panel.

2.  In the Create New Symbol dialog box, type the name of the symbol and select
    the behavior.

3.  Click OK.

    Flash Pro adds the symbol to the library and switches to symbol-editing
    mode. In symbol-editing mode, the name of the symbol appears above the
    upper-left corner of the Stage, and a cross hair indicates the symbol's
    registration point.

4.  To create the symbol content, use the Timeline, draw with the drawing tools,
    import media, or create instances of other symbols.

5.  To return to document-editing mode, do one of the following:
    - Click the Back button.

    - Select Edit \> Edit Document.

    - Click the scene name in the Edit bar.

      When you create a symbol, the registration point is placed at the center
      of the window in symbol-editing mode. You can place the symbol contents in
      the window in relation to the registration point. To change the
      registration point, when you edit a symbol, move the symbol contents in
      relation to the registration point.

## Convert animation on the Stage into a movie clip symbol

To reuse an animated sequence on the Stage, or to manipulate it as an instance,
select it and save it as a movie clip symbol.

1.  On the main Timeline, select every frame in every layer of the animation on
    the Stage that you want to use. For information on selecting frames, see
    [Insert frames in the Timeline](../timelines-and-animation/frames-and-keyframes.md#insert-frames-in-the-timeline).

2.  Do one of the following to copy the frames:
    - Right-click (Windows) or Control-click (Macintosh) any selected frame, and
      select Copy Frames from the context menu. To delete the sequence after
      converting it to a movie clip, select Cut.

    - Select Edit \> Timeline \> Copy Frames. To delete the sequence after
      converting it to a movie clip, select Cut Frames.

3.  Deselect your selection and make sure nothing on the Stage is selected.
    Select Insert \> New Symbol.

4.  Name the symbol. For Type, select Movie Clip, then click OK.

5.  On the Timeline, click Frame 1 on Layer 1, and select Edit \> Timeline \>
    Paste Frames.

    This action pastes the frames (and any layers and layer names) you copied
    from the main Timeline to the Timeline of this movie clip symbol. Any
    animation, buttons, or interactivity from the frames you copied now becomes
    an independent animation (a movie clip symbol) that you can reuse.

6.  To return to document-editing mode, do one of the following:
    - Click the Back button.

    - Select Edit \> Edit Document.

    - Click the scene name in the Edit bar above the Stage.

## Duplicate symbols

Duplicating a symbol lets you use an existing symbol as a starting point for
creating a symbol.

To create versions of the symbol with different appearances, also use instances.

### Duplicate a symbol using the Library panel

![](../img/dingbat.png) Select a symbol in the Library panel and do one of the
following:

- Right-click (Windows) or Control-click (Macintosh), and select Duplicate from
  the context menu.

- Select Duplicate from the Library Panel menu.

### Duplicate a symbol by selecting an instance

1.  Select an instance of the symbol on the Stage.

2.  Select Modify \> Symbol \> Duplicate Symbol.

    The symbol is duplicated, and the instance is replaced with an instance of
    the duplicate symbol.

## Edit symbols

When you edit a symbol, Flash Pro updates all the instances of that symbol in
your document. Edit the symbol in the following ways:

- In context with the other objects on the Stage by using the Edit In Place
  command. Other objects are dimmed to distinguish them from the symbol you are
  editing. The name of the symbol you are editing appears in an Edit bar at the
  top of the Stage, to the right of the current scene name.

- In a separate window, using the Edit In New Window command. Editing a symbol
  in a separate window lets you see the symbol and the main Timeline at the same
  time. The name of the symbol you are editing appears in the Edit bar at the
  top of the Stage.

  You edit the symbol by changing the window from the Stage view to a view of
  only the symbol, using symbol-editing mode. The name of the symbol you are
  editing appears in the Edit bar at the top of the Stage, to the right of the
  current scene name.

  When you edit a symbol, Flash Pro updates all instances of the symbol
  throughout the document to reflect your edits. While editing a symbol, use any
  of the drawing tools, import media, or create instances of other symbols.

- Change the registration point of a symbol (the point identified by the
  coordinates 0, 0) by using any symbol-editing method.

### Edit a symbol in place

1.  Do one of the following:
    - Double-click an instance of the symbol on the Stage.

    - Select an instance of the symbol on the Stage and right-click (Windows) or
      Control-click (Macintosh), and select Edit in Place.

    - Select an instance of the symbol on the Stage, and select Edit \> Edit In
      Place.

2.  Edit the symbol.
3.  To change the registration point, drag the symbol on the Stage. A cross hair
    indicates the location of the registration point.
4.  To exit edit-in-place mode and return to document-editing mode, do one of
    the following:
    - Click the Back button.

    - Select the current scene name from the Scene menu in the Edit bar.

    - Select Edit \> Edit Document.

    - Double-click outside the symbol content.

### Edit a symbol in a new window

1.  Select an instance of the symbol on the Stage and right-click (Windows) or
    Control-click (Macintosh), and select Edit In New Window.
2.  Edit the symbol.
3.  To change the registration point, drag the symbol on the Stage. A cross hair
    indicates the location of the registration point.
4.  Click the Close box in the upper-right corner (Windows) or upper-left corner
    (Macintosh) to close the new window, and click in the main document window
    to return to editing the main document.

### Edit a symbol in symbol-editing mode

1.  Do one of the following to select the symbol:
    - Double-click the symbol's icon in the Library panel.

    - Select an instance of the symbol on the Stage, and right-click (Windows)
      or Control-click (Macintosh), and select Edit from the context menu.

    - Select an instance of the symbol on the Stage and select Edit \> Edit
      Symbols.

    - Select the symbol in the Library panel and select Edit from the Library
      Panel menu, or right-click (Windows) or Control-click (Macintosh) the
      symbol in the Library panel and select Edit.

2.  Edit the symbol.
3.  To exit symbol-editing mode and return to editing the document, do one of
    the following:
    - Click the Back button at the left of the Edit bar at the top of the Stage.

    - Select Edit \> Edit Document.

    - Click the scene name in the Edit bar at the top of the Stage.

    - Double-click outside the symbol content.

More Help topics

[Creating buttons](./creating-buttons.md)

[Sharing library assets at runtime](./sharing-library-assets-across-files.md#sharing-library-assets-at-runtime)

[Work with libraries](./working-with-the-library.md#work-with-libraries)

[Embed fonts for consistent text appearance](../text/embed-fonts-for-consistent-text-appearance.md)

[Editing instance properties](./working-with-symbol-instances.md#editing-instance-properties)
