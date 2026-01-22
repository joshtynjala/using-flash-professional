# Add interactivity with code snippets

The Code Snippets panel is designed to make it easy for non-programmers to start
using simple ActionScript 3.0 quickly. It lets you add ActionScript 3.0 code to
your FLA file to enable common functionality. Using the Code Snippets panel does
not require knowledge of ActionScript 3.0.

With the Code Snippets panel, you can:

- Add code that affects the behavior of an object on the Stage

- Add code that controls the movement of the playhead in the Timeline

- (CS5.5 only) - Add code that allows touchscreen user-interaction

- Add new code snippets that you create to the panel

Using the code snippets included with Flash is also a good way to begin learning
ActionScript 3.0. By looking at the code in the snippets and following the
snippet instructions, you can begin understanding code structure and vocabulary.

## Before you begin

## Adobe recommends

> ![](../img/Trani.png)
> [Code snippets and AS3 enhancements](https://web.archive.org/web/20120103091115mp_/http://goo.gl/TuhWK)
>
> [Paul Trani](https://web.archive.org/web/20120103091115mp_/http://www.paultrani.com/blog/)
>
> This tutorial takes you through the enhanced code snippets panel in Flash
> Professional CS5.5. With great new capabilities for those new to ActionScript,
> this enhanced panel helps you quickly understand and use code snippets as well
> as save your own custom code snippets for future use.

When working with the Code Snippets panel, it is important to understand these
fundamentals of Flash:

- Many of the code snippets require you to customize a few items in the code. In
  Flash Pro CS5, you do this in the Actions panel. In Flash Pro CS5.5, you can
  do this by dragging the cursor from code elements in the HUD to the object you
  want the code to control. Each snippet contains specific instructions for this
  task.

- All of the included code snippets are ActionScript 3.0. ActionScript 3.0 is
  not compatible with ActionScript 2.0.

- Some snippets affect the behavior of an object, allowing it to be clicked or
  causing it to move or disappear. You apply these snippets to the object on the
  Stage.

- Some snippets cause an action to occur immediately when the playhead enters
  the frame that contains the snippet. You apply these snippets to a Timeline
  frame.

- When you apply a code snippet, the code is added to the current frame of the
  Actions layer in the Timeline. If you have not created an Actions layer
  yourself, Flash adds one above all other layers in the Timeline.

- For ActionScript to control an object on the Stage, the object must have an
  instance name assigned in the Property inspector.

- In Flash Pro CS5, each code snippet has a tool tip that describes what the
  snippet does. In Flash Pro CS5.5, you can click the Show Description and Show
  Code buttons that appear when you select a snippet in the panel.

#### Additional tutorials

- Tutorial:
  [Code snippets for beginning ActionScript 3 programmers and designers - Flash Pro CS5](https://web.archive.org/web/20120103091115mp_/http://www.adobe.com/devnet/flash/articles/code_snippets_panel.html)

## (Flash CS5) Add a code snippet to an object or Timeline frame

To add an action that affects an object or the playhead:

1.  Select an object on the Stage or a frame in the Timeline.

    If you select an object that is not a symbol instance or a TLF text object,
    Flash converts the object to a movie clip symbol when you apply the snippet.

    If you select an object that does not already have an instance name, Flash
    adds one when you apply the snippet.

2.  In the Code Snippets panel (Window \> Code Snippets), double-click the
    snippet you want to apply.

    If you selected an object on the Stage, Flash adds the snippet to the
    Actions panel in the frames containing the selected object.

    If you selected a Timeline frame, Flash adds the snippet to just that frame.

3.  In the Actions panel, view the newly added code and replace any necessary
    items according to the instructions at the top of the snippet.

## (Flash CS5.5) Add a code snippet to an object or Timeline frame

To add an action that affects an object or the playhead:

1.  Select the snippet you want to apply in the Code Snippets panel (Window \>
    Code Snippets).

2.  To display a description of the snippet, click the Show Description button
    that appears to the right of the selected snippet.

3.  To display the code within the snippet, click the Show Code button to the
    right of the snippet.

4.  If the snippet contains the text "instance_name_here", drag from that text
    to the instance on the Stage that you want to the code to control. To
    drag-and-drop, the symbol instance must be a movie clip or a button.

    If the instance does not yet have a name, a dialog box appears to allow you
    to enter a name for the instance.

    You can also click the text and enter the instance name directly in the
    code. Use this method of you are working with a shape or graphic symbol
    instance.

5.  If the snippet contains other colored text, select the text and enter the
    correct information according to the instructions inside the code snippet.

6.  When you finish editing the code snippet, click the Insert button.

    Flash adds the code to the Actions layer. If no Actions layer exists, Flash
    creates one.

    If you selected an object on the Stage, Flash adds the snippet to the
    Actions panel in the frames containing the selected object.

    If you selected a Timeline frame, Flash adds the snippet to the Actions
    layer in just that frame.

7.  (Optional) To view the inserted code, open the Actions panel (Window \>
    Actions).

## Add new snippets to the Code Snippets panel

You can add new code snippets to the Code Snippets panel in two ways:

- Enter a snippet in the Create New Code Snippet dialog box.

- Import a code snippet XML file.

To use the Create New Code Snippet dialog box:

1.  In the Code Snippets panel, choose Create New Code Snippet from the panel
    menu.

2.  In the dialog box, Enter the Title, Tool tip text, and ActionScript 3.0 code
    for your snippet.

    You can add any code that is currently selected in the Actions panel by
    clicking the Auto-Fill button.

3.  Select the Automatically replace instance_name_here check box if your code
    includes the string "instance_name_here" and you want Flash to replace it
    with the correct instance name when the snippet is applied.

    Flash adds the new snippet to the Code Snippets panel in a folder called
    Custom.

To import a code snippet in XML format:

1.  In the Code Snippets panel, choose Import Code Snippets XML from the panel
    menu.

2.  Select the XML file you want to import and click Open

To see the correct XML format for code snippets, choose Edit Code Snippets XML
from the panel menu.

To delete a code snippet, right-click the snippet in the panel and choose Delete
Code Snippet from the context menu.
