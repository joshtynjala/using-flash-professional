# Timeline layers

## Create and organize layers

Layers help you organize the artwork in your document. You can draw and edit
objects on one layer without affecting objects on another layer. In areas of the
Stage with nothing on a layer, you can see through it to the layers below.

To draw, paint, or otherwise modify a layer or folder, select the layer in the
Timeline to make it active. A pencil icon next to a layer or folder name in the
Timeline indicates that the layer or folder is active. Only one layer can be
active at a time (although more than one layer can be selected at a time).

When you create a Flash Pro document, it contains only one layer. To organize
the artwork, animation, and other elements in your document, add more layers.
You can also hide, lock, or rearrange layers. The number of layers you can
create is limited only by your computer's memory, and layers do not increase the
file size of your published SWF file. Only the objects you place into layers add
to the file size.

To organize and manage layers, create layer folders and place layers in them.
You can expand or collapse layer folders in the Timeline without affecting what
you see on the Stage. Use separate layers or folders for sound files,
ActionScript, frame labels, and frame comments. This helps you find these items
quickly to edit them.

To help create sophisticated effects, use special guide layers to make drawing
and editing easier, and to make mask layers.

There are five types of layers you can use in Flash:

- Normal layers contain most of the artwork in a FLA file.

- Mask layers contain objects used as masks to hide selected portions of layers
  below them. For more information, see
  [Using mask layers](./using-mask-layers.md).

- Masked layers are layers beneath a mask layer that you associate with the mask
  layer. Only the portion of the masked layer revealed by the mask is visible.
  For more information, see [Using mask layers](./using-mask-layers.md).

