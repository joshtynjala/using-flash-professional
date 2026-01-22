# Animation frame rate and performance

When you add animation to an application, consider the frame rate that you set
your FLA file to. Frame rate can affect the performance of your SWF file and the
computer that plays it. Setting a frame rate too high can lead to processor
problems, especially when you use many assets or use ActionScript to create
animation.

However, you also need to consider the frame rate setting, because it affects
how smoothly your animation plays. For example, an animation set to 12 frames
per second (fps) in the Property inspector plays 12 frames each second. If the
document's frame rate is set to 24 fps, the animation appears to animate more
smoothly than if it ran at 12 fps. However, your animation at 24 fps also plays
faster than it does at 12 fps, so the total duration (in seconds) is shorter.
Therefore, to make a 5‑second animation using a higher frame rate, you must add
additional frames to fill those five seconds than at a lower frame rate (and
thus, raises the total file size of your animation). A 5‑second animation at 24
fps typically has a higher file size than a 5‑second animation at 12 fps.

> **Note:** When you use an onEnterFrame event handler to create scripted
> animations, the animation runs at the document's frame rate, similar to if you
> created a motion tween on a timeline. An alternative to the onEnterFrame event
> handler is setInterval (see ActionScript 2.0 Language Reference). Instead of
> depending on frame rate, you call functions at a specified interval. Like
> onEnterFrame, the more frequently you use setInterval to call a function, the
> more resource intensive the animation is on your processor.

Use the lowest possible frame rate that makes your animation appear to play
smoothly at runtime, which helps reduce the strain on the end-user's processor.
High frame rates (more than 30 to 40 fps) put a lot of stress on processors, and
do not change the appearance of the animation much or at all at runtime.

Select a frame rate for your animation as early as possible in the development
process. When you test the SWF file, check the duration, and the SWF file size,
of your animation. The frame rate greatly affects the speed of the animation.
