# Undo, redo, and history

## Undo, Redo, and Repeat commands

To undo or redo actions on individual objects, or all objects within the current
document, specify either object-level or document-level Undo and Redo commands
(Edit \> Undo or Edit Redo). The default behavior is document-level Undo and
Redo.

You cannot undo some actions when using object-level Undo. Among these are
entering and exiting Edit mode; selecting, editing, and moving library items;
and creating, deleting, and moving scenes.

To reapply a step to the same object or to a different object, use the Repeat
command. For example, if you move a shape named shape_A, select Edit \> Repeat
to move the shape again, or select another shape, shape_B, and select Edit \>
Repeat to move the second shape by the same amount.

By default, Flash Pro supports 100 levels of undo for the Undo menu command.
Select the number of undo and redo levels, from 2 to 300, in Flash Preferences.

By default, when you undo a step by using Edit \> Undo or the History panel, the
file size of the document does not change, even if you delete an item in the
document. For example, if you import a video file into a document, and undo the
import, the file size of the document still includes the size of the video file.
Any items that you delete from a document when performing an Undo command are
preserved to in order to be able to restore the items with a Redo command.

## Using the History panel

The History panel (Window \> Other Panels \> History) shows a list of the steps
you've performed in the active document since you created or opened that
document, up to a specified maximum number of steps. (The History panel doesn't
show steps you've performed in other documents.) The slider in the History panel
initially points to the last step that you performed.

- To undo or redo individual steps or multiple steps at once, use the History
  panel. Apply steps from the History panel to the same object or to a different
  object in the document. However, you cannot rearrange the order of steps in
  the History panel. The History panel is a record of steps in the order in
  which they are performed.

  > **Note:** If you undo a step or a series of steps and then do something new
  > in the document, you can no longer redo the steps in the History panel; they
  > disappear from the panel.

- By default, Flash Pro supports 100 levels of undo for the History panel.
  Select the number of undo and redo levels, from 2 to 300, in Flash
  Preferences.

- To erase the history list for the current document, clear the History panel.
  After clearing the history list, you cannot undo the steps that are cleared.
  Clearing the history list does not undo steps; it removes the record of those
  steps from the current document's memory.

Closing a document clears its history. To use steps from a document after that
document is closed, copy the steps with the Copy Steps command or save the steps
as a command.

## Undo steps with the History panel

When you undo a step, the step is dimmed in the History panel.

- To undo the last step performed, drag the History panel slider up one step in
  the list.

- To undo multiple steps at once, drag the slider to point to any step, or click
  to the left of a step along the path of the slider. The slider scrolls
  automatically to that step, undoing all subsequent steps as it scrolls.

> **Note:** Scrolling to a step (and selecting the subsequent steps) is
> different from selecting an individual step. To scroll to a step, click to the
> left of the step.

## Replay steps with the History panel

When you replay steps with the History panel, the steps that play are the steps
that are selected (highlighted) in the History panel, not necessarily the step
currently indicated by the slider.

Apply steps in the History panel to any selected object in the document.

### Replay one step

![](../img/dingbat.png) In the History panel, select a step and click the Replay
button.

### Replay a series of adjacent steps

1.  Select steps in the History panel by doing one of the following:
    - Drag from one step to another. (Don't drag the slider; drag from the text
      label of one step to the text label of another step.)

    - Select the first step, then Shift-click the last step; or select the last
      step and Shift-click the first step.

2.  Click Replay. The steps replay in order, and a new step, labeled Replay
    Steps, appears in the History panel.

### Replay nonadjacent steps

1.  Select a step in the History panel, and Control-click (Windows) or
    Command-click (Macintosh) other steps. To deselect a selected step,
    Control-click or Command-click.
2.  Click Replay.

## Copy and paste steps between documents

Each open document has its own history of steps. To copy steps from one document
and paste them into another, use the Copy Steps command in the History panel
options menu. If you copy steps into a text editor, the steps are pasted as
JavaScript™ code.

1.  In the document containing the steps to reuse, select the steps in the
    History panel.
2.  In the History panel options menu, select Copy Steps.
3.  Open the document to paste the steps into.
4.  Select an object to apply the steps to.
5.  Select Edit \> Paste to paste the steps. The steps play back as they're
    pasted into the document's History panel. The History panel shows them as
    only one step, called Paste Steps.

More Help topics

[Set preferences in Flash](./set-preferences-in-flash.md)

[Automating tasks with the Commands menu](./automating-tasks-with-the-commands-menu.md)
