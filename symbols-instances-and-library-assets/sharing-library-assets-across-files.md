# Sharing library assets across files

## Sharing library assets at runtime

### About runtime shared library assets

Shared library assets let you use assets from one FLA file in another FLA file.
This can be useful in these situations:

- When more than one FLA file needs to use the same artwork or other assets.

- When a designer and a developer want to be able to edit artwork and
  ActionScript code in separate FLA files for a joint project.

Sharing library assets works like this:

- For runtime shared assets, assets from a source document are linked as
  external files in a destination document. Runtime assets are loaded into the
  destination document during document playback—that is, at runtime. The source
  document containing the shared asset does not need to be available on your
  local network when you author the destination document. The source document
  must be posted to a URL for the shared asset to be available to the
  destination document at runtime.

#### Tutorials and videos

- Tutorial:
  [Runtime Shared Library Tutorial](https://web.archive.org/web/20120115054337mp_/http://slekx.com/2010/01/flash-cs4-runtime-shared-library-tutorial/)
  (Flash CS4, includes some ActionScript 3.0, source: slekx.com)

### Working with runtime shared assets

Using runtime shared library assets involves two procedures. First, the author
of the source document defines a shared asset in the source document and enters
an identifier string for the asset and a URL _(HTTP or HTTPS only)_ where the
source document will be posted.

Second, the author of the destination document defines a shared asset in the
destination document and enters an identifier string and URL identical to those
used for the shared asset in the source document. Alternatively, the destination
document author can drag the shared assets from the posted source document into
the destination document library. The ActionScript version set in the Publish
settings must match that of the source document.

In either scenario, the source document must be posted to the specified URL for
the shared assets to be available for the destination document.

### Define runtime shared assets in a source document

To define sharing properties for an asset in a source document and make the
asset accessible for linking to destination documents, use the Symbol Properties
dialog box or the Linkage Properties dialog box.

1.  With the source document open, select Window \> Library:

2.  Do one of the following:
    - Select a movie clip, button, or graphic symbol in the Library panel, and
      select Properties from the Library Panel menu. Click Advanced.

    - Select a font symbol, sound, or bitmap, and select Linkage from the
      Library Panel menu.

3.  For Linkage, select Export For Runtime Sharing to make the asset available
    for linking to the destination document.

4.  Enter an identifier for the symbol. Do not include spaces. This is the name
    Flash Pro uses to identify the asset when linking to the destination
    document.

    > **Note:** Flash Pro also uses the linkage identifier to identify a movie
    > clip or button that is used as an object in ActionScript. See Working with
    > movie clips in
    > [Learning ActionScript 2.0 in Adobe Flash](https://web.archive.org/web/20120116125748/http://help.adobe.com/en_US/FlashPlatform/reference/actionscript/2/help.html?content=Part1_Learning_AS2_1.html)
    > or
    > [Working with movie clips](https://web.archive.org/web/20120115054337mp_/http://help.adobe.com/en_US/as3/dev/WS5b3ccc516d4fbf351e63e3d118a9b90204-7e1d.html)
    > in the ActionScript 3.0 Developer's Guide.

5.  Enter the URL where the SWF file containing the shared asset will be posted,
    and click OK.

    When you publish the SWF file, you must post the SWF file to the URL you
    specified so that the shared assets are available to destination documents.

### Link to runtime shared assets from a destination document

You can link to a shared asset by entering its URL or by dragging the asset into
the destination document.

#### Link a shared asset to a destination document by entering the identifier and URL

1.  In the destination document, select Window \> Library.
2.  Do one of the following:
    - Select a movie clip, button, graphic symbol, bitmap, or sound in the
      Library panel, and select Properties from the Library Panel menu. Click
      Advanced.

    - Select a font symbol, and select Linkage from the Library Panel menu.

3.  For Linkage, select Import For Runtime Sharing to link to the asset in the
    source document.
4.  Enter an identifier for the symbol, bitmap, or sound that is identical to
    the identifier used for the symbol in the source document. Do not include
    spaces.
5.  Enter the URL where the SWF source file containing the shared asset is
    posted, and click OK.

#### Link a shared asset to a destination document by dragging

1.  In the destination document, do one of the following:
    - Select File \> Open.

    - Select File \> Import \> Open External Library.

2.  Select the source document and click Open.
3.  Drag the shared asset from the source document Library panel into the
    Library panel or onto the Stage in the destination document.

#### Turn off sharing for a symbol in a destination document

1.  In the destination document, select the linked symbol in the Library panel
    and do one of the following:
    - If the asset is a movie clip, button, or graphic symbol, select Properties
      from the Library Panel menu.

    - If the asset is a font symbol, select Linkage from the Library Panel menu.

2.  Deselect Import For Runtime Sharing, and click OK.

## Sharing library assets at author-time

Sharing assets at author-time has these advantages:

- Allows you to avoid the need for redundant copies of assets used in more than
  one FLA file. For example, if you are developing a FLA for web browsers,
  another for iOS and another for Android, you can share assets among the 3
  files.

- When you edit a shared asset in one FLA file, the changes are reflected in
  other FLA files that use the asset when they are opened or brought into focus.

There are 2 ways of sharing library assets during authoring:

- Using symbols from external FLA files by linking to them from symbols in
  another FLA file.

- (CS5.5 only) Sharing symbols among FLA files that are part of the same Flash
  project in the Project panel. For information about using the Project panel,
  see
  [Working with Flash projects](../managing-documents/working-with-flash-projects.md).

Sharing by linking to symbols in separate FLA files works like this:

- For shared assets during authoring, update or replace any symbol in a FLA file
  you are authoring with any symbol in any other FLA file available on your
  local network.

- Update the symbol in the destination document as you author the document.

- The symbol in the destination document retains its original name and
  properties, but its contents are updated or replaced with those of the symbol
  you select.

Sharing symbols using the Project panel works like this (CS5.5 only):

- You create a project in the Project panel and create a FLA file in the
  project.

- In that FLA file, you specify which symbols you want to share with other files
  by checking the sharing checkbox for each item in the Library panel.

- Create a second FLA file in the project.

- Copy and paste layers, frames, or items on the Stage from the first FLA file
  to the second.

- Flash moves the shared library items in the pasted elements to a separate file
  called AuthortimeSharedAssets.FLA within the project folder.

The following assets types are sharable within a project: | Asset type |
Sharable on its own? | Sharable if inside a movie clip? | |
------------------------ | -------------------- |
-------------------------------- | | Movie clip symbol | Yes | Yes | | Graphic
symbol | Yes | Yes | | Button symbol | Yes | Yes | | Font symbol | No | Yes | |
FLV video | No | Yes | | Embeded video | No | Yes | | Sound (any format) | No |
Yes | | Bitmap (any format) | No | Yes | | Compiled clip (SWC) | No | Yes | |
Component (symbol-based) | Yes | Yes |

### Update or replace shared symbols

You can update or replace a movie clip, button, or graphic symbol in a document
with any other symbol in a FLA file accessible on your local network. The
original name and properties of the symbol in the destination document are
preserved, but the contents of the symbol are replaced with the contents of the
symbol you select. Any assets that the selected symbol uses are also copied into
the destination document.

1.  With the document open, select a movie clip, button, or graphic symbol in
    the Library panel and select Properties from the panel Options menu.
2.  If the Linkage and Source areas of the Symbol Properties dialog box are not
    showing, click Advanced.
3.  To select a new FLA file, click Browse.
4.  Navigate to a FLA file that contains the symbol to use to update or replace
    the selected symbol in the Library panel, and click Open.
5.  Navigate to a symbol, and click OK.
6.  Do one of the following:
    - CS5: In the Symbol Properties dialog box, under Source, select Always
      Update Before Publishing and click OK.

    - CS5.5: In the Symbol Properties dialog box, under Authortime Sharing,
      select Update Automatically and click OK

### Define assets for sharing in a project (CS5.5 only)

Sharing assets among FLA files in a project allows you to edit the asset in one
file and see the changes reflected in the other FLA files that use the asset.

1.  Create a Flash project. See
    [Create projects](../managing-documents/working-with-flash-projects.md#create-projects).

2.  In a FLA file in the project, for each library asset you want to share with
    other FLA files in the project, do one of the following:
    - Open the Library panel and select the Link checkbox next to the asset
      name.

    - With the asset selected in the Library panel, choose Properties from the
      panel Options menu and then click the Share with Project button.

3.  In the Timeline or on the Stage, copy layers, frames, or Stage items
    containing shared assets.

4.  In a separate FLA file in the same project, paste the layers, frames, or
    stage items into a separate FLA filer in the same project.

### Tutorials

- Tutorial:
  [Creating mobile projects with shared assets and the Project panel](https://web.archive.org/web/20120115054337mp_/http://www.adobe.com/devnet/flash/articles/shared-assets.html)
  (Yuki Shimizu, Adobe.com)
