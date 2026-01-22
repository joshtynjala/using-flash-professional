# Timelines and ActionScript

With ActionScript®, you can control the Timeline at runtime. Using ActionScript
allows you to create interaction and other capabilities in your FLA files that
is not possible with the Timeline alone.

## Absolute paths

An absolute path starts with the name of the level into which the document is
loaded and continues through the display list until it reaches the target
instance. You can also use the alias `_root` to refer to the topmost Timeline of
the current level. For example, an action in the movie clip `california` that
refers to the movie clip `oregon` could use the absolute path
`_root.westCoast.oregon`.

The first document to open in Flash Player is loaded at level 0. You must assign
each additional loaded document a level number. When you use an absolute
reference in ActionScript to reference a loaded document, use the form
`_level``X`, where `X` is the level number into which the document is loaded.
For example, the first document that opens in Flash Player is called `_level0`;
a document loaded into level 3 is called `_level3`.

To communicate between documents on different levels, you must use the level
name in the target path. The following example shows how the `portland` instance
would address the `atlanta` instance located in a movie clip called `georgia`
(`georgia` is at the same level as `oregon`):

    _level5.georgia.atlanta

You can use the `_root` alias to refer to the main Timeline of the current
level. For the main Timeline, the `_root` alias stands for `_level0` when
targeted by a movie clip also on `_level0`. For a document loaded into
`_level5`, `_root` is equal to `_level5` when targeted by a movie clip also on
level 5. For example, if the movie clips `southcarolina` and `florida` are both
loaded into the same level, an action called from the instance `southcarolina`
could use the following absolute path to target the instance `florida`:

    _root.eastCoast.florida

## Relative paths

A relative path depends on the relationship between the controlling Timeline and
the target Timeline. Relative paths can address targets only within their own
level of Flash Player. For example, you can't use a relative path in an action
on `_level0` that targets a Timeline on `_level5`.

In a relative path, use the keyword `this` to refer to the current Timeline in
the current level; use the `_parent` alias to indicate the parent Timeline of
the current Timeline. You can use the `_parent` alias repeatedly to go up one
level in the movie clip hierarchy within the same level of Flash Player. For
example, `_parent._parent` controls a movie clip up two levels in the hierarchy.
The topmost Timeline at any level in Flash Player is the only Timeline with a
`_parent` value that is undefined.

An action in the Timeline of the instance `charleston`, located one level below
`southcarolina`, could use the following target path to target the instance
`southcarolina`:

    _parent

To target the instance `eastCoast` (one level up) from an action in
`charleston`, you could use the following relative path:

    _parent._parent

To target the instance `atlanta` from an action in the Timeline of `charleston`,
you could use the following relative path:

    _parent._parent.georgia.atlanta

Relative paths are useful for reusing scripts. For example, you could attach the
following script to a movie clip that magnifies its parent by 150%:

    onClipEvent (load) {
        _parent._xscale = 150;
        _parent._yscale = 150;
    }

You can reuse this script by attaching it to any movie clip instance.

> **Note:** Flash Lite 1.0 and 1.1 support attaching scripts only to buttons.
> Attaching scripts to movie clips is not supported.

Whether you use an absolute or a relative path, you identify a variable in a
Timeline or a property of an object with a dot (`.`) followed by the name of the
variable or property. For example, the following statement sets the variable
`name` in the instance `form` to the value `"Gilbert"`:

    _root.form.name = "Gilbert";

## Using absolute and relative target paths

You can use ActionScript to send messages from one timeline to another. The
timeline that contains the action is called the _controlling timeline_, and the
timeline that receives the action is called the _target timeline_. For example,
there could be an action on the last frame of one timeline that tells another
timeline to play. To refer to a target timeline, you must use a target path,
which indicates the location of a movie clip in the display list.

The following example shows the hierarchy of a document named westCoast on level
0, which contains three movie clips: `california`, `oregon`, and `washington`.
Each of these movie clips in turn contains two movie clips.

    _level0
            westCoast
                    california
                            sanfrancisco
                            bakersfield
                    oregon
                            portland
                            ashland
                    washington
                            olympia
                            ellensburg

As on a web server, each timeline in Flash Pro can be addressed in two ways:
with an absolute path or with a relative path. The absolute path of an instance
is always a full path from a level name, regardless of which timeline calls the
action; for example, the absolute path to the instance `california` is
`_level0.westCoast.california`. A relative path is different when called from
different locations; for example, the relative path to `california` from
`sanfrancisco` is` _parent`, but from `portland`, it's
`_parent._parent.california`.

## Specify target paths

To control a movie clip, loaded SWF file, or button, you must specify a target
path. You can specify it manually, or by using the Insert Target Path dialog
box, or by creating an expression that evaluates to a target path. To specify a
target path for a movie clip or button, you must assign an instance name to the
movie clip or button. A loaded document doesn't require an instance name,
because you use its level number as an instance name (for example, `_level5`).

### Assign an instance name to a movie clip or button

1.  Select a movie clip or button on the Stage.
2.  Enter an instance name in the Property inspector.

### Specify a target path using the Insert Target Path dialog box

1.  Select the movie clip, frame, or button instance to which you want to assign
    the action.

    This becomes the controlling Timeline.

2.  In the Actions panel (Window \> Actions), go to the Actions toolbox on the
    left, and select an action or method that requires a target path.

3.  Click the parameter box or location in the script where you want to insert
    the target path.

4.  Click the Insert Target Path button ![](../img/targetPathbtn.png) above the
    Script pane.

5.  Select Absolute or Relative for the target path mode.

6.  Select a movie clip in the Insert Target Path display list, and click OK.

### Specify a target path manually

1.  Select the movie clip, frame, or button instance to which you want to assign
    the action.

    This becomes the controlling Timeline.

2.  In the Actions panel (Window \> Actions), go to the Actions toolbox on the
    left, and select an action or method that requires a target path.

3.  Click the parameter box or location in the script where you want to insert
    the target path.

4.  Enter an absolute or relative target path in the Actions panel.

### Use an expression as a target path

1.  Select the movie clip, frame, or button instance to which you want to assign
    the action.

    This becomes the controlling Timeline.

2.  In the Actions panel (Window \> Actions), go to the Actions toolbox on the
    left, and select an action or method that requires a target path.

3.  Do one of the following:
    - Enter an expression that evaluates to a target path in a parameter box.

    - Click to place the insertion point in the script. Then, in the Functions
      category of the Actions toolbox, double-click the `targetPath` function.
      The `targetPath` function converts a reference to a movie clip into a
      string.

    - Click to place the insertion point in the script. Then, in the Functions
      category of the Actions toolbox, select the `eval` function. The `eval`
      function converts a string to a movie clip reference that can be used to
      call methods such as `play`.

      The following script assigns the value 1 to the variable `i`. It then uses
      the `eval` function to create a reference to a movie clip instance and
      assigns it to the variable `x`. The variable `x` is now a reference to a
      movie clip instance and can call the MovieClip object methods.

          i = 1;
          x = eval("mc"+i);
          x.play();
          // this is equivalent to mc1.play();

      You can also use the `eval` function to call methods directly, as shown in
      the following example:

          eval("mc" + i).play();

More Help topics

[Structuring FLA files](../best-practices/structuring-fla-files.md)

[Organizing ActionScript in an application](../best-practices/organizing-actionscript-in-an-application.md)
