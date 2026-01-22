# Frame-by-frame animation

## Create frame-by-frame animations

Frame-by-frame animation changes the contents of the Stage in every frame and is
best suited to complex animation in which an image changes in every frame
instead of simply moving across the Stage. Frame-by-frame animation increases
file size more rapidly than tweened animation. In frame-by-frame animation,
Flash Pro stores the values for each complete frame.

To create a frame-by-frame animation, define each frame as a keyframe and create
a different image for each frame. Each new keyframe initially contains the same
contents as the keyframe preceding it, so you can modify the frames in the
animation incrementally.

1.  Click a layer name to make it the active layer, and select a frame in the
    layer where the animation is to start.
2.  If the frame isn't already a keyframe, select Insert \> Timeline \>
    Keyframe.
3.  Create the artwork for the first frame of the sequence. Use the drawing
    tools, paste graphics from the Clipboard, or import a file.
4.  To add a new keyframe whose contents are the same as those of the first
    keyframe, click the next frame to the right in the same row and select
    Insert \> Timeline \> Keyframe, or right-click (Windows) or Control‑click
    (Macintosh) and select Insert Keyframe.
5.  To develop the next increment of the animation, alter the contents of this
    frame on the Stage.
6.  To complete your frame-by-frame animation sequence, repeat steps 4 and 5
    until you've built the desired motion.
7.  To test the animation sequence, select Control \> Play or click the Play
    button on the Controller (Window \> Toolbars \> Controller).

## Use onion skinning

Usually, one frame of the animation sequence at a time appears on the Stage. To
help position and edit a frame-by-frame animation, view two or more frames on
the Stage at once. The frame under the playhead appears in full color, while
surrounding frames are dimmed, making it appear as if each frame were drawn on a
sheet of translucent onion-skin paper and the sheets were stacked on top of each
other. Dimmed frames cannot be edited.

### Simultaneously view several frames of an animation on the Stage

![](../img/dingbat.png) Click the Onion Skin button ![](../img/onion_skin.png).
All frames between the Start Onion Skin and End Onion Skin markers (in the
Timeline header) are superimposed as one frame in the Document window.

### Control onion skinning display

- To display onion skinned frames as outlines, click the Onion Skin Outlines
  button ![](../img/onion_skin_outlines.png).

- To change the position of either onion skin marker, drag its pointer to a new
  location. (Normally, the onion skin markers move in conjunction with the
  current frame pointer.)

- To enable editing of all frames between onion skin markers, click the Edit
  Multiple Frames button ![](../img/edit_multiple_frames.png). Usually, onion
  skinning lets you edit only the current frame. However, you can display the
  contents of each frame between the onion skin markers, and make each available
  for editing, regardless of which is the current frame.

> **Note:** Locked layers (those with a padlock icon) aren't displayed when
> onion skinning is turned on. To avoid a multitude of confusing images, lock or
> hide the layers you don't want to be onion skinned.

### Change the display of onion skin markers

![](../img/dingbat.png) Click the Modify Onion
Markers ![](../img/modify_onion_markers.png) button and select an item:

Always Show Markers  
Displays the onion skin markers in the Timeline header whether or not onion
skinning is on.

Anchor Onion  
Locks the onion skin markers to their current position in the Timeline header.
Usually, the onion skin range is relative to the current frame pointer and the
onion skin markers. Anchoring the onion skin markers prevents them from moving
with the current frame pointer.

Onion 2  
Displays two frames on either side of the current frame.

Onion 5  
Displays five frames on either side of the current frame.

Onion All  
Displays all frames on either side of the current frame.
