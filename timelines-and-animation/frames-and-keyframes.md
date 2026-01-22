# Frames and keyframes

Like films, Adobe® Flash® Professional CS5 documents divide lengths of time into
frames. In the Timeline, you work with these frames to organize and control the
content of your document. You place frames in the Timeline in the order you want
the objects in the frames to appear in your finished content.

A _keyframe_ is a frame where a new symbol instance appears in the Timeline. A
keyframe can also be a frame that includes ActionScript® code to control some
aspect of your document. You can also add a _blank keyframe_ to the Timeline as
a placeholder for symbols you plan to add later or to explicitly leave the frame
blank.

A _property keyframe_ is a frame in which you define a change to an object's
properties for an animation. Flash Pro can _tween_, or automatically fill in,
the property values between the property keyframes in order to produce fluid
animations. Because property keyframes let you produce animation without drawing
each individual frame, they make creating animation easier. A series of frames
containing tweened animation is called a _motion tween_.

A _tweened frame_ is any frame that is part of a motion tween.

A _static frame_ is any frame that is not part of a motion tween.

You arrange keyframes and property keyframes in the Timeline to control the
sequence of events in your document and its animation.

## Insert frames in the Timeline

- To insert a new frame, select Insert \> Timeline \> Frame (F5).

- To create a new keyframe, select Insert \> Timeline \> Keyframe (F6), or
  right-click (Windows) or Control‑click (Macintosh) the frame where you want to
  place a keyframe, and select Insert Keyframe from the context menu.

- To create a new blank keyframe, select Insert \> Timeline \> Blank Keyframe,
  or right-click (Windows) or Control‑click (Macintosh) the frame where you want
  to place the keyframe, and select Insert Blank Keyframe from the context menu.

## Select frames in the Timeline

Flash Pro offers two different methods for selecting frames in the Timeline. In
frame-based selection (the default), you select individual frames in the
Timeline. In span-based selection, the entire frame sequence, from one keyframe
to the next, is selected when you click any frame in the sequence. You can
specify span-based selection in Flash Pro Preferences.

- To select one frame, click the frame. If you have Span Based Selection
  enabled, Control-click (Windows) or Command-click (Macintosh) the frame.

- To select multiple contiguous frames, drag the cursor over the frames, or
  Shift-click additional frames.

- To select multiple non-contiguous frames, Control‑click (Windows) or
  Command-click (Macintosh) additional frames.

- To select all frames in the Timeline, select Edit \> Timeline \> Select All
  Frames.

- To select an entire span of static frames, double-click a frame between two
  keyframes. If you have Span Based Selection enabled, click any frame in the
  sequence.

- To select a whole span of frames (motion tween or inverse kinematics) click on
  it once if you have Span-based Selection enabled in the Preferences. If
  Span-based Selection is disabled, double-click on the span. To select multiple
  spans, click on each of them while holding the Shift key.

## Label frames in the Timeline

You can label frames in the Timeline as a way of helping organize its contents.
You can also label a frame in order to be able to refer to that frame in
ActionScript by it's label. That way, if you rearrange the Timeline and move the
label to a different frame number, the ActionScript will still refer to the
frame label and will not have to be updated.

Frame labels can only be applied to keyframes. A best practice is to create a
separate layer in the Timeline to contain your frame labels.

To add a frame label:

1.  Select the frame you wish to label in the Timeline.
2.  With the frame selected, enter the label name in the Label section of the
    Property inspector. Press Enter or Return.

## Enable span-based frame selection

Span-based frame selection allows you to select a range of frames between 2
keyframes with a single click.

1.  Select Edit \> Preferences.
2.  Select the General category.
3.  In the Timeline section, select Span Based Selection.
4.  Click OK.

## Copy or paste a frame or frame sequence

![](../img/dingbat.png) Do one of the following:

- Select the frame or sequence and select Edit \> Timeline \> Copy Frames.
  Select the frame or sequence that you want to replace, and select Edit \>
  Timeline \> Paste Frames.

- Alt‑drag (Windows) or Option-drag (Macintosh) a keyframe to the location where
  you want to copy it.

## Delete a frame or frame sequence

![](../img/dingbat.png) Select the frame or sequence and select Edit \>
Timeline \> Remove Frame, or right-click (Windows) or Control‑click (Macintosh)
the frame or sequence and select Remove Frame from the context menu.

Surrounding frames remain unchanged.

## Move a keyframe or frame sequence

![](../img/dingbat.png) Select a keyframe or frame sequence and then drag the
keyframe or sequence to the desired location.

## Change the length of a static frame sequence

![](../img/dingbat.png) Control-drag (Windows) or Command-drag (Macintosh) the
beginning or ending frame of the span to the left or right.

To change the length of a frame-by-frame animation sequence, see
[Create frame-by-frame animations](./frame-by-frame-animation.md#create-frame-by-frame-animations).

## Convert a keyframe to a frame

![](../img/dingbat.png) Select the keyframe and select Edit \> Timeline \> Clear
Keyframe, or right-click (Windows) or Control‑click (Macintosh) the keyframe and
select Clear Keyframe from the context menu.

The Stage contents of the cleared keyframe and all frames up to the subsequent
keyframe are replaced with the Stage contents of the frame preceding the cleared
keyframe.

## View a preview of frame content in the Timeline

In each keyframe of the Timeline, you can view a thumbnail preview of the items
in the keyframe.

![](../img/dingbat.png) Choose Preview from the Timeline panel Options menu at
the upper-right corner of the Timeline panel.

More Help topics

[The Timeline](../workspace/the-timeline.md)

[Animation basics](./animation-basics.md)

[Motion tween animation](./motion-tween-animation.md)