- Guide layers contain strokes that can be used to guide the arrangement of
  objects on other layers or the motion of classic tween animations on other
  layers. For more information, see Guide layers and
  [Create classic tween animation along a path](./working-with-classic-tween-animation.md#create-classic-tween-animation-along-a-path).

- Guided layers are layers associated with a guide layer. The objects on the
  guided layer can be arranged or animated along the strokes on the guide layer.
  Guided layers can contain static artwork and classic tweens, but not motion
  tweens.

- Motion Tween layers contain objects animated with motion tweens. For more
  information, see
  [About tween animation](./motion-tween-animation.md#about-tween-animation).

- Armature layers contain objects with inverse kinematics bones attached. For
  more information, see
  [About inverse kinematics](./inverse-kinematics.md#about-inverse-kinematics).

Normal, Mask, Masked, and Guide layers can contain motion tweens or inverse
kinematic bones. When these items are present in one of these layers, there are
limitations to the types of content that can be added to the layer. For more
information, see [Motion tween animation](./motion-tween-animation.md) and
[Inverse kinematics](./inverse-kinematics.md).

### Create a layer

When you create a layer, it appears above the selected layer. The newly added
layer becomes the active layer.

![](../img/dingbat.png) Do one of the following:

- Click the New Layer button ![](../img/new_layer.png) at the bottom of the
  Timeline.

- Select Insert \> Timeline \> Layer.

- Right-click (Windows) or Control-click (Macintosh) a layer name in the
  Timeline and select Insert Layer from the context menu.

### Create a layer folder

![](../img/dingbat.png) Do one of the following:

- Select a layer or folder in the Timeline and select Insert \> Timeline \>
  Layer Folder.

- Right-click (Windows) or Control-click (Macintosh) a layer name in the
  Timeline and select Insert Folder from the context menu. The new folder
  appears above the layer or folder you selected.

- Click the New Folder icon ![](../img/new_folder.png) at the bottom of the
  Timeline. The new folder appears above the layer or folder you selected.

### Organize layers and layer folders

To organize your document, rearrange layers and folders in the Timeline.

Layer folders help organize your workflow by letting you place layers in a tree
structure. To see the layers a folder contains without affecting which layers
are visible on the Stage, expand or collapse the folder. Folders can contain
both layers and other folders, allowing you to organize layers in much the same
way you organize files on your computer.

The layer controls in the Timeline affect all layers within a folder. For
example, locking a layer folder locks all layers within that folder.

- To move a layer or layer folder into a layer folder, drag the layer or layer
  folder name to the destination layer folder name.
- To change the order of layers or folders, drag one or more layers or folders
  in the Timeline to the desired position.
- To expand or collapse a folder, click the triangle to the left of the folder
  name.
- To expand or collapse all folders, Right-click (Windows) or Control-click
  (Macintosh) and select Expand All Folders or Collapse All Folders.

### Rename a layer or folder

By default, new layers are named by the order in which they are created: Layer
1, Layer 2, and so on. To better reflect their contents, rename layers.

![](../img/dingbat.png) Do one of the following:

- Double-click the name of the layer or folder in the Timeline and enter a new
  name.

- Right-click (Windows) or Control-click (Macintosh) the name of the layer or
  folder and select Properties from the context menu. Enter the new name in the
  Name box and click OK.

- Select the layer or folder in the Timeline and select Modify \> Timeline \>
  Layer Properties. Enter the new name in the Name box and click OK.

### Select a layer or folder

![](../img/dingbat.png) Do one of the following:

- Click the name of a layer or folder in the Timeline.

- Click any frame in the Timeline of the layer to select.

- Select an object on the Stage that is located in the layer to select.

- To select contiguous layers or folders, Shift-click their names in the
  Timeline.

- To select non-contiguous layers or folders, Control-click (Windows) or
  Command-click (Macintosh) their names in the Timeline.

### Copy frames from a single layer

1.  Select a range of frames in a layer. To select the entire layer, click the
    layer name in the Timeline.
2.  Select Edit \> Timeline \> Copy Frames.
3.  Click the frame where you want to begin pasting and select Edit \>
    Timeline \> Paste Frames.

### Copy frames from a layer folder

1.  Collapse the folder (click the triangle to the left of the folder name in
    the Timeline) and click the folder name to select the entire folder.
2.  Select Edit \> Timeline \> Copy Frames.
3.  To create a folder, select Insert \> Timeline \> Layer Folder.
4.  Click the new folder and select Edit \> Timeline \> Paste Frames.

### Delete a layer or folder

1.  To select the layer or folder, click its name in the Timeline or any frame
    in the layer.
2.  Do one of the following:
    - Click the Delete Layer button in the Timeline.

    - Drag the layer or folder to the Delete Layer button.

    - Right-click (Windows) or Control-click (Macintosh) the layer or folder
      name and select Delete Layer from the context menu.

      > **Note:** When you delete a layer folder, all the enclosed layers and
      > all their contents are also deleted.

### Lock or unlock one or more layers or folders

- To lock a layer or folder, click in the Lock column to the right of the name.
  To unlock the layer or folder, click in the Lock column again.

- To lock all layers and folders, click the padlock icon. To unlock all layers
  and folders, click it again.

- To lock or unlock multiple layers or folders, drag through the Lock column.

- To lock all _other_ layers or folders, Alt‑click (Windows) or Option-click
  (Macintosh) in the Lock column to the right of a layer or folder name. To
  unlock all layers or folders, Alt‑click or Option-click in the Lock column
  again.

### Copy and paste layers (CS5.5 only)

You can copy entire layers and layer folders in the timeline and paste them into
the same timeline or separate timelines. Any type of layer can be copied.

When you copy and paste layers, the layer folder structure of copied layers is
preserved.

1.  Select one or more layers in the Timeline by clicking the layer name.
    Shift-click to select contiguous layers. Control-click (Windows) or
    Command-click (Macintosh) to select non-contiguous layers.

2.  Choose Edit \> Timeline \>Copy Layers or Cut Layers. You can also
    right-click the layers and choose Copy Layers or Cut Layers from the context
    menu.

3.  In the timeline you want to paste into, select the layer immediately below
    where you want the pasted layers to be inserted.

4.  Choose Edit \> Timeline \> Paste Layers.

The layers appear in the Timeline above the layer you selected. If you have a
layer folder selected, the pasted layers appear inside the folder.

To paste a layer into a mask or guide layer you must first select a layer under
that mask or guide and then paste. You cannot paste either a mask, guide, or
folder layer underneath a mask or guide layer.

You can also duplicate layers by selecting layers and choosing Edit \>
Timeline \>Duplicate Layers. The new layers will have the word "copy" appended
to the layer name.

## View layers and layer folders

### Show or hide a layer or folder

A red X next to the name of a layer or folder in the Timeline indicates that a
layer or folder is hidden. In the publish settings, you can choose whether
hidden layers are included when you publish a SWF file.

- To hide a layer or folder, click in the Eye column to the right of the layer
  or folder name in the Timeline. To show the layer or folder, click in it
  again.

- To hide all the layers and folders in the Timeline, click the Eye icon. To
  show all layers and folders, click it again.

- To show or hide multiple layers or folders, drag through the Eye column.

- To hide all layers and folders other than the current layer or folder,
  Alt‑click (Windows) or Option-click (Macintosh) in the Eye column to the right
  of a layer or folder name. To show all layers and folders, Alt‑click or
  Option-click it again.

### View the contents of a layer as outlines

To distinguish which layer an object belongs to, display all objects on a layer
as colored outlines.

- To display all objects on that layer as outlines, click in the Outline column
  to the right of the layer's name. To turn off outline display, click in it
  again.

- To display objects on all layers as outlines, click the outline icon. To turn
  off outline display on all layers, click it again.

- To display objects on all layers _other_ than the current layer as outlines,
  Alt‑click (Windows) or Option-click (Macintosh) in the Outline column to the
  right of a layer's name. To turn off the outline display for all layers,
  Alt‑click or Option-click in it again.

### Change a layer's outline color

1.  Do one of the following:
    - Double-click the layer's icon (the icon to the left of the layer name) in
      the Timeline.

    - Right-click (Windows) or Control-click (Macintosh) the layer name and
      select Properties from the context menu.

    - Select the layer in the Timeline and select Modify \> Timeline \> Layer
      Properties.

2.  In the Layer Properties dialog box, click the Outline Color box, select a
    new color, and click OK.

> **Note:** Motion paths on the layer also use the layer outline color.

More Help topics

[Change the appearance of the Timeline](../workspace/the-timeline.md#change-the-appearance-of-the-timeline)
