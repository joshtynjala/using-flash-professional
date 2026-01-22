# Best practices - Behaviors conventions

## About behaviors conventions

Behaviors are prewritten ActionScript 2.0 code that you can add to parts of a
FLA file. Many developers enter ActionScript code either into one or several
frames on the main Timeline or in external ActionScript files. However, when you
use behaviors, sometimes code is placed directly on symbol instances (such as
buttons, movie clips, or components) instead of being placed on the timeline.

Behaviors are not supported by ActionScript 3.0.

## Comparing timeline code with object code

To avoid problems that decentralized ActionScript 2.0 code creates, carefully
plan a document that uses behaviors. Many developers do not place ActionScript
on symbol instances, and instead place their code on the Timeline (timeline
code) or in classes. Because behaviors add code to many locations in a FLA file,
your ActionScript is not centralized and can be difficult to locate. When code
is not centralized, it is difficult to understand interactions between the
snippets of code, and it is impossible to write elegant code. Decentralized code
can potentially lead to problems debugging code or editing files.

If you use behaviors, try the following features to facilitate working with
behaviors and decentralized ActionScript:

Script Navigator  
Makes your timeline code or code on individual objects easy to find and edit in
the Actions panel.

Find And Replace  
Lets you search for strings and replace them in a FLA file.

Script Pinning  
Lets you pin multiple scripts from various objects and work with them
simultaneously in the Actions panel. This method works best with the Script
navigator.

Movie Explorer  
Lets you view and organize the contents of a FLA file, and select elements
(including scripts) for further modification.

## When to use behaviors

The main difference between a FLA file with behaviors and a FLA file without
behaviors is the workflow you must use for editing the project. If you use
behaviors, you must select each instance on the Stage, or select the Stage, and
open the Actions or Behaviors panel to make modifications. If you write your own
ActionScript and put all your code on the main Timeline, you only have to make
your changes on the Timeline.

If you have a FLA file with symbols, you can select one of the instances on the
Stage, and use the Add menu on the Behaviors panel to add a behavior to that
instance. The behavior you select automatically adds code that attaches to the
instance, using "object code" such as the `on()` handler. You can also select a
frame on a timeline, and add different behaviors to a frame using the Behaviors
panel.

Decide how to structure your FLA file. Examine how and where to use behaviors
and ActionScript in your FLA file. Consider the following questions:

- What code do the behaviors contain?

- Do you have to modify the behavior code? If so, by how much? To modify the
  behavior code to any extent, do not use behaviors. You usually cannot edit
  behaviors by using the Behaviors panel if you make modifications to the
  ActionScript. To significantly edit the behaviors in the Actions panel, it is
  usually easier to write all of the ActionScript yourself in a centralized
  location.

- What other ActionScript do you need, and does other ActionScript have to
  interact with the behavior code? Debugging and modifications are easier to
  make from a central location. For example, if code on a timeline interacts
  with behaviors placed on objects, avoid behaviors.

- How many behaviors do you have to use, and where do you plan to put them in
  the FLA file? If your behaviors are all placed on a timeline, they might work
  well in your document. Or, your workflow might not be affected if you use only
  a small number of behaviors. However, if you use many behaviors on a lot of
  object instances, writing your own code on the Timeline or in external
  ActionScript files might be more efficient.

Remember, ActionScript 3.0 does not support behaviors.

## Using behaviors consistently

Use behaviors consistently throughout a document when they are your main or only
source of ActionScript. Use behaviors when you have little or no additional code
in the FLA file, or have a consistent system in place for managing the behaviors
that you use.

If you add ActionScript to a FLA file, put code in the same locations where
behaviors are added, and document how and where you add code.

For example, if you place code on instances on the Stage (object code), on the
main Timeline (frame scripts), and also in external AS files, examine your file
structure. Your project will be difficult to manage if you have code in all of
these places. However, if you logically use behaviors and structure your code to
work in a particular way surrounding those behaviors (place everything on object
instances), at least your workflow is consistent. The document will be easier to
modify later.

## Sharing files that use behaviors

If you plan to share your FLA file with other users and you use ActionScript
placed on or inside objects (such as movie clips), it can be difficult for those
users to find your code's location, even when they use the Movie Explorer to
search through the document.

Document the use of behaviors if you are working with a complex document.
Depending on the size of the application, create a flow chart, list, or use good
documentation comments in a central location on the main Timeline.

If you are creating a FLA file with code placed in many locations throughout the
document and plan to share the file, leave a comment on Frame 1 on the main
Timeline to tell users where to find the code and how the file is structured.
The following example shows a comment (on Frame 1) that tells users the location
of the ActionScript:

    /*
        ActionScript placed on component instances and inside movie clips using behaviors.
        Use the Movie Explorer to locate ActionScript
    */

> **Note:** This technique is not necessary if your code is easy to find, the
> document is not shared, or all of your code is placed on frames of the main
> Timeline.
