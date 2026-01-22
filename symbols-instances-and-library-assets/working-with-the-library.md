# Working with the library

## Work with libraries

The library in a Flash Pro document stores media assets that you create in the
Flash Pro authoring environment or import to use in the document. You can create
vector artwork or text directly in Flash Pro; import vector artwork, bitmaps,
video, and sound; and create symbols. A _symbol_ is a graphic, a button, a movie
clip, or text that you create once and can reuse multiple times. You can also
use ActionScript to add media content to a document dynamically.

The library also contains any components that you have added to your document.
Components appear in the library as compiled clips.

You can open the library of any Flash Pro document while you are working in
Flash Pro, to make the library items from that file available for the current
document.

You can create permanent libraries in your Flash Pro application that are
available whenever you start Flash Pro. Flash Pro also includes several sample
libraries containing buttons, graphics, movie clips, and sounds.

You can export library assets as a SWF file to a URL to create a runtime-shared
library. This lets you link to the library assets from Flash Pro documents that
import symbols using runtime sharing.

The Library panel (Window \> Library) displays a scroll list with the names of
all items in the library, which lets you view and organize these elements as you
work. An icon next to an item's name in the Library panel indicates the item's
file type.

### Open a library in another Flash file

1.  From the current document, select File \> Import \> Open External Library.

2.  Navigate to the Flash Pro file whose library you want to open and click
    Open.

    The selected file's library opens in the current document, with the filename
    at the top of the Library panel. To use items from the selected file's
    library in the current document, drag the items to the current document's
    Library

### Resize the Library panel

![](../img/dingbat.png) Do one of the following:

- Drag the lower-right corner of the panel.

- Click the Wide State button to enlarge the Library panel so it shows all the
  columns.

- Click the Narrow State button to reduce the width of the Library panel.

### Change the width of columns

![](../img/dingbat.png) Position the pointer between column headers and drag to
resize.

You cannot change the order of columns.

### Work with folders in the Library panel

You can organize items in the Library panel using folders. When you create a new
symbol, it is stored in the selected folder. If no folder is selected, the
symbol is stored at the root of the library.

#### Create a new folder

![](../img/dingbat.png) Click the New Folder button ![](../img/new_folder.png)
at the bottom of the Library panel.

#### Open or close a folder

![](../img/dingbat.png) Double-click the folder, or Select the folder and select
Expand Folder or Collapse Folder from the Panel menu for the Library panel.

#### Open or close all folders

![](../img/dingbat.png) Select Expand All Folders or Collapse All Folders from
the Panel menu for the Library panel.

#### Move an item between folders

![](../img/dingbat.png) Drag the item from one folder to another.

If an item with the same name exists in the new location, Flash Pro prompts you
to replace it with the item you are moving.

### Sort items in the Library panel

Columns in the Library panel list the name of an item, its type, the number of
times it's used in the file, its linkage status and identifier (if the item is
associated with a shared library or is exported for ActionScript), and the date
on which it was last modified.

You can sort items in the Library panel alphanumerically by any column. Items
are sorted within folders.

![](../img/dingbat.png) Click the column header to sort by that column. Click
the triangle button to the right of the column headers to reverse the sort
order.

### Work with common libraries

You can use the sample common libraries included with Flash Pro to add buttons
or sounds to your documents. You can also create custom common libraries, which
you can then use with any documents that you create.

#### Use an item from a common library in a document

1.  Select Window \> Common Libraries, and select a library from the submenu.

2.  Drag an item from the common library into the library for the current
    document.

#### Create a common library for your SWF application

1.  Create a Flash Pro file with a library containing the symbols that you want
    to include in the common library.

