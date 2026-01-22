# Using mask layers

## About mask layers

For spotlight effects and transitions, use a mask layer to create a hole through
which underlying layers are visible. A mask item can be a filled shape, a type
object, an instance of a graphic symbol, or a movie clip. Group multiple layers
under a single mask layer to create sophisticated effects.

To create dynamic effects, animate a mask layer. For a filled shape used as a
mask, use shape tweening; for a type object, graphic instance, or movie clip,
use motion tweening. When using a movie clip instance as a mask, animate the
mask along a motion path.

To create a mask layer, place a mask item on the layer to use as a mask. Instead
of having a fill or stroke, the mask item acts as a window that reveals the area
of linked layers beneath it. The rest of the mask layer conceals everything
except what shows through the mask item. A mask layer can contain only one mask
item. A mask layer cannot be inside a button, and you cannot apply a mask to
another mask.

To create a mask layer from a movie clip, use ActionScript. A mask layer created
with ActionScript can be applied only to another movie clip. See Using Movie
Clips as Masks in
[_Learning ActionScript 2.0 in Adobe Flash_](https://web.archive.org/web/20111117080717mp_/http://www.adobe.com/go/learn_cs5_learningas2_en).

> **Note:** The 3D tools cannot be used on objects on mask layers and layers
> containing 3D objects cannot be used as mask layers. For more information
> about the 3D tools, see
> [3D graphics](../creating-and-editing-artwork/3d-graphics.md).

## Work with mask layers

You can use mask layers to reveal portions of a picture or graphic in the layer
below. To create a mask, you specify that a layer is a mask layer, and either
draw or place a filled shape on that layer. You can use any filled shape,
including groups, text, and symbols, as a mask. The mask layer reveals the area
of linked layers beneath the filled shape.

### Create a mask layer

1.  Select or create a layer containing the objects to appear inside the mask.
2.  Select Insert \> Timeline \> Layer to create a new layer above it. A mask
    layer always masks the layer immediately below it; create the mask layer in
    the proper place.
3.  Place a filled shape, text, or an instance of a symbol on the mask layer.
    Flash Pro ignores bitmaps, gradients, transparency, colors, and line styles
    in a mask layer. Any filled area is completely transparent in the mask; any
    non-filled area is opaque.
4.  Right-click (Windows) or Control‑click (Macintosh) the mask layer's name in
    the Timeline, and select Mask. A mask layer icon indicates the mask layer.
    The layer immediately below it is linked to the mask layer, and its contents
    show through the filled area on the mask. The masked layer name is indented,
    and its icon changes to a masked layer icon.
5.  To display the mask effect in Flash Pro, lock the mask layer and the masked
    layer.

### Mask additional layers after creating a mask layer

![](../img/dingbat.png) Do one of the following:

- Drag an existing layer directly below the mask layer.

- Create a new layer anywhere below the mask layer.

- Select Modify \> Timeline \> Layer Properties, and select Masked.

### Unlink layers from a mask layer

![](../img/dingbat.png) Select the layer to unlink and do one of the following:

- Drag the layer above the mask layer.

- Select Modify \> Timeline \> Layer Properties, and select Normal.

### Animate a filled shape, type object, or graphic symbol instance on a mask layer

1.  Select the mask layer in the Timeline.
2.  To unlock the mask layer, click in the Lock column.
3.  Do one of the following:
    - If the mask object is a filled shape, apply shape tweening to the object.

    - If the mask object is a type object or graphic symbol instance, apply
      motion tweening to the object.

4.  When the animation operation is complete, click in the Lock column for the
    mask layer to re-lock the layer.

### Animate a movie clip on a mask layer

1.  Select the mask layer in the Timeline.
2.  To edit the movie clip in place and to display the movie clip's Timeline,
    double-click the movie clip on the Stage.
3.  Apply motion tweening to the movie clip.
4.  When the animation procedure is complete, click the Back button to return to
    document-editing mode.
5.  To lock the layer again, click in the Lock column for the mask layer.

More Help topics

[Motion tween animation](./motion-tween-animation.md)
