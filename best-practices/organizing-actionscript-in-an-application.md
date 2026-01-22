# Best practices - Organizing ActionScript in an application

## Keeping actions together

Whenever possible, put your ActionScript® in a single location. Organizing your
code in one place helps you edit projects more efficiently, because you can
avoid searching in different places when you debug or modify the ActionScript.
If you put code in a FLA file, put ActionScript on Frame 1 or Frame 2 in a layer
called _actions_ on the topmost layer in the Timeline. Alternatively, you might
put all of your code in ActionScript files. Some Flash Pro applications do not
always put all code in a single place (in particular, ActionScript 2.0-based
applications that use screens or behaviors).

You can usually put all your code in the same location (on a frame, or in
ActionScript files), with the following advantages:

- Code is easy to find in a potentially complex source file.

- Code is easy to debug.

## Attaching code to objects

Avoid attaching ActionScript to objects in a FLA file, even in simple SWF files.
(Only ActionScript 1.0 and 2.0. can be attached to objects; ActionScript 3.0
cannot.) Attaching code to an object means that you select a movie clip,
component, or button instance; open the Actions panel; and add ActionScript
using the `on()` or `onClipEvent()` handler functions.

Attaching ActionScript code to objects is strongly discouraged for the following
reasons:

- It is difficult to locate, and the FLA files are difficult to edit.

- It is difficult to debug.

- ActionScript that is written on the timeline or in classes is more elegant and
  easier to build upon.

- It encourages poor coding style.

- The contrast between two styles of coding can be confusing to people learning
  ActionScript; it forces students and readers to learn different coding styles,
  additional syntax, and a poor and limited coding style.

  Avoid attaching ActionScript 2.0 to a button called `myButton_btn`, which
  looks like the following:

      on (release) {
          //do something
      }

  However, placing ActionScript 2.0 with the same purpose on the timeline (which
  is encouraged), looks like the following code:

      myButton_btn.onRelease = function() {
          //do something
      };

  > **Note:** Different practices apply when using behaviors, which sometimes
  > involves attaching code to objects.

More Help topics

[Best practices - Behaviors conventions](./behaviors-conventions.md)

[Using the MVC design pattern](./swf-application-authoring-guidelines.md#using-the-mvc-design-pattern)

[Organizing files and storing code](./swf-application-authoring-guidelines.md#organizing-files-and-storing-code)

[Comparing timeline code with object code](./behaviors-conventions.md#comparing-timeline-code-with-object-code)
