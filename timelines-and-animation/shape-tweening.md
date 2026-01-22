# Shape tweening

## About shape tweens

In shape tweening, you draw a vector shape at one specific frame in the
Timeline, and change that shape or draw another shape at another specific frame.
Flash Pro then interpolates the intermediate shapes for the frames in between,
creating the animation of one shape morphing into another.

Shape tweens work best with simple shapes. Avoid shapes with cutouts or negative
spaces in them. Experiment with the shapes you want to use to determine the
results. You can use shape hints to tell Flash Pro which points on the beginning
shape should correspond to specific points on the end shape.

You can also tween the position and color of shapes within a shape tween.

To apply shape tweening to groups, instances, or bitmap images, break these
elements apart. See
[Break apart a symbol instance](../symbols-instances-and-library-assets/working-with-symbol-instances.md#break-apart-a-symbol-instance).

To apply shape tweening to text, break the text apart twice to convert the text
to objects. See
[Break apart a symbol instance](../symbols-instances-and-library-assets/working-with-symbol-instances.md#break-apart-a-symbol-instance).

## Create a shape tween

The following steps show how to create a shape tween from frame 1 to frame 30 of
the Timeline. However, you can create tweens in any part of the Timeline that
you choose.

1.  In frame 1, draw a square with the Rectangle tool.

2.  Select frame 30 of the same layer and add a blank keyframe by choosing
    Insert \> Timeline \> Blank Keyframe or pressing F7.

3.  On the Stage, draw a circle with the Oval tool in frame 30.

    You should now have a keyframe in frame 1 with a square and a keyframe in
    frame 30 with a circle.

4.  In the Timeline, select one of the frames in between the two keyframes in
    the layer containing the two shapes.

5.  Choose Insert \> Shape Tween.

    Flash interpolates the shapes in all the frames between the two keyframes.

6.  To preview the tween, scrub the playhead across the frames in the Timeline,
    or press the Enter key.

7.  To tween motion in addition to shape, move the shape in frame 30 to a
    location on the Stage that is different from the location of the shape in
    frame 1.

    Preview the animation by pressing the Enter key.

8.  To tween the color of the shape, make the shape in frame 1 a different color
    from the shape in frame 30.

9.  To add easing to the tween, select one of the frames between the two
    keyframes and enter a value in the Ease field in the Property inspector.

    Enter a negative value to ease the beginning of the tween. Enter a positive
    value to ease the end of the tween.

## Control shape changes with shape hints

To control more complex or improbable shape changes, you can use shape hints.
Shape hints identify points that should correspond in starting and ending
shapes. For example, if you are tweening a drawing of a face as it changes
expression, you can use a shape hint to mark each eye. Then, instead of the face
becoming an amorphous tangle while the shape change takes place, each eye
remains recognizable and changes separately during the shift. Shape hints
contain letters (a through z) for identifying which points correspond in the
starting and ending shapes. You can use up to 26 shape hints.

Shape hints are yellow in a starting keyframe, green in an ending keyframe, and
red when not on a curve.

For best results when tweening shapes, follow these guidelines:

- In complex shape tweening, create intermediate shapes and tween them instead
  of just defining a starting and ending shape.

- Make sure that shape hints are logical. For example, if you're using three
  shape hints for a triangle, they must be in the same order on the original
  triangle and on the triangle to be tweened. The order cannot be _abc_ in the
  first keyframe and _acb_ in the second.

- Shape hints work best if you place them in counterclockwise order beginning at
  the top-left corner of the shape.

### Use shape hints

1.  Select the first keyframe in a shape-tweened sequence.
2.  Select Modify \> Shape \> Add Shape Hint. The beginning shape hint appears
    as a red circle with the letter _a_ somewhere on the shape.
3.  Move the shape hint to a point to mark.
4.  Select the last keyframe in the tweening sequence. The ending shape hint
    appears somewhere on the shape as a green circle with the letter _a_.
5.  Move the shape hint to the point in the ending shape that should correspond
    to the first point you marked.
6.  To view how the shape hints change the shape tweening, play the animation
    again. To fine-tune the tweening, move the shape hints.
7.  Repeat this process to add additional shape hints. New hints appear with the
    letters that follow (_b_, _c_, and so on).

### View all shape hints

![](../img/dingbat.png) Select View \> Show Shape Hints. The layer and keyframe
that contain shape hints must be active for Show Shape Hints to be available.

### Remove a shape hint

![](../img/dingbat.png) Drag it off the Stage.

### Remove all shape hints

![](../img/dingbat.png) Select Modify \> Shape \> Remove All Hints.
