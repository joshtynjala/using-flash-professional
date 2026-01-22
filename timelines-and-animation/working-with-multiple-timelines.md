# Working with multiple timelines

## About multiple timelines and levels

Flash® Player has a stacking order of levels. Every Flash Pro document has a
main Timeline located at level 0 in Flash Player. You can use the `loadMovie`
command to load other Flash Pro documents (SWF files) into Flash Player at
different levels.

If you load documents into levels above level 0, the documents stack on top of
one another like drawings on transparent paper; when there is no content on the
Stage, you can see through to the content on lower levels. If you load a
document into level 0, it replaces the main timeline. Each document loaded into
a level of Flash Player has its own timeline.

Timelines can send messages to each other with ActionScript. For example, an
action on the last frame of one movie clip can tell another movie clip to play.
To use ActionScript to control a timeline, you must use a target path to specify
the location of the timeline.

For more information, see the `MovieClip.loadMovie` method in the
[_ActionScript 2.0 Language Reference_](https://open-flash.github.io/mirrors/as2-language-reference/index.html).

## About nested movie clips and parent-child hierarchy

When you create a movie clip instance in a Flash Pro document, the movie clip
has its own timeline. Every movie clip symbol has its own timeline. The movie
clip's timeline is nested inside the main timeline of the document. You can also
nest a movie clip instance inside another movie clip symbol.

When a movie clip is created inside a Flash Pro document, or nested inside
another movie clip, it becomes a child of that document or movie clip, which
becomes the parent. Relationships between nested movie clips are hierarchical:
modifications made to the parent affect the child. The root Timeline for each
level is the parent of all the movie clips on its level, and because it is the
top-most Timeline, it has no parent. In the Movie Explorer panel, you can view
the hierarchy of nested movie clips in a document by choosing Show Symbol
Definitions from the panel menu.

To understand movie clip hierarchy, consider the hierarchy on a computer: the
hard disk has a root directory (or folder) and subdirectories. The root
directory is analogous to the main (or root) Timeline of a Flash Pro document:
it is the parent of everything else. The subdirectories are analogous to movie
clips.

You can use the movie clip hierarchy in Flash Pro to organize related objects.
For example, you could create a Flash Pro document containing a car that moves
across the Stage. You can use a movie clip symbol to represent the car and set
up a motion tween to move it across the Stage.

To add wheels that rotate, you can create a movie clip for a car wheel, and
create two instances of this movie clip, named `frontWheel` and `backWheel`.
Then you can place the wheels on the car movie clip's Timeline—not on the main
Timeline. As children of `car`, `frontWheel` and `backWheel` are affected by any
changes made to `car`; they move with the car as it tweens across the Stage.

To make both wheel instances spin, you can set up a motion tween that rotates
the wheel symbol. Even after you change `frontWheel` and `backWheel`, they
continue to be affected by the tween on their parent movie clip, `car`; the
wheels spin, but they also move with the parent movie clip `car` across the
Stage.

More Help topics

[Symbols, instances, and library assets](../symbols-instances-and-library-assets/index.md)