2.  Place the Flash Pro file in the user-level Libraries folder on your hard
    disk.
    - On Windows® XP, the path is
      `C:\Documents and Settings\<username>\Local Settings\Application Data\Adobe\Flash CS5\<language>\Configuration\Libraries\`

    - On Windows® Vista®, the path is
      `C:\Users\<username>\Local Settings\Application Data\Adobe\Flash CS5\<language>\Configuration\Libraries\`

    - On Mac OS, the path is
      `<HardDisk>/Users/<username>/Library/Application Support/Adobe/Flash CS5/<language>/Configuration/Libraries/`

### Conflicts between library assets

If you import or copy a library asset into a document that already contains a
different asset of the same name, choose whether to replace the existing item
with the new item. This option is available with all the methods for importing
or copying library assets.

The Resolve Library Items dialog box appears when you attempt to place items
that conflict with existing items in a document. A conflict exists when you copy
an item from a source document that already exists in the destination document
and the items have different modification dates. Avoid naming conflicts by
organizing your assets inside folders in your document's library. The dialog box
also appears when you paste a symbol or component into your document's Stage and
you already have a copy of the symbol or component that has a different
modification date from the one you're pasting.

If you choose not to replace the existing items, Flash Pro attempts to use the
existing item instead of the conflicting item that you are pasting. For example,
if you copy a symbol named Symbol 1 and paste the copy into the Stage of a
document that already contains a symbol named Symbol 1, Flash Pro creates an
instance of the existing Symbol 1.

If you choose to replace the existing items, Flash Pro replaces the existing
items (and all their instances) with the new items of the same name. If you
cancel the Import or Copy operation, the operation is canceled for all items
(not just those items that conflict in the destination document).

Only identical library item types may be replaced with each other. That is, you
cannot replace a sound named Test with a bitmap named Test. In such cases, the
new items are added to the library with the word Copy appended to the name.

> **Note:** Replacing library items using this method is not reversible. Save a
> backup of your FLA file before you perform complex paste operations that are
> resolved by replacing conflicting library items. If the Resolve Library
> Conflict dialog box appears when you are importing or copying library assets
> into a document, resolve the naming conflict.

#### Resolve naming conflicts between library assets

![](../img/dingbat.png) Do one of the following in the Resolve Library Conflict
dialog box:

- To preserve the existing assets in the destination document, click Don't
  Replace Existing Items.

- To replace the existing assets and their instances with the new items of the
  same name, click Replace Existing Items.

## Work with library items

When you select an item in the Library panel, a thumbnail preview of the item
appears at the top of the Library panel. If the selected item is animated or is
a sound file, you can use the Play button in the library preview window or the
Controller to preview the item.

### Use a library item in the current document

![](../img/dingbat.png) Drag the item from the Library panel onto the Stage.

The item is added to the current layer.

### Convert an object on the Stage to a symbol in the library

![](../img/dingbat.png) Drag the item from the Stage onto the current Library
panel.

### Use a library item from the current document in another document

![](../img/dingbat.png) Drag the item from the Library panel or Stage into the
Library panel or Stage of another document.

### Copy library items from a different document

1.  Select the document that contains the library items.
2.  Select the library items in the Library panel.
3.  Select Edit \> Copy.
4.  Select the document that you want to copy the library items to.
5.  Select that document's Library panel.
6.  Select Edit \> Paste.

### Edit a library item

1.  Select the item in the Library panel.
2.  Select one of the following from the Panel menu for the Library panel:
    - To edit an item in Flash Pro, select Edit.

    - To edit an item in another application, select Edit With and then select
      an external application.

> **Note:** When starting a supported external editor, Flash Pro opens the
> original imported document.

### Rename a library item

Changing the library item name of an imported file does not change the filename.

1.  Do one of the following:
    - Double-click the item's name.

    - Select the item and select Rename from the Panel menu for the Library
      panel.

    - Right-click (Windows) or Control‑click (Macintosh) the item and select
      Rename from the context menu.

2.  Enter the new name in the box.

### Delete a library item

When you delete an item from the library, all instances or occurrences of that
item in the document are also deleted.

![](../img/dingbat.png) Select the item and click the Trash Can icon at the
bottom of the Library panel.

### Find unused library items

To organize your document, you can find unused library items and delete them.

> **Note:** It is not necessary to delete unused library items to reduce a Flash
> Pro document's file size, because unused library items are not included in the
> SWF file. However, items linked for export are included in the SWF file.

![](../img/dingbat.png) Do one of the following:

- Select Unused Items from the Panel menu for the Library panel.

- Sort library items by the Use Count column, which indicates whether an item is
  in use.

### Update imported files in the library

If you use an external editor to modify files that you have imported into Flash
Pro, such as bitmaps or sound files, you can update the files in Flash Pro
without reimporting them. You can also update symbols that you have imported
from external Flash Pro documents. Updating an imported file replaces its
contents with the contents of the external file.

1.  Select the imported file in the Library panel.
2.  Select Update from the Panel menu for the Library panel.

### Copy library assets between documents

You can copy library assets from a source document into a destination document
in a variety of ways. You can also share symbols between documents as shared
library assets during authoring or at runtime.

If you attempt to copy assets that have the same name as existing assets in the
destination document, the Resolve Library Conflicts dialog box lets you choose
whether to overwrite the existing assets or to preserve the existing assets and
add the new assets with modified names. Organize library assets in folders to
minimize name conflicts when copying assets between documents.

#### Copy a library asset by copying and pasting

1.  Select the asset on the Stage in the source document.

2.  Select Edit \> Copy.

3.  Make the destination document the active document.

4.  To paste the asset in the center of the visible pasteboard, place the
    pointer on the Stage and select Edit \> Paste In Center. To place the asset
    in the same location as in the source document, select Edit \> Paste In
    Place.

#### Copy a library asset by dragging

![](../img/dingbat.png) With the destination document open, select the asset in
the Library panel in the source document and drag the asset into the Library
panel in the destination document.

#### Copy a library asset by opening the source document library in the destination document

1.  With the destination document active, select File \> Import \> Open External
    Library.

2.  Select the source document, and click Open.

3.  Drag an asset from the source document library onto the Stage or into the
    library of the destination document.

More Help topics

[Working with Text Layout Framework (TLF) text](../text/working-with-text-layout-framework-tlf-text.md)

[Using imported artwork](../using-imported-artwork/index.md)

[Sound](../sound/index.md)

[Video](../video/index.md)

[Symbols, instances, and library assets](../symbols-instances-and-library-assets/index.md)

[Configuration folders installed with Flash (CS5)](../actionscript/actionscript-publish-settings-cs5.md#configuration-folders-installed-with-flash-cs5)

[Sharing library assets at runtime](./sharing-library-assets-across-files.md#sharing-library-assets-at-runtime)

[Creating buttons](./creating-buttons.md)
